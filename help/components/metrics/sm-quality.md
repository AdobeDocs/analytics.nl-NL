---
title: Metrische waarden voor de stroomkwaliteit van media
description: De beschikbare metriek wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Metrische waarden voor de stroomkwaliteit van media

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Quality] voor een rapportreeks toelaat. Zie [ het stromen de kwaliteitsdimensies van Media ](../dimensions/sm-quality.md) voor beschikbare dimensies.*

De metriek van de kwaliteit van de Media van het stromen verstrekt extra rapporteringsfunctionaliteit aan gegevensinzameling door de bibliotheken van de de inzamelingsmedia van het stromen. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Streaming Media Collection Add-on]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Quality]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Gemiddelde bitsnelheid | Een gewogen gemiddelde van alle bitsnelheidwaarden voor de afspeelduur van een afspeelsessie. | Media sluiten | `a.media.qoe.bitrateAverage` |
| Door bitsnelheden gewijzigde stromen | Een Booleaanse waarde die wordt geactiveerd wanneer de bitsnelheid tijdens het afspelen minstens één keer verandert. | Media sluiten | `a.media.qoe.bitrateChange` |
| Wijzigingen in bitsnelheid | Het aantal keren dat de bitsnelheid is gewijzigd. | Media sluiten | `a.media.qoe.bitrateChangeCount` |
| Door buffer beïnvloede stromen | Een Booleaanse waarde die wordt geactiveerd wanneer de video een bufferstatus heeft die minstens één keer plaatsvindt. | Media sluiten | `a.media.qoe.buffer` |
| Buffer-gebeurtenissen | Het aantal keren dat de video tijdens een afspeelsessie als buffer is opgetreden. | Media sluiten | `a.media.qoe.bufferCount` |
| Totale bufferduur | De hoeveelheid tijd die een video besteedde aan het bufferen over alle buffergebeurtenissen, in seconden. | Media sluiten | `a.media.qoe.bufferTime` |
| Druppels voor begin | Een Booleaanse waarde die activeert wanneer een gebruiker het programma sluit voordat de hoofdinhoud van een video wordt gestart. | Media sluiten | `a.media.qoe.dropBeforeStart` |
| Gedropte frames | Een geheel getal dat het totale aantal frames vertegenwoordigt dat tijdens een afspeelsessie is gedropt. | Media sluiten | `a.media.qoe.droppedFrameCount` |
| Vervallen streams die door het frame zijn beïnvloed | Een Booleaanse waarde die wordt geactiveerd wanneer frames tijdens een afspeelsessie worden neergezet. | Media sluiten | `a.media.qoe.droppedFrames` |
| Fout bij streams | Een Booleaanse waarde die wordt geactiveerd wanneer tijdens het afspelen van een video een fout optreedt. | Media sluiten | `a.media.qoe.error` |
| Foutgebeurtenissen | Een geheel getal dat het totale aantal fouten vertegenwoordigt dat tijdens een afspeelsessie is aangetroffen. | Media sluiten | `a.media.qoe.errorCount` |
| Begintijd | De hoeveelheid tijd die nodig is om een video te starten, in milliseconden. Deze waarde wordt in seconden omgezet en opgeslagen door Adobe. | Media sluiten | `a.media.qoe.timeToStart` |
