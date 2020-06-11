---
title: Instanties
description: Het aantal treffers dat een variabele is ingesteld (en niet wordt herhaald).
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---


# Instanties

Metrisch van &quot;Instanties&quot;toont het aantal tijden een afmeting uitdrukkelijk in een beeldverzoek werd bepaald. Sommige dimensies, zoals [eVars](../dimensions/evar.md), behouden de waarden van de afmeting voorbij de hit waarop ze zijn ingesteld. Deze metrische waarde is handig wanneer u wilt zien hoe vaak een waarde voor de dimensie is ingesteld zonder de resultaten waarop die waarde zich bevond.

## Hoe deze metrische waarde wordt berekend

Van alle klappen in een rapportreeks, omvat slechts tochten die uitdrukkelijk een afmetingswaarde in het beeldverzoek plaatsen. Bepaalde afmetingen, zoals [eVars](../dimensions/evar.md), blijven bestaan na de hit waarop ze zijn ingesteld. Metriek zoals de [paginaweergaven](page-views.md) en [Voorvallen](occurrences.md) tellen zowel initiële als permanente waarden. Deze metrische waarde telt geen persistente waarden.