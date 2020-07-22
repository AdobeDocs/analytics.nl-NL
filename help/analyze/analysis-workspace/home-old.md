---
description: Aan de slag met Adobe Analytics.
keywords: Analysis Workspace
title: Aan de slag
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 98%

---


# Analysis Workspace

Analysis Workspace is een van de vlaggenschipprojecten van Adobe waarmee u praktische, op data gebaseerde beslissingen kunt nemen voor uw bedrijf. Met de meest algemene visualisatie, de vrije-vormtabel, kunt u gemakkelijk maatrapporten maken met behulp van dimensies, metrics, segmenten en datumbereiken.

## Vereisten

[Data naar Adobe Analytics verzenden met Adobe Experience Platform Launch](/help/implement/launch/validate-publish-prod.md): voor het gebruik van Analysis Workspace is een werkende implementatie vereist. Zorg dat uw organisatie data naar Adobe verzendt voordat u de tool gebruikt. Andere implementaties, zoals DTM of verouderde handmatige implementaties, kunnen ook werken.

## Een gerangschikt basisrapport opvragen in Workspace

Vraag een gerangschikt basisrapport op met Analysis Workspace. Een gerangschikt rapport toont een samengevoegde totale mening van elk afmetingspunt, die de grootste waarden eerst toont. Deze rapporttypen zijn handig om te zien welke componenten van uw site het meest effectief zijn, zoals welke pagina&#39;s het meeste verkeer krijgen of welke producten het best verkopen.

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
3. Klik in de bovenste navigatiebalk op Workspace.
4. Klik op de knop &#39;Create New Project&#39; (Nieuw project maken).
5. Controleer of de optie voor &#39;Leeg project&#39; is geselecteerd in het modale pop-upmenu en klik vervolgens op Create (Maken).
6. Links ziet u een lijst met dimensies, metrics, segmenten en datumbereiken. Zoek de dimensie voor pagina&#39;s (oranje) en sleep deze naar het canvas op de plek met de tekst &#39;Drop a Dimension Here&#39; (Dimensie hier neerzetten).
7. Als de rapportsuite al data bevat, ziet u een rapport met de beste pagina&#39;s voor deze maand. Analysis Workspace vult het rapport automatisch in met de metric voor [voorvallen](/help/components/metrics/occurrences.md).
8. Zoek de metric voor bezoeken (groen) en sleep deze **op** of **naast** de metrische koptekst Occurences (Voorvallen). (Plaats deze niet boven de metric.) Als u de metric voor bezoeken bovenop Voorvallen plaatst, wordt de metric in de rapportage vervangen. Als u metric voor bezoeken naast Voorvallen sleept, worden beide metrics naast elkaar getoond.
9. Als u uw project wilt bewaren, klikt u op *[!UICONTROL Project] > [!UICONTROL Save]* in het menu linksboven.

## Een basisrapport voor trends opvragen in Workspace

Vraag een basisrapport voor trends op met Analysis Workspace. Een trendsrapport toont een tijdweergave van metrics tijdens de geselecteerde datumreeks. Deze rapporttypen zijn nuttig om trends in een bepaalde tijdsperiode te identificeren, en kunnen worden gebruikt om het succes (of de mislukking) van genomen bedrijfsbesluiten te meten. Zo kunt u bijvoorbeeld een rapport over paginaweergaven binnen een periode inzien om na te gaan of het herontwerp van een bepaalde site heeft geleid tot meer of juist minder verkeer.

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
3. Klik in de bovenste navigatiebalk op Workspace.
4. Klik op de knop &#39;Create New Project&#39; (Nieuw project maken).
5. Controleer of de optie voor &#39;Leeg project&#39; is geselecteerd in het modale pop-upmenu en klik vervolgens op Create (Maken).
6. Links ziet u een lijst met dimensies, metrics, segmenten en datumbereiken. Zoek dimensie voor paginaweergaven en sleep deze naar de kleine ruimte op het canvas met het label &#39;Drop a Metric Here&#39; (Hier een metric neerzetten). Plaats de dimensie niet in de ruimte die is gereserveerd voor dimensies (tenminste niet voor deze oefening).
7. Merk op dat als de rapportreeks data bevat, u een rapport van de paginaweergaven voor de huidige maand zou moeten zien. Het datumbereik &quot;Dag&quot; wordt automatisch ingevoegd door Analysis Workspace, zodat u de trend van het aantal paginaweergaven voor de huidige maand kunt zien.
8. Zoek het datumbereik &quot;Week&quot; (paars) in de lijst met componenten voor het datumbereik aan de linkerkant. Klik op de titel van het datumbereik om alle componenten van het datumbereik uit te vouwen en weer te geven, of gebruik de zoekbalk.
9. Sleep het datumbereik Week boven op de kop van het datumbereik Dag op het canvas om het te vervangen.
10. Let op: uw trendsrapport wordt nu per week geaggregeerd in plaats van per dag.
11. Als u uw project wilt bewaren, klikt u op *[!UICONTROL Project] > [!UICONTROL Save]* in het menu linksboven.

## Experimenteren met de tool

Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metrics naar uw Workspace-project om te zien wat er beschikbaar is.

Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op *[!UICONTROL Project] > [!UICONTROL New]*.

## Problemen oplossen

**Wanneer ik een metric sleep, zie ik het bericht &quot;Ongeldige data&quot;.**

De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. Plaats de metrics in plaats daarvan naast elkaar.

**Wanneer ik een metric sleep, zie ik geen echte data - alleen maar nullen.**

Als u een Workspace-rapport hebt gemaakt, maar het rapport bevat geen data, kunt u een paar dingen controleren:

* Controleer de rapportsuite en zorg ervoor dat deze is gevuld met data.
* Als u een segment in uw rapport gebruikt, kan het zijn dat de segmentcriteria niet met enige data overeenkomen. Verwijder het segment of pas de segmentdefinitie aan.
* Controleer of het datumbereik rechtsboven de verwachte waarde heeft.
* Navigeer naar uw website en gebruik de tool voor foutopsporing om te verifiëren dat de data worden verzameld.

## Aanvullende resources

* [Opmerkingen bij de release van Analysis Workspace](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md): lees meer over de nieuwste functies van de tool.
* [Analysis Workspace op YouTube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): leer hoe u de meeste functies van Analysis Workspace kunt gebruiken met deze uitgebreide afspeellijst.
* Tips voor producten: tips van de dag en korte video&#39;s worden af en toe rechtsonder in Analysis Workspace weergegeven. Als u deze tips afsluit, kunt u ze altijd later bekijken via *[!UICONTROL Help] > [!UICONTROL Tips]*.
* [Analysis Workspace-community](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): bespreek Analysis Workspace met medegebruikers en stem over nieuwe functies die u graag in de tool zou willen zien.
* Blogberichten:
   * [Empowering Organizations with Smarter Analysis](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/) (Organisaties krijgen meer mogelijkheden met slimmere analyse)
   * [New Adobe Analytics Capabilities Make Powerful Insights More Accessible](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/) (Nieuwe Adobe Analytics-functies maken krachtige inzichten toegankelijker)
   * [5 Tips to Maximize Your Productivity with Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/) (Vijf tips om uw productiviteit te maximaliseren met Analysis Workspace)
   * [Faster Insights with Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/) (Snellere inzichten met Analysis Workspace)
   * [Why You Should Be Using Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/) (Waarom u Analysis Workspace moet gebruiken)

## Volgende stappen

U kunt uw kennis van Analysis Workspace op allerlei manieren verdiepen. Hier volgen enkele basisbeginselen die door Adobe worden aanbevolen:

### Voor eindgebruikers meer willen weten over het gebruik van Analysis Workspace

* [Meer informatie over de Workspace-interface](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md): nu dat u een basisrapport hebt gemaakt, kunt u zich meer vertrouwd maken met de rest van de interface.
* [Visualisaties in Workspace](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md): vrije-vormtabellen zijn slechts één type visualisatie in Analysis Workspace. Leer hoe u andere visualisaties gebruikt, zoals lijngrafieken, staafgrafieken en geo-kaarten.
* [Dimensies in Workspace](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): wilt u meer weten over wat dimensies zijn en hoe u ze kunt gebruiken in meer dan alleen gerangschikte rapporten?
* [Metrics in Workspace](/help/analyze/analysis-workspace/components/apply-create-metrics.md): leer meer over wat metrics zijn en hoe u metrics toepast in andere delen van vrije-vormtabellen.
* [Inleiding tot segmentatie](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md): leer wat segmenten zijn en vraag een basisrapport op door een segment te gebruiken.
* [Datumbereiken in Workspace](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): leer over relatieve en doorlopende datums, en hoe u ze in Workspace-projecten gebruikt.
* Projecten delen in Workspace: laat uw collega het fantastische Workspace-project zien dat u hebt gemaakt.
* [(Geavanceerd) Deelvensters in Workspace](/help/analyze/analysis-workspace/c-panels/panels.md): gebruik de geavanceerde functies in Workspace, zoals de functies voor attributie en voor het vergelijken van segmenten.

### Voor analisten en beheerders die zoeken naar hoogwaardige toepassingen van Workspace in hun organisatie

* [Analysis Workspace-machtigingen](https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/admin-getting-started.html): wijs Workspace-rechten toe aan gebruikers via de Adobe Admin Console.
* [Sjablonen in Workspace](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md): maak en werk met sjablonen zodat uw collega&#39;s aan de slag kunnen met een projectruimte die volledig aan hun behoeften voldoet.
* [Workspace richten op doelgroep](/help/analyze/analysis-workspace/curate-share/curate.md): maak een project waarbij het aantal beschikbare componenten wordt beperkt, zodat de werkruimte toegankelijker wordt voor minder ervaren gebruikers
