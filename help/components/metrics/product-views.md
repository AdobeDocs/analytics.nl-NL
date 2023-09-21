---
title: Productweergaven
description: Het aantal weergaven aan productpagina's.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Productweergaven

De &#39;productweergaven&#39; [metrisch](overview.md) toont het aantal keren dat een product is bekeken. Deze metrische waarde is handig wanneer u de meest bekeken producten wilt zien of wilt zien hoe de totale productweergave zich in de loop der tijd ontwikkelt.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers die aanpassen **ofwel** van het volgende:

* De waarde `prodView` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele; of
* De [`products`](/help/implement/vars/page-vars/products.md) de variabele wordt ingesteld en de `events` variable is empty.
