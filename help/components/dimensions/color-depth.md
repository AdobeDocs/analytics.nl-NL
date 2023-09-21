---
title: Kleurdiepte
description: De kleurdiepte van het apparaat.
feature: Dimensions
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Kleurdiepte

De kleurdiepte [dimensie](overview.md) meldt hoeveel kleuren het apparaat ondersteunt. Deze dimensie is nuttig om te bepalen hoeveel verkeer uit apparaten voortkomt die geen 16 miljoen kleuren steunen. Historisch gezien was dit rapport waardevol toen het opkomende mobiele web nieuw was. De meeste apparaten in het huidige tijdperk ondersteunen echter 16 miljoen kleuren (0-255 voor rood, groen en blauw). <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een opzoektabel en zet de bitwaarde om in een beter leesbare indeling. Het verzamelt gegevens van [`c` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement gebruikt de `screen.colorDepth` variabele om de queryreeks voor de afbeeldingsaanvraag te vullen. Als u AppMeasurement gebruikt (zoals door markeringen in Adobe Experience Platform), werkt deze afmeting uit de doos. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `c` de parameter van het vraagkoord op elke slag met een geldige beetjewaarde.

## Dimension-items

Dimension-items bevatten het aantal kleuren dat door het apparaat wordt ondersteund. Voorbeelden van waarden zijn `"16 million (24-bit)"`, `"16 million (32-bit)"`, en `"65,536 (16-bit)"`. Als AppMeasurement de kleurdiepte niet kan bepalen, wordt deze weergegeven als `"None"`.

>[!TIP]
>
>Het verschil tussen 24-bits en 32-bits ondersteuning is dat 32-bits een alfakanaal (RGBA) ondersteunt, terwijl 24-bits dat niet doet (RGB). Zie [Kleurdiepte](https://en.wikipedia.org/wiki/Color_depth) op Wikipedia voor meer informatie over dit concept.
