---
title: Streaming mediaservices - kerngegevens
description: De beschikbare metriek wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat.
feature: Metrics
exl-id: f4ff5f84-18b6-4e67-b808-133faeaf8605
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Streaming mediaservices - kerngegevens

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat. Zie [&#x200B; Streaming media diensten kernafmetingen &#x200B;](../dimensions/sm-core.md) voor beschikbare dimensies.*

De streaming media de kernmetriek van de diensten verstrekken basisrapporteringsfunctionaliteit aan gegevens die door de inzamelingsbibliotheken van de media van de stromen worden verzameld. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Core]** onder [&#x200B; Media die &#x200B;](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Average minute audience]** | De totale hoeveelheid tijd die aan een bepaald stuk van inhoud wordt doorgebracht, die door zijn lengte voor elk van zijn playbackzittingen wordt gedeeld.<br>`[Time spent] / [Media length]` | Media sluiten | `a.media.`<br>`averageMinuteAudience` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`averageMinuteAudience` |
| **[!UICONTROL Content completes]** | Triggers wanneer een stuk van inhoud voltooit. Deze maatstaf betekent niet noodzakelijkerwijs dat ze de inhoud volledig hebben bekeken, maar dat ze vooruit hadden kunnen slaan. Het betekent alleen dat ze het einde van de inhoud hebben bereikt. | | `a.media.complete` | `xdm.mediaReporting.`<br>`sessionDetails.isCompleted` |
| **[!UICONTROL Paused impacted streams]** | Een Booleaanse waarde die activeert wanneer een of meer pauzes zijn opgetreden tijdens het afspelen van inhoud. | Media sluiten | `a.media.pause` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasPauseImpactedStreams` |
| **[!UICONTROL Pause events]** | Het aantal pauzes dat is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.pauseCount` | `xdm.mediaReporting.`<br>`sessionDetails.pauseCount` |
| **[!UICONTROL Total pause duration]** | De totale duur van alle pauze-gebeurtenissen, in seconden. | Media sluiten | `a.media.pauseTime` | `xdm.mediaReporting.`<br>`sessionDetails.pauseTime` |
| **[!UICONTROL Content starts]** | Het eerste frame met media wordt gebruikt. Als een gebruiker tijdens een advertentie of tijdens het bufferen neerslaat, wordt deze gebeurtenis niet geactiveerd. | Media sluiten | `a.media.play` | `xdm.mediaReporting.`<br>`sessionDetails.isPlayed` |
| **[!UICONTROL 10% progress marker]**<br>**[!UICONTROL 25% progress marker]**<br>**[!UICONTROL 50% progress marker]**<br>**[!UICONTROL 75% progress marker]**<br>**[!UICONTROL 95% progress marker]** | De afspeelkop geeft de aangegeven markering voor inhoud op basis van lengte door. Elke markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress10`<br>`a.media.progress25`<br>`a.media.progress50`<br>`a.media.progress75`<br>`a.media.progress95` | `xdm.mediaReporting.`<br>`sessionDetails.hasProgress10`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress25`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress50`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress75`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress95` |
| **[!UICONTROL Content resumes]** | Een Booleaanse waarde die activeert wanneer de inhoud wordt hervat na meer dan 30 minuten buffertijd, pauze of wachttijd. Wordt ook geactiveerd door de speler op de trackPlay VideoInfo. | Media sluiten | `a.media.resume` | `xdm.mediaCollection.`<br>`sessionDetails.hasResume`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasResume` |
| **[!UICONTROL Content segment views]** | Een Booleaanse waarde die activeert op het eerste frame van het bekeken segment. | Media sluiten | `a.media.segmentView` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasSegmentView` |
| **[!UICONTROL Media starts]** | Een Booleaanse waarde die wordt geactiveerd wanneer het medium voor het eerst wordt geladen. Deze gebeurtenis bevat advertenties, buffering en fouten. | Start media | `a.media.view` | `xdm.mediaReporting.`<br>`sessionDetails.isViewed` |
| **[!UICONTROL Content time spent]** | De totale gebeurtenisduur voor alle gebeurtenissen van het type PLAY op de hoofdinhoud, in seconden. | Media sluiten | `a.media.timePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.timePlayed` |
| **[!UICONTROL Unique time played]** | De totale hoeveelheid tijd dat de unieke inhoud wordt afgespeeld, in seconden. Deze metrische waarde sluit de tijd uit die wordt afgespeeld wanneer herhaalde inhoud wordt weergegeven, zoals achterwaarts zoeken. | Media sluiten | `a.media.`<br>`uniqueTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`uniqueTimePlayed` |
