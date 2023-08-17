---
description: Algemene overzichtsinformatie over Adobe Analytics
title: Adobe Analytics-overzicht
feature: Analytics Basics
hide: true
hidefromtoc: true
source-git-commit: d5a7dfe720cc84b67208e7d30434295caf1e2aac
workflow-type: tm+mt
source-wordcount: '3108'
ht-degree: 3%

---

# Adobe Analytics-overzicht

Adobe Analytics stelt organisaties in staat gegevens te verzamelen en actioneerbare inzichten te verkrijgen van elke interactie met digitale klanten. Met diepgaande analyse, veelzijdige rapportering en voorspellende intelligentie, krijgen organisaties de inzichtelijke basis die zij nodig hebben om betere ervaringen voor hun klanten te bouwen.

## Belangrijkste voordelen

Hieronder volgen enkele belangrijke manieren waarop Adobe Analytics organisaties kan helpen om kritische inzichten te verwerven om hun klanten beter te kunnen dienen.

Zie voor meer informatie over de voordelen die Adobe Analytics biedt de [Adobe Analytics-productpagina](https://business.adobe.com/products/analytics/adobe-analytics.html).

### Webanalyse

Adobe Analytics biedt de volgende complexe segmentatie en voorspellende hulpmiddelen voor het analyseren van websiteverkeer:

* [Ad-hocanalyse in Analysis Workspace](/help/analyze/analysis-workspace/home.md)

* [Stroomanalyse](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)

* [Geavanceerde segmentering](/https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html)

### Marketing Analytics

Adobe Analytics helpt organisaties te begrijpen waar klanten met hun merken in wisselwerking staan, welke kanalen klanten verkiezen, en welke ervaringen met hen resoneren.

De volgende belangrijke functies in Adobe Analytics bieden de volgende marketingmogelijkheden:

* Multikanaalgegevensverzameling

* [Offline gegevensintegratie](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en)

* [Ad-hocanalyse in Analysis Workspace](/help/analyze/analysis-workspace/home.md)

### Attributie

De attributie laat organisaties zien hoe de verschillende interactie door de klantenreis omzetting beïnvloedt. Naast meer traditionele attributieopties, zoals Lineair of First Touch-modellen, gebruikt Attribution in Adobe Analytics ook machinaal leren en geavanceerde statistische modellen om de precieze impact van elke aanraking te begrijpen.

Zie voor meer informatie [Attributiemodellen en terugzoekvensters](/help/analyze/analysis-workspace/attribution/models.md).


### Predictieve analyse

Voor voorspellende analyses wordt gebruikgemaakt van machinaal leren en geavanceerde statistische modellering om klantgegevens te analyseren, patronen te vinden en toekomstig gedrag, zoals churn, te voorspellen of het waarschijnlijk is om om te zetten. Het staat gegevensanalisten toe om uit reusachtige gegevensreeksen voordeel te halen die anders zouden kunnen worden verspild.

De volgende belangrijke functies in Adobe Analytics bieden deze voorspellende mogelijkheden:

* [Anomalische detectie](#anomaly-detection)

* [Bijdrage-analyse](#contribution-analysis)

* [Intelligente waarschuwingen](#intelligent-alerts)

## Vereisten voor het gebruik van Adobe Analytics

Voordat je Adobe Analytics kunt gebruiken, moet je beschikken over:

* Een geldige Adobe Analytics-licentie

  Adobe Analytics heeft een sitelicentie nodig. Neem contact op met uw Adobe-accountvertegenwoordiger voor meer informatie. <!--is this phrased correctly? Is this important? -->

* Een ondersteunde browser

  Elke gebruiker die Adobe Analytics opent, moet een ondersteunde browser gebruiken. Zie de klasse [Adobe Analytics-systeemvereisten](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/sys-reqs.html?lang=en).

<!-- are there more? -->

## De interface Analytics begrijpen

De interface van Adobe Analytics bestaat uit de volgende hoofdgebieden:

### Werkruimte, tabblad

De [!UICONTROL Workspace] bevat een lijst met Analysis Workspace-projecten.

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Werkruimte**] tab.

   ![Werkruimte, tabblad](assets/landing-all2.png)

Voor meer informatie over de functies en functies die beschikbaar zijn op de [!UICONTROL Workspace] tab, zie [Openingspagina van Adobe Analytics](/help/analyze/landing.md).

### Tabblad Rapporten

Met ingang van 31 december 2023 is de Adobe voornemens de rapporten en analyses en de bijbehorende verslagen en kenmerken te beëindigen.

Gebruik in plaats daarvan de opdracht [!UICONTROL **Rapporten**] gebied in de linkerspoorstaaf op de [!UICONTROL **Werkruimte**] tab. Zie voor meer informatie *Navigeren op het tabblad Rapporten* in [Openingspagina van Adobe Analytics](/help/analyze/landing.md).

### Tabblad Componenten

De [!UICONTROL Components] bevat functies die u helpen uw gegevensanalyse af te stemmen en in te schakelen.

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Componenten**] tab, dan selecteren [!UICONTROL **Alle componenten**].

   ![Werkruimte, tabblad](assets/components-tab.png)

2. Selecteer om het even welke volgende producteigenschappen om het te vormen: (Afhankelijk van uw toestemmingen, zouden niet alle eigenschappen kunnen zichtbaar zijn.)


   | Productfunctie | -functie | Meer informatie |
   |---------|----------|----------|
   | Segmenten | Met Adobe Analytics kunt u krachtige, doelgerichte publiekssegmenten maken, beheren, delen en toepassen op uw rapporten met behulp van de analysemogelijkheden, de Adobe Experience Cloud, Adobe Target en andere producten voor geïntegreerde Adobe. | [Analytics-segmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=en) |
   | Berekende standaarden | Berekende en Geavanceerde berekende (of Afgeleide) metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.  Zij staan marketers, productmanagers, en analisten toe om vragen van de gegevens te stellen zonder het moeten de implementatie van Analytics veranderen. | [Berekende en Geavanceerde berekende (Afgeleide) metriek](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html?lang=en) |
   | Datumbereiken | Analysis Workspace bevat een lijst met standaarddatumbereiken die gebruikers kunnen gebruiken bij het samenstellen van analyses. Bovendien kunt u aangepaste datumbereiken maken en deze beschikbaar maken voor gebruikers in Analysis Workspace. | [Aangepaste datumbereiken maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=en) <!-- should create an article in the Components Guide for managing/creating date ranges. This article in the Tools Guide needs updating. --> |
   | Virtuele rapportsuites |  |  |
   | Waarschuwingen | Intelligente waarschuwingen maken een gedetailleerdere controle mogelijk op waarschuwingen en integreren de detectie van anomalieën met het waarschuwingssysteem. | [Intelligente waarschuwingen](https://experienceleague.adobe.com/docs/analytics/components/alerts/intellligent-alerts.html?lang=en) |
   | Targets | Met doelen kunt u de prestaties van uw website meten en de voortgang afstemmen op de doeldoelen. Wanneer u doelen maakt, selecteert u welke maateenheden voor kenmerken of variabelen u wilt meten of u kunt kiezen of u de hele site wilt meten aan de hand van de geselecteerde maatstaf. <p>Doelstellingen maken deel uit van Rapporten en Analytics. Meer informatie over rapporten en analyses [Aankondiging einde levensduur](https://express.adobe.com/page/6WnF8JK6IRDhf/).</p> | [Targets](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/targets.html?lang=en) |
   | Kalendergebeurtenissen | Voor rapporten die in tijd trended, staan de kalendergebeurtenissen u toe om gebeurtenissen grafisch te tonen en te zien of de campagnes of andere gebeurtenissen uw plaatsverkeer, opbrengst, of een andere metrisch hebben beïnvloed. | [Kalendergebeurtenissen](https://experienceleague.adobe.com/docs/analytics/components/t-calendar-event.html?lang=en) |
   | Annotaties | Met annotaties in Workspace kunt u op effectieve wijze contextuele gegevensnuances en inzichten aan uw organisatie meedelen. Met deze sjablonen kunt u kalendergebeurtenissen koppelen aan specifieke dimensies en metriek. | [Annotaties beheren](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/manage-annotations.html?lang=en) |
   | Classificatiesets | Classificatiesets bieden één interface voor het beheer van classificaties en regels. <p>Een classificatie is een manier om de veranderlijke gegevens van Analytics te categoriseren, dan tonend de gegevens op verschillende manieren wanneer u rapporten produceert. U brengt een relatie tot stand tussen een variabele waarde en metagegevens die betrekking hebben op die waarde. Classificaties kunnen worden gebruikt voor de meeste aangepaste afmetingen, zoals trackingcode, proefdrukken en eVars.</p> | [Overzicht van classificatiesets](https://experienceleague.adobe.com/docs/analytics/components/classifications/sets/overview.html?lang=en) |
   | Locaties | Als u Adobe Analytics-classificatiegegevens wilt importeren van een cloudbestemming, moet u eerst de locatie toevoegen en configureren waar u de classificatiegegevens wilt verzamelen. U kunt locaties maken, bewerken of verwijderen. | [Locatiebeheer](https://experienceleague.adobe.com/docs/analytics/components/locations/locations-manager.html?lang=en) |
   | Geplande projecten | Wanneer het leiden van geplande projecten, kunt u terugkomende projectprogramma&#39;s uitgeven en schrappen; onderzoek naar een programma in de onderzoeksbar of door de filteropties in de linkerspoorstaaf te gebruiken; en filter door markering, goedgekeurde programma&#39;s, eigenaars en meer. | [Geplande projecten](/help/components/scheduled-projects-manager.md) |
   | Bladwijzers | Met bladwijzers hebt u toegang tot de rapporten die u het meest gebruikt. De bladwijzers die u maakt, worden toegevoegd aan het Experience Cloud en zijn beschikbaar in geïntegreerde functies zoals gegevensconnectors. <p>Bladwijzers maken deel uit van Rapporten en Analytics. Meer informatie over rapporten en analyses [Aankondiging einde levensduur](https://express.adobe.com/page/6WnF8JK6IRDhf/). | [Bladwijzermanager](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/bookmarks.html?lang=en) |
   | Dashboards | De dashboards worden gecreeerd om metriek te visualiseren en interactieve analytische capaciteit van gegevens te verstrekken. Door op punten binnen een dashboard te klikken, kunt u de gegevens snel en gemakkelijk segmenteren om informatie uit uw analyse af te leiden. <p>Dashboards maken deel uit van Data Workbench. Meer informatie over de Data Workbench [Aankondiging einde levensduur](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=en). | [Dashboardbeheer](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/dashboard-manage.html?lang=en) |
   | Geplande rapporten | Gebruikers op beheerniveau kunnen geplande rapporten in de hele organisatie bekijken en beheren. | [Wachtrij voor geplande rapporten](https://experienceleague.adobe.com/docs/analytics/components/scheduled-reports-admin.html?lang=en) |
   | Rapportinstellingen | Deze instellingen verwijzen naar verouderde Adobe Analytics-producten, waarbij Analysis Workspace en de bijbehorende componenten zijn uitgesloten. Als u de Analysis Workspace-instellingen wilt aanpassen, gaat u naar Componenten > Voorkeuren. |  |
   | Voorkeuren | Beheer instellingen voor Analysis Workspace en de bijbehorende componenten voor alle nieuwe projecten of deelvensters die u maakt. Bestaande projecten en deelvensters worden niet beïnvloed. | [Voorkeuren](/help/analyze/analysis-workspace/user-preferences.md) |

   {style="table-layout:auto"}

### Gereedschappen, tabblad

Het tabblad Gereedschappen...

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Gereedschappen**] tab, dan selecteren [!UICONTROL **Alle gereedschappen**].

   ![Werkruimte, tabblad](assets/tools-tab.png)

2. Selecteer om het even welke volgende producteigenschappen om het te vormen:

   | Productfunctie | -functie | Meer informatie |
   |---------|----------|----------|
   | Data Warehouse | Data Warehouse verwijst naar de kopie van analysegegevens voor opslag en aangepaste rapporten, die u kunt uitvoeren door de gegevens te filteren. <p>Met Aanvraagbeheer kunt u aanvragen weergeven, dupliceren en opnieuw de prioriteit geven.</p> | [Verzoeken in Data Warehouse beheren](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=en) |
   | Activity Map | Activity Map is ontworpen om linkactiviteiten te rangschikken met behulp van visuele overlays en biedt een dashboard met realtime analyses om de betrokkenheid van het publiek van uw webpagina&#39;s te controleren. Het laat u opstelling verschillende meningen om de versnelling van klantenactiviteit visueel te identificeren, marketing initiatieven te kwantificeren, en op publieksbehoeften en gedrag te handelen. | [Overzicht van Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html?lang=en) |
   | Recommendations Classic |  |  |
   | Zoeken en promoten |  |  |
   | Mobiele services |  |  |
   | Analysedashboards (mobiele app) |  |  |
   | Report Builder |  |  |

   {style="table-layout:auto"}

### Tabblad Beheer

Het tabblad Beheer...

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Beheerder**] tab, dan selecteren [!UICONTROL **Alle beheerders**].

   ![Werkruimte, tabblad](assets/admin-tab.png)

## Aan de slag voor beheerders, analisten en eindgebruikers

Er zijn drie typen Adobe Analytics-gebruikers in een standaardorganisatie: beheerders, analisten en eindgebruikers.

Beheerders implementeren en configureren Adobe Analytics; analisten stellen projecten in en maken analyses met behulp van Analysis Workspace, en eindgebruikers krijgen activering van hun klanten door hun eigen analyses te maken of door met analisten te werken om deze te maken.

Vouw de onderstaande secties uit om te leren hoe deze gebruikers aan de slag kunnen met Adobe Analytics.

### Aan de slag met beheerders

Analysebeheerders zijn verantwoordelijk voor het kiezen van de implementatiemethode die het meest geschikt is voor hun organisatie.

Nadat Adobe Analytics is geïmplementeerd, moeten beheerders verschillende configuratietaken uitvoeren om ervoor te zorgen dat analisten en eindgebruikers de volledige waarde van Adobe Analytics krijgen.

#### Bepaal de soorten gegevens die moeten worden verzameld

Met Adobe Analytics kunt u gegevens verzamelen van verschillende soorten kanalen en deze samenbrengen om zinvolle, real-time klantinzichten te bieden.

Hieronder vindt u een aantal ondersteunde kanalen waarop gegevens kunnen worden verzameld:

* Mobiele telefoons

* Het internet van de dingen

* TV

* Spraakassistenten

* Verbonden auto&#39;s

* En meer (er worden regelmatig nieuwe ondersteunde kanalen toegevoegd)

De [implementatiemethode](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) u kiest bepaalt het type gegevens dat kan worden verzameld.

#### Adobe Analytics implementeren

Er zijn verschillende implementatiemethoden beschikbaar wanneer u Adobe Analytics implementeert op uw website of mobiele app.

Voor informatie over elke beschikbare methode raadpleegt u [Adobe Analytics implementeren](https://experienceleague.adobe.com/docs/analytics/implementation/home.html).

| | Implementatiemethoden |
|---------|---------|
| **Websites** | <ul><li>Web SDK-extensie (aanbevolen)</li><li>Web SDK</li><li>Extensie Analytics</li><li>Verouderd JavaScript</li></ul> |
| **Mobiele apps** | <ul><li>Mobile SDK-extensie (aanbevolen)</li><li>Extensie Analytics</li></ul> |

{style="table-layout:auto"}

#### Adobe Analytics configureren

Analysebeheerders moeten de volgende taken uitvoeren voordat ze Adobe Analytics beschikbaar maken voor gebruikers in de organisatie:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Beheerdersrollen definiëren | Adobe Analytics ondersteunt verschillende typen beheerders | [Beheerdersrollen in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html?lang=en) |
| Machtigingen definiëren | Analysebeheerders moeten productprofielen toewijzen in de Admin Console voor Adobe Analytics, Report Suite Tools en Analytics Tools. | [Machtigingen voor analyse in de Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=en) |
| Stel rapportsuites in en definieer instellingen voor uw bedrijf | Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te produceren.<p>Beheerders kunnen ook [virtuele rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=en) voor verdere segmentgegevens.</p> | <ul><li>[Een rapportsuite maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html?lang=en)</li><li>[Overzicht van bedrijfsinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=en)</li></ul> |
| Gegevens importeren | Met Adobe Analytics-gegevensbronnen kunt u extra online- of offlinegegevens importeren voor rapportage. | [Overzicht van gegevensbronnen](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en) |
| Gegevens classificeren met classificaties | Met classificaties kunt u gegevens classificeren om beter gebruik te maken van variabelen, zodat u meer inhoud in één variabele kunt opnemen. | |
| Componenten beheren | Gebruik het Woordenboek van Gegevens en de beheersgebieden voor elk componenttype om te bepalen welke componenten in uw implementatie van Analytics beschikbaar zijn, evenals die voor uw organisatie worden goedgekeurd.<p>Dit zou een voortdurende activiteit moeten zijn om ervoor te zorgen dat de componenten effectief in uw organisatie worden gebruikt. </p> | <ul><li>[Overzicht van gegevenswoordenboek](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html?lang=en)</li><li>[Het berekende manager van metriek](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=en)</li><li>[Instellingen beheren](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=en)</li><li>[Aangepaste datumbereiken maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=en)</li></ul> |
| Analyse van anomaly-detectie en -bijdrage | | |
| Geavanceerde segmentering | | |
| Soorten publiek publiceren naar Audience Manager | | |
| Attributie | | |
| Activity Manager rapporteren | | |
| Integraties | U kunt informatie uit andere toepassingen in Adobe Analytics oppervlakken. <p>Hieronder vindt u een aantal algemene integraties:</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=en">Analyses voor doel</a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=en">Media Analytics</a></li> | |

{style="table-layout:auto"}

### Aan de slag met analisten

Iedereen in een organisatie kan Adobe Analytics gebruiken om actioneerbare inzichten over klantengedrag over websites en apps te bereiken, maar Adobe Analytics is ontworpen met gegevensanalisten voor ogen.

Hier volgen enkele belangrijke taken en functies waarmee analisten vertrouwd moeten zijn om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten.

| Functie | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Projecten maken en delen in Analysis Workspace | Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen. Gebruikend de belemmering-en-dalingsinterface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset te leiden, projecten met iedereen in uw organisatie te delen en te plannen.<p>Gegevensanalisten zijn vaak verantwoordelijk voor het maken van projecten in Analysis Workspace voor gebruikers binnen hun organisatie.</p><p>Nadat de projecten worden gecreeerd, delen de analisten die projecten met [eindgebruikers](#end-users)(niet-analisten) in hun organisaties die om de gegevens hebben verzocht en hen helpen begrijpen hoe deze te interpreteren.</p> | <ul><li>[Projecten maken](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[Projecten delen](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attributie | De analisten kunnen aanpassen hoe de afmetingspunten krediet voor succesgebeurtenissen door diverse attributiemodellen en terugkijkvensters in Analysis Workspace te gebruiken krijgen.<p>Lineaire-attributiemodellen geven hetzelfde krediet aan elk aanraakpunt voorafgaand aan een conversie, terwijl First Touch het eerste aanraakpunt volledig crediteert. Er zijn veel andere toewijzingsmodellen beschikbaar, waaronder het Algorithmic-model, dat statistische technieken gebruikt om de optimale allocatie van krediet dynamisch te bepalen. </p> | [Attributiemodellen en terugzoekvensters](/help/analyze/analysis-workspace/attribution/models.md) |
| Anomalische detectie | Statistische modellering in Analysis Workspace vindt automatisch onverwachte tendensen in uw gegevens door metriek te analyseren en een ondergrens, bovengrens, en verwachte waaier van waarden te bepalen. Wanneer een onverwachte punt of daling voorkomt, alarmeert het systeem u in het rapport. | [Overzicht van anomaliedetectie](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| Bijdrage-analyse | Gebruik Analysis Workspace om verborgen patronen in uw gegevens te ontdekken om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-gebonden waarden, en plotselinge pieken of vallen voor metriek over publiekssegmenten te identificeren. | [Overzicht van bijdrageanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| Intelligente waarschuwingen | Maak en beheer waarschuwingen op basis van gegevensanomalieën en &#39;gestapelde&#39; waarschuwingen die meerdere metriek in één waarschuwing vastleggen. | [Overzicht van intelligente waarschuwingen](help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md) |
| Gegevens exporteren | Met Data Warehouse- en gegevensfeeds kunt u gegevens exporteren naar verschillende cloudinstellingen, zoals Google Cloud Platform, Azure RBAC, Azure SAS en Amazon S3. | [Handleiding voor exporteren van analysemogelijkheden](https://experienceleague.adobe.com/docs/analytics/export/home.html) |
| Activiteitenoverzicht | Activity Map is een Adobe Analytics-toepassing die is ontworpen om linkactiviteiten met behulp van visuele overlays te rangschikken en die een dashboard van realtime analyses biedt om de betrokkenheid van het publiek van uw webpagina&#39;s te controleren.<p>Met Activity Map kunt u verschillende weergaven instellen om visueel de versnelling van klantactiviteiten te identificeren, marketinginitiatieven te kwantificeren en op de behoeften en het gedrag van het publiek in te spelen.</p> | [Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html) |
| Report Builder | Report Builder is een invoegtoepassing voor Microsoft Excel. Met Report Builder kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens die in uw Excel-werkbladen worden ingevoegd. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft. | [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html) |

{style="table-layout:auto"}

<!-- * Realtime reporting? -->

### Aan de slag voor eindgebruikers

Eindgebruikers die geen professionele analisten zijn, kunnen in hun organisatie samenwerken met analisten om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten, of ze kunnen de basisbeginselen van Analysis Workspace leren om actioneerbare inzichten over hun klanten te krijgen.

#### Werken met analisten

Meestal zijn gebruikers in een organisatie die meer willen weten over het gedrag van klanten op de verschillende sites, geen professionele analisten.

In het ideale geval moeten deze gebruikers met [analisten](#analysts) binnen een organisatie:

1. Definieer de vereisten voor de analyses door aan de analist uit te leggen wat hij of zij van klanten wil leren.

1. Herzie de analyses om ervoor te zorgen dat zij aan de doelstellingen voldoen.

1. Bespreek de gegevens die bij de analyses zijn verkregen.

1. Wijzig de analyses naar wens in de loop van de tijd.

#### Analyses maken in Analysis Workspace

Je hoeft geen gegevensanalist te zijn om actioneerbare inzichten van Adobe Analytics te krijgen.

Sommige gebruikers vinden het nuttig om met een gegevensanalist te werken aan opstelling een project in Analysis Workspace en te verklaren hoe te om de gegevens te interpreteren, zoals die in [Werken met analisten](#work-with-analysts); andere gebruikers kunnen comfortabel het project bouwen en de gegevens zelf interpreteren.

Met Analysis Workspace kunt u snel analyses maken om inzichten te verzamelen en deze inzichten vervolgens met anderen te delen. Gebruikend belemmering-en-dalings browser interface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset in werking te stellen, en projecten met iedereen te delen en te plannen u kiest.

Ga voor informatie over het maken van analyses in Analysis Workspace naar [Analysis Workspace-overzicht](/help/analyze/analysis-workspace/home.md).

### Aan de slag met ontwikkelaars

[Analyse-API&#39;s](https://developer.adobe.com/analytics-apis/docs/2.0/) staat u toe om de servers van de Adobe direct te roepen om bijna om het even welke actie uit te voeren die u in het gebruikersinterface kunt uitvoeren.

U kunt rapporten maken om te verkennen, inzichten op te halen of belangrijke vragen over uw gegevens te beantwoorden. U kunt ook componenten van Adobe Analytics beheren, zoals het maken van segmenten of berekende metriek.

## Video-overzicht

Meer informatie over de basisbeginselen van Adobe Analytics vindt u in *Introductie tot Adobe Analytics - Skill Builder Webinar* video. De video doorloopt u de basisbeginselen van hoe gegevens worden vastgelegd, hoe gegevens naar Adobe Analytics worden verzonden en welke visualisatiemogelijkheden u kunt gebruiken in Adobe Analytics. De video verstrekt een stichting voor u om gegevens te bouwen, op te stellen, te verzamelen en te interpreteren, toestaand u om activeerbare inzichten en aanbevelingen te verstrekken die op de verzamelde gegevens worden gebaseerd.

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Voor vragen over welk gereedschap u wilt gebruiken, raadpleegt u [Welk Adobe Analytics-gereedschap moet ik gebruiken?](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/which-analytics-tool.html).

## Ga verder met Customer Journey Analytics

Customer Journey Analytics is de volgende generatie Analytics-oplossing van de Adobe waarmee u de kracht van Analysis Workspace kunt gebruiken met gegevens uit Adobe Experience Platform. Het kan onderbreken, filtreren, vragen, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden.

Hier volgen enkele voordelen van Customer Journey Analytics ten opzichte van Adobe Analytics:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, props en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Datasets kunnen een onbeperkt aantal unieke dimensies en metriek hebben.

* **Onbeperkte unieke waarden**: Adobe Experience Platform is niet beperkt tot enige unieke beperking.

* **Historische gegevens wijzigen**: Met Adobe Experience Platform kunnen gegevens worden verwijderd of gecorrigeerd.

* **Gegevens uit meerdere rapporten**: Bestaande implementaties van meerdere datasets kunnen worden gecombineerd in Platform.

Zie voor meer informatie [Overzicht van Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en).

