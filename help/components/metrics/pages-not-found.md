---
title: Pagina's niet gevonden (cijfers)
description: Het aantal treffers dat een fout bevat.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# Pagina&#39;s niet gevonden

*Deze Help-pagina beschrijft hoe &#39;Pagina&#39;s niet gevonden&#39; werkt als metrisch. Zie de [Pagina&#39;s niet gevonden](../dimensions/pages-not-found.md) dimensie voor meer informatie.*

De metrische waarde &#39;Pagina&#39;s niet gevonden&#39; geeft het aantal treffers aan waar de pagina een fout bevatte. Deze metrische waarde is nuttig wanneer u wilt zien welke pagina&#39;s of URL&#39;s foutberichten bevatten (zoals 404), zodat u de oorzaak van de fout kunt bepalen en deze kunt corrigeren.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle treffers waar [`pageType`](/help/implement/vars/page-vars/pagetype.md) variable is gelijk aan de waarde van `"errorPage"`. Het is het metrische equivalent van [Pagina&#39;s niet gevonden](../dimensions/pages-not-found.md) dimensie.
