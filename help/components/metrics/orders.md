---
title: Orders
description: Het aantal verrichte aankopen.
feature: Metrics
exl-id: b05abb6d-983f-43fe-80ad-a0ddf90de466
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# Orders

De &#39;bestellingen&#39; [metrisch](overview.md) geeft het totale aantal aankoopgebeurtenissen op uw site weer. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingspunten tot een orde hebben bijgedragen. U kunt bijvoorbeeld de bovenste campagnes zien (met de [Code bijhouden](../dimensions/tracking-code.md) dimensie of hoogste interne zoektermen (met een [eVar](../dimensions/evar.md)) die heeft bijgedragen aan aankopen.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers waar `purchase` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele.
