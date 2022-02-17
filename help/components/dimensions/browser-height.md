---
title: Browserhoogte - ingesloten
description: De hoogte van het browservenster in pixels.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Hoogte browser

De afmetingen &#39;Browserhoogte - gespaard&#39; geven de hoogte van het browservenster weer, geclassificeerd in groepen van 100 pixels. Deze dimensie is handig als u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze dimensie is anders dan de schermhoogte. Browserhoogte is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de schermhoogte de hoogte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
"Browser height: " + window.innerHeight + " pixels\nScreen height: " + screen.height + " pixels";
```

Browserhoogte is altijd kleiner dan of gelijk aan schermhoogte, aangezien browsernavigatie of -randen niet in de browserhoogte zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`bh` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `window.innerHeight` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de methode `bh` de parameter van het vraagkoord op de eerste klap van elk bezoek.

Adobe houdt de browserhoogte tijdens een bezoek aan. Als de hoogte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Dimension-items bevatten alle verzamelde browserhoogten, geclassificeerd in groepen van 100 pixels. Als de browserhoogte van een hit bijvoorbeeld `720`, dan wordt het gegroepeerd in het afmetingsitem `700 to 799`.
