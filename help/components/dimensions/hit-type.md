---
title: Type hit
description: Hiermee wordt bepaald of de hit een voor- of achtergrondhit was.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Type hit

De afmeting &#39;Type kit&#39; bepaalt of een mobiele toepassing zich op de voor- of achtergrond bevond toen de hit naar Adobe-gegevensverzamelingsservers werd verzonden. Deze dimensie is alleen van belang voor rapportensuites die gegevens voor mobiele toepassingen bevatten. Browsergegevens die via AppMeasurement zijn verzameld, rapporteren de treffer altijd als &quot;Voorgrond&quot;.

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten het vak voor alle mobiele SDK-implementaties op versie 4.13.6 of hoger. Als u de mobiele SDK niet gebruikt, worden alle hits weergegeven onder de dimensie Voorgrond. Als de optie Oudere rapportage en kenmerken voor achtergrondoorgangen uitschakelen is ingeschakeld, worden achtergrondopdrachten alleen weergegeven in [Virtuele rapportsuites](../vrs/vrs-mobile-visit-processing.md).

## Dimension-items

Dimension-items bevatten `"Foreground"` en `"Background"`. Elke hit die niet op de achtergrond van een mobiele toepassing is verzonden, behoort tot de categorie `"Foreground"` dimensie-item. Elke hit die wordt verzonden waar de mobiele toepassing zich op de achtergrond bevond, behoort tot de `"Background"` dimensie-item.
