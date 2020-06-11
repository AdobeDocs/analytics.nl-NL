---
title: Type hit
description: Hiermee wordt bepaald of de hit een voor- of achtergrondhit was.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Type hit

De afmeting &#39;Type hit&#39; bepaalt of een mobiele toepassing zich op de voor- of achtergrond bevond toen de hit naar Adobe-servers voor gegevensverzameling werd verzonden. Deze dimensie is alleen van belang voor rapportensuites die gegevens voor mobiele toepassingen bevatten. Browsergegevens die via AppMeasurement zijn verzameld, rapporteren de treffer altijd als &quot;Voorgrond&quot;.

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten het vak voor alle mobiele SDK-implementaties op versie 4.13.6 of hoger. Als u de mobiele SDK niet gebruikt, worden alle treffers weergegeven onder de waarde voor de dimensie Voorgrond. Als &quot;Verouderde rapportering en Attributie voor AchtergrondHits onbruikbaar maken&quot;wordt gecontroleerd, dan zullen de achtergrondopdrachten slechts in [Virtuele rapportreeksen](../vrs/vrs-mobile-visit-processing.md)verschijnen.

## Dimensiewaarden

Dimensiewaarden zijn onder andere `"Foreground"` en `"Background"`. Elke hit die niet op de achtergrond van een mobiele toepassing is verzonden, behoort tot de waarde van de `"Foreground"` dimensie. Elke hit die wordt verzonden op de locatie waar de mobiele toepassing zich op de achtergrond bevond, behoort tot de waarde van de `"Background"` dimensie.
