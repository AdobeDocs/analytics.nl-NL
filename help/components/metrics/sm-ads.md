---
title: Streaming-mediaservices en meetgegevens
description: De beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Streaming-mediaservices en meetgegevens

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [ Streaming media diensten en dimensies ](../dimensions/sm-ads.md) voor beschikbare dimensies.*

Streaming-mediaservices en metriek bieden aanvullende rapportagefuncties voor gegevensverzameling via bibliotheken met streaming-mediaservices. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Ad completes]** | Wordt geactiveerd wanneer een video is voltooid. | Advertentie sluiten | `a.media.ad.complete` | `xdm.mediaReporting.`<br>`advertisingDetails.isCompleted` |
| **[!UICONTROL Ad starts]** | Wordt geactiveerd wanneer een video-advertentie wordt gestart. | Ad Start | `a.media.ad.view` | `xdm.mediaReporting.`<br>`advertisingDetails.isStarted` |
| **[!UICONTROL Ad time spent]** | De totale hoeveelheid tijd die is besteed aan het bekijken van de advertentie, in seconden. | Advertentie sluiten | `a.media.ad.timePlayed` | `xdm.mediaReporting.`<br>`advertisingDetails.timePlayed` |
| **[!UICONTROL Media time spent]** | Hiermee wordt de gebeurtenisduur voor alle gebeurtenissen &#39;[!UICONTROL Play]&#39; (zowel hoofd- als advertentie-inhoud) in seconden samengevat. | Media sluiten | `a.media.totalTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.totalTimePlayed` |
