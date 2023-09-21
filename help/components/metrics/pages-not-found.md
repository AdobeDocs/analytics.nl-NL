---
title: Pagina's niet gevonden (cijfers)
description: Het aantal treffers dat een fout bevat.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Pagina&#39;s niet gevonden

*Deze Help-pagina beschrijft hoe &#39;Pagina&#39;s niet gevonden&#39; werkt als metrisch. Zie de [Pagina&#39;s niet gevonden](../dimensions/pages-not-found.md) dimensie voor meer informatie.*

&#39;Pagina&#39;s niet gevonden&#39; [metrisch](overview.md) toont het aantal treffers waar een afmeting werd geplaatst of voortgeduurd op het tijdstip dat een bezoeker een fout ontmoette. Deze metrische waarde is handig wanneer u wilt zien welke pagina&#39;s of URL&#39;s foutberichten bevatten (zoals 404). U kunt deze informatie vervolgens doorgeven aan uw webontwikkelingsteam, dat de oorzaak van de fout kan vaststellen en deze kan verhelpen.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle treffers waar [`pageType`](/help/implement/vars/page-vars/pagetype.md) variable is gelijk aan de waarde van `"errorPage"`. Het is het metrische equivalent van [Pagina&#39;s niet gevonden](../dimensions/pages-not-found.md) dimensie.
