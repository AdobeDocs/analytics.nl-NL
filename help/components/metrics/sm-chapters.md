---
title: Hoofdstukgegevens voor streaming-mediaservices
description: De beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat.
feature: Metrics
exl-id: bef379d5-9dc9-404f-8197-1ba66d11299d
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Hoofdstukgegevens voor streaming-mediaservices

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ Streaming media de hoofdstukdimensies van de diensten ](../dimensions/sm-chapters.md) voor beschikbare dimensies.*

De het hoofdstukmetriek van de de media van het stromen de diensten verstrekken extra rapporteringsfunctionaliteit aan gegevensinzameling door de inzamelingsbibliotheken van de media van de stromen. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Chapter completes]** | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk is voltooid. | Hoofdstuk sluiten | `a.media.chapter.complete` | `xdm.mediaReporting.`<br>`chapterDetails.isCompleted` |
| **[!UICONTROL Chapter starts]** | Een Booleaanse waarde die wordt geactiveerd wanneer een hoofdstuk begint. | Begin hoofdstuk | `a.media.chapter.view` | `xdm.mediaReporting.`<br>`chapterDetails.isStarted` |
| **[!UICONTROL Chapter time spent]** | De hoeveelheid tijd die aan het hoofdstuk wordt doorgebracht, in seconden. | Hoofdstuk sluiten | `a.media.chapter.timePlayed` | `xdm.mediaReporting.`<br>`chapterDetails.timePlayed` |
