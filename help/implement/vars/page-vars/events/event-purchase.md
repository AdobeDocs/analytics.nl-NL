---
title: Aankoopgebeurtenis
description: Gebruik de aankoopgebeurtenis om gegevens te verzamelen voor de metriek 'Bestellingen', 'Eenheden' en 'Opbrengst'.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Aankoopgebeurtenis

De aankoopgebeurtenis is een waarde in de `events` variabele. Deze waarde is nuttig voor organisaties die gegevens willen verzamelen rond de opbrengst die hun plaats produceert. Zij is sterk afhankelijk van de [`products`](../products.md) en de [`purchaseID`](../purchaseid.md) variabelen.

Wanneer u een aankoopgebeurtenis instelt, heeft dit invloed op de volgende metriek:

* De metrische toename van &#39;Orders&#39; met 1
* De metrische stappen &#39;Eenheden&#39; met het aantal producten in de `products` variabele
* De metrische verhogingen van de &quot;Inkomsten&quot; met de som van de prijsparameters in de `products` variabele

## Aanschafgebeurtenis instellen in Adobe Experience Platform Launch

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] sectie en stel het vervolgkeuzemenu voor gebeurtenissen in op [!UICONTROL purchase].

Andere afhankelijke variabelen zoals `products` en `purchaseID` hebben geen specifieke velden in Launch. Gebruik de douane code redacteur na syntaxis AppMeasurement voor deze variabelen.

## Stel de aankoopgebeurtenis in in de aangepaste code-editor van AppMeasurement en Launch

De aankoopgebeurtenis is een tekenreeks die is ingesteld als onderdeel van de gebeurtenisvariabele.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## De-duplicatie van gebeurtenissen aanschaffen

Wanneer u een aankoopgebeurtenis activeert, controleert Adobe het volgende:

* Bevat de hit de `purchaseID` variabele? Als dat niet het geval is, gebruikt Adobe de gegevens van de hit om een &quot;tijdelijke aankoop-id&quot; te maken. Deze tijdelijke aankoop-id geldt alleen voor de bezoeker van de hit. De vorige vijf tijdelijke aankoop-id&#39;s worden per rapportsuite opgeslagen voor elke bezoeker-id.
* Komt de tijdelijke aankoop-id overeen met een van de laatste vijf opgeslagen tijdelijke aankoop-id&#39;s? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
* Als de `purchaseID` variabele is gedefinieerd, komt deze overeen met een waarde die al is verzameld in de rapportsuite voor alle bezoekers? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
