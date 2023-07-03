---
title: Beide voorvallen
description: Het aantal treffers dat beide regels overstemde.
feature: Metrics
exl-id: 3b6cbe94-98db-4ba4-aab2-ce59cdbc420a
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Beide voorvallen

De maatstaf &#39;Bot occurrences&#39; toont het aantal treffers dat overeenkomt [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd gebaseerde afmetingen (bijvoorbeeld [Dag](../dimensions/day.md), [Week](../dimensions/week.md), of [Maand](../dimensions/month.md))

Het gebruiken van een andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke treffer om te zien of past het beide regels aan die uw organisatie heeft gevormd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de hit niet gerapporteerd en wordt deze metrische waarde met één verhoogd. Deze maatstaf omvat beide paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en link tracking hits ([`tl()`](/help/implement/vars/functions/tl-method.md)), overwegende [Bodt paginaweergaven](bot-page-views.md) geen resultaten voor het bijhouden van koppelingen opnemen.
