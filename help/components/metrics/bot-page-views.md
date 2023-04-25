---
title: Bodt paginaweergaven
description: Het aantal paginaweergaven dat overeenkomt met beide regels.
source-git-commit: 61a0292bf2f8ff22b414c2e91da476c1da69d163
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Bodt paginaweergaven

De maatstaf van de weergave Bot-pagina toont het aantal overeenkomende pagina-hits [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd gebaseerde afmetingen (bijvoorbeeld [Dag](../dimensions/day.md), [Week](../dimensions/week.md), of [Maand](../dimensions/month.md))

Het gebruiken van een andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke getroffen pagina om te zien of past het beide regels aan die uw organisatie heeft gevormd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de treffer van de pagina uitgesloten van rapportage en wordt deze metrische waarde met één verhoogd. Deze metrische waarde bevat geen treffers voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)).
