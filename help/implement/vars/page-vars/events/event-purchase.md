---
title: Aankoopgebeurtenis
description: Gebruik de aankoopgebeurtenis om gegevens te verzamelen voor de metriek 'Bestellingen', 'Eenheden' en 'Opbrengst'.
feature: Appmeasurement Implementation
exl-id: 5ad148d6-cf45-4dea-846a-255004300bc2
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Aankoopgebeurtenis

De aankoopgebeurtenis is een waarde in de variabele `events` . Deze waarde is nuttig voor organisaties die gegevens willen verzamelen rond de opbrengst die hun plaats produceert. Deze is sterk afhankelijk van de variabelen [`products`](../products.md) en [`purchaseID`](../purchaseid.md) .

Wanneer u een aankoopgebeurtenis instelt, heeft dit invloed op de volgende metriek:

* De metrische toename van &#39;Orders&#39; met 1
* De metrische stappen &#39;Units&#39; van het aantal producten in de variabele `products`
* De maatstaf &#39;Opbrengst&#39; verhoogt met de som van de prijsparameters in de variabele `products`

>[!NOTE]
>
>Ontvangsten worden niet vermenigvuldigd met het veld Hoeveelheid. `s.products="Womens;Socks;5;4.50"` geeft bijvoorbeeld $22,50 niet door aan inkomsten; het geeft $4,50 door. Zorg ervoor dat uw implementatie de totale opbrengsten voor het vermelde aantal doorgeeft. Bijvoorbeeld `s.products="Womens;Socks;5;22.50"` .

## De aankoopgebeurtenis instellen met de Web SDK

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), gebruikt de aankoopgebeurtenis de volgende gebieden XDM:

* Orders worden toegewezen aan `xdm.commerce.purchases.value` .
* Eenheden worden toegewezen aan de som van alle `xdm.productListItems[].quantity` -velden. Zie [`products`](../products.md) voor meer informatie.
* Opbrengsten worden toegewezen aan de som van alle `xdm.productListItems[].priceTotal` -velden.

```json
{
  "xdm": {
    "commerce": {
      "purchases": {
        "value": 1
      }
    }
  }
}
```

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruikt de aanschafgebeurtenis `data.__adobe.analytics.events`, na het koordsyntaxis van AppMeasurement.

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "events": "purchase"
      }
    }
  }
}
```

## De aankoopgebeurtenis instellen met de extensie Adobe Analytics

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Events] en stel de vervolgkeuzelijst [!UICONTROL Events] in op [!UICONTROL purchase] .

Andere afhankelijke variabelen zoals `products` en `purchaseID` hebben geen specifieke velden in de extensie Analytics in Adobe Experience Platform Data Collection. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis voor deze variabelen.

## Aankoopgebeurtenis instellen in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De aankoopgebeurtenis is een tekenreeks die is ingesteld als onderdeel van de gebeurtenisvariabele.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## De-duplicatie van gebeurtenissen aanschaffen

Wanneer u een aankoopgebeurtenis activeert, controleert Adobe het volgende:

* Bevat de hit de variabele `purchaseID` ? Als dat niet het geval is, gebruikt Adobe informatie uit de hit om een &quot;tijdelijke aankoop-id&quot; te maken. Deze tijdelijke aankoop-id geldt alleen voor de bezoeker van de hit. De vorige vijf tijdelijke aankoop-id&#39;s worden per rapportsuite opgeslagen voor elke bezoeker-id.
* Komt de tijdelijke aankoop-id overeen met een van de laatste vijf opgeslagen tijdelijke aankoop-id&#39;s? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
* Als de variabele `purchaseID` is gedefinieerd, komt deze overeen met een waarde die al is verzameld in de rapportsuite voor alle bezoekers? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
