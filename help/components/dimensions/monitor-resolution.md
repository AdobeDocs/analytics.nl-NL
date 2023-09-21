---
title: Monitorresolutie
description: De resolutie van de monitor van de bezoeker in pixel.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Monitorresolutie

De &#39;monitorresolutie&#39; [dimensie](overview.md) geeft de hoogte en breedte van de actieve weergave in pixels weer. Deze dimensie is handig wanneer u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers of hoe breed bezoekers hun browservenster kunnen maken. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze dimensie is anders dan de hoogte en breedte van de browser. De hoogte/breedte van de browser is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de monitorresolutie het aantal pixels van de gehele monitor is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserafmetingen zijn altijd kleiner dan monitorresolutie, omdat browsernavigatie of -randen niet in de afmetingen zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`s` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `screen.width` en `screen.height` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `s` parameter querytekenreeks in afbeeldingsaanvragen.

## Dimension-items

Dimensionen bevatten alle verzamelde monitorresoluties. Voorbeelden van waarden zijn `1920 x 1080`, `1366 x 768`, en `1280 x 720`.
