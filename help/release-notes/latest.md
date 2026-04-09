---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 5dde5298f522d6045f8872c878f6796dcfa0f710
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (april 2026)

**Laatste update**: 9 April, 2026

Deze opmerkingen hebben betrekking op de releaseperiode van april 2026. De versies van Adobe Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie en beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ---- |
| {de verbeteringen van Activity Map **Activity Map van 0} omvatten de volgende verhogingen:**<br/></p><ul><li>Ondersteuning voor de Activity Map Overlay-extensie met Web SDK-implementaties van Adobe Analyticcs.</li><li>Ondersteuning voor WebSDK-tracking (wanneer de tracking naar Analytics gaat).</li><li>Bijgewerkte opmaak in de hele gebruikersinterface.</li></ul><p>(Koppeling met documentatie die moet worden gevolgd.)</p> | | April 2026 |
| **MCP servers voor Adobe Analytics** <br/> u kunt Adobe Analytics in uw bestaande agentische werkschema&#39;s nu binden gebruikend MCP (ModelProtocol van de Context). U kunt rapporten en inzichten vragen in de natuurlijke taal.<p>(Koppeling met documentatie die moet worden gevolgd.)</p> | | Eind april 2026 |
| **Streaming media de diensten: De planningsgegevens van de steun** <br/> u kunt geplande gegevens van voorbij levende het stromen inhoud van Media aan gemakkelijker en nauwkeuriger volgen kijkerschap nu uploaden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |
| **de Extra API het formatteren van de datumwaaier**<br/> Twee nieuwe formaten worden nu gesteund voor het specificeren van datumwaaiers in Analytics 2.0 API- rapportverzoeken. Dit omvat een datumformule en een gemengde indeling. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#date-range-field--supported-formats) | | Maart 2026 |
| **Facultatieve afmeting in API verzoeken van het rapport**<br/> de afmetingsvoorwerp van A wordt niet vereist in de verzoeken van het Rapport API. Als geen afmeting wordt gespecificeerd, toont de reactie gegevens voor een rapport van Totalen. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#using-dimension-in-report-payload-requests) | | Maart 2026 |
| **Datum-trended gevorderd geavanceerd API rapport**<br/> Nieuwe Adobe Analytics 2.0 API Datum-trended Geavanceerde Gids van het Rapport. Maak geavanceerde date-trended API-rapporten met behulp van vergelijkingen tussen datumbereiken en segmenten. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/advanced/) | | Maart 2026 |

## Oplossingen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-442813, AN-442410, AN-441943, AN-441717, AN-434855, AN-431409, AN-429 777, AN-429048, AN-428892, AN-428189, AN-425215
**Classificaties**: AN-443453, AN-443275, AN-443148, AN-442906, AN-442232, AN-442207, AN-42 441901, AN-441807, AN-441671, AN-441901, AN-441807, AN-441671, AN-4413 AN-441149, AN-441132, AN-441085, AN-441048, AN-440846, AN-440727, AN-4071 440511, AN-440496, AN-432100
**de Eendelen van Gegevens en Data Warehouse**: AN-442211, AN-441719, AN-441183, AN-441011, AN-440625, AN-438953
**Migratie**: AN-442467, AN-440380, AN-440357
**de Uitvoer**:
**Report Builder**: AN-441136, AN-438147, AN-425150
**het Melden**: AN-441506, AN-440919, AN-440545, AN-440300
**de suites van het Rapport**: AN-439429, AN-439423, AN-430988
**Geplande rapporten**:
**Segmentatie**:
**Andere**: AN-423359, AN-406242, AN-397985


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Livestream verwerkingsverbeteringen** | donderdag 14 januari 2026 | Adobe is van plan om de opmaak van LiveStream-ladingen te verbeteren en te wijzigen. Deze updates zorgen voor een betere pariteit tussen LiveStream en andere Adobe Analytics-functies, zoals Analysis Workspace. Een voorproefeindpunt is beschikbaar dat u toestaat om de geplande veranderingen te testen. Zie {de versienota&#39;s van 0} LiveStream [&#x200B; voor de volledige lijst van veranderingen en voorproef eindpuntdetails. &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/) Adobe is van plan om op 13 april 2026 een harde curator te maken met de bijgewerkte payload-indeling. |
| **TLS 1.2 de verwijdering van de manuscriptsuites** | donderdag 11 februari 2026 | Kennisgeving aan beheerders: Adobe is van plan op 27 mei 2026 de ondersteuning voor de volgende TLS 1.2-coderingssuites van Adobe-servers voor gegevensverzameling te verwijderen.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_GCM_SHA256`</li><li>`TLS_RSA_WITH_AES_256_GCM_SHA384`</li></ul><p>Voor de meeste implementaties is geen actie van de klant vereist. Deze wijziging heeft vooral invloed op analysegegevens die worden verzonden vanuit verouderde native toepassingen die verouderde TLS-bibliotheken gebruiken, en op een klein aantal webbezoekers in verouderde browsers of besturingssystemen. Als u de ondersteuning voor deze coderingssuites verwijdert, wordt de beveiliging verbeterd en wordt Adobe afgestemd op moderne coderingsstandaarden. Minder dan 0,1% van het gegevensverzamelingsverkeer is op dit moment afhankelijk van deze cijfersuites.</p> |
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
