---
title: Beide voorvallen
description: Het aantal treffers dat beide regels overstemde.
feature: Metrics
exl-id: 94cbbee4-8455-48b1-b804-534ed8fccdc9
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Beide voorvallen

De metrische &quot;Bot voorkomen&quot;[ ](overview.md) toont het aantal treffers die [ Bot regels ](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) overstemden.

Aangezien beide rapportages van de rest van uw gegevens van het rapportpakket worden gescheiden, werkt dit metrisch slechts met de volgende afmetingen:

* [Bot-naam](../dimensions/bot-name.md)
* [Pagina](../dimensions/page.md)
* Op tijd-gebaseerde afmetingen (bijvoorbeeld, [ Dag ](../dimensions/day.md), [ Week ](../dimensions/week.md), of [ Maand ](../dimensions/month.md))

Het gebruiken van om het even welke andere afmeting met dit metrisch keert geen gegevens terug.

## Hoe deze metrische waarde wordt berekend

Adobe controleert elke hit om te zien of deze overeenkomt met beide regels die uw organisatie heeft geconfigureerd. Als een bepaalde hit overeenkomt met een beide-regel, wordt de hit niet gerapporteerd en wordt deze metrische waarde met één verhoogd. Deze metrisch omvat zowel paginameningen ([`t()`](/help/implement/vars/functions/t-method.md)) en verbinding volgende klappen ([`tl()`](/help/implement/vars/functions/tl-method.md)), terwijl [ de meningen van de de paginapagina Bot ](bot-page-views.md) verbindingsvolgende klappen niet omvatten.
