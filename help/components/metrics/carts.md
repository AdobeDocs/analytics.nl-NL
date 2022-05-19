---
title: Houtskaarten
description: Het aantal treffers waarbij een bezoeker het eerste product aan een winkelwagentje heeft toegevoegd.
feature: Metrics
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
source-git-commit: 932a6c1452d4710b11c1ce5551c845ef6721f137
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Houtskaarten

De maatstaf &#39;Kaarten&#39; toont het aantal treffers waar een bezoeker zijn eerste product aan een winkelwagen heeft toegevoegd.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers waar `scOpen` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele.

## Verschil tussen carts, Cart views en Cart additions

Aangezien &#39;Kaarten&#39;, &#39;Kaartweergaven&#39; en &#39;Kart-toevoegingen&#39; gebeurtenissen zijn die implementatie vereisen, bepaalt uw organisatie het exacte verschil tussen deze meetgegevens. Nochtans, ontwierp Adobe deze metriek voor de volgende logica:

* &#39;Houttjes&#39; worden slechts één keer per aankoop geactiveerd wanneer een bezoeker zijn eerste product aan zijn winkelwagentje toevoegt.
* De weergave &#39;Winkelwagentje&#39; wordt telkens geactiveerd wanneer een bezoeker zijn winkelwagentje bekijkt.
* &#39;Winkeltoevoegingen&#39; activeren elk product dat aan de wagen wordt toegevoegd.

Wanneer een klant zijn eerste product aan een winkelwagentje toevoegt, is het beoogde gedrag dat zowel de toevoeging van &quot;Houttjes&quot; als &quot;Kart&quot; wordt geactiveerd. Ook hier zijn deze richtsnoeren niet concreet; uw organisatie bepaalt de nauwkeurige implementatielogica.
