---
title: Orders
description: Het aantal verrichte aankopen.
feature: Metrics
exl-id: b05abb6d-983f-43fe-80ad-a0ddf90de466
source-git-commit: a1fbd3f483d3a236fe5dc3246f5e90c1b3f51ba9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Orders

De metrische &quot;Orders&quot;[&#128279;](overview.md) toont het totale aantal aankoopgebeurtenissen die op uw plaats worden gemaakt. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingspunten tot een orde hebben bijgedragen. Bijvoorbeeld, kon u de hoogste campagnes zien (gebruikend de [ het Volgen code ](../dimensions/tracking-code.md) dimensie) of hoogste interne onderzoekstermijnen (gebruikend een [ eVar ](../dimensions/evar.md)) die tot aankopen bijdroeg.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers waar `purchase` in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele bestaat.
