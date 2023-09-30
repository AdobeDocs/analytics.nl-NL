---
title: Gemiddelde sessielengte (mobiel)
description: De gemiddelde sessielengte voor het mobiele apparaat.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# Gemiddelde sessielengte (mobiel)

De &#39;gemiddelde sessielengte (mobiel)&#39; [metrisch](overview.md) toont de gemiddelde hoeveelheid tijd een bepaald afmetingspunt per afmetingspunt aanwezig is. Het lijkt op het [[!UICONTROL Time spent per visit (seconds)]](time-spent-per-visit.md) metrisch, behalve dit metrisch gebruikt mobiele SDK-specifieke componenten als deel van zijn berekening.

## Hoe deze metrische waarde wordt berekend

Deze metrisch wordt berekend gebruikend [Levenscycluswaarden](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'`.
