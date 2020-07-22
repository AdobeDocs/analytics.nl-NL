---
title: Type hit
description: Hiermee wordt bepaald of de hit een voor- of achtergrondhit was.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Type hit

De afmeting &#39;Type hit&#39; bepaalt of een mobiele toepassing zich op de voor- of achtergrond bevond toen de hit naar Adobe-servers voor gegevensverzameling werd verzonden. Deze dimensie is alleen van belang voor rapportensuites die gegevens voor mobiele toepassingen bevatten. Browsergegevens die via AppMeasurement zijn verzameld, rapporteren de treffer altijd als &quot;Voorgrond&quot;.

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten het vak voor alle mobiele SDK-implementaties op versie 4.13.6 of hoger. Als u de mobiele SDK niet gebruikt, worden alle hits weergegeven onder de dimensie Voorgrond. Als &quot;Verouderde rapportering en Attributie voor AchtergrondHits onbruikbaar maken&quot;wordt gecontroleerd, dan zullen de achtergrondopdrachten slechts in [Virtuele rapportreeksen](../vrs/vrs-mobile-visit-processing.md)verschijnen.

## Dimensie-items

Dimensie-items omvatten `"Foreground"` en `"Background"`. Elke hit die niet op de achtergrond van een mobiele toepassing is verzonden, behoort tot het `"Foreground"` dimensie-item. Elke hit die wordt verzonden waar de mobiele toepassing zich op de achtergrond bevond, behoort tot het `"Background"` dimensie-item.
