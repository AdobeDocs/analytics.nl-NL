---
title: Streaming-mediaservices en meetgegevens
description: De beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Streaming-mediaservices en meetgegevens

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [&#x200B; Streaming media diensten en dimensies &#x200B;](../dimensions/sm-ads.md) voor beschikbare dimensies.*

Streaming-mediaservices en metriek bieden aanvullende rapportagefuncties voor gegevensverzameling via bibliotheken met streaming-mediaservices. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [&#x200B; Media die &#x200B;](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Advertentie voltooid | Wordt geactiveerd wanneer een video is voltooid. | Advertentie sluiten | `a.media.ad.complete` |
| Advertentie wordt gestart | Wordt geactiveerd wanneer een video-advertentie wordt gestart. | Ad Start | `a.media.ad.view` |
| Toegevoegde tijd | De totale hoeveelheid tijd die is besteed aan het bekijken van de advertentie, in seconden. | Advertentie sluiten | `a.media.ad.timePlayed` |
| Mediatijd besteed | Hiermee wordt de gebeurtenisduur voor alle PLAY-gebeurtenissen (zowel hoofd- als advertentie-inhoud) in seconden samengevat. | Media sluiten | `a.media.totalTimePlayed` |

{style="table-layout:auto"}
