---
title: Browserbreedte - gespaard
description: De breedte van het browservenster in pixels.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '273'
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

Deze dimensie wint gegevens van het [`bw` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `window.innerWidth` in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `bw` vraagkoord op de eerste klap van elk bezoek omvat.

Adobe blijft de browserbreedte voor een bezoek behouden. Als de breedte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimensie-items

Dimensie-items omvatten alle verzamelde browserbreedten, geclassificeerd in groepen van 100 pixels. Als de browserbreedte van een hit bijvoorbeeld is `1280`, wordt deze gegroepeerd in het dimensie-item `1200 to 1299`.
