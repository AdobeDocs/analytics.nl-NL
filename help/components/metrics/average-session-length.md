---
title: Gemiddelde sessielengte (mobiel)
description: De gemiddelde sessielengte voor het mobiele apparaat.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: 7966c7d9add0011831c97fbe0dfcca2acd8afb58
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Gemiddelde sessielengte (mobiel)

De metrische waarde &#39;Gemiddelde sessielengte (mobiel)&#39; geeft de gemiddelde tijdsduur aan dat een bepaald afmetingsitem per afmetingsitem aanwezig is. Het lijkt op het [Gemiddelde tijd op de site](average-time-on-site.md) metrisch, behalve dit metrisch gebruikt mobiele SDK specifieke componenten als deel van zijn berekening.

## Hoe deze metrische waarde wordt berekend

Deze metrisch wordt berekend gebruikend [mobiele meetgegevens](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html) `'Total session length' / ('Launches' - 'First launches'`.
