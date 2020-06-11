---
title: Productweergaven
description: Het aantal weergaven aan productpagina's.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Productweergaven

De metrische weergave &#39;Productweergave&#39; toont het aantal keren dat een product is weergegeven. Deze metrische waarde is handig wanneer u de meest bekeken producten wilt zien of wilt zien hoe de totale productweergave zich in de loop der tijd ontwikkelt.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal treffers die **één van beiden** van het volgende aanpassen:

* De waarde `prodView` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele. of
* De [`products`](/help/implement/vars/page-vars/products.md) `events` variabele wordt ingesteld en de variabele bevat geen winkelwagentgebeurtenissen. Elke gebeurtenis die niet op maat is (`event1` - `event1000`), is een winkelwagentje.