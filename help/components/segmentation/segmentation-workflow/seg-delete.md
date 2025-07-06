---
description: Begrijp de overwegingen u zich van bewust zou moeten zijn alvorens u segmenten schrapt.
title: Segmenten verwijderen
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# Segmenten verwijderen

Dit artikel bevat een aantal overwegingen die u in acht moet nemen voordat u segmenten verwijdert.

Wanneer u een segment verwijdert:

* Geplande rapporten en dashboards die dit segment hebben toegepast blijven normaal werken.
* Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt.

<!--

For example: Assume you have 2 segments with the same name in different report suites:

  | Segment name | Report suite |
  |---|---|
  | Visits from California | mainprod |
  | Visits from California | maindev |

  You have a visualization that references the segment for the **[!UICONTROL mainprod]** report suite. Then you delete that segment because the segment is a duplicate. The bookmark will continue to run, referencing the definition of the deleted segment. If you change the segment definition for the remaining segment to include Catalina Island and Tijuana Mexico, the segment applied to the bookmark will not change. The segment will use the old definition. To fix this, update the bookmark to reference the new definition. If you are unsure whether a bookmark, dashboard or scheduled report is using a deleted segment, you could change the name of the remaining segment to indicate whether the bookmark is using the remaining segment.

-->