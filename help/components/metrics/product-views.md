---
title: Productweergaven
description: Het aantal weergaven aan productpagina's.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# Productweergaven

De metrische weergave &#39;Productweergave&#39; toont het aantal keren dat een product is weergegeven. Deze metrische waarde is handig wanneer u de meest bekeken producten wilt zien of wilt zien hoe de totale productweergave zich in de loop der tijd ontwikkelt.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers die aanpassen **ofwel** van het volgende:

* De waarde `prodView` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele; of
* De [`products`](/help/implement/vars/page-vars/products.md) variabele wordt ingesteld en er zijn geen winkelwagentgebeurtenissen in de `events` variabele. Elke gebeurtenis die niet van toepassing is (`event1` - `event1000`) is een winkelwagentje.
