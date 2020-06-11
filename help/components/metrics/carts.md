---
title: Houtskaarten
description: Het aantal treffers waarbij een bezoeker het eerste product aan een winkelwagentje heeft toegevoegd.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Houtskaarten

De maatstaf &#39;Winkelwagentjes&#39; toont het aantal keren dat een bezoeker iets uit zijn winkelwagentje heeft verwijderd. Deze metrische waarde is handig wanneer u het gedeelte van de conversietrechter wilt begrijpen waarin klanten niet langer geïnteresseerd zijn in een product.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers waar `scOpen` in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele bestaat.

## Verschil tussen carts- en cartweergaven

Omdat de &quot;Wegen&quot;en &quot;de meningen van de Kaart gebeurtenissen zijn die implementatie vereisen, bepaalt uw organisatie het nauwkeurige verschil tussen deze twee metriek. Adobe heeft deze maatstaven echter ontworpen voor het volgende:

* &#39;Houttjes&#39; worden slechts één keer per aankoop geactiveerd wanneer een bezoeker zijn eerste product aan zijn winkelwagentje toevoegt.
* &#39;Winkeltoevoegingen&#39; activeren elk product dat aan de wagen wordt toegevoegd.

Voor het eerste product worden zowel &#39;Karretjes&#39; als &#39;Kart-toevoegingen&#39; geactiveerd. Ook hier zijn deze richtsnoeren niet concreet; uw organisatie bepaalt de nauwkeurige implementatielogica.
