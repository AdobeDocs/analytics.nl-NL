---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 1ef9c5fc39174f9b0313fc8b738ed0da35273c18
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (januari 2026)

**Laatste update**: 14 Januari, 2026

Deze releaseopmerkingen hebben betrekking op de releaseperiode januari 2026. De versies van Adobe Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **de reeksen van de Classificatie regelbouwer** | [&#x200B; de functionaliteit van de bouwer van de 0&rbrace; Regel is nu beschikbaar in classificatiereeksen. &#x200B;](/help/components/classifications/sets/manage/rules.md) U definieert regels binnen de context van een classificatieset. De regels worden toegepast (wanneer geactiveerd) op alle rapportreeks en zeer belangrijke afmetingscombinaties die aan de classificatiereeks worden geabonneerd.</p> |  | zaterdag 23 januari 2026 |
| **Verbeterde gegevensvoer** | De volgende verbeteringen zijn beschikbaar voor gegevensfeeds:<ul><li>Verbeterde gebruikerservaring.</li><li>Nieuwe ervaring voor het maken en beheren van kolomsjablonen.</li><li>U kunt nu kiezen wanneer u een kolomsjabloon maakt voor hergebruik in toekomstige gegevensfeeds. U kunt sjablonen ook verwijderen, bewerken en kopiëren.<br/> eerder, elke gegevensvoer die werd gecreeerd resulteerde in een nieuw kolommalplaatje, dat in een groot aantal ongebruikte kolommalplaatjes en geen manier resulteerde om hen te schrappen of te beheren.</li><li>Toevoegen en filteren op tags.</li><li>Bekijk de geschiedenis van taken voor het doorvoeren van gegevens. (Wanneer de verzoekperiode begon, toen het begon, eindigde, etc.)</li><li>Verstuur of verwerk gegevensfeeds opnieuw. (Vanaf de pagina Taakgeschiedenis)</li><li>Laat aankomen toestaan. U kunt nu gegevens opnemen die zijn ontvangen nadat de gegevensinvoertaak de gegevens heeft verwerkt binnen de ingestelde rapportfrequentie.</li><li>Wanneer u een einddatum voor een gegevensinvoer kiest, wordt de einddatum die u kiest, opgenomen als de laatste dag van de gegevensinvoer.<br/> eerder, werd de einddatum uitgesloten van de gegevensvoer.</li><li>Een exportfrequentie van 15 minuten is nu mogelijk, maar is standaard niet beschikbaar. Om deze optie beschikbaar te maken in uw omgeving, dient u eerst contact op te nemen met de klantenservice van Adobe en te verzoeken dat uw rapportenpakket is geconfigureerd voor ondersteuning van 15-minuten export.</li></ul><p>**Nota:** met deze verbeteringen, worden URLs aan de pagina&#39;s van de gegevensvoer in Adobe Analytics ook bijgewerkt. Werk eventuele bestaande bladwijzers vóór 30 april 2026 bij om naar de nieuwe pagina&#39;s met gegevensfeeds te verwijzen.</p>(Koppeling met documentatie die moet worden gevolgd.)</p> | woensdag 20 januari 2026 | woensdag 24 februari 2026 <p>(Oorspronkelijk gepland voor vrijgave op 10 februari 2026)</p> |
| **de lijsten van de Soort door veelvoudige kolommen** | U kunt de gegevens van een vrije-vormlijst door veelvoudige kolommen in Analysis Workspace nu sorteren, of zij dimensies of metriek zijn.<p>Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioriteitsnummering wordt weergegeven naast het sorteerpictogram.</p><p>Voor meer informatie, zie [&#x200B; Filter en sorteer vrije vormlijsten &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).</p> | donderdag 28 januari 2026 | donderdag 18 februari 2026 |
| **Streaming media de diensten: De planningsgegevens van de steun** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |

## Oplossingen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-423389, AN-422636, AN-422482, AN-422027, AN-421134, AN-420187, AN-406 271, AN-406188, AN-405997, AN-405983, AN-405796, AN-405033, AN-404893, AN-4048 404353, AN-404352, AN-404048, AN-404353, AN-404352, AN-404048, AN-40252 3, AN-396149, AN-390990, AN-390728, AN-390646, AN-383484, AN-376980, AN-371729 AN-347570
**Classificaties**: AN-423985, AN-423092, AN-423067, AN-422913, AN-422908, AN-42793, AN-422 AN-4222126, AN-422705, AN-422422, AN-422126, AN-422098, AN-422077, AN-4220 421351, AN-406583, AN-406295, AN-406295, AN-406123, AN-40605 404743, AN-404372
**de inzameling van Gegevens**: AN-422488
**de Eendelen van Gegevens en Data Warehouse**: AN-423186, AN-422789, AN-422239, AN-421552, AN-421393, AN-42139 21231, AN-420149, AN-406345, AN-406217, AN-405073, AN-404822, AN-40474, AN-38 9691
**Privacy**:
**Report Builder**: AN-422120, AN-421937, AN-406296, AN-402951, AN-399748
**het Melden**:
**Geplande rapporten**: AN-423087, AN-422686
**de vergelijking van het Segment**:
**Andere**: AN-423401, AN-422819, AN-422775, AN-422626, AN-422238, AN-422160 2071, AN-421687, AN-420045, AN-404891, AN-404608, AN-390912


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Livestream verwerkingsverbeteringen** | donderdag 14 januari 2026 | Adobe is van plan om de opmaak van LiveStream-ladingen te verbeteren en te wijzigen. Deze updates zorgen voor een betere pariteit tussen LiveStream en andere Adobe Analytics-functies, zoals Analysis Workspace. Een voorproefeindpunt is beschikbaar dat u toestaat om de geplande veranderingen te testen. Zie {de versienota&#39;s van 0} LiveStream [ voor de volledige lijst van veranderingen en voorproef eindpuntdetails. ] Adobe is van plan om op 13 april 2026 een harde curator te maken met de bijgewerkte payload-indeling. |
| **Verouderde Report Builder** | donderdag 18 juni 2025 | De oude Report Builder-add-in wordt in juni 2026 opgeheven. Alle gebruikers zouden moeten beginnen hun erfeniswerkboeken aan [&#x200B; nieuwe Report Builder &#x200B;](/help/analyze/report-builder/rb-overview.md) te bevorderen. De nieuwe Report Builder is beschikbaar voor zowel Adobe Analytics- als Customer Journey Analytics-klanten. Het heeft [&#x200B; dichtbij eigenschappariteit &#x200B;](/help/analyze/report-builder/convert-workbooks.md#unsupported) plus vele nieuwe geschikte eigenschappen en verbeteringen UI. Om het verbeteringsproces te vergemakkelijken, omvat de nieuwe Report Builder een gemakkelijke werkboekomzettingseigenschap. De nieuwe Report Builder is alleen beschikbaar als add-in via de Microsoft Store. Vele organisaties vereisen een intern goedkeuringsproces alvorens toe:voegen-binnen ter beschikking kan worden gesteld aan gebruikers. Wacht tijd en werk nu met uw organisatie om ervoor te zorgen dat u voldoende tijd hebt om uw werkboeken te upgraden vóór de EOL-datum. |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [&#x200B; de Zorg van de Klant van Adobe &#x200B;](https://helpx.adobe.com/contact.html) te contacteren. |
| **Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [&#x200B; Adobe Analytics 2.0 API &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/console) moet migreren.</p><p>Zie [&#x200B; Adobe Analytics 1.4 API EOL FAQ &#x200B;](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [&#x200B; de versienota&#39;s van AppMeasurement &#x200B;](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [&#x200B; de versienota&#39;s van Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [&#x200B; het stromen de versienota&#39;s van de media diensten &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [&#x200B; producten van Adobe Experience Cloud &#x200B;](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
