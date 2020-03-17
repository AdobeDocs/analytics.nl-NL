---
description: Aan de slag met Adobe Analytics.
keywords: Analysis Workspace
title: Aan de slag-handleiding
topic: Reports and analytics
uuid: 851feadb-5e30-45ab-9f66-02bdf844fa54
translation-type: tm+mt
source-git-commit: 984d6034d14cc4256d93bd4f7d1a7f01b63b71e9

---


# Werkruimte Analyse

De analysewerkruimte is een van de vlaggenschipprogramma&#39;s van Adobe voor het nemen van op gegevens gebaseerde beslissingen voor uw organisatie. De gemeenschappelijkste visualisatie, de vrije vormlijst, laat u gemakkelijk aangepaste rapporten creëren gebruikend afmetingen, metriek, segmenten, en datumwaaiers.

## Vereisten

[Gegevens naar Adobe Analytics verzenden met Adobe Experience Platform Launch](/help/implement/launch/validate-publish-prod.md): Het gebruiken van de Werkruimte van de Analyse vereist een werkende implementatie. Zorg ervoor dat uw organisatie gegevens naar Adobe verzendt voordat u het hulpprogramma gebruikt. Andere implementaties, zoals DTM of oudere handmatige implementaties, kunnen ook werken.

## Een rapport met een standaardpositie in Workspace samenstellen

Trek een basis gerangschikt rapport gebruikend de Werkruimte van de Analyse. Een gerangschikt rapport geeft een geaggregeerde totaalweergave van elke waarde van de dimensie weer, waarbij eerst de grootste waarden worden weergegeven. Deze typen rapporten zijn handig om te zien welke componenten van uw site het meest effectief zijn, zoals welke pagina&#39;s het meeste verkeer krijgen of welke producten het meest verkopen.

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
2. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
3. Klik in de bovenste navigatiebalk op Werkruimte.
4. Klik op de knop Nieuw project maken.
5. Controleer of Leeg project is geselecteerd in het modaal pop-upmenu en klik vervolgens op Maken.
6. Links ziet u een lijst met dimensies, metriek, segmenten en datumbereiken. Zoek de pagina-afmetingen (oranje gekleurd) en sleep deze naar het canvas waar de tekst &#39;Een dimensie hier neerzetten&#39; staat.
7. Merk op dat als de rapportreeks gegevens heeft, een rapport dat de hoogste pagina&#39;s voor deze maand toont kan worden gezien. De Werkruimte van de analyse bevolkte automatisch het rapport met metrische [Voorvallen](/help/components/c-variables/c-metrics/metrics-occurrences.md) .
8. Zoek de metrische (gekleurde groene) bezoekerslijst en sleep deze **boven** of **naast** de metrische koptekst Voorkomt (en plaats deze niet boven de metrische koptekst). Als u metrisch van Bezoekingen bovenop Voorkomen sleept, wordt metrisch vervangen in rapportering. Als u metrisch van Bezoekingen naast Voorkomen sleept, worden beide metriek getoond zij aan zij.
9. Als u uw project wilt bewaren, klik *[!UICONTROL Project][!UICONTROL Save]*> in het hogere linkermenu.

## Trek een fundamenteel trendrapport in Werkruimte

Trek een fundamenteel trended rapport gebruikend de Werkruimte van de Analyse. Een trended-rapport toont een weergave van metrische gegevens die de geselecteerde datumreeks gebruiken in de tijd. Deze types van rapporten zijn nuttig om tendensen in tijd te identificeren, en kunnen worden gebruikt om succes of mislukking van bedrijfsbesluiten te meten die worden genomen. Bijvoorbeeld, kon u een rapport bekijken van de paginameningen dat in tijd wordt trended om te zien of hielp een plaatsherontwerp verkeer verhogen of verminderen.

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
2. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
3. Klik in de bovenste navigatiebalk op Werkruimte.
4. Klik op de knop Nieuw project maken.
5. Controleer of Leeg project is geselecteerd in het modaal pop-upmenu en klik vervolgens op Maken.
6. Links ziet u een lijst met dimensies, metriek, segmenten en datumbereiken. Zoek de afmetingen voor de paginaweergaven en sleep deze naar de kleine ruimte op het canvas met de naam &#39;Hier een metrische waarde neerzetten&#39;. Vermijd het weglaten in de ruimte die is gereserveerd voor afmetingen (tenminste voor deze oefening).
7. Merk op dat als de rapportreeks gegevens heeft, u een rapport van de basispaginameningen over de huidige maand trended zou moeten zien. De Werkruimte van de analyse wordt automatisch gebracht in de de datumwaaier van &quot;Dag&quot;zodat kunt u de trend van paginameningen voor de huidige maand zien.
8. Zoek het datumbereik van de week (paars gekleurd) in de lijst met componenten voor het datumbereik aan de linkerkant. Klik op de titel van het datumbereik om alle componenten van het datumbereik uit te vouwen en weer te geven, of gebruik de zoekbalk.
9. Sleep het datumbereik van de week boven op de kop van het datumbereik van Dag op het canvas om het te vervangen.
10. Let op: uw trended-rapport wordt nu geaggregeerd per week in plaats van per dag.
11. Als u uw project wilt bewaren, klik *[!UICONTROL Project][!UICONTROL Save]*> in het hogere linkermenu.

## Experimenteren met het gereedschap

Aangezien de Werkruimte van de Analyse een rapporteringshulpmiddel is, heeft het geen invloed op gegevensinzameling. Er zijn geen gevolgen om zonder onderscheid componenten naar een project te slepen om te zien wat werkt. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is.

Als u per ongeluk een ongeldige component naar uw werkruimteproject sleept of een stap wilt terugkeren, drukt u op ctrl+Z (Windows) of cmd+Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door op *[!UICONTROL Project][!UICONTROL New]*> in het menu linksboven te klikken.

## Problemen oplossen

**Wanneer ik metrisch over sleep, zegt het &quot;Ongeldige gegevens&quot;.**

Ongeldige gegevens betekenen dat Adobe geen gegevens kan retourneren met de combinatie van afmetingen en metriek die in het rapport wordt gebruikt. Twee metriek die bijvoorbeeld boven op elkaar zijn gestapeld, kunnen niet als gegevens worden geretourneerd, omdat er geen manier is om twee metriek op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

**Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul.**

Als u met succes een werkruimterapport creeert maar er geen gegevens zijn, kunt u een paar dingen controleren:

* Controleer de rapportsuite en zorg ervoor dat deze is gevuld met gegevens.
* Als u een segment in uw rapport gebruikt, zouden de segmentcriteria geen gegevens kunnen aanpassen. Probeer het segment te verwijderen of de segmentdefinitie aan te passen.
* Controleer de datumwaaier in hoger recht en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer naar uw website en gebruik Foutopsporing om te controleren of er gegevens worden verzameld.

## Aanvullende bronnen

* [Opmerkingen](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md)bij de release Analyse Workspace: Lees meer over de nieuwste functies die in het gereedschap zijn geïntroduceerd.
* [Analyse van werkruimte op YouTube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): Leer hoe u de meeste functies in de analysewerkruimte kunt gebruiken via deze uitgebreide afspeellijst.
* Tips voor producten: Tips van de dag worden samen met korte video&#39;s af en toe weergegeven in de rechterbenedenhoek van de analysewerkruimte. Als deze uiteinden worden genegeerd, kunnen ze op elk gewenst moment via *[!UICONTROL Help]>[!UICONTROL Tips]*worden bereikt.
* [Werkruimte](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace)voor analyse: Bespreek de Werkruimte van de Analyse met medegebruikers, en stem over eigenschappen u in het hulpmiddel wilt zien.
* Blogberichten:
   * [Organisaties meer mogelijkheden bieden met slimmere analyse](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [Nieuwe Adobe Analytics-mogelijkheden maken krachtige inzichten toegankelijker](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [5 tips om uw productiviteit te maximaliseren met analysewerkruimte](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [Snellere inzichten met analysewerkruimte](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Waarom u de werkruimte Analyse moet gebruiken](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## Volgende stappen

Er zijn veel richtingen om uw begrip van de Werkruimte van de Analyse te verdiepen. Hier volgen enkele basisbeginselen die door Adobe worden aanbevolen:

### Voor eindgebruikers die kennis willen uitbreiden over het gebruik van de analysewerkruimte

* [Gegevens over de interface](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md)van de werkruimte: Nu u een basisrapport hebt gecreeerd, wordt vertrouwd met de rest van de interface.
* [Visualisaties in werkruimte](visualizations/freeform-analysis-visualizations.md): De lijsten van de vrije vorm zijn slechts één type van visualisatie in de Werkruimte van de Analyse. Leer hoe u andere visualisaties gebruikt, zoals lijngrafieken, staafgrafieken en geo-overzichten.
* [Afmetingen in werkruimte](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): Meer weten over welke afmetingen en hoe u deze kunt gebruiken in meer dan alleen gerangschikte rapporten?
* [Metrische gegevens in werkruimte](/help/analyze/analysis-workspace/components/apply-create-metrics.md): Leer meer over welke metriek zijn en hoe te om hen in andere delen van vrije vormlijsten te gebruiken.
* [Inleiding tot segmentatie](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md): Leer over welke segmenten zijn en trek een basisrapport gebruikend een segment.
* [Datumbereiken in werkruimte](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): Leer over relatieve en roldata, en gebruik hen in werkruimteprojecten.
* Projecten delen in Workspace: Toon uw collega het fantastische project van de Werkruimte u creeerde.
* [(Geavanceerd) Deelvensters in werkruimte](c-panels/panels.md): Geavanceerde functies in Workspace gebruiken, zoals Attribution and Segment Comparison.

### Voor analisten en beheerders die de kwaliteit van de werkruimte in hun organisatie willen verbeteren

* [Machtigingen voor](https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html)analysewerkruimte: Wijs gebruikersmachtigingen toe aan Workspace via de Adobe Admin Console.
* [Maak een document](/help/implement/prepare/solution-design.md)voor het ontwerp van een oplossing: Begin te plannen hoe uw organisatie extra dimensies of metriek specifiek voor uw plaats verzamelt.
* [Sjablonen in werkruimte](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md): Creeer malplaatjes zodat kunnen uw collega&#39;s met een projectruimte beginnen die aan hun behoeften wordt aangepast.
* [Werkruimte krommen](curate-share/curate.md): Maak een project dat beschikbare componenten beperkt, waardoor de werkruimte toegankelijker wordt voor minder bekende gebruikers
