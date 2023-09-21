---
title: Instanties
description: Het aantal treffers dat een variabele is ingesteld (en niet wordt herhaald).
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---

# Instanties

De &#39;instanties&#39; [metrisch](overview.md) toont het aantal tijden een afmeting uitdrukkelijk in een beeldverzoek werd bepaald. Sommige afmetingen, zoals [eVars](../dimensions/evar.md), blijven dimensie-items voorbij de hit waarop ze zijn ingesteld. Deze metrische waarde is handig wanneer u wilt zien hoe vaak een dimensie-item is ingesteld zonder de resultaten waarop die waarde betrekking heeft.

## Hoe deze metrische waarde wordt berekend

Van alle klappen in een rapportreeks, omvat slechts tochten die uitdrukkelijk een afmetingspunt in het beeldverzoek plaatsen. Sommige afmetingen, zoals [eVars](../dimensions/evar.md)blijven staan na de hit waarop ze zijn ingesteld. Metrisch [Paginaweergaven](page-views.md) en [Voorval](occurrences.md) tel zowel aanvankelijke als blijvende waarden. Deze metrische waarde telt geen persistente waarden.

Een bezoeker arriveert bijvoorbeeld op uw site en gebruikt interne zoekopdracht. U volgt interne zoekopdracht in eVar1. Nadat ze eenmaal een interne zoekopdracht hebben uitgevoerd, bezoeken ze nog vijf pagina&#39;s voordat ze vertrekken.

Als u een rapport weergeeft in Workspace, ziet u één eVar1-instantie en zes instanties. Het ene exemplaar dat op de pagina met zoekresultaten wordt geactiveerd, terwijl het voorval zowel de beginwaarde als de blijvend waarden heeft geteld.
