---
title: Monitorresolutie
description: De resolutie van de monitor van de bezoeker in pixel.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
source-git-commit: e3a1c1fde3809cb73b1bda091b8be43778515d1a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Monitorresolutie

De &quot;resolutie van de Monitor&quot;[ afmeting ](overview.md) toont de hoogte en de breedte van de actieve vertoning in pixel. Deze dimensie is handig wanneer u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers of hoe breed bezoekers hun browservenster kunnen maken. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze afmeting is verschillend dan browser [ hoogte ](browser-height.md) en [ breedte ](browser-width.md). De hoogte/breedte van de browser is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de monitorresolutie het aantal pixels van de gehele monitor is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "; Browser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserafmetingen zijn altijd kleiner dan monitorresolutie, omdat browsernavigatie of -randen niet in de afmetingen zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van het [`s` vraagkoord ](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met behulp van de JavaScript-variabele `screen.width` en `screen.height` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak.

Als u buiten AppMeasurement (bijvoorbeeld via de API) een gegevensverzamelingsmethode gebruikt, moet u de parameter van de `s` querytekenreeks opnemen in afbeeldingsaanvragen. Als de queryreeks `s` ontbreekt of als een bibliotheek voor gegevensverzameling anders de monitorresolutie niet kan verzamelen, worden die gegevens vermeld onder [!UICONTROL `Not Specified`] .

## Dimension-objecten

Dimension-items bevatten alle verzamelde monitorresoluties. Voorbeelden van waarden zijn `1920 x 1080` , `1366 x 768` en `1280 x 720` .
