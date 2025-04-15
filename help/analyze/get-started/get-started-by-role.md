---
description: Algemene overzichtsinformatie over Adobe Analytics, inclusief informatie over de interface van Analytics en om aan de slag te gaan voor beheerders, analisten, gebruikers en ontwikkelaars.
title: Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars
feature: Analytics Basics
exl-id: 11800de5-224a-4bd2-8cb1-a6318925db71
source-git-commit: 9a2d4c582b6a3946b658924851e5b5ada2f5a7ee
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 5%

---

# Aan de slag voor beheerders, analisten, eindgebruikers en ontwikkelaars

Er zijn vier typen Adobe Analytics-gebruikers in een organisatie die doorgaans werkt:

* **Beheerders:** Adobe Analytics implementeren en configureren.

* **Analisten:** projecten instellen en analyses maken met behulp van Analysis Workspace

* **Eindgebruikers:** Verkrijg bruikbare inzichten over hun klanten, door hun eigen analyses te maken of door samen te werken met analisten om ze te maken

* **Ontwikkelaars:** gebruik de Adobe Analytics 2.0 API&#39;s om de servers van Adobe rechtstreeks aan te roepen om bijna elke actie uit te voeren die in de gebruikersinterface kan worden uitgevoerd, zoals het maken van rapporten om te verkennen, inzichten te verkrijgen of belangrijke vragen over gegevens te beantwoorden.

In de onderstaande informatie wordt beschreven hoe elk van deze gebruikers aan de slag kan gaan met Adobe Analytics.

## Aan de slag voor beheerders

Analytics-beheerders zijn verantwoordelijk voor het kiezen van de implementatiemethode die het meest geschikt is voor hun organisatie.

Nadat Adobe Analytics is geïmplementeerd, moeten beheerders verschillende configuratietaken uitvoeren om ervoor te zorgen dat analisten en eindgebruikers de volledige waarde van Adobe Analytics krijgen. Beheerders moeten ook regelmatig toezicht houden op hun analyseomgeving om ervoor te zorgen dat het systeem efficiënt werkt.

### Bepaal de soorten gegevens die moeten worden verzameld

Met Adobe Analytics kunt u gegevens verzamelen van verschillende soorten kanalen en deze samenbrengen om zinvolle, real-time klantinzichten te bieden.

Hieronder vindt u een aantal ondersteunde kanalen waarop gegevens kunnen worden verzameld:

* Mobiele telefoons

* Het internet der dingen

* TV

* Spraakassistenten

* Verbonden auto&#39;s

* En meer (er worden regelmatig nieuwe ondersteunde kanalen toegevoegd)

De [implementatiemethode](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) die u kiest, bepaalt het type gegevens dat kan worden verzameld.

### Adobe Analytics implementeren

Er zijn verschillende implementatiemethoden beschikbaar bij het implementeren van Adobe Analytics op uw website of mobiele app.

Zie [Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) implementeren voor meer informatie over elke beschikbare methode.

| | Implementatiemethoden |
|---------|---------|
| **Websites** | <ul><li>Web-SDK-extensie (aanbevolen)</li><li>Web SDK</li><li>Extensie Analytics</li><li>Legacy JavaScript</li></ul> |
| **Mobiele apps** | <ul><li>Mobile SDK-extensie (aanbevolen)</li><li>Extensie Analytics</li></ul> |

{style="table-layout:auto"}

### Adobe Analytics configureren

Analytics-beheerders moeten de volgende taken uitvoeren voordat ze Adobe Analytics beschikbaar maken voor gebruikers in de organisatie:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Beheerdersrollen definiëren | Adobe Analytics ondersteunt verschillende soorten beheerders | [Beheerdersrollen in Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html) |
| Machtigingen definiëren | Analysebeheerders moeten productprofielen toewijzen in de Admin Console for Adobe Analytics, Report Suite Tools en Analytics Tools. | [ Toestemmingen van Analytics in Admin Console ](/help/admin/admin-console/permissions/analytics-tools.md) |
| Stel rapportsuites in en definieer instellingen voor uw bedrijf | Een rapportenreeks is een silo van gegevens die Adobe Analytics gebruikt om rapporten te produceren.<p>Beheerders kunnen ook virtuele rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html) instellen [om gegevens verder te segmenteren.</p> | <ul><li>[Een rapportsuite maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html)</li><li>[Overzicht bedrijfsinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html)</li></ul> |
| Gegevens importeren | Met Adobe Analytics-gegevensbronnen kunt u aanvullende online of offline gegevens importeren voor rapportage. | [Overzicht van gegevensbronnen](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html) |
| Gegevens classificeren met classificaties | Met classificaties kunt u gegevens classificeren om beter gebruik te maken van variabelen, zodat u meer inhoud in één variabele kunt opnemen. | [Overzicht van classificaties](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) |
| Onderdelen beheren | Gebruik de gegevenswoordenlijst en de beheergebieden voor elk onderdeeltype om te bepalen welke onderdelen beschikbaar zijn in uw Analytics-implementatie en welke zijn goedgekeurd voor uw organisatie.<p>Dit moet een doorlopende activiteit zijn om ervoor te zorgen dat componenten effectief worden gebruikt in uw organisatie. </p> | <ul><li>[Overzicht van gegevenswoordenboek](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html)</li><li>[ Berekende metriekmanager ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html)</li><li>[ beheert plaatsen ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html)</li><li>[Aangepaste datumbereiken maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html)</li></ul> |
| Anomalische detectie | Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde statistiek is veranderd ten opzichte van eerdere gegevens. | [Overzicht van anomaliedetectie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| Bijdrage analyse | Bijdrageanalyse ontdekt verborgen patronen in uw gegevens om statistische afwijkingen te verklaren en correlaties te identificeren achter onverwachte klantacties, niet-uitgaande waarden en plotselinge pieken of dalen voor geselecteerde statistieken in convergente doelgroepsegmenten. | [Overzicht van bijdrageanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) |
| Analytische segmentatie | Hiermee kunt u krachtige, gerichte doelgroepsegmenten bouwen, beheren, delen en toepassen op uw rapporten met behulp van Analytics-mogelijkheden, de Adobe Experience Cloud, Adobe Target en andere geïntegreerde Adobe-producten. | [Analytics-segmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html) |
| Publiceer publiek naar Audience Manager | Adobe Audience Manager is een krachtig platform voor gegevensbeheer waarmee u unieke publieksprofielen kunt maken van de integratie van gegevens van eerste, tweede (partner) en andere bedrijven. | [Overzicht van Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| Integraties | U kunt informatie uit andere toepassingen ophalen in Adobe Analytics. <p>Hieronder volgen enkele veelvoorkomende integraties:</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html"> Analytics voor Doel </a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html">De collectie streaming media</a></li> | [Analytics Integration](https://experienceleague.adobe.com/docs/analytics/integration/home.html) |

{style="table-layout:auto"}

### Adobe Analytics bewaken

Er zijn verschillende functies beschikbaar om u te helpen bij het bewaken van uw Adobe Analytics-omgeving.

Analytics-beheerders moeten op de hoogte zijn van de volgende functies die beschikbaar zijn om belangrijke aspecten van uw Analytics-omgeving te monitoren:

| Taak | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Activiteitenbeheer voor rapportage | Met Reporting Activity Manager kunt u de rapportagecapaciteit voor elke rapportsuite in uw organisatie bekijken. Het biedt gedetailleerde zichtbaarheid in het rapporteren van verbruik en helpt u om capaciteitsproblemen tijdens piekrapportagetijden eenvoudig te diagnosticeren en te verhelpen. | [ Meldend Manager van de Activiteit ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html) |
| Gebruik van serveroproepen | Een serveraanroep, ook wel een &quot;hit&quot; of &quot;image request&quot; genoemd, is een instantie waarin gegevens naar Adobe-servers worden verzonden om te worden verwerkt. Er is een dashboard voor het gebruik van serveroproepen beschikbaar dat uw verbruiksgegevens van serveroproepen bijhoudt en vergelijkt met uw contractuele limiet. U kunt waarschuwingen instellen om overschrijdingen te voorkomen. | [Overzicht van het gebruik van serveroproepen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html) |
| Logbestanden | Logbestanden om u te helpen zien wanneer gebruikers zich aanmelden, hun gebruik, toegang, rapportsuites en beheerderswijzigingen. | [Logboeken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html) |

{style="table-layout:auto"}

## Aan de slag voor analisten

Hoewel iedereen in een organisatie Adobe Analytics kan gebruiken om bruikbare inzichten te verkrijgen over het gedrag van klanten op websites en in apps, is Adobe Analytics ontworpen met data-analisten in gedachten.

Hieronder volgen de belangrijkste taken en functies waarmee analisten bekend moeten zijn om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten.

| Functie | Beoogd gebruik | Meer informatie |
|---------|----------|---------|
| Projecten maken en delen in Analysis Workspace | Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen. Gebruikend de belemmering-en-dalingsinterface, kunt u uw analyse amberen, visualisaties toevoegen om gegevens aan het leven te brengen, een dataset te leiden, projecten met iedereen in uw organisatie te delen en te plannen.<p>Gegevensanalisten zijn vaak verantwoordelijk voor het maken van projecten in Analysis Workspace voor gebruikers binnen hun organisatie.</p><p>Nadat projecten zijn gemaakt, delen analisten die projecten met de [eindgebruikers](#end-users) (niet-analisten) in hun organisaties die de gegevens hebben opgevraagd en helpen ze hen te begrijpen hoe ze deze moeten interpreteren.</p> | <ul><li>[Projecten maken](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[Deel projecten](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| Attributie | Analisten kunnen aanpassen hoe dimensie-items worden toegekend voor succesgebeurtenissen door gebruik te maken van verschillende attributiemodellen en terugblikperioden in Analysis Workspace.<p>Lineaire attributiemodellen geven evenveel krediet aan elk contactpunt dat leidt tot een conversie, terwijl First Touch volledig krediet geeft aan het eerste contactpunt. Er zijn veel andere attributiemodellen beschikbaar, waaronder het Algoritmische model, dat statistische technieken gebruikt om de optimale toewijzing van krediet dynamisch te bepalen. </p> | [Toeschrijvingsmodellen en overzichtsperioden](/help/analyze/analysis-workspace/attribution/models.md) |
| Detectie van afwijkingen | Statistische modellering in Analysis Workspace vindt automatisch onverwachte trends in uw gegevens door metrische gegevens te analyseren en een ondergrens, bovengrens en verwacht bereik van waarden te bepalen. Wanneer er een onverwachte piek of daling optreedt, waarschuwt het systeem u in het rapport. | [Overzicht van anomaliedetectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Bijdrage analyse | Gebruik Analysis Workspace om verborgen patronen in uw gegevens te ontdekken om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-gebonden waarden, en plotselinge pieken of vallen voor metriek over publiekssegmenten te identificeren. | [ Analyse van de Bijdrage ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) in [ Anomaly Overzicht van de Opsporing ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) |
| Waarschuwingen | Maak en beheer waarschuwingen op basis van gegevensafwijkingen en &#39;gestapelde&#39; waarschuwingen die meerdere metrische gegevens in één melding vastleggen. | [Overzicht van waarschuwingen](/help/components/c-alerts/intellligent-alerts.md) |
| Gegevens exporteren | Met datawarehouse en datafeeds kunt u gegevens exporteren naar verschillende cloudbestemmingen, zoals Google Cloud Platform, Azure RBAC, Azure SAS en Amazon S3. | [Exportgids voor Analytics](https://experienceleague.adobe.com/docs/analytics/export/home.html) |
| Kaart van de activiteiten | Activity Map is een Adobe Analytics-toepassing die is ontworpen om linkactiviteit te rangschikken met behulp van visuele overlays en een dashboard met realtime analyses te bieden om de betrokkenheid van het publiek op uw webpagina&#39;s te volgen.<p>Met Activity Map kunt u verschillende weergaven instellen om de versnelling van klantactiviteit visueel te identificeren, marketinginitiatieven te kwantificeren en te reageren op de behoeften en het gedrag van het publiek.</p> | [Activiteitenkaart](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html) |
| Report Builder | Report Builder is een invoegtoepassing voor Microsoft Excel. Met Report Builder kunt u aangepaste aanvragen maken op basis van Adobe Analytics-gegevens die in uw Excel-werkbladen worden ingevoegd. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft. | [Rapport Builder](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/rb-overview) |

<!-- * Realtime reporting? -->

## Aan de slag voor eindgebruikers

Eindgebruikers die geen professionele analisten zijn, kunnen in hun organisatie samenwerken met analisten om de volledige kracht van Adobe Analytics en Analysis Workspace te benutten, of ze kunnen de basisbeginselen van Analysis Workspace leren om actioneerbare inzichten over hun klanten te krijgen.

### Werken met analisten

Meestal zijn gebruikers in een organisatie die meer willen weten over het gedrag van klanten op de verschillende sites, geen professionele analisten.

Idealiter zouden deze gebruikers moeten samenwerken met [analisten](#analysts) binnen een organisatie om:

1. Definieer vereisten voor de analyses door aan de analist uit te leggen wat hij hoopt te weten te komen over klanten.

1. Bekijk de analyses om er zeker van te zijn dat ze aan de doelstellingen voldoen.

1. Bespreek de gegevens die uit de analyses zijn verkregen.

1. Pas de analyses in de loop van de tijd zo nodig aan.

### Analyses maken in Analysis Workspace

Je hoeft geen data-analist te zijn om bruikbare inzichten uit Adobe Analytics te halen.

Sommige gebruikers vinden het misschien handig om samen te werken met een gegevensanalist om een project in te stellen in Analysis Workspace en uit te leggen hoe de gegevens moeten worden geïnterpreteerd, zoals beschreven in [Werken met analisten](#work-with-analysts); andere gebruikers kunnen zich op hun gemak voelen bij het bouwen van het project en het zelf interpreteren van de gegevens.

Met Analysis Workspace kunt u snel analyses maken om inzichten te verzamelen en deze inzichten vervolgens met anderen te delen. Met behulp van de browserinterface met slepen en neerzetten kunt u uw analyse maken, visualisaties toevoegen om gegevens tot leven te brengen, een gegevensset samenstellen en projecten delen en plannen met wie u maar wilt.

Voor informatie over hoe te om analyses in Analysis Workspace tot stand te brengen, zie [ overzicht van Analysis Workspace ](/help/analyze/analysis-workspace/home.md).

## Aan de slag met ontwikkelaars

[ Analytics APIs ](https://developer.adobe.com/analytics-apis/docs/2.0/) staat u toe om de servers van Adobe direct te roepen om bijna om het even welke actie uit te voeren die u in het gebruikersinterface kunt uitvoeren.

U kunt rapporten maken om te verkennen, inzichten op te halen of belangrijke vragen over uw gegevens te beantwoorden. U kunt ook componenten van Adobe Analytics beheren, zoals het maken van segmenten of berekende metriek.

>[!MORELIKETHIS]
>
>[Een document voor het ontwerp van een oplossing maken](/help/implement/prepare/solution-design.md)
>
