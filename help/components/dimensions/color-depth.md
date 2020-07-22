---
title: Kleurdiepte
description: De kleurdiepte van het apparaat.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Kleurdiepte

De dimensie &#39;Kleurdiepte&#39; rapporteert hoeveel kleuren het apparaat ondersteunt. Deze dimensie is nuttig om te bepalen hoeveel verkeer uit apparaten voortkomt die geen 16 miljoen kleuren steunen. Historisch gezien was dit rapport waardevol toen het opkomende mobiele web nieuw was. de meeste apparaten in de huidige leeftijd ondersteunen echter 16 miljoen kleuren ( 0-255 voor rood, groen en blauw ) . <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een opzoektabel en zet de bitwaarde om in een beter leesbare indeling. Het verzamelt gegevens van het [`c` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken. AppMeturement gebruikt de `screen.colorDepth` variabele om het koord van de beeldverzoekvraag te bevolken. Als u AppMeasurement gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `c` vraagkoord op elke slag met een geldige beetjewaarde omvat.

## Dimensie-items

Dimensie-items bevatten het aantal kleuren dat door het apparaat wordt ondersteund. Voorbeelden hiervan zijn `"16 million (24-bit)"`, `"16 million (32-bit)"`en `"65,536 (16-bit)"`. Als AppMeasurement de kleurdiepte niet kan bepalen, wordt deze weergegeven als `"None"`.

>[!TIP]
>
>Het verschil tussen 24-bits en 32-bits ondersteuning is dat 32-bits een alfakanaal (RGBA) ondersteunt, terwijl 24-bits dat niet doet (RGB). Zie [Kleurdiepte](https://en.wikipedia.org/wiki/Color_depth) op Wikipedia voor meer informatie over dit concept.
