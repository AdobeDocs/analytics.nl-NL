---
description: Algemene overzichtsinformatie over Adobe Analytics, inclusief informatie over de interface van Analytics en om aan de slag te gaan voor beheerders, analisten, gebruikers en ontwikkelaars.
title: Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars
feature: Analytics Basics
exl-id: 11800de5-224a-4bd2-8cb1-a6318925db71
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '1691'
ht-degree: 4%

---

# Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars

Er zijn vier typen Adobe Analytics-gebruikers in een organisatie die doorgaans werkt:

* **Beheerders:** voer en vorm Adobe Analytics uit.

* **Analysts:** de projecten van de opstelling en creeer analyses gebruikend Analysis Workspace

* **Eind - gebruikers:** verkrijgt actionable inzicht over hun klanten, of door hun eigen analyses te creëren of met analisten te werken om hen tot stand te brengen

* **Ontwikkelaars:** gebruik Adobe Analytics 2.0 APIs om de servers van de Adobe direct te roepen om bijna om het even welke actie uit te voeren die in het gebruikersinterface kan worden uitgevoerd, zoals het creëren van rapporten om te onderzoeken, inzichten te krijgen, of belangrijke vragen over gegevens te beantwoorden.

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

De [ implementatiemethode ](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) u kiest bepaalt het type van gegevens dat kan worden verzameld.

### Adobe Analytics implementeren

Er zijn verschillende implementatiemethoden beschikbaar wanneer u Adobe Analytics implementeert op uw website of mobiele app.

Voor informatie over elke beschikbare methode, zie [ Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) uitvoeren.

| | Implementatiemethoden |
|---------|---------|
| **Websites** | <ul><li>Web SDK-extensie (aanbevolen)</li><li>Web SDK</li><li>Extensie Analytics</li><li>Legacy JavaScript</li></ul> |
| **Mobiele apps** | <ul><li>Mobile SDK-extensie (aanbevolen)</li><li>Extensie Analytics</li></ul> |

{style="table-layout:auto"}

### Adobe Analytics configureren

Analysebeheerders moeten de volgende taken uitvoeren voordat ze Adobe Analytics beschikbaar maken voor gebruikers in de organisatie:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Beheerdersrollen definiëren | Adobe Analytics ondersteunt verschillende typen beheerders | [ de rollen van de Beheerder in Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html) |
| Machtigingen definiëren | Analysebeheerders moeten productprofielen toewijzen in de Admin Console voor Adobe Analytics, Report Suite Tools en Analytics Tools. | [ Toestemmingen van Analytics in de Admin Console ](/help/admin/admin-console/permissions/analytics-tools.md) |
| Stel rapportsuites in en definieer instellingen voor uw bedrijf | Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te produceren.<p>De beheerders kunnen opstelling [ virtuele rapportreeksen ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html) ook aan verdere segmentgegevens.</p> | <ul><li>[Een rapportsuite maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html)</li><li>[ Overzicht van de Montages van het Bedrijf ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html)</li></ul> |
| Gegevens importeren | Met Adobe Analytics-gegevensbronnen kunt u extra online- of offlinegegevens importeren voor rapportage. | [ Overzicht van gegevensbronnen ](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html) |
| Gegevens classificeren met classificaties | Met classificaties kunt u gegevens classificeren om beter gebruik te maken van variabelen, zodat u meer inhoud in één variabele kunt opnemen. | [ Overzicht van Classificaties ](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) |
| Componenten beheren | Gebruik het Woordenboek van Gegevens en de beheersgebieden voor elk componenttype om te bepalen welke componenten in uw implementatie van Analytics beschikbaar zijn, evenals die voor uw organisatie worden goedgekeurd.<p>Dit zou een voortdurende activiteit moeten zijn om ervoor te zorgen dat de componenten effectief in uw organisatie worden gebruikt. </p> | <ul><li>[ Overzicht van het Woordenboek van Gegevens ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html)</li><li>[ Berekende metriekmanager ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html)</li><li>[ beheert plaatsen ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html)</li><li>[Aangepaste datumbereiken maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html)</li></ul> |
| Anomalische detectie | Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens. | [Overzicht van anomaliedetectie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Bijdrage-analyse | De Analyse van de bijdrage ontdekt verborgen patronen binnen uw gegevens om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-verbindende waarden, en plotselinge pieken of vallen voor geselecteerde metriek over convergent publiekssegmenten te identificeren. | [Overzicht van bijdrageanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) |
| Segmentatie van analyse | Hiermee kunt u krachtige, doelgerichte publiekssegmenten maken, beheren, delen en toepassen op uw rapporten met behulp van de analysemogelijkheden, de Adobe Experience Cloud, Adobe Target en andere producten voor geïntegreerde Adobe. | [Analytics-segmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html) |
| Publish-publiek naar Audience Manager | Adobe Audience Manager is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van eerste, tweede (partner) en andere bedrijven. | [Overzicht van Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Integraties | U kunt informatie uit andere toepassingen in Adobe Analytics oppervlakken. <p>Hieronder vindt u een aantal algemene integraties:</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html"> Analytics voor Doel </a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html"> de het stromen Inzameling van Media </a></li> | [Analytics Integration](https://experienceleague.adobe.com/docs/analytics/integration/home.html) |

{style="table-layout:auto"}

### Monitor Adobe Analytics

Er zijn verschillende functies beschikbaar waarmee u uw Adobe Analytics-omgeving kunt bewaken.

De beheerders van Analytics zouden zich van de volgende eigenschappen beschikbaar moeten bewust zijn helpen belangrijke aspecten van uw milieu van Analytics controleren:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Activity Manager rapporteren | De manager van de Activiteit van de Rapportering laat u de rapporteringscapaciteit voor elke rapportreeks in uw organisatie zien. Het biedt gedetailleerde zichtbaarheid in het rapporteren van verbruik en helpt u om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te diagnosticeren en te verhelpen. | [ Meldend Manager van de Activiteit ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html) |
| Gebruik van serveroproepen | Een serveraanroep, ook wel een &quot;hit&quot; of een &quot;verzoek om een afbeelding&quot; genoemd, is een instantie waarin gegevens naar Adobe servers worden verzonden om te worden verwerkt. Een dashboard van het Gebruik van de Vraag van de Server is beschikbaar dat uw gegevens van het de vraagverbruik van de server bijhoudt en het met uw contractuele grens vergelijkt. U kunt waarschuwingen instellen om overgangen te voorkomen. | [ overzicht van het Gebruik van de Vraag van de Server ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html) |
| Logbestanden | Logbestanden waarmee u kunt zien wanneer gebruikers zich aanmelden, hoe ze deze gebruiken, gebruiken, gebruiken, gebruiken, rapporten met suites en Admin wijzigen. | [Logboeken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html) |

{style="table-layout:auto"}

## Aan de slag met analisten

Iedereen in een organisatie kan Adobe Analytics gebruiken om actioneerbare inzichten over klantengedrag over websites en apps te bereiken, maar Adobe Analytics is ontworpen met gegevensanalisten voor ogen.

Hier volgen enkele belangrijke taken en functies waarmee analisten vertrouwd moeten zijn om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten.

| Functie | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Projecten maken en delen in Analysis Workspace | Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen. Gebruikend de belemmering-en-dalingsinterface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset te leiden, projecten met iedereen in uw organisatie te delen en te plannen.<p>Gegevensanalisten zijn vaak verantwoordelijk voor het maken van projecten in Analysis Workspace voor gebruikers binnen hun organisatie.</p><p>Nadat de projecten worden gecreeerd, delen de analisten die projecten met het [ eind gebruikers ](#end-users) (niet-analisten) in hun organisaties die om de gegevens verzochten en hen helpen begrijpen hoe te om het te interpreteren.</p> | <ul><li>[ creeer projecten ](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[ de projecten van het Aandeel ](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attributie | De analisten kunnen aanpassen hoe de afmetingspunten krediet voor succesgebeurtenissen door diverse attributiemodellen en terugkijkvensters in Analysis Workspace te gebruiken krijgen.<p>Lineaire-attributiemodellen geven hetzelfde krediet aan elk aanraakpunt voorafgaand aan een conversie, terwijl First Touch het eerste aanraakpunt volledig crediteert. Er zijn veel andere toewijzingsmodellen beschikbaar, waaronder het Algorithmic-model, dat statistische technieken gebruikt om de optimale allocatie van krediet dynamisch te bepalen. </p> | [ modellen van de Attributie en raadplegingsvensters ](/help/analyze/analysis-workspace/attribution/models.md) |
| Anomalische detectie | Statistische modellering in Analysis Workspace vindt automatisch onverwachte tendensen in uw gegevens door metriek te analyseren en een ondergrens, bovengrens, en verwachte waaier van waarden te bepalen. Wanneer een onverwachte punt of daling voorkomt, alarmeert het systeem u in het rapport. | [Overzicht van anomaliedetectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Bijdrage-analyse | Gebruik Analysis Workspace om verborgen patronen in uw gegevens te ontdekken om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-gebonden waarden, en plotselinge pieken of vallen voor metriek over publiekssegmenten te identificeren. | [ Analyse van de Bijdrage ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) in [ Anomaly Overzicht van de Opsporing ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Waarschuwingen | Maak en beheer waarschuwingen op basis van gegevensanomalieën en &#39;gestapelde&#39; waarschuwingen die meerdere metriek in één waarschuwing vastleggen. | [ overzicht van het alarm ](/help/components/c-alerts/intellligent-alerts.md) |
| Gegevens exporteren | Met Data Warehouse- en gegevensfeeds kunt u gegevens exporteren naar verschillende cloudinstellingen, zoals Google Cloud Platform, Azure RBAC, Azure SAS en Amazon S3. | [ Gids van de Uitvoer van Analytics ](https://experienceleague.adobe.com/docs/analytics/export/home.html) |
| Activiteitenoverzicht | Activity Map is een Adobe Analytics-toepassing die is ontworpen om linkactiviteiten met behulp van visuele overlays te rangschikken en die een dashboard van realtime analyses biedt om de betrokkenheid van het publiek van uw webpagina&#39;s te controleren.<p>Met Activity Map kunt u verschillende weergaven instellen om visueel de versnelling van klantactiviteiten te identificeren, marketinginitiatieven te kwantificeren en op de behoeften en het gedrag van het publiek in te spelen.</p> | [ Activity Map ](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html) |
| Report Builder | Report Builder is een add-in voor Microsoft Excel. Met Report Builder kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens die in uw Excel-werkbladen worden ingevoegd. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft. | [ Report Builder ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) |

<!-- * Realtime reporting? -->

## Aan de slag voor eindgebruikers

Eindgebruikers die geen professionele analisten zijn, kunnen in hun organisatie samenwerken met analisten om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten, of ze kunnen de basisbeginselen van Analysis Workspace leren om actioneerbare inzichten over hun klanten te krijgen.

### Werken met analisten

Meestal zijn gebruikers in een organisatie die meer willen weten over het gedrag van klanten op de verschillende sites, geen professionele analisten.

Ideaal gezien, zouden deze gebruikers met [ analisten ](#analysts) binnen een organisatie moeten werken:

1. Definieer de vereisten voor de analyses door aan de analist uit te leggen wat hij of zij van klanten wil leren.

1. Herzie de analyses om ervoor te zorgen dat zij aan de doelstellingen voldoen.

1. Bespreek de gegevens die bij de analyses zijn verkregen.

1. Wijzig de analyses naar wens in de loop van de tijd.

### Analyses maken in Analysis Workspace

Je hoeft geen gegevensanalist te zijn om actioneerbare inzichten van Adobe Analytics te krijgen.

Sommige gebruikers zouden het nuttig kunnen vinden om met een gegevensanalist te werken aan opstelling een project in Analysis Workspace en verklaren hoe te om de gegevens te interpreteren, zoals die in [ het Werk met analisten ](#work-with-analysts) worden beschreven; andere gebruikers zouden comfortabel het project kunnen bouwen en de gegevens zelf interpreteren.

Met Analysis Workspace kunt u snel analyses maken om inzichten te verzamelen en deze inzichten vervolgens met anderen te delen. Gebruikend belemmering-en-dalings browser interface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset in werking te stellen, en projecten met iedereen te delen en te plannen u kiest.

Voor informatie over hoe te om analyses in Analysis Workspace tot stand te brengen, zie [ overzicht van Analysis Workspace ](/help/analyze/analysis-workspace/home.md).

## Aan de slag met ontwikkelaars

[ Analytics APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) staat u toe om de servers van de Adobe direct te roepen om bijna om het even welke actie uit te voeren die u in het gebruikersinterface kunt uitvoeren.

U kunt rapporten maken om te verkennen, inzichten op te halen of belangrijke vragen over uw gegevens te beantwoorden. U kunt ook componenten van Adobe Analytics beheren, zoals het maken van segmenten of berekende metriek.
