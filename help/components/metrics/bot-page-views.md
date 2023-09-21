---
title: Boven pagina weergeven
description: Het aantal paginaweergaven dat overeenkomt met beide regels.
feature: Metrics
exl-id: 9b1efcb1-10ca-40fb-8f20-e6da105366d9
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Boven pagina weergeven

De weergaven Boot-pagina [metrisch](overview.md) toont het aantal overeenkomende pagina-treffers [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd gebaseerde afmetingen (bijvoorbeeld [Dag](../dimensions/day.md), [Week](../dimensions/week.md), of [Maand](../dimensions/month.md))

Het gebruiken van om het even welke andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke getroffen pagina om te zien of past het beide regels aan die uw organisatie heeft gevormd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de treffer van de pagina uitgesloten van rapportage en wordt deze metrische waarde met één verhoogd. Deze metrische waarde bevat geen treffers voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)).
