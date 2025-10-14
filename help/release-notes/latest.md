---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 46d2360e8314d5b21e141799477b0f67367e56df
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (release oktober 2025)

**Laatste update**: 14 oktober 2025

Deze opmerkingen hebben betrekking op de releaseperiode van oktober tot begin november 2025. De versies van Adobe Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **criteria van de Filter inbegrepen in lijnvisualisaties en sparklines** | Alle zoekfiltercriteria die u toepast op een tabelfilter in vrije vorm worden nu altijd opgenomen in de sparklines. Bovendien kunt u de criteria van de onderzoeksfilter in om het even welke verbonden lijnvisualisatie omvatten.<p>U kunt lijnvisualisaties vormen om de criteria van de onderzoeksfilter te omvatten door sparkline in de metrische kolomkopbal van de verbonden lijst te selecteren.</p><p>Eerder waren de criteria van de onderzoeksfilter niet inbegrepen in vonklines of verbonden lijnvisualisaties.</p><p>Voor meer informatie, zie [&#x200B; trended gegevens van de Mening voor een vrije vormlijst &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md).</p> | | donderdag 15 oktober 2025 |
| **Analyseer AI verkeer met een nieuw de afmetingspunt van het Type van Referteur** | Een nieuw het type van Referrer afmetingspunt zal beschikbaar zijn helpen verkeer analyseren dat uit hulpmiddelen AI komt. <p>Dit nieuwe het type van Referteur afmetingspunt, genoemd de Gelijke hulpmiddelen van AI, zal groeperen verwijzend domeinen van belangrijke hulpmiddelen AI, toestaand u om tendensen voor de groep als geheel te bekijken. De initiële lijst met verwijzende domeinen in deze nieuwe categorie omvat (maar is niet beperkt tot):</p><ul><li>chatgpt.com</li><li>claude.ai</li><li>m365.cloud.microsoft</li><li>grok.com</li><li>gemini.google.com</li><li>perplexity.ai</li></ul><p>Het nieuwe dimensie-item is beschikbaar in alle aan Adobe Analytics gerelateerde tools, zoals Analysis Workspace, Report Builder, Data Warehouse, Data Feeds, enzovoort.</p><p>Overweeg het volgende wanneer het gebruiken van dit nieuwe afmetingspunt:</p><ul><li>Het is niet altijd mogelijk om verwijzingsverkeer te onderscheiden dat van resultaten kwam die op &quot;AI wijze&quot;in een onderzoeksmotor worden verstrekt tegenover die die uit klikproductie van traditionele onderzoeksresultaten kwamen.</li><li>Het nieuwe Conversational AI hulpmiddeldimensie punt concentreert zich op belangrijke leveranciers met het meeste verkeer. Een nieuwe trend onthult een stijgend aantal imitatorplaatsen met domeinen gelijkend op belangrijke AI hulpmiddelleveranciers. Dit is waarschijnlijk het gevolg van het gemak waarmee personen of groepen hun eigen AI-tools kunnen maken en deze op internet kunnen hosten. Omdat dit een snel evoluerende ruimte is, gelieve het ondersteuningsteam van Adobe te contacteren als u vindt dat een populaire plaats niet inbegrepen is.</li><li>De dimensie van het verwijzingstype, met inbegrip van het nieuwe Conversational AI hulpmiddelen afmetingspunt, is beschikbaar slechts voor gegevens die door Adobe Analytics worden verwerkt. </li></ul><p>(Koppeling met documentatie die moet worden gevolgd.)</p> |   | donderdag 15 oktober 2025 |
| **Streaming media de diensten: De planningsgegevens van de steun** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>(De verbinding van de Documentatie te volgen.) <!--For more information, see [Upload schedule data to track live content](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/track-schedule-data)--></p> |  | donderdag 29 oktober 2025 |
| **Streaming media de diensten: Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Bij het verzamelen van streaming mediagegevens in Adobe Experience Platform, moeten de XDM-veldpaden die worden weergegeven onder de kop &quot;XDM Field Path&quot; van de documentatie voor Streaming Media-parameters, niet langer worden gebruikt. In plaats daarvan, moeten de klanten die de analytische bronschakelaar uitvoerden om het stromen media gegevens in Platform vóór 9 Mei te verzamelen, 2025 hun bestaande configuraties aan mediaReporting gebiedspaden, zoals aangetoond onder de rubriek van &quot;het Pad van het Gebied van XDM&quot;van de het stromen de parameterdocumentatie van Media te migreren.<p> Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [&#x200B; Audio en videoparameters &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/audio-video-parameters), [&#x200B; Advertentieparameters &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/ad-parameters), [&#x200B; de parameters van het Hoofdstuk &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/chapter-parameters), [&#x200B; de staatsparameters van de Speler &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/player-state-parameters), en [&#x200B; de parameters van de Kwaliteit &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/quality-parameters). (Geen actie wordt vereist voor klanten die de bron van Analytics schakelaar na 9 Mei, 2025 uitvoeren, en reeds mediaReporting XDM wegen gebruiken.)</p><p>Gegevensinvoer op de afgekeurde XDM-veldpaden gaat door tot eind oktober 2025. Na die tijd, zullen de afgekeurde gebiedspaden volledig worden verwijderd en niet meer zichtbaar in het Schema UI van Adobe Experience Platform, en de gegevens zullen worden verzonden slechts gebruikend mediaReporting gebiedspaden.</p><p>Voor meer informatie, zie [&#x200B; migreren een implementatie van de Verbinding van Analytics Source aan bijgewerkte het stromen van XDM media gebieden &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. </p> |  | Oktober 2025 |
| **Adobe Analytics 2.0 API de reeksverwezenlijking van het Rapport** | Maak rapportsuites in Adobe Analytics met de 2.0 API&#39;s. De nieuwe POST-methode vervangt de API-aanmaak van de 1.4-rapportsuite ter voorbereiding op de aanstaande veroudering van de 1.4-API&#39;s. | | 26 oktober 2022 |

## Oplossingen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-399209, AN-397146, AN-394992, AN-390795
**Classificaties**: AN-400583, AN-399205, AN-398580, AN-398257, AN-395921, AN-394973
**de inzameling van Gegevens**:
**de Eendelen van Gegevens en Data Warehouse**: AN-400938, AN-399075, AN-398924, AN-398573, AN-396574, AN-393946
**Privacy**:
**Report Builder**: AN-401127, AN-400618, AN-392971, AN-391692
**het Melden**:
**Geplande rapporten**:
**de vergelijking van het Segment**:
**Andere**: AN-396084


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Verouderde Report Builder** | donderdag 18 juni 2025 | De oude Report Builder-add-in wordt in juni 2026 opgeheven. Alle gebruikers zouden moeten beginnen hun erfeniswerkboeken aan [&#x200B; nieuwe Report Builder &#x200B;](/help/analyze/report-builder/rb-overview.md) te bevorderen. De nieuwe Report Builder is beschikbaar voor zowel Adobe Analytics- als Customer Journey Analytics-klanten. Het heeft [&#x200B; dichtbij eigenschappariteit &#x200B;](/help/analyze/report-builder/convert-workbooks.md#unsupported) plus vele nieuwe geschikte eigenschappen en verbeteringen UI. Om het verbeteringsproces te vergemakkelijken, omvat de nieuwe Report Builder een gemakkelijke werkboekomzettingseigenschap. De nieuwe Report Builder is alleen beschikbaar als add-in via de Microsoft Store. Vele organisaties vereisen een intern goedkeuringsproces alvorens toe:voegen-binnen ter beschikking kan worden gesteld aan gebruikers. Wacht tijd en werk nu met uw organisatie om ervoor te zorgen dat u voldoende tijd hebt om uw werkboeken te upgraden vóór de EOL-datum. |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [&#x200B; de Zorg van de Klant van Adobe &#x200B;](https://helpx.adobe.com/nl/contact.html) te contacteren. |
| **Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [&#x200B; Adobe Analytics 2.0 API &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/console) moet migreren.</p><p>Zie [&#x200B; Adobe Analytics 1.4 API EOL FAQ &#x200B;](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [&#x200B; de versienota&#39;s van AppMeasurement &#x200B;](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [&#x200B; de versienota&#39;s van Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=nl-NL)
* [&#x200B; het stromen de versienota&#39;s van de media diensten &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* De recentste versie werkt voor [&#x200B; producten van Adobe Experience Cloud &#x200B;](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
