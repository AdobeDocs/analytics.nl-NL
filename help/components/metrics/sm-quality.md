---
title: Kwaliteitsgegevens voor streaming mediaservices
description: De beschikbare metriek wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat.
feature: Metrics
exl-id: a64829b5-d45b-44c6-80c3-5acf1a6d9919
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Kwaliteitsgegevens voor streaming mediaservices

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat. Zie {de kwaliteitsdimensies van 0} Streaming van de media diensten [ voor beschikbare afmetingen.](../dimensions/sm-quality.md)*

Kwaliteitsgegevens voor streaming mediaservices bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via bibliotheken met streaming-mediaservices. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Quality]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Average bitrate]** | Een gewogen gemiddelde van alle bitsnelheidwaarden voor de afspeelduur van een afspeelsessie. | Media sluiten | `a.media.qoe.`<br>`bitrateAverage` | `xdm.mediaReporting.`<br>`qoeDataDetails.bitrateAverage` |
| **[!UICONTROL Bitrate change impacted streams]** | Een Booleaanse waarde die wordt geactiveerd wanneer de bitsnelheid tijdens het afspelen minstens één keer verandert. | Media sluiten | `a.media.qoe.`<br>`bitrateChange` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasBitrateChangeImpactedStreams` |
| **[!UICONTROL Bitrate changes]** | Het aantal keren dat de bitsnelheid is gewijzigd. | Media sluiten | `a.media.qoe.`<br>`bitrateChangeCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrateChangeCount`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateChangeCount` |
| **[!UICONTROL Buffer impacted streams]** | Een Booleaanse waarde die wordt geactiveerd wanneer de video een bufferstatus heeft die minstens één keer plaatsvindt. | Media sluiten | `a.media.qoe.`<br>`buffer` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasBufferImpactedStreams` |
| **[!UICONTROL Buffer events]** | Het aantal keren dat de video tijdens een afspeelsessie als buffer is opgetreden. | Media sluiten | `a.media.qoe.`<br>`bufferCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.bufferCount` |
| **[!UICONTROL Total buffer duration]** | De hoeveelheid tijd die een video besteedde aan het bufferen over alle buffergebeurtenissen, in seconden. | Media sluiten | `a.media.qoe.`<br>`bufferTime` | `xdm.mediaReporting.`<br>`qoeDataDetails.bufferTime` |
| **[!UICONTROL Drops before start]** | Een Booleaanse waarde die activeert wanneer een gebruiker het programma sluit voordat de hoofdinhoud van een video wordt gestart. | Media sluiten | `a.media.qoe.`<br>`dropBeforeStart` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`isDroppedBeforeStart` |
| **[!UICONTROL Dropped frames]** | Een geheel getal dat het totale aantal frames vertegenwoordigt dat tijdens een afspeelsessie is gedropt. | Media sluiten | `a.media.qoe.`<br>`droppedFrameCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.droppedFrames`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.droppedFrames` |
| **[!UICONTROL Dropped frame impacted streams]** | Een Booleaanse waarde die wordt geactiveerd wanneer frames tijdens een afspeelsessie worden neergezet. | Media sluiten | `a.media.qoe.`<br>`droppedFrames` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasDroppedFrameImpactedStreams` |
| **[!UICONTROL Error impacted streams]** | Een Booleaanse waarde die wordt geactiveerd wanneer tijdens het afspelen van een video een fout optreedt. | Media sluiten | `a.media.qoe.`<br>`error` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasErrorImpactedStreams` |
| **[!UICONTROL Error events]** | Een geheel getal dat het totale aantal fouten vertegenwoordigt dat tijdens een afspeelsessie is aangetroffen. | Media sluiten | `a.media.qoe.`<br>`errorCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.errorCount` |
| **[!UICONTROL Time to start]** | De hoeveelheid tijd die nodig is om een video te starten, in milliseconden. Adobe converteert deze waarde en slaat deze op in seconden. | Media sluiten | `a.media.qoe.`<br>`timeToStart` | `xdm.mediaCollection.`<br>`qoeDataDetails.timeToStart`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.timeToStart` |
