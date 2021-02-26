---
description: Deze sectie bevat de belangrijkste concepten voor de Adobe Analytics, een korte beschrijving van het concept, en een specifieke documentatiekoppeling met extra informatie over het onderwerp.
title: Adobe Analytics - Belangrijkste concepten
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 96%

---


# Adobe Analytics - Belangrijkste concepten

Deze sectie bevat de belangrijkste concepten voor de Adobe Analytics, een korte beschrijving van het concept, en een specifieke documentatiekoppeling met extra informatie over het onderwerp.

## Analytics-tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Product | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| Analysis Workspace | Browseroplossing voor het bouwen van robuuste, aangepaste analyseprojecten en democratiserende inzichten. Biedt meer rapportflexibiliteit dan Reports and Analytics | [Analysis Workspace home](/help/analyze/analysis-workspace/home.md) |
| Reports and Analytics (voorheen SiteCatalyst) | Browseroplossing voor rapportage en analyse. Startertool in het Analytics-pakket. | [Reports and Analytics home](/help/analyze/reports-analytics/getting-started.md) |
| Report Builder | Excel-invoegtoepassing waarmee u aangepaste verzoeken van de gegevens kunt maken op basis van Adobe Analytics-data, en deze visualiseren met Microsoft Excel. | [Report Builder Home](/help/analyze/report-builder/home.md) |
| Data Workbench (voorheen Insight) | Ontworpen voor het verzamelen, verwerken, analyseren en visualiseren van data van zowel online als offline klanteninteracties via meerdere kanalen. | [Data Workbench-client](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html) |
| Data Warehouse | Onbewerkte gegevens voor opslag en aangepaste rapporten, die u kunt uitvoeren door de data te filteren. Niveau niet bereikt. | [Data Warehouse Home](/help/export/data-warehouse/data-warehouse.md) |
| Adobe Mobile Services | Verenigt mobiele marketingmogelijkheden voor mobiele applicaties uit de hele Adobe Experience Cloud, zodat u de betrokkenheid van gebruikers met uw applicaties kunt begrijpen en verbeteren. | [Mobile Services Home](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (voorheen Genesis) | Importeer trackingdata van applicaties van derden naar Analytics, zodat de prestaties op één centrale locatie volledig zichtbaar zijn. Met ingang van 1 augustus 2021 is Adobe voornemens de integratie van gegevensconnectors te beëindigen. | [Data Connectors Home](/help/import/data-connectors/data-connectors-eol.md) |
| Dynamic Tag Management (DTM) | Hiermee kunt u uw Analytics-, Target- en andere tags op al uw sites beheren, ongeacht het aantal domeinen. | [DTM Home](/help/implement/other/dtm/dtm-implementation-overview.md) |
| Adobe Launch | De volgende generatie mogelijkheden voor websitetags en mobiel SDK-beheer van Adobe. | [Adobe Launch Home](https://docs.adobe.com/content/help/en/launch/using/overview.html) |

## Belangrijke terminologie {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klik [hier](/help/technotes/terms.md) voor een uitgebreide woordenlijst met termen in Adobe Analytics.

| Term | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| Props (aangepast verkeer) | Dimensies voor het traceren van de verkeersactiviteit op de site per pagina. Props blijven niet bestaan tussen pagina&#39;s. Belangrijke toepassingen van verkeersvariabelen: <ul> <li>Eenvoudig tellen om ‘de populairste’ van een bepaalde waarde te vinden</li> <li>Zichtbaarheid van de weg die gebruikers volgen door uw site</li> </ul> <br>Voorbeelden van verkeersvariabelen: paginanaam, sitesecties, browsers. | [Props](/help/admin/admin/c-traffic-variables/traffic-var.md) |
| eVar (aangepaste conversie) | Dimensies die gedurende een door u aangepaste periode blijven bestaan. Opties voor vervaldatums zijn onder andere het verlopen van gebeurtenissen, bezoeken of X-dagen. Deze opties moeten worden gestuurd door het type analyse dat op de betreffende variabele wordt uitgevoerd. <br> Belangrijke verschillen tussen eVars en props: <ul> <li>Props worden vaak gebruikt voor padanalyse omdat persistentie is verwijderd.</li> <li>eVars worden vaak gebruikt voor conversieanalyse.</li> </ul> <br>Voorbeelden van conversievariabelen: interne zoektermen, interne aanbiedingen, externe campagnes (s.campaign). | [eVars](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) |
| Gebeurtenissen/cijfers (s.events) | Cijfers die belangrijke acties meten waarvan wij willen dat de bezoekers ze op onze site uitvoeren. Er zijn drie typen gebeurtenissen: teller, numerieke waarden en valuta. Gebeurtenissen zijn vooral handig wanneer ze worden toegevoegd aan eVar-rapporten (conversievariabelen). De eVar geeft kwalitatieve informatie over wat er is gebeurd en de gebeurtenis geeft kwantitatieve informatie over wat er is gebeurd. <br> Belangrijke verschillen tussen eVars en gebeurtenissen: <ul> <li>eVars vertellen ons wie en wat invloed heeft gehad op welke conversie</li> <li>Gebeurtenissen meet hoeveel conversies hebben plaatsgevonden</li> </ul> <br> Voorbeelden van conversiegebeurtenissen: bestellingen, applicaties starten, leads, omzet. | [Gebeurtenissen](/help/admin/admin/c-success-events/success-event.md) |
| Onderdelen | Dimensies, cijfers, segmenten en tijdgranulariteit (datumbereiken) die u naar een project kunt slepen en neerzetten. | [Onderdelen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) |
| Dimensies | Verzameling van eVars, profielen, classificaties en standaard door Adobe verzamelde waarden. | [Dimensies](/help/components/dimensions/overview.md) |
| Cijfers | Verzameling van geïmplementeerde gebeurtenissen en berekende standaarden. | [Cijfers](/help/analyze/analysis-workspace/components/apply-create-metrics.md) |
| Berekende standaarden | Mogelijkheid om aangepaste cijfers af te leiden van bestaande cijfers die door uw implementatie zijn vastgelegd. | [Berekende standaarden](/help/components/c-calcmetrics/cm-overview.md) |
| Segmenten | Mogelijkheid om krachtige, doelgerichte doelgroepsegmenten te maken, te beheren, te delen en toe te passen op uw Analytics-rapporten. Segmenten worden gedeeld tussen Analytics-producten en kunnen worden gedeeld in de Experience Cloud. | [Segmentering](/help/components/segmentation/seg-home.md) |
| Tijd (datumbereiken) | Mogelijkheid om datums te filteren in elke tijdsperiode en aangepaste datumbereiken te maken die opnieuw kunnen worden gebruikt in uw analyse. | [Datumbereik](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md) |
| Visualisaties | Rijke beelden die data tot leven kunnen brengen in uw projecten. | [Visualisaties](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) |
| Curation | Mogelijkheid om de onderdelen te beperken die toegankelijk zijn in een project of vitruele rapportsuite. | [VRS-kromming](/help/components/vrs/vrs-components.md) <br> [Projectcursus](/help/analyze/analysis-workspace/curate-share/curate.md) |

## Belangrijke verslagen

| Rapport | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| Lijst met volledige dimensies/rapporten | Definitie van alle dimensies/rapporten die beschikbaar zijn in Adobe Analytics. | [Dimensies](/help/components/dimensions/overview.md) |
| Advertising Analytics | Analyseer al uw Google- en Bing-paid-searchdata naast elkaar in Adobe Analytics. Dimensies die door de integratie worden gemaakt, zijn advertentieplatform, trefwoord, typeovereenkomst, enz. De gecreëerde cijfers zijn AMO-impressies, AMO-klikken, AMO-kosten, gemiddelde, positie en gemiddelde kwaliteitsscore. | [Advertising Analytics](/help/integrate/c-advertising-analytics/overview.md) |
| Audience Analytics | Verrijk binnenkomende Analytics-treffers met het doelgroepslidmaatschap van een gebruiker in AAM. u kunt AAM-doelgroepsdata zoals demografische informatie (bijv. geslacht of inkomensniveau), psychografische informatie (bijv. interesses en hobby&#39;s), CRM-data en impressiedata opnemen in elke Analytics-workflow. Dimensies die door deze integratie worden gemaakt, zijn doelgroeps-id en doelgroepnaam. | [Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md) |
| Attribution IQ | Hiermee krijgt u inzicht in de manier waarop zinvolle betrokkenheid plaatsvindt tijdens een klanttraject, door een intelligente identificatie van beslissingspunten die klanten bij de beoogde resultaten brengen, waarmee u uw marketinginitiatieven effectief kunt optimaliseren. De modellen omvatten eerste, laatste, lineair, participatie, j-vormig, omgekeerd j-vormig, u-vorm, dezelfde aanraking, aangepast en tijdverval. | [Attribution IQ](/help/analyze/analysis-workspace/c-panels/attribution.md) |
| Anomaliedetectie | Een statistische methode om te bepalen hoe een bepaalde meting is gewijzigd ten opzichte van eerdere data. AD is standaard ingeschakeld voor alle trendvisualisaties in de Analysis Workspace. | [Anomaliedetectie](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| Contributieanalyse | Onderzoekt het “waarom” achter de optredende anomalieën door een geautomatiseerde analyse uit te voeren van elk cijfer en elke dimensie waartoe u toegang hebt. | [Contributieanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| Cohortanalyse | Een cohort is een groep mensen die gedurende een bepaalde periode een aantal kenmerken delen. Cohortanalyse helpt bij het analyseren van het behoud en verloop van uw gebruikers. | [Cohortanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) |
| Klanttrajectrapporten | Hier wordt informatie weergegeven over het pad dat uw gebruikers door uw site of app volgen. Prop, eVars en gebeurtenissen kunnen in deze analyse in de Analysis Workspace worden gebruikt. | [Analysis Workspace Fallout](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md) <br> [Analysis Workspace Flow](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) <br> [Reports and Analytics-paden](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) |
| Marketingkanalen | Rapporten die u helpen ontdekken welke externe kanalen gebruikers naar uw site leiden en welke het meest effectief zijn voor conversie. Biedt attributieweergaven van eerste en laatste aanraking. Dit is het aangewezen externe rapport voor verkeersbronnen in Adobe Analytics (meer dan Campagnes of de Verkeersbronnen) omdat dit de meest uitgebreide blik geeft op betaalde en organische kanalen. | [Marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) |
| Mobile | Hier wordt informatie weergegeven over websites die via een mobiel apparaat of tablet worden benaderd. | [Mobiel rapport](/help/components/dimensions/mobile-dimensions.md) |
| Mobiele app | Geeft basisgebruiksgegevens weer over uw mobiele apps. Deze rapporten zijn beschikbaar zodra onze SDK is geïmplementeerd en de rapportage is ingeschakeld.  Daarnaast heeft Adobe Mobile Services een aparte mobiele app-interface gemaakt met uitgebreidere appdata, waarmee u de betrokkenheid van gebruikers bij uw apps kunt begrijpen en verbeteren.  Ga [hier](https://mobilemarketing.adobe.com) naar de interface. | [Adobe Mobile Services](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) |
| Producten | Bepaalt hoe afzonderlijke producten en productgroepen (categorieën) bijdragen aan de diverse conversiecijfers zoals omzet of aantal betalingen. | [Productrapport](/help/components/dimensions/product.md) |
| Segmentvergelijking | Ontdekt de statistisch meest significante verschillen tussen segmenten door een geautomatiseerde analyse van elk cijfer en elke dimensie waartoe u toegang hebt. | [Segmentvergelijking](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) |
| Rapport Sitecontent | Geeft informatie weer over welke pagina&#39;s en gebieden van uw site het meest actief zijn en welke servers het meest worden gebruikt. | [Rapport Sitecontent](/help/components/dimensions/page.md) |
| Rapport Sitecijfers | Geeft kwantitatieve informatie over uw website weer zoals unieke bezoekers, bestellingen, omzet, enzovoort. Elk cijfer kan worden opgenomen rapporten van verschillende items. | [Rapport Sitecijfers](/help/components/metrics/overview.md) |
| Bezoekersprofiel | Rapporten die u helpen aankooppatronen van klanten van diverse profielcategorieën (zoals landen, staten, postcodes en domeinen) te zien. | [Bezoekersprofiel](/help/components/dimensions/language.md) |
| Bezoekersbehoud | Geeft informatie weer over de loyaliteit van uw klanten, bijvoorbeeld hoeveel bezoekers hoe vaak naar uw site terugkeren. | [Bezoekersbehoud](/help/components/dimensions/customer-loyalty.md) |
| Projecten koppelen, delen en plannen | Methoden om uw werk op te slaan en/of te delen met anderen in de Analytics-interface. | [Bestanden verzenden en plannen](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md) |

## Belangrijke cijfers {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Naam cijfer | Definitie | Documentatiekoppeling |
| --- | --- | --- |
| Volledige lijst cijfers | Definitie van alle cijfers in Adobe Analytics. | [Overzicht van cijfers](/help/components/metrics/overview.md) |
| Unieke bezoekers | Het aantal niet-dubbele bezoekers van de website gedurende een bepaalde periode. | [Unieke bezoekers](/help/components/metrics/unique-visitors.md) |
| Bezoeken | Een reeks paginaweergaven tijdens een sessie. Het bezoek begint wanneer iemand een pagina op de site voor het eerst weergeeft, en eindigt na 30 minuten inactiviteit. | [Bezoeken](/help/components/metrics/visits.md) |
| Paginaweergaven | Een paginaweergave treedt op wanneer een bezoeker een pagina op uw website weergeeft. | [Paginaweergaven](/help/components/metrics/page-views.md) |
| Instanties | Het aantal keren dat een variabele is gedefinieerd. Telkens wanneer Adobe Analytics een waarde binnen een variabele ziet, worden de instanties vermeerderd met 1 in het betreffende rapport. | [Instanties](/help/components/metrics/instances.md) |
| Voorvallen | Het aantal keren dat een variabele is gedefinieerd of bleef bestaan. | [Voorvallen](/help/components/metrics/occurrences.md) |

## Importopties {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Optie | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| Classificatie-import | Importeert metadata op vastgelegde dimensies via browser of FTP-upload. Handmatige methode vergeleken met Rule Builder. | [Classificatie-import](/help/components/classifications/importer/c-working-with-saint.md) |
| Rule Builder | Maak automatisch metadataclassificaties van dimensies op basis van door de gebruiker gedefinieerde regels. | [Classification Rule Builder](/help/components/classifications/crb/classification-rule-builder.md) |
| Klantkenmerken | CRM-data die naar Experience Cloud zijn geüpload voor gebruik in Adobe Analytics en Adobe Target. | [Klantkenmerken](https://docs.adobe.com/content/help/nl-NL/core-services/interface/customer-attributes/attributes.html) |
| Databronnen | Importeert offline cijfers in Analytics op dimensies of eenvoudig per dag. | [Databronnen](/help/import/c-data-sources/datasrc-home.md) |
| Adobe Exchange Data Connectors | Zie [Analytics-tools.](/help/import/data-connectors/data-connectors-eol.md) |  |
| Native integratie | Audience Analytics en Advertising Analytics. | Zie de sectie “Belangrijke rapporten”. |

## Exportopties {#concept_C62B688E259141CF92C048E8110464BE}

| Optie | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| UI-downloads en -planning | Exporteert data vanuit Analysis Workspace als CSV of PDF. | [PDF- of CSV-bestanden downloaden](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Zie Tools voor Analytics. |  |
| Analytics-API | Maak zelf aangepaste query&#39;s voor Analytics-data. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Zie Tools voor Analytics. |  |
| Analytics-datafeed | De meest granulaire manier om data uit Analytics te halen. Stel een feed op basis van trefferniveau op vanuit Analytics. | [Analytics-datafeed](/help/export/analytics-data-feed/data-feed-overview.md) |

## Dataverzameling en -validatie {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/bron | Beschrijving | Documentatiekoppeling |
| --- | --- | --- |
| Bronnen voor ontwikkelaars | Documentatie met een overzicht van de bibliotheken die beschikbaar zijn voor het verzamelen van Analytics-data op alle beschikbare platforms (web, mobiele app, video, flash, enz.) | [Documenten voor ontwikkelaars](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementatiehandleiding | Een beschrijving van dataverzamelingsvariabelen en details over het implementeren van code voor dataverzameling in JavaScript. | [Implementatiehandleiding](/help/implement/home.md) |
| App-meting (s_code) | Globaal variabelenbeheer. | [AppMeasurement](/help/implement/js/migrate-from-hcode.md) |
| App-SDK’s | Aangepast pakket met een vooraf ingevulde versie van het configuratiebestand voor apps. | <ul><li>[iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/en/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM en Adobe Launch | Zie Tools voor Analytics. |  |
| VISTA | Hiermee kunt u serverlogica toepassen om data te wijzigen of te segmenteren terwijl deze worden verzameld. | [VISTA-regels](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md) |
| Verwerkingsregels | Mogelijkheid om variabelen in te stellen, te wijzigen en te kopiëren in de Analytics-UI om te wijzigen welke data worden verzameld. | [Verwerkingsregels](/help/admin/admin/c-processing-rules/processing-rules.md) |
| Foutopsporingsopties | Er zijn verscheidene debuggers en pakketsniffers beschikbaar helpen uw implementatie, met inbegrip van debugger van Adobe Experience Cloud bevestigen. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=nl) |
| API voor data-invoer | De API voor het invoegen van data biedt een mechanisme voor dataverzameling op de server en verzending naar Experience Cloud-servers. In plaats van JavaScript-beacons op elke webpagina te gebruiken voor het verzenden van bezoekersdata naar Experience Cloud-servers worden met serverdataverzameling alleen data verzameld op basis van webbrowserverzoeken en webserverreacties. | [Stappen voor de implementatie de API voor het invoegen van Adobe Analytics-data met POST](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
