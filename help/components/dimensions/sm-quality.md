---
title: Afmetingen van de stroomkwaliteit van media
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Quality] inschakelt voor een rapportsuite.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Afmetingen van de stroomkwaliteit van media

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat. Zie {de kwaliteitsmetriek van Media 0} Streaming ](../metrics/sm-quality.md) voor beschikbare metriek.*[

De afmetingen voor de streamingmedia zorgen voor rapportage over de kwaliteit van de inhoud die de bezoeker gebruikt. Voor het gebruik van deze afmetingen is de instructie [!UICONTROL Adobe Streaming Media Collection add-on] vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Quality]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Naam Dimensionen | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Gemiddelde bitsnelheid | De gemiddelde bitsnelheid, in 100-KBPS emket-intervallen. Deze wordt berekend als een gewogen gemiddelde van alle bitsnelheidwaarden in verhouding tot de afspeelduur voor een bepaalde afspeelsessie. | Media sluiten | `a.media.qoe.bitrateAverageBucket` |
| Wijzigingen in bitsnelheid | Het aantal wijzigingen in bitsnelheid dat is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.qoe.bitrateChangeCount` |
| Buffer-gebeurtenissen | Het aantal keren dat de mediaspeler tijdens een afspeelsessie een bufferstatus heeft ingevoerd. | Media sluiten | `a.media.qoe.bufferCount` |
| Totale bufferduur | De totale hoeveelheid tijd die wordt besteed aan bufferen, in seconden. | Media sluiten | `a.media.qoe.bufferTime` |
| Gedropte frames | Het totale aantal gedropte frames dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.droppedFrameCount` |
| Fouten | Het totale aantal fouten dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.errorCount` |
| Externe fout-id&#39;s | Alle unieke fout-id&#39;s van externe bronnen, zoals CDN-fouten. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.externalErrors` |
| Player SDK fout-id&#39;s | Alle unieke fout-id&#39;s die worden gegenereerd door de inhoudsspeler SDK. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.playerSdkErrors` |
| Begintijd | Deze waarde wordt standaard ingesteld op `0` als deze niet is ingesteld via het object QoSObject. Stel de waarde in milliseconden in. Analysis Workspace rapporteert deze dimensie in seconden. | Media starten, Media sluiten | `a.media.qoe.timeToStart` |

{style="table-layout:auto"}
