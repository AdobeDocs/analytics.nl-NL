---
title: Kwaliteitsdimensies voor streaming mediaservices
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Quality] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: e3794d8c-3c03-425d-850c-a735b579324b
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Kwaliteitsdimensies voor streaming mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat. Zie [ Streaming media de kwaliteitsmetriek van de diensten ](../metrics/sm-quality.md) voor beschikbare metriek.*

De kwaliteitsdimensies van streaming mediaservices bieden rapportage over de kwaliteit van de inhoud die de bezoeker verbruikt. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Quality]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Naam van afmetingen | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Average bitrate]** | De gemiddelde bitsnelheid, in 100-KBPS emket-intervallen. Deze wordt berekend als een gewogen gemiddelde van alle bitsnelheidwaarden in verhouding tot de afspeelduur voor een bepaalde afspeelsessie. | Media sluiten | `a.media.qoe.`<br>`bitrateAverageBucket` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrate`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateAverageBucket` |
| **[!UICONTROL Bitrate changes]** | Het aantal wijzigingen in bitsnelheid dat is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.qoe.`<br>`bitrateChangeCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrateChangeCount`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateChangeCount` |
| **[!UICONTROL Buffer events]** | Het aantal keren dat de mediaspeler tijdens een afspeelsessie een bufferstatus heeft ingevoerd. | Media sluiten | `a.media.qoe.`<br>`bufferCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bufferCount` |
| **[!UICONTROL Total buffer duration]** | De totale hoeveelheid tijd die wordt besteed aan bufferen, in seconden. | Media sluiten | `a.media.qoe.`<br>`bufferTime` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bufferTime` |
| **[!UICONTROL Dropped frames]** | Het totale aantal gedropte frames dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.`<br>`droppedFrameCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`droppedFrames`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`droppedFrames` |
| **[!UICONTROL Errors]** | Het totale aantal fouten dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.`<br>`errorCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`errorCount` |
| **[!UICONTROL External error IDs]** | Alle unieke fout-id&#39;s van externe bronnen, zoals CDN-fouten. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.`<br>`externalErrors` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`externalErrors` |
| **[!UICONTROL Player SDK error IDs]** | Alle unieke fout-id&#39;s die door de SDK van de inhoudsspeler worden gegenereerd. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.`<br>`playerSdkErrors` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`playerSdkErrors` |
| **[!UICONTROL Time to start]** | Deze waarde wordt standaard ingesteld op `0` als deze niet is ingesteld via het object QoSObject. Stel de waarde in milliseconden in. Analysis Workspace rapporteert deze dimensie in seconden. | Media starten, Media sluiten | `a.media.qoe.`<br>`timeToStart` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`timeToStart`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`timeToStart` |
