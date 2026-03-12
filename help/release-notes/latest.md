---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 4ed79fc004e27007e4591af3d0ee14ccfb0c0582
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (maart 2026)

**Laatste update**: 11 Maart, 2026

Deze opmerkingen hebben betrekking op de releaseperiode maart 2026. De versies van Adobe Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie en beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ---- |
| **de lijsten van de Soort door veelvoudige kolommen** <br/> u kunt de gegevens van een vrije vormlijst door veelvoudige kolommen in Analysis Workspace nu sorteren, of zij dimensies of metriek zijn.<p>Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioriteitsnummering wordt weergegeven naast het sorteerpictogram.</p><p>Voor meer informatie, zie [&#x200B; Filter en sorteer vrije vormlijsten &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).</p> | donderdag 28 januari 2026 | donderdag 4 maart 2026 <p>(Oorspronkelijk gepland voor 18 februari 2026)</p> |
| **Report Builder: Het zicht van de beheerder aan alle geplande werkboeken**<br/> toe:voegen-binnen Report Builder Excel omvat een nieuwe filteroptie die beheerders toestaat om alle geplande werkboeken voor een bepaalde org te zien, ongeacht wie hen opende. Deze filteroptie is alleen beschikbaar voor analytische beheerders. Het is beschikbaar op zowel het lusje van het Werkboek als het lusje van de Oudheid wanneer het bekijken van geplande werkboeken.<p>De mogelijkheid om alle geplande werkboeken weer te geven is vooral handig wanneer u werkboeken migreert tussen gedistribueerde teams, omdat hiermee beheerders alle oudere werkboeken gemakkelijk kunnen vinden voordat ze worden gemigreerd.</p><p>Eerder konden beheerders alleen de werkboeken zien die ze hadden gepland, niet de werkboeken die door andere gebruikers waren gepland.</p><p>Voor meer informatie, zie [&#x200B; Beheerde geplande werkboeken &#x200B;](/help/analyze/report-builder/manage-schedules-reportbuilder.md).</p> | | woensdag 10 maart 2026 |
| **Update aan de Benaderende functie van de Telling**<br/> het HLL probabilistische algoritme dat in de Benaderende functie van de Telling wordt gebruikt zal spoedig worden bijgewerkt. De resulterende uitvoer voor getallen die deze functie gebruiken, kan als volgt enigszins afwijken van historische getallen:</p><ul><li>Bij het tellen van zeer kleine hoeveelheden unieke waarden, zullen de resultaten worden verbeterd om nauwkeurige tellingen te gebruiken eerder dan het gebruiken van ramingen.</li><li>Wanneer u iets groter telt, behouden telramingen dezelfde nauwkeurigheid als vóór deze update (schattingen zijn nauwkeurig binnen 5 procent van het exacte getal, 95 procent van de tijd).</li></ul><p>Voor meer informatie over de Benaderende functie van de Telling Distinct, zie [&#x200B; Benaderende Telling Distinct &#x200B;](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md#approximate-count-distinct) in [&#x200B; Geavanceerde functies &#x200B;](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md)</p> | | woensdag 10 maart 2026 |
| **Hands-on leerprogramma voor Analysis Workspace**<br/> A nieuwe hands-on leerprogramma is nu beschikbaar om nieuwe gebruikers door de grondbeginselen van het gebruiken van panelen, visualisaties, en componenten in Analysis Workspace te begeleiden. <p>(De verbinding van de Documentatie te volgen.) <!--For more information, see "Learning paths" in "Customer Journey Analytics landing page".--></p> | | donderdag 18 maart 2026 |
| **pas een verdeling op a paneel**<br/> toe u een verdeling op een paneel nu kunt toepassen. Wanneer u een uitsplitsing toepast op paneelniveau, wordt de uitsplitsing toegepast op alle kolommen in alle vrije-vormtabellen in het deelvenster. | Maart 2026 | Mei 2026 |
| **Streaming media de diensten: De planningsgegevens van de steun** <br/> u kunt geplande gegevens van voorbij levende het stromen inhoud van Media aan gemakkelijker en nauwkeuriger volgen kijkerschap nu uploaden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |

## Oplossingen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-440336, AN-440216, AN-440121, AN-438445, AN-438216, AN-437856, AN-437 776, AN-437765, AN-437365, AN-432793, AN-432094, AN-431557, AN-431200, AN-4296 21, AN-429424, AN-427973, AN-426089, AN-42583, AN-424359
**Classificaties**: AN-440143, AN-439891, AN-439844, AN-438994, AN-438057, AN-438052, AN-437 435335, AN-435150, AN-433050, AN-432062, AN-435150, AN-433050, AN-4318 429642
**de Eendelen van Gegevens en Data Warehouse**: AN-439441, AN-437086, AN-433064, AN-432121, AN-431755, AN-428239 27049, AN-425036, AN-424972, AN-423509, AN-335417, AN-283958, AN-256948
**Migratie**:
**de Uitvoer**: AN-432030
**Report Builder**: AN-437895, AN-437083, AN-434288, AN-434209, AN-433224, AN-430622
**het Melden**: AN-434545, AN-431206, AN-428043
**Geplande rapporten**:
**Segmentatie**:
**Andere**: AN-440076, AN-434783, AN-434542, AN-434233, AN-43368, AN-432138 31322, AN-431012, AN-429067, AN-423285


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Livestream verwerkingsverbeteringen** | donderdag 14 januari 2026 | Adobe is van plan om de opmaak van LiveStream-ladingen te verbeteren en te wijzigen. Deze updates zorgen voor een betere pariteit tussen LiveStream en andere Adobe Analytics-functies, zoals Analysis Workspace. Een voorproefeindpunt is beschikbaar dat u toestaat om de geplande veranderingen te testen. Zie {de versienota&#39;s van 0} LiveStream [&#x200B; voor de volledige lijst van veranderingen en voorproef eindpuntdetails. &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/) Adobe is van plan om op 13 april 2026 een harde curator te maken met de bijgewerkte payload-indeling. |
| **TLS 1.2 de verwijdering van de manuscriptsuites** | donderdag 11 februari 2026 | Kennisgeving aan beheerders: Adobe is van plan op 27 mei 2026 de ondersteuning voor de volgende TLS 1.2-coderingssuites van Adobe-servers voor gegevensverzameling te verwijderen.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li></ul><p>Voor de meeste implementaties is geen actie van de klant vereist. Deze wijziging heeft vooral invloed op analysegegevens die worden verzonden vanuit verouderde native toepassingen die verouderde TLS-bibliotheken gebruiken, en op een klein aantal webbezoekers in verouderde browsers of besturingssystemen. Als u de ondersteuning voor deze coderingssuites verwijdert, wordt de beveiliging verbeterd en wordt Adobe afgestemd op moderne coderingsstandaarden. Minder dan 0,1% van het gegevensverzamelingsverkeer is op dit moment afhankelijk van deze cijfersuites.</p> |
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
