---
title: Gemiddelde sessielengte (mobiel)
description: De gemiddelde sessielengte voor het mobiele apparaat.
translation-type: tm+mt
source-git-commit: 625af73ad2fbe4b44bce00a122c4e65d8964323f
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Gemiddelde sessielengte (mobiel)

De metrische waarde &#39;Gemiddelde sessielengte (mobiel)&#39; geeft de gemiddelde tijdsduur aan dat een bepaalde afmetingswaarde per afmetingswaarde aanwezig is. Het is gelijkaardig aan de [Gemiddelde tijd op plaats](average-time-on-site.md) metrisch, behalve dit metrisch gebruikt mobiele SDK specifieke componenten als deel van zijn berekening.

## Hoe deze metrische waarde wordt berekend

Deze metrisch wordt berekend gebruikend de [mobiele metriek](https://docs.adobe.com/content/help/en/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html) `'Total session length' / ('Launches' - 'First launches'`.
