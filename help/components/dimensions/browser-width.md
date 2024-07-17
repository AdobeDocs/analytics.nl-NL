---
title: Browserbreedte - gespaard
description: De breedte van het browservenster in pixels.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: 2601b0e5c3fa78237ce693801b8dd8c95b853b81
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Browserbreedte

De &quot;Browser breedte - gespleet&quot;[ afmeting ](overview.md) toont de breedte van het browser venster, dat in vooraf bepaalde groepen wordt geclassificeerd. Deze dimensie is handig wanneer u wilt begrijpen hoe breed bezoekers uw inhoud zien. Als u de breedte begrijpt waarin uw inhoud doorgaans wordt weergegeven, kunt u die inhoud optimaliseren.

Deze dimensie verschilt van de schermbreedte. Browserbreedte is het aantal pixels binnen de zichtbare browserruimte, terwijl de schermbreedte de breedte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
console.log(`Browser width: ${window.innerWidth} pixels\nScreen width: ${screen.width} pixels`);
```

De breedte van de browser is altijd kleiner dan of gelijk aan de schermbreedte, omdat de breedte van de browser geen schuifbalken of randen bevat.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van het [`bw` vraagkoord ](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `window.innerWidth` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de parameter voor de `bw` querytekenreeks opnemen bij de eerste hit van elk bezoek.

Adobe houdt browserbreedte voor een bezoek aan. Als de breedte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Tot Dimensionen behoren alle verzamelde browserbreedten, geclassificeerd in vooraf gedefinieerde groepen. Als de browserbreedte van een hit bijvoorbeeld `1280` is, wordt deze gegroepeerd in het dimensie-item `1200 to 1299` .
