---
title: Kwaliteitsdimensies voor streaming mediaservices
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Quality] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: e3794d8c-3c03-425d-850c-a735b579324b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Kwaliteitsdimensies voor streaming mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat. Zie [&#x200B; Streaming media de kwaliteitsmetriek van de diensten &#x200B;](../metrics/sm-quality.md) voor beschikbare metriek.*

De kwaliteitsdimensies van streaming mediaservices bieden rapportage over de kwaliteit van de inhoud die de bezoeker verbruikt. Voor het gebruik van deze afmetingen is de instructie [!UICONTROL Adobe Analytics for Streaming Media Ad-on] vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Quality]** onder [&#x200B; Media die &#x200B;](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Naam van afmetingen | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Gemiddelde bitsnelheid | De gemiddelde bitsnelheid, in 100-KBPS emket-intervallen. Deze wordt berekend als een gewogen gemiddelde van alle bitsnelheidwaarden in verhouding tot de afspeelduur voor een bepaalde afspeelsessie. | Media sluiten | `a.media.qoe.bitrateAverageBucket` |
| Wijzigingen in bitsnelheid | Het aantal wijzigingen in bitsnelheid dat is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.qoe.bitrateChangeCount` |
| Buffer-gebeurtenissen | Het aantal keren dat de mediaspeler tijdens een afspeelsessie een bufferstatus heeft ingevoerd. | Media sluiten | `a.media.qoe.bufferCount` |
| Totale bufferduur | De totale hoeveelheid tijd die wordt besteed aan bufferen, in seconden. | Media sluiten | `a.media.qoe.bufferTime` |
| Gedropte frames | Het totale aantal gedropte frames dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.droppedFrameCount` |
| Fouten | Het totale aantal fouten dat tijdens een afspeelsessie is opgetreden. | Media sluiten | `a.media.qoe.errorCount` |
| Externe fout-id&#39;s | Alle unieke fout-id&#39;s van externe bronnen, zoals CDN-fouten. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.externalErrors` |
| Player SDK-fout-id&#39;s | Alle unieke fout-id&#39;s die door de SDK van de inhoudsspeler worden gegenereerd. U moet de gewenste foutcodes of id&#39;s opgeven. Er zijn meerdere fout-id&#39;s toegestaan. | Media sluiten | `a.media.qoe.playerSdkErrors` |
| Begintijd | Deze waarde wordt standaard ingesteld op `0` als deze niet is ingesteld via het object QoSObject. Stel de waarde in milliseconden in. Analysis Workspace rapporteert deze dimensie in seconden. | Media starten, Media sluiten | `a.media.qoe.timeToStart` |

{style="table-layout:auto"}
