---
title: Browserbreedte - gespaard
description: De breedte van het browservenster in pixels.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Browserbreedte

De dimensie &#39;Browserbreedte - gespit&#39; geeft de breedte van het browservenster weer, geclassificeerd in groepen van 100 pixels. Deze dimensie is handig wanneer u wilt begrijpen hoe breed bezoekers uw inhoud zien. Als u begrijpt hoe breed uw inhoud doorgaans wordt weergegeven, kunt u inhoud optimaliseren voor weergave.

Deze dimensie is anders dan de schermbreedte. Browserbreedte is het aantal pixels binnen de zichtbare browserruimte, terwijl de schermbreedte de breedte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

De breedte van de browser is altijd kleiner dan of gelijk aan de schermbreedte, omdat de breedte van de browser geen schuifbalken of randen bevat.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`bw` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `window.innerWidth` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de methode `bw` de parameter van het vraagkoord op de eerste klap van elk bezoek.

Adobe blijft de browserbreedte voor een bezoek behouden. Als de breedte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Dimension-items omvatten alle verzamelde browserbreedten, geclassificeerd in groepen van 100 pixels. Als de browserbreedte van een hit bijvoorbeeld `1280`, dan wordt het gegroepeerd in het afmetingsitem `1200 to 1299`.
