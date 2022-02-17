---
title: Houtskaarten
description: Het aantal treffers waarbij een bezoeker het eerste product aan een winkelwagentje heeft toegevoegd.
feature: Metrics
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Houtskaarten

De maatstaf &#39;Kaarten&#39; toont het aantal treffers waar een bezoeker zijn eerste product aan een winkelwagen heeft toegevoegd.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers waar `scOpen` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele.

## Verschil tussen carts- en cartweergaven

Omdat de &quot;Wegen&quot;en &quot;de meningen van de Kaart gebeurtenissen zijn die implementatie vereisen, bepaalt uw organisatie het nauwkeurige verschil tussen deze twee metriek. Nochtans, ontwierp Adobe deze metriek voor het volgende:

* &#39;Houttjes&#39; worden slechts één keer per aankoop geactiveerd wanneer een bezoeker zijn eerste product aan zijn winkelwagentje toevoegt.
* &#39;Winkeltoevoegingen&#39; activeren elk product dat aan de wagen wordt toegevoegd.

Voor het eerste product worden zowel &#39;Karretjes&#39; als &#39;Kart-toevoegingen&#39; geactiveerd. Ook hier zijn deze richtsnoeren niet concreet; uw organisatie bepaalt de nauwkeurige implementatielogica.
