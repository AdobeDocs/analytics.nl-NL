---
title: Metrische gegevens over het bijhouden van de status van streaming-mediaservices
description: De beschikbare metriek wanneer u [!UICONTROL Player State Tracking] voor een rapportreeks toelaat.
feature: Metrics
exl-id: 324936cc-0c7a-4710-a618-b24cc6a2c2cf
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Metrische gegevens over het bijhouden van de status van streaming-mediaservices

Streaming media services player state tracking metrics bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via streaming media services libraries. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Player State Tracking]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Streams die worden beïnvloed door ondertiteling | Wordt geactiveerd als ten minste één ondertitelingsstatus is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.closedcaptioning.set` |
| Telling van ondertiteling gesloten | Het aantal keren dat de video een Closed Captioning-status inging. | Media sluiten | `a.media.states.closedcaptioning.count` |
| Totale duur van ondertiteling gesloten | De hoeveelheid tijd dat de video in een gesloten Captioning staat was, in seconden. | Media sluiten | `a.media.states.closedcaptioning.time` |
| Streams die worden beïnvloed door volledig scherm | Wordt geactiveerd als ten minste één status Volledig scherm is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.fullscreen.set` |
| Volledig scherm | Het aantal keren dat de video de status Volledig scherm heeft ingeschakeld. | Media sluiten | `a.media.states.fullscreen.count` |
| Totale duur volledig scherm | De hoeveelheid tijd dat de video zich in een volledig scherm bevond, in seconden. | Media sluiten | `a.media.states.fullscreen.time` |
| Streams die worden beïnvloed door focus | Wordt geactiveerd als ten minste één status In focus tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.states.infocus.set` |
| In focusaantallen | Het aantal keren dat de video een status In focus heeft ingevoerd. | Media sluiten | `a.media.states.infocus.count` |
| Totale duur in focus | De hoeveelheid tijd in seconden dat de video zich in de status In focus bevond. | Media sluiten | `a.media.states.infocus.time` |
| Streams die worden beïnvloed door dempen | Wordt geactiveerd als ten minste één muistoestand is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.mute.set` |
| Aantal dempen | Het aantal keren dat de video een dempingsstatus heeft ingevoerd. | Media sluiten | `a.media.states.mute.count` |
| Totale duur dempen | De hoeveelheid tijd dat de video in een Dempestatus, in seconden was. | Media sluiten | `a.media.states.mute.time` |
| Streams beïnvloed door beeld-in-beeld | Wordt geactiveerd als ten minste één status Beeld-in-beeld is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.states.pictureinpicture.set` |
| Aantal afbeeldingen in beeld | Het aantal keren dat de video een status Beeld-in-beeld heeft ingevoerd. | Media sluiten | `a.media.states.pictureinpicture.count` |
| Totale duur van afbeelding in beeld | De hoeveelheid tijd in seconden dat de video zich in de status Beeld-in-beeld bevond. | Media sluiten | `a.media.states.pictureinpicture.time` |

{style="table-layout:auto"}
