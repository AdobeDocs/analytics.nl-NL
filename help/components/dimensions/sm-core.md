---
title: Basisdimensies voor streaming mediaservices
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Core] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 1316a646-a31a-49a4-a670-d56d90dd462b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 1%

---

# Basisdimensies voor streaming mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat. Zie [ Streaming media diensten kernmetriek ](../metrics/sm-core.md) voor beschikbare metriek.*

De belangrijkste dimensies van de streaming media diensten verstrekken basisrapporteringsfunctionaliteit aan gegevens die door het stromen de dienstenbibliotheken van media worden verzameld. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Core]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Inhoud | Inhoud-id van de inhoud. | Media starten, Media sluiten | `a.media.name` |
| Inhoudskanaal | Het distributiestation of kanaal waar de inhoud wordt gespeeld. Elke tekenreekswaarde is geldig. | Media starten, Media sluiten | `a.media.channel` |
| Lengte van inhoud (variabele) | De maximumlengte (of duur) van de verbruikte inhoud, in seconden. Deze dimensie is vereist voor verschillende meeteenheden, waaronder &#39;Gemiddeld aantal minuten voor publiek&#39;. Als deze afmeting niet wordt geplaatst, zijn de afhankelijke metriek niet beschikbaar.<br><br> de classificatieafmeting van A genoemd &quot;Video lengte&quot;is ook beschikbaar, die een gelijkaardig doel verstrekt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Media starten, Media sluiten | `a.media.length` |
| Inhoudsnaam (variabele) | De vriendelijke naam van de inhoud. Er is ook een classificatie met de naam &#39;Videonaam&#39; beschikbaar, die een vergelijkbaar doel biedt. Deze dimensie en de classificatie worden behandeld als twee verschillende dimensies. | Media starten, Media sluiten | `a.media.friendlyName` |
| Naam van inhoudspeler | De naam van de inhoudsspeler. | Media starten, Media sluiten | `a.media.playerName` |
| Inhoudssegment | Het interval dat het gedeelte van de inhoud beschrijft dat is weergegeven, in minuten. Het segment wordt berekend als min en max van de waarden van de afspeelkop tijdens een afspeelsessie. | Media sluiten | `a.media.segment` |
| Inhoudstype | Het type inhoud. Geldige waarden zijn `song` , `podcast` , `audiobook` , `radio` , `VoD` , `Live` , `Linear` , `UGC` , `DVoD` of een aangepaste waarde. | Media starten, Media sluiten | `a.contentType` |
| Media-pad | Het pad dat de bezoeker heeft gekozen om de inhoud te bereiken. | Start media | `a.media.path` |
| Het type Stream | Het streamtype. Geldige waarden zijn `audio` en `video` . | Media starten, Media sluiten | `a.media.streamType` |

{style="table-layout:auto"}

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| Videolengte | Inhoud | De maximumlengte (of duur) van de verbruikte inhoud, in seconden. Metriek die van inhoudslengte afhangen kan deze classificatie niet gebruiken; u moet berekende metrisch tot stand brengen om metriek zoals &quot;Gemiddeld minieme publiek&quot;te verkrijgen gebruikend deze classificatie. |
| Videonaam | Inhoud | De vriendelijke naam van de inhoud. Dit is het classificatiequivalent van Content Name (variable). |

{style="table-layout:auto"}
