---
title: Basisdimensies voor streaming mediaservices
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Core] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 1316a646-a31a-49a4-a670-d56d90dd462b
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Basisdimensies voor streaming mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat. Zie [ Streaming media diensten kernmetriek ](../metrics/sm-core.md) voor beschikbare metriek.*

De belangrijkste dimensies van de streaming media diensten verstrekken basisrapporteringsfunctionaliteit aan gegevens die door het stromen de dienstenbibliotheken van media worden verzameld. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Core]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Content]** | Inhoud-id van de inhoud. | Media starten, Media sluiten | `a.media.`<br>`name` | `xdm.mediaCollection.`<br>`sessionDetails.name`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.name` |
| **[!UICONTROL Content channel]** | Het distributiestation of kanaal waar de inhoud wordt gespeeld. Elke tekenreekswaarde is geldig. | Media starten, Media sluiten | `a.media.`<br>`channel` | `xdm.mediaCollection.`<br>`sessionDetails.channel`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.channel` |
| **[!UICONTROL Content length (variable)]** | De maximumlengte (of duur) van de verbruikte inhoud, in seconden. Deze afmeting wordt vereist voor verscheidene metriek, met inbegrip van &quot;[!UICONTROL Average minute audience]&quot;. Als deze afmeting niet wordt geplaatst, zijn de afhankelijke metriek niet beschikbaar.<br><br> de classificatiedimensie van A genoemd &quot;[!UICONTROL Video length]&quot;is ook beschikbaar, die een gelijkaardig doel verstrekt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Media starten, Media sluiten | `a.media.`<br>`length` | `xdm.mediaCollection.`<br>`sessionDetails.length`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.length` |
| **[!UICONTROL Content name (variable)]** | De vriendelijke naam van de inhoud. Een classificatie genoemd &quot;[!UICONTROL Video name]&quot;is ook beschikbaar, die een gelijkaardig doel verstrekt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Media starten, Media sluiten | `a.media.`<br>`friendlyName` | `xdm.mediaCollection.`<br>`sessionDetails.friendlyName`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.friendlyName` |
| **[!UICONTROL Content player name]** | De naam van de inhoudsspeler. | Media starten, Media sluiten | `a.media.`<br>`playerName` | `xdm.mediaCollection.`<br>`sessionDetails.playerName`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.playerName` |
| **[!UICONTROL Content segment]** | Het interval dat het gedeelte van de inhoud beschrijft dat is weergegeven, in minuten. Het segment wordt berekend als min en max van de waarden van de afspeelkop tijdens een afspeelsessie. | Media sluiten | `a.media.`<br>`segment` | `xdm.mediaReporting.`<br>`sessionDetails.segment` |
| **[!UICONTROL Content type]** | Het type inhoud. Geldige waarden zijn `song` , `podcast` , `audiobook` , `radio` , `VoD` , `Live` , `Linear` , `UGC` , `DVoD` of een aangepaste waarde. | Media starten, Media sluiten | `a.contentType` | `xdm.mediaCollection.`<br>`sessionDetails.contentType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.contentType` |
| **[!UICONTROL Media path]** | Het pad dat de bezoeker heeft gekozen om de inhoud te bereiken. | Start media | `a.media.path` | |
| **[!UICONTROL Stream type]** | Het streamtype. Geldige waarden zijn `audio` en `video` . | Media starten, Media sluiten | `a.media.`<br>`streamType` | `xdm.mediaCollection.`<br>`sessionDetails.streamType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.streamType` |

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| **[!UICONTROL Video length]** | [!UICONTROL Content] | De maximumlengte (of duur) van de verbruikte inhoud, in seconden. De metriek die van inhoudslengte afhangen kan deze classificatie niet gebruiken; u moet berekende metrisch tot stand brengen om metriek zoals &quot;[!UICONTROL Average minute audience]&quot;te verkrijgen gebruikend deze classificatie. |
| **[!UICONTROL Video name]** | [!UICONTROL Content] | De vriendelijke naam van de inhoud. Het is het classificatieequivalent van &#39;[!UICONTROL Content name (variable)]&#39;. |
