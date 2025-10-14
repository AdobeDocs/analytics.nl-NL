---
title: Boven pagina weergeven
description: Het aantal paginaweergaven dat overeenkomt met beide regels.
feature: Metrics
exl-id: d6699880-3faa-4df9-ad49-c7998f6ce45b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Boven pagina weergeven

De de paginameningen van de &quot;Bot&quot;[&#x200B; metrische &#x200B;](overview.md) toont het aantal paginareeksen die [&#x200B; Bot regels &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) overstemden.

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd-gebaseerde afmetingen (bijvoorbeeld, [&#x200B; Dag &#x200B;](../dimensions/day.md), [&#x200B; Week &#x200B;](../dimensions/week.md), of [&#x200B; Maand &#x200B;](../dimensions/month.md))

Het gebruiken van om het even welke andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke treffer van de pagina om te zien of past het beide regels aan die uw organisatie heeft gevormd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de treffer van de pagina uitgesloten van rapportage en wordt deze metrische waarde met één verhoogd. Deze metrische waarde omvat geen kloppingen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)).
