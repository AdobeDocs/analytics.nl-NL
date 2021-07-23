---
title: Browserbreedte - gespaard
description: De breedte van het browservenster in pixels.
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '0'
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

Deze dimensie wint gegevens van [`bw` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met behulp van de JavaScript-variabele `window.innerWidth` in de browser. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u `bw` parameter van het vraagkoord op de eerste klap van elk bezoek omvat.

Adobe blijft de browserbreedte voor een bezoek behouden. Als de breedte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Dimension-items omvatten alle verzamelde browserbreedten, geclassificeerd in groepen van 100 pixels. Als de browserbreedte van een hit bijvoorbeeld `1280` is, wordt deze gegroepeerd in het dimensie-item `1200 to 1299`.
