---
description: Deze sectie bevat de belangrijkste concepten voor de Adobe Analytics, een korte beschrijving van het concept, en een specifieke documentatiekoppeling met extra informatie over het onderwerp.
title: Adobe Analytics - Belangrijkste concepten
translation-type: tm+mt
source-git-commit: 4b6107fe57787e639fb06ef957d6230d1bc45bd1
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 99%

---


# Adobe Analytics - Belangrijkste concepten

Deze sectie bevat de belangrijkste concepten voor de Adobe Analytics, een korte beschrijving van het concept, en een specifieke documentatiekoppeling met extra informatie over het onderwerp.

## Analytics-tools {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| Product | Beschrijving | Documentatiekoppeling |
|--- |--- |--- |
| Analysis Workspace | Browseroplossing voor het bouwen van robuuste, aangepaste analyseprojecten en democratiserende inzichten. Biedt meer rapportflexibiliteit dan Reports &amp; Analytics. | [adobe.ly/aaworkspacedocs](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) |
| Reports &amp; Analytics (voorheen SiteCatalyst) | Browseroplossing voor rapportage en analyse. Startertool in het Analytics-pakket. | [Reports &amp; Analytics Home](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/getting-started.html) |
| Report Builder | Excel-invoegtoepassing waarmee u aangepaste verzoeken van de gegevens kunt maken op basis van Adobe Analytics-data, en deze visualiseren met Microsoft Excel. | [Report Builder Home](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/home.html) |
| Ad Hoc Analysis (voorheen Discover) | Java-gebaseerde tool voor geavanceerde digitale analyse. | [Ad Hoc Analysis Home](https://docs.adobe.com/content/help/en/analytics/analyze/ad-hoc-analysis/adhoc-home.html) |
| Data Workbench (voorheen Insight) | Ontworpen voor het verzamelen, verwerken, analyseren en visualiseren van data van zowel online als offline klanteninteracties via meerdere kanalen. | [Data Workbench-client](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html) |
| Data Warehouse | Onbewerkte gegevens voor opslag en aangepaste rapporten, die u kunt uitvoeren door de data te filteren. Niveau niet bereikt. | [Data Warehouse Home](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) |
| Adobe Mobile Services | Verenigt mobiele marketingmogelijkheden voor mobiele applicaties uit de hele Adobe Experience Cloud, zodat u de betrokkenheid van gebruikers met uw applicaties kunt begrijpen en verbeteren. | [Mobile Services Home](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors (voorheen Genesis) | Importeer trackingdata van applicaties van derden naar Analytics, zodat de prestaties op één centrale locatie volledig zichtbaar zijn. | [Data Connectors Home](https://marketing.adobe.com/developer/documentation/genesis/c-overview-how-it-works) |
| Dynamic Tag Management (DTM) | Hiermee kunt u uw Analytics-, Target- en andere tags op al uw sites beheren, ongeacht het aantal domeinen. | [DTM Home](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/dtm-implementation-overview.html) |
| Adobe Launch | De volgende generatie mogelijkheden voor websitetags en mobiel SDK-beheer van Adobe. | [Adobe Launch Home](https://docs.adobe.com/content/help/en/launch/using/overview.html) |

## Belangrijke terminologie {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Klik [hier](https://docs.adobe.com/content/help/en/analytics/technotes/terms.html) voor een uitgebreide woordenlijst met termen in Adobe Analytics.

| Term | Beschrijving | Documentatiekoppeling |
|--- |--- |--- |
| Props (aangepast verkeer) | Dimensies voor het traceren van de verkeersactiviteit op de site per pagina. Props blijven niet bestaan tussen pagina&#39;s. Belangrijke toepassingen van verkeersvariabelen: <ul><li>Eenvoudig tellen om ‘de populairste’ van een bepaalde waarde te vinden</li><li>Zichtbaarheid van de weg die gebruikers volgen door uw site </li></ul><br>Voorbeelden van verkeersvariabelen: paginanaam, sitesecties, browsers.</br> | [Props](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/traffic-variables/traffic-var.html) |
| eVar (aangepaste conversie) | Dimensies die gedurende een door u aangepaste periode blijven bestaan. Opties voor vervaldatums zijn onder andere het verlopen van gebeurtenissen, bezoeken of X-dagen. Deze opties moeten worden gestuurd door het type analyse dat op de betreffende variabele wordt uitgevoerd.<br>Belangrijke verschillen tussen eVars en props:</br><ul><li>Props worden vaak gebruikt voor padanalyse omdat persistentie is verwijderd.</li><li>eVars worden vaak gebruikt voor conversieanalyse.</li></ul><br>Voorbeelden van conversievariabelen: interne zoektermen, interne aanbiedingen, externe campagnes (s.campaign).</br> | [eVars](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| Gebeurtenissen/cijfers (s.events) | Cijfers die belangrijke acties meten waarvan wij willen dat de bezoekers ze op onze site uitvoeren. Er zijn drie typen gebeurtenissen: teller, numerieke waarden en valuta. Gebeurtenissen zijn vooral handig wanneer ze worden toegevoegd aan eVar-rapporten (conversievariabelen). De eVar geeft kwalitatieve informatie over wat er is gebeurd en de gebeurtenis geeft kwantitatieve informatie over wat er is gebeurd. <br>Belangrijke verschillen tussen eVars en gebeurtenissen:</br><ul><li>eVars vertellen ons wie en wat invloed heeft gehad op welke conversie</li><li>Gebeurtenissen meet hoeveel conversies hebben plaatsgevonden</li></ul><br>Voorbeelden van conversiegebeurtenissen: bestellingen, applicaties starten, leads, omzet.</br> | [Gebeurtenissen](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html) |
| Onderdelen | Dimensies, cijfers, segmenten en tijdgranulariteit (datumbereiken) die u naar een project kunt slepen en neerzetten. | [Onderdelen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) |
| Dimensies | Verzameling van eVars, profielen, classificaties en standaard door Adobe verzamelde waarden. | [Dimensies](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-descriptions.html) |
| Cijfers | Verzameling van geïmplementeerde gebeurtenissen en berekende standaarden. | [Cijfers](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/apply-create-metrics.html) |
| Berekende standaarden | Mogelijkheid om aangepaste cijfers af te leiden van bestaande cijfers die door uw implementatie zijn vastgelegd. | [Berekende standaarden](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/cm-overview.html) |
| Segmenten | Mogelijkheid om krachtige, doelgerichte doelgroepsegmenten te maken, te beheren, te delen en toe te passen op uw Analytics-rapporten. Segmenten worden gedeeld tussen Analytics-producten en kunnen worden gedeeld in de Experience Cloud. | [Segmentering](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) |
| Tijd (datumbereiken) | Mogelijkheid om datums te filteren in elke tijdsperiode en aangepaste datumbereiken te maken die opnieuw kunnen worden gebruikt in uw analyse. | [Datumbereik](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) |
| Visualisaties | Rijke beelden die data tot leven kunnen brengen in uw projecten. | [Visualisaties](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) |
| Curation | Mogelijkheid om de onderdelen te beperken die toegankelijk zijn in een project of vitruele rapportsuite. | [VRS-selectie](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-components.html)<br>[Projectselectie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html)</br><br>[Vergelijking](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) |

## Belangrijke verslagen

| Rapport | Beschrijving | Documentatiekoppeling |
|--- |--- |--- |
| Lijst met volledige dimensies/rapporten | Definitie van alle dimensies/rapporten die beschikbaar zijn in Adobe Analytics. | [Dimensies](https://docs.adobe.com/content/help/en/analytics/components/variables/c-variables.html) |
| Advertising Analytics | Analyseer al uw Google- en Bing-paid-searchdata naast elkaar in Adobe Analytics. Dimensies die door de integratie worden gemaakt, zijn advertentieplatform, trefwoord, typeovereenkomst, enz. De gecreëerde cijfers zijn AMO-impressies, AMO-klikken, AMO-kosten, gemiddelde, positie en gemiddelde kwaliteitsscore. | [Advertising Analytics](https://docs.adobe.com/help/en/analytics/integration/advertising-analytics/overview.html) |
| Audience Analytics | Verrijk binnenkomende Analytics-treffers met het doelgroepslidmaatschap van een gebruiker in AAM. u kunt AAM-doelgroepsdata zoals demografische informatie (bijv. geslacht of inkomensniveau), psychografische informatie (bijv. interesses en hobby&#39;s), CRM-data en impressiedata opnemen in elke Analytics-workflow. Dimensies die door deze integratie worden gemaakt, zijn doelgroeps-id en doelgroepnaam. | [Audience Analytics](https://docs.adobe.com/content/help/en/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Attribution IQ | Hiermee krijgt u inzicht in de manier waarop zinvolle betrokkenheid plaatsvindt tijdens een klanttraject, door een intelligente identificatie van beslissingspunten die klanten bij de beoogde resultaten brengen, waarmee u uw marketinginitiatieven effectief kunt optimaliseren. De modellen omvatten eerste, laatste, lineair, participatie, j-vormig, omgekeerd j-vormig, u-vorm, dezelfde aanraking, aangepast en tijdverval. | [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution.html) |
| Anomaliedetectie | Een statistische methode om te bepalen hoe een bepaalde meting is gewijzigd ten opzichte van eerdere data. AD is standaard ingeschakeld voor alle trendvisualisaties in de Analysis Workspace. | [Anomaliedetectie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Contributieanalyse | Onderzoekt het “waarom” achter de optredende anomalieën door een geautomatiseerde analyse uit te voeren van elk cijfer en elke dimensie waartoe u toegang hebt. | [Contributieanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Cohortanalyse | Een cohort is een groep mensen die gedurende een bepaalde periode een aantal kenmerken delen. Cohortanalyse helpt bij het analyseren van het behoud en verloop van uw gebruikers. | [Cohortanalyse](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) |
| Klanttrajectrapporten | Hier wordt informatie weergegeven over het pad dat uw gebruikers door uw site of app volgen. Prop, eVars en gebeurtenissen kunnen in deze analyse in de Analysis Workspace worden gebruikt. | [Analysis Workspace-uitval](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)[Analysis Workspace-flow](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html)[Reports &amp; Analytics-paden](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-paths.html) |
| Marketingkanalen | Rapporten die u helpen ontdekken welke externe kanalen gebruikers naar uw site leiden en welke het meest effectief zijn voor conversie. Biedt attributieweergaven van eerste en laatste aanraking. Dit is het aangewezen externe rapport voor verkeersbronnen in Adobe Analytics (meer dan Campagnes of de Verkeersbronnen) omdat dit de meest uitgebreide blik geeft op betaalde en organische kanalen. | [Marketingkanalen](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-getting-started-mchannel.html) |
| Mobile | Hier wordt informatie weergegeven over websites die via een mobiel apparaat of tablet worden benaderd. | [Mobiel rapport](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-mobile.html) |
| Mobiele app | Geeft basisgebruiksgegevens weer over uw mobiele apps. Deze rapporten zijn beschikbaar zodra onze SDK is geïmplementeerd en de rapportage is ingeschakeld.  Daarnaast heeft Adobe Mobile Services een aparte mobiele app-interface gemaakt met uitgebreidere appdata, waarmee u de betrokkenheid van gebruikers bij uw apps kunt begrijpen en verbeteren.  Ga [hier](https://mobilemarketing.adobe.com) naar de interface. | [Adobe Mobile Services](https://docs.adobe.com/content/help/en/mobile-services/using/home.html) | Producten | Bepaalt hoe afzonderlijke producten en productgroepen (categorieën) bijdragen aan de diverse conversiecijfers zoals omzet of aantal betalingen. | [Productrapport](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-products.html) |
| Segmentvergelijking | Ontdekt de statistisch meest significante verschillen tussen segmenten door een geautomatiseerde analyse van elk cijfer en elke dimensie waartoe u toegang hebt. | [Segmentvergelijking](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html) |
| Rapport Sitecontent | Geeft informatie weer over welke pagina&#39;s en gebieden van uw site het meest actief zijn en welke servers het meest worden gebruikt. | [Rapport Sitecontent](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-content.html) |
| Rapport Sitecijfers | Geeft kwantitatieve informatie over uw website weer zoals unieke bezoekers, bestellingen, omzet, enzovoort. Elk cijfer kan worden opgenomen rapporten van verschillende items. | [Rapport Sitecijfers](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-site-metrics.html) |
| Bezoekersprofiel | Rapporten die u helpen aankooppatronen van klanten van diverse profielcategorieën (zoals landen, staten, postcodes en domeinen) te zien. | [Bezoekersprofiel](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-profile.html) |
| Bezoekersbehoud | Geeft informatie weer over de loyaliteit van uw klanten, bijvoorbeeld hoeveel bezoekers hoe vaak naar uw site terugkeren. | [Bezoekersbehoud](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-visitor-retention.html) |
| Projecten koppelen, delen en plannen | Methoden om uw werk op te slaan en/of te delen met anderen in de Analytics-interface. | [Bestanden verzenden en plannen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/send-schedule-files.html) |

## Belangrijke cijfers {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| Naam cijfer | Definitie | Documentatiekoppeling |
|---|---|---|
| Volledige lijst cijfers | Definitie van alle cijfers in Adobe Analytics. | [Overzicht van cijfers](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-overview.html) |
| Unieke bezoekers | Het aantal niet-dubbele bezoekers van de website gedurende een bepaalde periode. | [Unieke bezoekers](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/reports-unique-visitors-v15-dsc.html) |
| Bezoeken | Een reeks paginaweergaven tijdens een sessie. Het bezoek begint wanneer iemand een pagina op de site voor het eerst weergeeft, en eindigt na 30 minuten inactiviteit. | [Bezoeken](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-visit.html) |
| Paginaweergaven | Een paginaweergave treedt op wanneer een bezoeker een pagina op uw website weergeeft. | [Paginaweergaven](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-page-view.html) |
| Instanties | Het aantal keren dat een variabele is gedefinieerd. Telkens wanneer Adobe Analytics een waarde binnen een variabele ziet, worden de instanties vermeerderd met 1 in het betreffende rapport. | [Instanties](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-instance.html) |
| Voorvallen | Het aantal keren dat een variabele is gedefinieerd of bleef bestaan. | [Voorvallen](https://docs.adobe.com/content/help/en/analytics/components/variables/metrics/metrics-occurrences.html) |

## Importopties {#concept_7C6DF03B5F9149E2A77F36C739432059}

| Optie | Beschrijving | Documentatiekoppeling |
|---|---|---|
| Classificatie-import | Importeert metadata op vastgelegde dimensies via browser of FTP-upload. Handmatige methode vergeleken met Rule Builder. | [Classificatie-import](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) |
| Rule Builder | Maak automatisch metadataclassificaties van dimensies op basis van door de gebruiker gedefinieerde regels. | [Classification Rule Builder](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-rulebuilder/classification-rule-builder.html) |
| Klantkenmerken | CRM-data die naar Experience Cloud zijn geüpload voor gebruik in Adobe Analytics en Adobe Target. | [Klantkenmerken](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) |
| Databronnen | Importeert offline cijfers in Analytics op dimensies of eenvoudig per dag. | [Databronnen](https://docs.adobe.com/content/help/en/analytics/import/data-sources/datasrc-home.html) |
| Adobe Exchange Data Connectors | Zie [Analytics-tools.](/help/landing/an-key-concepts.md) |  |
| Native integratie | Audience Analytics en Advertising Analytics. | Zie de sectie “Belangrijke rapporten”. |

## Exportopties {#concept_C62B688E259141CF92C048E8110464BE}

| Optie | Beschrijving | Documentatiekoppeling |
|---|---|---|
| UI-downloads en -planning | Exporteert data vanuit Analysis Workspace als CSV of PDF. | [PDF- of CSV-bestanden downloaden](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Zie Tools voor Analytics. |
| Analytics-API | Maak zelf aangepaste query&#39;s voor Analytics-data. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Zie Tools voor Analytics. |  |
| Analytics-datafeed | De meest granulaire manier om data uit Analytics te halen. Stel een feed op basis van trefferniveau op vanuit Analytics. | [Analytics-datafeed](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html) |

## Dataverzameling en -validatie {#concept_E07350D4CA5047DAA7D81F762F29606A}

| Methode/bron | Beschrijving | Documentatiekoppeling |
|--- |--- |--- |
| Bronnen voor ontwikkelaars | Documentatie met een overzicht van de bibliotheken die beschikbaar zijn voor het verzamelen van Analytics-data op alle beschikbare platforms (web, mobiele app, video, flash, enz.) | [Documenten voor ontwikkelaars](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| Implementatiehandleiding | Een beschrijving van dataverzamelingsvariabelen en details over het implementeren van code voor dataverzameling in JavaScript. | [Implementatiehandleiding](https://docs.adobe.com/content/help/en/analytics/implementation/home.html) |
| App-meting (s_code) | Globaal variabelenbeheer. | [AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) |
| App-SDK’s | Aangepast pakket met een vooraf ingevulde versie van het configuratiebestand voor apps. | <ul><li>[iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/en/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM en Adobe Launch | Zie Tools voor Analytics. |  |
| VISTA | Hiermee kunt u serverlogica toepassen om data te wijzigen of te segmenteren terwijl deze worden verzameld. | [VISTA-regels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/processing-rule-order.html) |
| Verwerkingsregels | Mogelijkheid om variabelen in te stellen, te wijzigen en te kopiëren in de Analytics-UI om te wijzigen welke data worden verzameld. | [Verwerkingsregels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| Foutopsporingsopties | Er zijn verschillende foutopsporingstools en ‘packet sniffers’ beschikbaar om uw implementatie te helpen valideren, waaronder de Adobe Experience Cloud-foutopsporing. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=nl) |
| API voor data-invoer | De API voor het invoegen van data biedt een mechanisme voor dataverzameling op de server en verzending naar Experience Cloud-servers. In plaats van JavaScript-beacons op elke webpagina te gebruiken voor het verzenden van bezoekersdata naar Experience Cloud-servers worden met serverdataverzameling alleen data verzameld op basis van webbrowserverzoeken en webserverreacties. | [Stappen voor de implementatie de API voor het invoegen van Adobe Analytics-data met POST](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
