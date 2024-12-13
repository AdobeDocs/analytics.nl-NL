---
title: Metingen in het hoofdstuk Streaming media
description: De beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat.
feature: Metrics
exl-id: bef379d5-9dc9-404f-8197-1ba66d11299d
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Metingen in het hoofdstuk Streaming media

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ Streaming het hoofdstukdimensies van Media ](../dimensions/sm-chapters.md) voor beschikbare dimensies.*

Metrische gegevens van het hoofdstuk Streaming Media bieden aanvullende rapportfunctionaliteit voor gegevensverzameling via bibliotheken voor het streamen van media-verzamelingen. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Hoofdstuk voltooit | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk is voltooid. | Hoofdstuk sluiten | `a.media.chapter.complete` |
| Hoofdstuk start | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk begint. | Begin hoofdstuk | `a.media.chapter.view` |
| Tijd van hoofdstuk doorgebracht | De hoeveelheid tijd die aan het hoofdstuk wordt doorgebracht, in seconden. | Hoofdstuk sluiten | `a.media.chapter.timePlayed` |

{style="table-layout:auto"}
