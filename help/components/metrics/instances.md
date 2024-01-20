---
title: Instanties
description: Het aantal treffers dat een variabele is ingesteld (en niet wordt herhaald).
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
source-git-commit: 813d209980ad02c412970a698c282c1358921ed6
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Instanties

De &#39;instanties&#39; [metrisch](overview.md) toont het aantal tijden een afmeting uitdrukkelijk in een beeldverzoek werd bepaald. Sommige afmetingen, zoals [eVars](../dimensions/evar.md), blijven dimensie-items voorbij de hit waarop ze zijn ingesteld. Deze metrische waarde is handig wanneer u wilt zien hoe vaak een dimensie-item is ingesteld zonder de resultaten waarop die waarde betrekking heeft.

## Hoe deze metrische waarde wordt berekend

Van alle klappen in een rapportreeks, omvat slechts tochten die uitdrukkelijk een afmetingspunt in het beeldverzoek plaatsen. Sommige afmetingen, zoals [eVars](../dimensions/evar.md)blijven staan na de hit waarop ze zijn ingesteld. Metrisch [Paginaweergaven](page-views.md) en [Voorval](occurrences.md) tel zowel aanvankelijke als blijvende waarden. Deze metrische waarde telt geen persistente waarden.

Een bezoeker arriveert bijvoorbeeld op uw site en gebruikt interne zoekopdracht. U volgt interne zoekopdracht in eVar1. Nadat ze eenmaal een interne zoekopdracht hebben uitgevoerd, bezoeken ze nog vijf pagina&#39;s voordat ze vertrekken.

Als u een rapport weergeeft in Workspace, ziet u één eVar1-instantie en zes instanties. Eén instantie telt op de pagina met zoekresultaten, terwijl de metrische waarde van het voorkomen de beginwaarde en de daaropvolgende waarden telt.

## Vergelijken met vergelijkbare cijfers

* **Instanties vs. [Voorval](occurrences.md)**: Instanties bevatten geen resultaten wanneer een dimensie-item aanwezig blijft. Komt tellingsklappen voor waar een afmetingspunt werd geplaatst of voortgeduurd.
* **Instanties vs. [Paginaweergaven](page-views.md)**: Instanties omvatten alle typen hit, inclusief aanroepen voor het bijhouden van paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)), verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) en gegevens uit samenvatting [Gegevensbronnen](/help/import/data-sources/overview.md). Metrische paginaweergaven bevatten alleen aanroepen voor het bijhouden van paginaweergaven, exclusief aanroepen voor het bijhouden van koppelingen en samenvattingsgegevensbronnen.
