---
title: Gemiddelde sessielengte (mobiel)
description: De gemiddelde sessielengte voor het mobiele apparaat.
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Gemiddelde sessielengte (mobiel)

De metrische waarde &#39;Gemiddelde sessielengte (mobiel)&#39; geeft de gemiddelde tijdsduur aan dat een bepaald afmetingsitem per afmetingsitem aanwezig is. De methode is vergelijkbaar met de metrische [Gemiddelde tijd op de site](average-time-on-site.md), behalve dat bij deze metrische methode specifieke componenten van de mobiele SDK worden gebruikt als onderdeel van de berekening.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde wordt berekend met behulp van [mobiele metriek](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html) `'Total session length' / ('Launches' - 'First launches'`.
