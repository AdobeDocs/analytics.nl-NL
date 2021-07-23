---
title: Kleurdiepte
description: De kleurdiepte van het apparaat.
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Kleurdiepte

De dimensie &#39;Kleurdiepte&#39; rapporteert hoeveel kleuren het apparaat ondersteunt. Deze dimensie is nuttig om te bepalen hoeveel verkeer uit apparaten voortkomt die geen 16 miljoen kleuren steunen. Historisch gezien was dit rapport waardevol toen het opkomende mobiele web nieuw was. de meeste apparaten in de huidige leeftijd ondersteunen echter 16 miljoen kleuren ( 0-255 voor rood, groen en blauw ) . <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een opzoektabel en zet de bitwaarde om in een beter leesbare indeling. Het verzamelt gegevens van [`c` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken. AppMeturement gebruikt `screen.colorDepth` variabele om het koord van de de vraagvraag van het beeldverzoek te bevolken. Als u AppMeasurement gebruikt (zoals door markeringen in Adobe Experience Platform), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u `c` de parameter van het vraagkoord op elke slag met een geldige beetjewaarde omvat.

## Dimension-items

Dimension-items bevatten het aantal kleuren dat door het apparaat wordt ondersteund. Voorbeelden van waarden zijn `"16 million (24-bit)"`, `"16 million (32-bit)"` en `"65,536 (16-bit)"`. Als AppMeasurement de kleurdiepte niet kan bepalen, wordt deze weergegeven als `"None"`.

>[!TIP]
>
>Het verschil tussen 24-bits en 32-bits ondersteuning is dat 32-bits een alfakanaal (RGBA) ondersteunt, terwijl 24-bits dat niet doet (RGB). Zie [Kleurdiepte](https://en.wikipedia.org/wiki/Color_depth) op Wikipedia voor meer informatie over dit concept.
