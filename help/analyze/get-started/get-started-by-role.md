---
description: Algemene overzichtsinformatie over Adobe Analytics, inclusief informatie over de interface van Analytics en om aan de slag te gaan voor beheerders, analisten, gebruikers en ontwikkelaars.
title: Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars
feature: Analytics Basics
exl-id: 11800de5-224a-4bd2-8cb1-a6318925db71
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1672'
ht-degree: 5%

---

# Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars

Er zijn vier typen Adobe Analytics-gebruikers in een organisatie die doorgaans werkt:

* **Beheerders:** voer en vorm Adobe Analytics uit.

* **Analysts:** de projecten van de opstelling en creeer analyses gebruikend Analysis Workspace

* **Eind - gebruikers:** verkrijgt actionable inzicht over hun klanten, of door hun eigen analyses te creëren of met analisten te werken om hen tot stand te brengen

* **Ontwikkelaars:** gebruik Adobe Analytics 2.0 APIs om de servers van Adobe direct te roepen om bijna om het even welke actie uit te voeren die in het gebruikersinterface, zoals het creëren van rapporten kan worden uitgevoerd om te onderzoeken, inzichten te krijgen, of belangrijke vragen over gegevens te beantwoorden.

De informatie hieronder schetst hoe elk van deze gebruikers met Adobe Analytics kan beginnen.

## Aan de slag met beheerders

Analysebeheerders zijn verantwoordelijk voor het kiezen van de implementatiemethode die het meest geschikt is voor hun organisatie.

Nadat Adobe Analytics is geïmplementeerd, moeten beheerders verschillende configuratietaken uitvoeren om ervoor te zorgen dat analisten en eindgebruikers de volledige waarde van Adobe Analytics krijgen. Beheerders moeten ook regelmatig toezicht houden op hun analyseomgeving om ervoor te zorgen dat het systeem efficiënt werkt.

### Bepaal de soorten gegevens die moeten worden verzameld

Met Adobe Analytics kunt u gegevens verzamelen van verschillende soorten kanalen en deze samenbrengen om zinvolle, real-time klantinzichten te bieden.

Hieronder vindt u een aantal ondersteunde kanalen waarop gegevens kunnen worden verzameld:

* Mobiele telefoons

* Het internet van de dingen

* TV

* Spraakassistenten

* Verbonden auto&#39;s

* En meer (er worden regelmatig nieuwe ondersteunde kanalen toegevoegd)

De [&#x200B; implementatiemethode &#x200B;](/help/implement/home.md) u kiest bepaalt het type van gegevens dat kan worden verzameld.

### Adobe Analytics implementeren

Er zijn verschillende implementatiemethoden beschikbaar wanneer u Adobe Analytics implementeert op uw website of mobiele app.

Voor informatie over elke beschikbare methode, zie [&#x200B; Adobe Analytics &#x200B;](/help/implement/home.md) uitvoeren.

| | Implementatiemethoden |
|---------|---------|
| **Websites** | <ul><li>Web SDK-extensie (aanbevolen)</li><li>Web SDK</li><li>Extensie Analytics</li><li>Legacy JavaScript</li></ul> |
| **Mobiele apps** | <ul><li>Mobile SDK-extensie (aanbevolen)</li><li>Extensie Analytics</li></ul> |

{style="table-layout:auto"}

### Adobe Analytics configureren

Analysebeheerders moeten de volgende taken uitvoeren voordat ze Adobe Analytics beschikbaar maken voor gebruikers in de organisatie:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Beheerdersrollen definiëren | Adobe Analytics ondersteunt verschillende typen beheerders | [&#x200B; de rollen van de Beheerder in Adobe Analytics &#x200B;](/help/admin/admin-console/admin-roles-in-analytics.md) |
| Machtigingen definiëren | Analysebeheerders moeten productprofielen toewijzen in de Admin Console for Adobe Analytics, Report Suite Tools en Analytics Tools. | [&#x200B; Toestemmingen van Analytics in Admin Console &#x200B;](/help/admin/admin-console/permissions/analytics-tools.md) |
| Stel rapportsuites in en definieer instellingen voor uw bedrijf | Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te produceren.<p>De beheerders kunnen opstelling [&#x200B; virtuele rapportreeksen &#x200B;](/help/components/vrs/vrs-about.md) ook aan verdere segmentgegevens.</p> | <ul><li>[Een rapportsuite maken](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md)</li><li>[&#x200B; Overzicht van de Montages van het Bedrijf &#x200B;](/help/admin/tools/company/c-company-settings.md)</li></ul> |
| Gegevens importeren | Met Adobe Analytics-gegevensbronnen kunt u extra online- of offlinegegevens importeren voor rapportage. | [&#x200B; Overzicht van gegevensbronnen &#x200B;](/help/import/data-sources/overview.md) |
| Gegevens classificeren met classificaties | Met classificaties kunt u gegevens classificeren om beter gebruik te maken van variabelen, zodat u meer inhoud in één variabele kunt opnemen. | [&#x200B; Overzicht van Classificaties &#x200B;](/help/components/classifications/classifications-overview.md) |
| Componenten beheren | Gebruik het Woordenboek van Gegevens en de beheersgebieden voor elk componenttype om te bepalen welke componenten in uw implementatie van Analytics beschikbaar zijn, evenals die voor uw organisatie worden goedgekeurd.<p>Dit zou een voortdurende activiteit moeten zijn om ervoor te zorgen dat de componenten effectief in uw organisatie worden gebruikt. </p> | <ul><li>[&#x200B; Overzicht van het Woordenboek van Gegevens &#x200B;](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)</li><li>[&#x200B; Berekende metriekmanager &#x200B;](/help/components/calculated-metrics/workflow/cm-manager.md)</li><li>[&#x200B; beheert plaatsen &#x200B;](/help/components/segmentation/segmentation-workflow/seg-manage.md)</li><li>[Aangepaste datumbereiken maken](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md)</li></ul> |
| Anomalische detectie | Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens. | [Overzicht van anomaliedetectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Bijdrage-analyse | De Analyse van de bijdrage ontdekt verborgen patronen binnen uw gegevens om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-verbindende waarden, en plotselinge pieken of vallen voor geselecteerde metriek over convergent publiekssegmenten te identificeren. | [Overzicht van bijdrageanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) |
| Segmentatie van analyse | Hiermee kunt u krachtige, doelgerichte publiekssegmenten maken, beheren, delen en toepassen op uw rapporten met behulp van de analysemogelijkheden, de Adobe Experience Cloud, Adobe Target en andere geïntegreerde Adobe-producten. | [Analytics-segmentatie](/help/components/segmentation/seg-home.md) |
| Publiceer publiek naar Audience Manager | Adobe Audience Manager is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van eerste, tweede (partner) en andere bedrijven. | [Overzicht van Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md) |
| Integraties | U kunt informatie uit andere toepassingen in Adobe Analytics oppervlakken. <p>Hieronder vindt u een aantal algemene integraties:</p><ul><li><a href="/help/analyze/analysis-workspace/c-panels/a4t-panel.md"> Analytics voor Doel </a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=nl-NL"> Streaming media diensten </a></li> | [Analytics Integration](/help/integrate/home.md) |

{style="table-layout:auto"}

### Monitor Adobe Analytics

Er zijn verschillende functies beschikbaar waarmee u uw Adobe Analytics-omgeving kunt bewaken.

De beheerders van Analytics zouden zich van de volgende eigenschappen beschikbaar moeten bewust zijn helpen belangrijke aspecten van uw milieu van Analytics controleren:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Activity Manager rapporteren | De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien. Het biedt gedetailleerde zichtbaarheid in het rapporteren van verbruik en helpt u om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te diagnosticeren en te verhelpen. | [&#x200B; Meldend Manager van de Activiteit &#x200B;](/help/admin/tools/reporting-activity-manager/reporting-activity.md) |
| Gebruik van serveroproepen | Een serveraanroep, ook wel een &quot;hit&quot; of &quot;image request&quot; genoemd, is een instantie waarin gegevens naar Adobe-servers worden verzonden om te worden verwerkt. Een dashboard van het Gebruik van de Vraag van de Server is beschikbaar dat uw gegevens van het de vraagverbruik van de server bijhoudt en het met uw contractuele grens vergelijkt. U kunt waarschuwingen instellen om overgangen te voorkomen. | [&#x200B; overzicht van het Gebruik van de Vraag van de Server &#x200B;](/help/admin/tools/server-call-usage/overage-overview.md) |
| Logbestanden | Logbestanden waarmee u kunt zien wanneer gebruikers zich aanmelden, hoe ze deze gebruiken, gebruiken, gebruiken, gebruiken, rapporten met suites en Admin wijzigen. | [Logboeken](/help/admin/tools/logs.md) |

{style="table-layout:auto"}

## Aan de slag met analisten

Iedereen in een organisatie kan Adobe Analytics gebruiken om actioneerbare inzichten over klantengedrag over websites en apps te bereiken, maar Adobe Analytics is ontworpen met gegevensanalisten voor ogen.

Hier volgen enkele belangrijke taken en functies waarmee analisten vertrouwd moeten zijn om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten.

| Functie | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Projecten maken en delen in Analysis Workspace | Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen. Gebruikend de belemmering-en-dalingsinterface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset te leiden, projecten met iedereen in uw organisatie te delen en te plannen.<p>Gegevensanalisten zijn vaak verantwoordelijk voor het maken van projecten in Analysis Workspace voor gebruikers binnen hun organisatie.</p><p>Nadat de projecten worden gecreeerd, delen de analisten die projecten met het [&#x200B; eind gebruikers &#x200B;](#end-users) (niet-analisten) in hun organisaties die om de gegevens verzochten en hen helpen begrijpen hoe te om het te interpreteren.</p> | <ul><li>[&#x200B; creeer projecten &#x200B;](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[&#x200B; de projecten van het Aandeel &#x200B;](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attributie | De analisten kunnen aanpassen hoe de afmetingspunten krediet voor succesgebeurtenissen door diverse attributiemodellen en terugkijkvensters in Analysis Workspace te gebruiken krijgen.<p>Lineaire-attributiemodellen geven hetzelfde krediet aan elk aanraakpunt voorafgaand aan een conversie, terwijl First Touch het eerste aanraakpunt volledig crediteert. Er zijn veel andere toewijzingsmodellen beschikbaar, waaronder het Algorithmic-model, dat statistische technieken gebruikt om de optimale allocatie van krediet dynamisch te bepalen. </p> | [&#x200B; modellen van de Attributie en raadplegingsvensters &#x200B;](/help/analyze/analysis-workspace/attribution/models.md) |
| Anomalische detectie | Statistische modellering in Analysis Workspace vindt automatisch onverwachte tendensen in uw gegevens door metriek te analyseren en een ondergrens, bovengrens, en verwachte waaier van waarden te bepalen. Wanneer een onverwachte punt of daling voorkomt, alarmeert het systeem u in het rapport. | [Overzicht van anomaliedetectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Bijdrage-analyse | Gebruik Analysis Workspace om verborgen patronen in uw gegevens te ontdekken om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-gebonden waarden, en plotselinge pieken of vallen voor metriek over publiekssegmenten te identificeren. | [&#x200B; Analyse van de Bijdrage &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) in [&#x200B; Anomaly Overzicht van de Opsporing &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Waarschuwingen | Maak en beheer waarschuwingen op basis van gegevensanomalieën en &#39;gestapelde&#39; waarschuwingen die meerdere metriek in één waarschuwing vastleggen. | [&#x200B; overzicht van het alarm &#x200B;](/help/components/alerts/alerts-overview.md) |
| Gegevens exporteren | Met Data Warehouse en Data Feeds kunt u gegevens exporteren naar verschillende cloudinstellingen, zoals Google Cloud Platform, Azure RBAC, Azure SAS en Amazon S3. | [&#x200B; Gids van de Uitvoer van Analytics &#x200B;](/help/export/home.md) |
| Activiteitenoverzicht | Activity Map is een Adobe Analytics-toepassing die ontworpen is om linkactiviteiten te rangschikken met behulp van visuele overlays en die een dashboard van realtime analyses biedt om de betrokkenheid van het publiek van uw webpagina&#39;s te controleren.<p>Met Activity Map kunt u verschillende weergaven instellen om visueel de versnelling van klantactiviteiten te identificeren, marketinginitiatieven te kwantificeren en op de behoeften en het gedrag van het publiek in te spelen.</p> | [&#x200B; Activity Map &#x200B;](/help/analyze/activity-map/overview.md) |
| Report Builder | Report Builder is een invoegtoepassing voor Microsoft Excel. Met Report Builder kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens die in uw Excel-werkbladen worden ingevoegd. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft. | [&#x200B; Report Builder &#x200B;](/help/analyze/report-builder/rb-overview.md) |

<!-- * Realtime reporting? -->

## Aan de slag voor eindgebruikers

Eindgebruikers die geen professionele analisten zijn, kunnen in hun organisatie samenwerken met analisten om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten, of ze kunnen de basisbeginselen van Analysis Workspace leren om actioneerbare inzichten over hun klanten te krijgen.

### Werken met analisten

Meestal zijn gebruikers in een organisatie die meer willen weten over het gedrag van klanten op de verschillende sites, geen professionele analisten.

Ideaal gezien, zouden deze gebruikers met [&#x200B; analisten &#x200B;](#analysts) binnen een organisatie moeten werken:

1. Definieer de vereisten voor de analyses door aan de analist uit te leggen wat hij of zij van klanten wil leren.

1. Herzie de analyses om ervoor te zorgen dat zij aan de doelstellingen voldoen.

1. Bespreek de gegevens die bij de analyses zijn verkregen.

1. Wijzig de analyses naar wens in de loop van de tijd.

### Analyses maken in Analysis Workspace

Je hoeft geen gegevensanalist te zijn om actioneerbare inzichten van Adobe Analytics te krijgen.

Sommige gebruikers zouden het nuttig kunnen vinden om met een gegevensanalist te werken aan opstelling een project in Analysis Workspace en verklaren hoe te om de gegevens te interpreteren, zoals die in [&#x200B; het Werk met analisten &#x200B;](#work-with-analysts) worden beschreven; andere gebruikers zouden comfortabel het project kunnen bouwen en de gegevens zelf interpreteren.

Met Analysis Workspace kunt u snel analyses maken om inzichten te verzamelen en deze inzichten vervolgens met anderen te delen. Gebruikend belemmering-en-dalings browser interface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset in werking te stellen, en projecten met iedereen te delen en te plannen u kiest.

Voor informatie over hoe te om analyses in Analysis Workspace tot stand te brengen, zie [&#x200B; overzicht van Analysis Workspace &#x200B;](/help/analyze/analysis-workspace/home.md).

## Aan de slag met ontwikkelaars

[&#x200B; Analytics APIs &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/) staat u toe om de servers van Adobe direct te roepen om bijna om het even welke actie uit te voeren die u in het gebruikersinterface kunt uitvoeren.

U kunt rapporten maken om te verkennen, inzichten op te halen of belangrijke vragen over uw gegevens te beantwoorden. U kunt ook componenten van Adobe Analytics beheren, zoals het maken van segmenten of berekende metriek.

>[!MORELIKETHIS]
>
>[Een document voor het ontwerp van een oplossing maken](/help/implement/prepare/solution-design.md)
>
