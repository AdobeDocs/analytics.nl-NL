---
title: Metrische gegevens over het bijhouden van de status van streaming-mediaservices
description: De beschikbare metriek wanneer u [!UICONTROL Player State Tracking] voor een rapportreeks toelaat.
feature: Metrics
exl-id: 324936cc-0c7a-4710-a618-b24cc6a2c2cf
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Metrische gegevens over het bijhouden van de status van streaming-mediaservices

Streaming media services player state tracking metrics bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via streaming media services libraries. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Player State Tracking]** onder [&#x200B; Media die &#x200B;](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Streams impacted by closed captioning]** | Wordt geactiveerd als ten minste één ondertitelingsstatus is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.`<br>`closedcaptioning.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Closed captioning counts]** | Het aantal keren dat de video een Closed Captioning-status inging. | Media sluiten | `a.media.states.`<br>`closedcaptioning.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Closed captioning total duration]** | De hoeveelheid tijd dat de video in een gesloten Captioning staat was, in seconden. | Media sluiten | `a.media.states.`<br>`closedcaptioning.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Streams impacted by full screen]** | Wordt geactiveerd als ten minste één status Volledig scherm is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.`<br>`fullscreen.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Full screen counts]** | Het aantal keren dat de video de status Volledig scherm heeft ingeschakeld. | Media sluiten | `a.media.states.`<br>`fullscreen.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Full screen total duration]** | De hoeveelheid tijd dat de video zich in een volledig scherm bevond, in seconden. | Media sluiten | `a.media.states.`<br>`fullscreen.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Streams impacted by in focus]** | Wordt geactiveerd als ten minste één status In focus tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.states.`<br>`infocus.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL In focus counts]** | Het aantal keren dat de video een status In focus heeft ingevoerd. | Media sluiten | `a.media.states.`<br>`infocus.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL In focus total duration]** | De hoeveelheid tijd in seconden dat de video zich in de status In focus bevond. | Media sluiten | `a.media.states.`<br>`infocus.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Streams impacted by mute]** | Wordt geactiveerd als ten minste één muistoestand is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.`<br>`mute.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Mute counts]** | Het aantal keren dat de video een dempingsstatus heeft ingevoerd. | Media sluiten | `a.media.states.`<br>`mute.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Mute total duration]** | De hoeveelheid tijd dat de video in een Dempestatus, in seconden was. | Media sluiten | `a.media.states.`<br>`mute.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Streams impacted by picture in picture]** | Wordt geactiveerd als ten minste één status Beeld-in-beeld is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.`<br>`pictureinpicture.set` | `mediaReporting.states.`<br>`[*].isSet` |
| **[!UICONTROL Picture in picture counts]** | Het aantal keren dat de video een status Beeld-in-beeld heeft ingevoerd. | Media sluiten | `a.media.states.`<br>`pictureinpicture.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Picture in picture total duration]** | De hoeveelheid tijd in seconden dat de video zich in de status Beeld-in-beeld bevond. | Media sluiten | `a.media.states.`<br>`pictureinpicture.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
