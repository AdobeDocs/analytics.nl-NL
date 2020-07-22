---
title: Instanties
description: Het aantal treffers dat een variabele is ingesteld (en niet wordt herhaald).
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---


# Instanties

Metrisch van &quot;Instanties&quot;toont het aantal tijden een afmeting uitdrukkelijk in een beeldverzoek werd bepaald. Sommige dimensies, zoals [eVars](../dimensions/evar.md), blijven dimensie-items na de hit waarop ze zijn ingesteld. Deze metrische waarde is handig wanneer u wilt zien hoe vaak een dimensie-item is ingesteld zonder de resultaten waarop die waarde betrekking heeft.

## Hoe deze metrische waarde wordt berekend

Van alle klappen in een rapportreeks, omvat slechts tochten die uitdrukkelijk een afmetingspunt in het beeldverzoek plaatsen. Bepaalde afmetingen, zoals [eVars](../dimensions/evar.md), blijven bestaan na de hit waarop ze zijn ingesteld. Metriek zoals de [paginaweergaven](page-views.md) en [Voorvallen](occurrences.md) tellen zowel initiële als permanente waarden. Deze metrische waarde telt geen persistente waarden.