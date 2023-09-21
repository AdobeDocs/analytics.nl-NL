---
title: Week
description: De week waarop metrisch voorkwam.
feature: Dimensions
exl-id: 944ec843-998c-473f-b8e6-16cf126745b4
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Week

De &#39;week&#39; [dimensie](overview.md) meldt de week dat een bepaalde metrische waarde voorkwam. Het eerste dimensie-item is de eerste week in het datumbereik en het laatste dimensie-item is de laatste week in het datumbereik. Deze dimensie is essentieel voor trended rapporten, aangezien het u toestaat om metriek in tijd te zien.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

In Analysis Workspace bevatten dimensieitems de datum (maand, dag en jaar) van de eerste dag van de week.

In Data Warehouse, omvatten de afmetingspunten genummerde weken die op de de datumwaaier van het verzoek worden gebaseerd. De eerste volledige week is bijvoorbeeld `"Week 1"`. Als een verzoek een gedeeltelijke week omvat, worden de gegevens gegroepeerd in het afmetingspunt `"Week 0"`.
