---
title: Instanties
description: Het aantal treffers dat een variabele is ingesteld (en niet wordt herhaald).
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---

# Instanties

Metrisch van &quot;Instanties&quot;toont het aantal tijden een afmeting uitdrukkelijk in een beeldverzoek werd bepaald. Sommige afmetingen, zoals [eVars](../dimensions/evar.md), blijven dimensie-items voorbij de hit waarop ze zijn ingesteld. Deze metrische waarde is handig wanneer u wilt zien hoe vaak een dimensie-item is ingesteld zonder de resultaten waarop die waarde betrekking heeft.

## Hoe deze metrische waarde wordt berekend

Van alle klappen in een rapportreeks, omvat slechts tochten die uitdrukkelijk een afmetingspunt in het beeldverzoek plaatsen. Sommige afmetingen, zoals [eVars](../dimensions/evar.md)blijven staan na de hit waarop ze zijn ingesteld. Metrisch [Paginaweergaven](page-views.md) en [Voorval](occurrences.md) tel zowel aanvankelijke als blijvende waarden. Deze metrische waarde telt geen persistente waarden.
