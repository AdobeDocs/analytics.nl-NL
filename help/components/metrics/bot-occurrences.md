---
title: Beide voorvallen
description: Het aantal treffers dat beide regels overstemde.
feature: Metrics
exl-id: 3b6cbe94-98db-4ba4-aab2-ce59cdbc420a
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Beide voorvallen

De &#39;beide voorvallen&#39; [metrisch](overview.md) toont het aantal treffers die overeenkomen [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd gebaseerde afmetingen (bijvoorbeeld [Dag](../dimensions/day.md), [Week](../dimensions/week.md), of [Maand](../dimensions/month.md))

Het gebruiken van om het even welke andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke hit om te zien of deze overeenkomt met beide regels die uw organisatie heeft geconfigureerd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de hit niet gerapporteerd en wordt deze metrische waarde met één verhoogd. Deze maatstaf omvat beide paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en link tracking hits ([`tl()`](/help/implement/vars/functions/tl-method.md)), overwegende [Boven pagina weergeven](bot-page-views.md) geen resultaten voor het bijhouden van koppelingen opnemen.
