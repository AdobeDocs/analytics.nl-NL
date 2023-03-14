---
title: Gemiddelde sessielengte (mobiel)
description: De gemiddelde sessielengte voor het mobiele apparaat.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: 47d5a532505aff48d43972836c78620870bd8221
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# Gemiddelde sessielengte (mobiel)

De metrische waarde &#39;Gemiddelde sessielengte (mobiel)&#39; geeft de gemiddelde tijdsduur aan dat een bepaald afmetingsitem per afmetingsitem aanwezig is. Het lijkt op het [Tijd doorgebracht per bezoek [seconden]](https://experienceleague.adobe.com/docs/analytics/components/metrics/time-spent-per-visit.html) metrisch, behalve dit metrisch gebruikt mobiele SDK specifieke componenten als deel van zijn berekening.

## Hoe deze metrische waarde wordt berekend

Deze metrisch wordt berekend gebruikend [mobiele meetgegevens](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html) `'Total session length' / ('Launches' - 'First launches'`.
