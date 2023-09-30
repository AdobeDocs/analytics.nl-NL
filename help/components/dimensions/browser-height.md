---
title: Browserhoogte - ingesloten
description: De hoogte van het browservenster in pixels.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Hoogte browser

De &#39;Browser height - buckted&#39; [dimensie](overview.md) Hiermee geeft u de hoogte van het browservenster weer, geclassificeerd in vooraf gedefinieerde groepen. Deze dimensie is handig als u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze afmetingen verschillen van de schermhoogte. Browserhoogte is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de schermhoogte de hoogte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
"Browser height: " + window.innerHeight + " pixels\nScreen height: " + screen.height + " pixels";
```

Browserhoogte is altijd kleiner dan of gelijk aan schermhoogte, aangezien browsernavigatie of -randen niet in de browserhoogte zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`bh` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `window.innerHeight` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `bh` de parameter van het vraagkoord op de eerste klap van elk bezoek.

Adobe houdt browserhoogte voor een bezoek aan. Als de hoogte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Tot Dimensionen behoren alle verzamelde browserhoogten, geclassificeerd in vooraf gedefinieerde groepen. Als de browserhoogte van een hit bijvoorbeeld `720`, dan wordt het gegroepeerd in het afmetingsitem `700 to 799`.
