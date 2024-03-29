---
title: Browserbreedte - gespaard
description: De breedte van het browservenster in pixels.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Browserbreedte

De &#39;browserbreedte - gespit&#39; [dimensie](overview.md) Hiermee geeft u de breedte van het browservenster weer, geclassificeerd in vooraf gedefinieerde groepen. Deze dimensie is handig wanneer u wilt begrijpen hoe breed bezoekers uw inhoud zien. Als u de breedte begrijpt waarin uw inhoud doorgaans wordt weergegeven, kunt u die inhoud optimaliseren.

Deze dimensie verschilt van de schermbreedte. Browserbreedte is het aantal pixels binnen de zichtbare browserruimte, terwijl de schermbreedte de breedte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

De breedte van de browser is altijd kleiner dan of gelijk aan de schermbreedte, omdat de breedte van de browser geen schuifbalken of randen bevat.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`bw` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `window.innerWidth` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `bw` de parameter van het vraagkoord op de eerste klap van elk bezoek.

Adobe houdt browserbreedte voor een bezoek aan. Als de breedte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Tot Dimensionen behoren alle verzamelde browserbreedten, geclassificeerd in vooraf gedefinieerde groepen. Als de browserbreedte van een hit bijvoorbeeld `1280`, dan wordt het gegroepeerd in het afmetingsitem `1200 to 1299`.
