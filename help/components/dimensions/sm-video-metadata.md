---
title: Metagegevens van videoservices streamen
description: Beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Metagegevens van videoservices streamen

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Video Metadata] voor een rapportreeks toelaat. Zie [ Streaming media diensten videometriek van metriek ](../metrics/sm-video-metadata.md) voor beschikbare metriek.*

Streaming media services en dimensies bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via bibliotheken voor het verzamelen van streaming mediaservices. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Video Metadata]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Ad loads]** | Het type geladen advertentie. | | `a.media.adLoad` | `xdm.mediaCollection.`<br>`sessionDetails.adLoad` |
| **[!UICONTROL Day part]** | De tijd van de dag waarop de inhoud werd uitgezonden of afgespeeld. Elke tekenreekswaarde wordt ondersteund. | Media starten, Media sluiten | `a.media.dayPart` | `xdm.mediaCollection.`<br>`sessionDetails.dayPart`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.dayPart` |
| **[!UICONTROL Episode]** | Het afleveringsnummer. | Media starten, Media sluiten | `a.media.episode` | `xdm.mediaCollection.`<br>`sessionDetails.episode`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.episode` |
| **[!UICONTROL Media feed type]** | Het type diervoeder. | Media starten, Media sluiten | `a.media.feed` | `xdm.mediaCollection.`<br>`sessionDetails.feed`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.feed` |
| **[!UICONTROL Genre]** | Het type of de groep inhoud zoals gedefinieerd door de inhoudsproducent. Deze dimensie ondersteunt meerdere waarden, gescheiden door komma&#39;s. | Media starten, Media sluiten | `a.media.genre` | `xdm.mediaCollection.`<br>`sessionDetails.genre`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.genreList` |
| **[!UICONTROL MVPD]** | De MVPD zoals opgegeven door Adobe-verificatie. | Media starten, Media sluiten | `a.media.pass.mvpd` | `xdm.mediaCollection.`<br>`sessionDetails.mvpd`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.mvpd` |
| **[!UICONTROL Network]** | De netwerk- of kanaalnaam. | Media starten, Media sluiten | `a.media.network` | `xdm.mediaCollection.`<br>`sessionDetails.network`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.network` |
| **[!UICONTROL Season]** | Het seizoensnummer waartoe de show behoort. | Media starten, Media sluiten | `a.media.season` | `xdm.mediaCollection.`<br>`sessionDetails.season`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.season` |
| **[!UICONTROL Show]** | De naam van het programma of de serie. | Media starten, Media sluiten | `a.media.show` | `xdm.mediaCollection.`<br>`sessionDetails.show`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.show` |
| **[!UICONTROL Show type]** | Een geheel getal dat het type inhoud vertegenwoordigt.<br>`0`: Volledige episode <br>`1`: Voorproef of aanhangwagen <br>`2`: Clip <br>`3`: Andere | Media starten, Media sluiten | `a.media.type` | `xdm.mediaCollection.`<br>`sessionDetails.showType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.showType` |

