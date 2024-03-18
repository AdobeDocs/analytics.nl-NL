---
title: Aankoopgebeurtenis
description: Gebruik de aankoopgebeurtenis om gegevens te verzamelen voor de metriek 'Bestellingen', 'Eenheden' en 'Opbrengst'.
feature: Variables
exl-id: 5ad148d6-cf45-4dea-846a-255004300bc2
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Aankoopgebeurtenis

De aankoopgebeurtenis is een waarde in het dialoogvenster `events` variabele. Deze waarde is nuttig voor organisaties die gegevens willen verzamelen rond de opbrengst die hun plaats produceert. Zij is sterk afhankelijk van de [`products`](../products.md) en [`purchaseID`](../purchaseid.md) variabelen.

Wanneer u een aankoopgebeurtenis instelt, heeft dit invloed op de volgende metriek:

* De metrische toename van &#39;Orders&#39; met 1
* De metrische stappen &#39;Eenheden&#39; in verhouding tot het aantal producten in de `products` variabel
* De maatstaf &quot;inkomsten&quot; verhoogt met de som van de prijsparameters in het `products` variabel

>[!NOTE]
>
>Ontvangsten worden niet vermenigvuldigd met het veld Hoeveelheid. Bijvoorbeeld: `s.products="Womens;Socks;5;4.50"` geeft $22,50 niet door aan inkomsten; het geeft $4,50 door. Zorg ervoor dat uw implementatie de totale opbrengsten voor het vermelde aantal doorgeeft. Bijvoorbeeld: `s.products="Womens;Socks;5;22.50"`.

## De aankoopgebeurtenis instellen met de Web SDK

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md) Voor de aankoopgebeurtenis worden de volgende XDM-velden gebruikt:

* Bestellingen worden toegewezen aan `xdm.commerce.purchases.value`.
* Eenheden worden toegewezen aan de som van alle eenheden `xdm.productListItems[].quantity` velden.
* Opbrengsten worden toegewezen aan de som van alle `xdm.productListItems[].priceTotal` velden.

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md), de aankoopgebeurtenis gebruikt `data.__adobe.analytics.events`, volgens tekenreekssyntaxis van AppMeasurement.

## De aankoopgebeurtenis instellen met de extensie Adobe Analytics

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] en stelt u de [!UICONTROL Events] vervolgkeuzelijst naar [!UICONTROL purchase].

Andere afhankelijke variabelen zoals `products` en `purchaseID` hebben geen specifieke velden in de extensie Analytics in Adobe Experience Platform Data Collection. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement voor deze variabelen.

## Stel de aankoopgebeurtenis in het AppMeasurement en de aangepaste code-editor voor de extensie Analytics in

De aankoopgebeurtenis is een tekenreeks die is ingesteld als onderdeel van de gebeurtenisvariabele.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## De-duplicatie van gebeurtenissen aanschaffen

Wanneer u een aankoopgebeurtenis activeert, controleert de Adobe het volgende:

* Bevat de treffer de `purchaseID` variabele? Als dat niet het geval is, gebruikt de Adobe informatie uit de hit om een &#39;tijdelijke aankoop-id&#39; te maken. Deze tijdelijke aankoop-id geldt alleen voor de bezoeker van de hit. De vorige vijf tijdelijke aankoop-id&#39;s worden per rapportsuite opgeslagen voor elke bezoeker-id.
* Komt de tijdelijke aankoop-id overeen met een van de laatste vijf opgeslagen tijdelijke aankoop-id&#39;s? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
* Als de `purchaseID` variabele is gedefinieerd, komt deze overeen met een waarde die al is verzameld in de rapportsuite voor alle bezoekers? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
