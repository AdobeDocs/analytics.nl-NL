---
title: Streaming mediaservices en dimensies
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Ads] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Streaming mediaservices en dimensies

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Ads] voor een rapportreeks toelaat. Zie [ Streaming Media en metriek ](../metrics/sm-ads.md) voor beschikbare metriek.*

Streaming-mediaservices en -dimensies bieden extra rapportagefunctionaliteit voor gegevensverzameling via Streaming-mediaservices-bibliotheken. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Ads]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Ad]** | De unieke id voor de advertentie. | Advertentie starten, en sluiten | `a.media.ad.`<br>`name` | `xdm.mediaCollection.`<br>`advertisingDetails.name`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.name` |
| **[!UICONTROL Ad name (variable)]** | De vriendelijke naam van de advertentie. Een classificatiedimensie genoemd &quot;[!UICONTROL Ad name]&quot;is ook beschikbaar, die een gelijkaardig doel verstrekt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Advertentie starten, en sluiten | `a.media.ad.`<br>`friendlyName` | `xdm.mediaCollection.`<br>`advertisingDetails.friendlyName`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.friendlyName` |
| **[!UICONTROL Ad player name]** | De naam van de speler die de advertentie rendert. | Advertentie starten, en sluiten | `a.media.ad.`<br>`playerName` | `xdm.mediaCollection.`<br>`advertisingDetails.playerName`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.playerName` |
| **[!UICONTROL Ad length (variable)]** | De lengte van de video en, in seconden. | Advertentie starten, en sluiten | `a.media.ad.`<br>`length` | `xdm.mediaCollection.`<br>`advertisingDetails.length`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.length` |
| **[!UICONTROL Ad pod]** | De unieke id voor de advertentiepod. | Advertentie starten, en sluiten | `a.media.ad.`<br>`pod` | |
| **[!UICONTROL Ad in pod position]** | De indexpositie van de advertentie binnen het bovenliggende element en het einde (geïndexeerd op 0). | Advertentie starten, en sluiten | `a.media.ad.`<br>`podPosition` | `xdm.mediaCollection.`<br>`advertisingDetails.podPosition`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.podPosition` |
| **[!UICONTROL Advertiser]** | Het bedrijf of merk in de advertentie. | Advertentie starten, en sluiten | `a.media.ad.`<br>`advertiser` | `xdm.mediaCollection.`<br>`advertisingDetails.advertiser`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.advertiser` |
| **[!UICONTROL Campaign ID]** | De id van de advertentiecampagne | Advertentie starten, en sluiten | `a.media.ad.`<br>`campaign` | `xdm.mediaCollection.`<br>`advertisingDetails.campaignID`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.campaignID` |

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| **[!UICONTROL Asset ID]** | [[!UICONTROL Content]](sm-core.md) | De unieke id voor de inhoud van het media-element. Voorbeelden zijn de aflevering-id van de tv-serie, de id van het filmelement of de livegebeurtenis. Deze id&#39;s worden doorgaans afgeleid van metagegevensautoriteiten zoals EIDR, TMS/Gracenote, Rovi of van andere bedrijfseigen of interne systemen. |
| **[!UICONTROL Content rating]** | [[!UICONTROL Content]](sm-core.md) | De classificatie zoals gedefinieerd door de ouderlijke richtlijnen van TV. |
| **[!UICONTROL First air date]** | [[!UICONTROL Content]](sm-core.md) | De datum waarop de inhoud voor het eerst op de televisie is uitgezonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt u aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| **[!UICONTROL First digital date]** | [[!UICONTROL Content]](sm-core.md) | De datum waarop de inhoud voor het eerst via een digitaal kanaal of platform is verzonden. Aangezien deze classificatiedimensie een tekenreeks is, is elke datumnotatie toegestaan. Adobe raadt u aan een consistente datumnotatie te gebruiken, zoals `YYYY-MM-DD` . |
| **[!UICONTROL Ad length]** | [!UICONTROL Ad] | De lengte van de video en, in seconden. |
| **[!UICONTROL Ad name]** | [!UICONTROL Ad] | De vriendelijke naam van de advertentie. Het is het classificatieequivalent van &#39;[!UICONTROL Ad name (variable)]&#39;. |
| **[!UICONTROL Creative ID]** | [!UICONTROL Ad] | De id van de advertentie. |
| **[!UICONTROL Pod name]** | [!UICONTROL Ad pod] | De vriendelijke naam van de advertentiepod. |
| **[!UICONTROL Pod position]** | [!UICONTROL Ad pod] | De verschuiving van het advertentieeinde binnen de inhoud, in seconden. |
