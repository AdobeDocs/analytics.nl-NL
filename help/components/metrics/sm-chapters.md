---
title: Metingen in het hoofdstuk Streaming media
description: De beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Metingen in het hoofdstuk Streaming media

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ Streaming het hoofdstukdimensies van Media ](../dimensions/sm-chapters.md) voor beschikbare dimensies.*

Metrische gegevens van het hoofdstuk Streaming Media bieden aanvullende rapportfunctionaliteit voor gegevensverzameling via bibliotheken voor het streamen van media-verzamelingen. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Streaming Media Collection Add-on]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Hoofdstuk voltooit | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk is voltooid. | Hoofdstuk sluiten | `a.media.chapter.complete` |
| Hoofdstuk start | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk begint. | Begin hoofdstuk | `a.media.chapter.view` |
| Tijd van hoofdstuk doorgebracht | De hoeveelheid tijd die aan het hoofdstuk wordt doorgebracht, in seconden. | Hoofdstuk sluiten | `a.media.chapter.timePlayed` |

{style="table-layout:auto"}
