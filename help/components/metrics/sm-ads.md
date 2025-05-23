---
title: Streaming media en meetgegevens
description: De beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Streaming media en meetgegevens

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [ Streaming Media en dimensies ](../dimensions/sm-ads.md) voor beschikbare afmetingen.*

Streaming media en metriek bieden aanvullende rapportfunctionaliteit voor gegevensverzameling via bibliotheken voor het streamen van mediaverzamelingen. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Advertentie voltooid | Wordt geactiveerd wanneer een video is voltooid. | Advertentie sluiten | `a.media.ad.complete` |
| Advertentie wordt gestart | Wordt geactiveerd wanneer een video-advertentie wordt gestart. | Ad Start | `a.media.ad.view` |
| Toegevoegde tijd | De totale hoeveelheid tijd die is besteed aan het bekijken van de advertentie, in seconden. | Advertentie sluiten | `a.media.ad.timePlayed` |
| Mediatijd besteed | Hiermee wordt de gebeurtenisduur voor alle PLAY-gebeurtenissen (zowel hoofd- als advertentie-inhoud) in seconden samengevat. | Media sluiten | `a.media.totalTimePlayed` |

{style="table-layout:auto"}
