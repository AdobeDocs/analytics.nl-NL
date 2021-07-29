---
title: Aankoopgebeurtenis
description: Gebruik de aankoopgebeurtenis om gegevens te verzamelen voor de metriek 'Bestellingen', 'Eenheden' en 'Opbrengst'.
exl-id: 5ad148d6-cf45-4dea-846a-255004300bc2
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# Aankoopgebeurtenis

De aankoopgebeurtenis is een waarde in de variabele `events`. Deze waarde is nuttig voor organisaties die gegevens willen verzamelen rond de opbrengst die hun plaats produceert. Deze is sterk afhankelijk van de variabelen [`products`](../products.md) en [`purchaseID`](../purchaseid.md).

Wanneer u een aankoopgebeurtenis instelt, heeft dit invloed op de volgende metriek:

* De metrische toename van &#39;Orders&#39; met 1
* De metrische stappen &#39;Eenheden&#39; met het aantal producten in de variabele `products`
* De metrische verhogingen van de &quot;Inkomsten&quot; met de som van prijsparameters in de `products` variabele

>[!NOTE]
>
>Ontvangsten worden niet vermenigvuldigd met het veld Hoeveelheid. `s.products="Womens;Socks;5;4.50"` geeft bijvoorbeeld $22,50 niet door aan inkomsten; het geeft $4,50. Zorg ervoor dat uw implementatie de totale opbrengsten voor het vermelde aantal doorgeeft. Bijvoorbeeld,`s.products="Womens;Socks;5;22.50"`.

## Aankoopgebeurtenis instellen met labels in Adobe Experience Platform

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Events] en stel het vervolgkeuzemenu voor gebeurtenissen in op [!UICONTROL purchase].

Andere afhankelijke variabelen zoals `products` en `purchaseID` hebben geen specifieke velden in de gebruikersinterface voor gegevensverzameling. Gebruik de aangepaste code-editor die volgt op de syntaxis AppMeasurement voor deze variabelen.

## Stel de aankoopgebeurtenis in in AppMeasurement en de aangepaste code-editor

De aankoopgebeurtenis is een tekenreeks die is ingesteld als onderdeel van de gebeurtenisvariabele.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## De-duplicatie van gebeurtenissen aanschaffen

Wanneer u een aankoopgebeurtenis activeert, controleert Adobe het volgende:

* Bevat de hit de variabele `purchaseID`? Als dat niet het geval is, gebruikt Adobe informatie uit de hit om een &quot;tijdelijke aankoop-id&quot; te maken. Deze tijdelijke aankoop-id geldt alleen voor de bezoeker van de hit. De vorige vijf tijdelijke aankoop-id&#39;s worden per rapportsuite opgeslagen voor elke bezoeker-id.
* Komt de tijdelijke aankoop-id overeen met een van de laatste vijf opgeslagen tijdelijke aankoop-id&#39;s? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
* Als de `purchaseID` variabele wordt bepaald, komt het om het even welke waarde aan die reeds in de rapportreeks over alle bezoekers wordt verzameld? Als dat het geval is, wordt de afbeeldingsaanvraag beschouwd als een dubbele aankoop. Niet alle conversievariabelen, inclusief de aankoopgebeurtenis, worden in de rapportage weergegeven.
