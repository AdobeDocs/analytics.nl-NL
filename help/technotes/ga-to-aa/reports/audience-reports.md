---
title: Poortrapporten in Adobe Analytics
description: Leer hoe u op het publiek gebaseerde rapporten kunt maken met Analysis Workspace.
feature: Third-party Integration
exl-id: 739b0c3d-3f74-41fa-a2cc-f02c17d85ce2
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 0%

---

# Poortverslagen

De rapporten van het publiek tonen informatie over de types van mensen die uw plaats bezoeken.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics](create-report.md) als u het gereedschap nog niet kent in Adobe Analytics.

## Actieve gebruikers

Actieve gebruikers laten het totale aantal gebruikers van uw site zien in de voorafgaande 1, 7, 14 of 28 dagen. Hoewel Adobe niet de nauwkeurige berekening heeft die in Google Analytics wordt gebruikt, kunt u de metrische Unieke Bezoekers gebruiken om een gededupliceerde telling van gebruikers aan uw plaats te zien die op de geselecteerde datumwaaier wordt gebaseerd.

Een lijngrafiek van unieke bezoekers verkrijgen:

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de lijnvisualisatie naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep vervolgens het gereedschap **Unieke bezoekers** In de kleinere ruimte met het label &#39;Hier een metrisch teken neerzetten&#39;.
3. Als een andere granulariteit gewenst is, sleept u het gewenste datumbereik (bijvoorbeeld **Dag**, **Week**, **Maand**, enz.) boven op de koptekst van de bestaande datumdimensie.

Zie [Unieke bezoekers](/help/components/metrics/unique-visitors.md) in de gebruikershandleiding voor componenten voor meer informatie over hoe Adobe unieke bezoekers berekent.

## Lifetime-waarde

De waarde van het leven is een eigenschap die extra gespecialiseerde implementatie op beide platforms vereist. Adobe raadt aan samen te werken met een implementatieconsultant om deze gegevens te verkrijgen.

## Cohortanalyse

De Analyse van de kabel toont hoe vaak de zelfde gebruikers aan uw plaats terugkeren.

Een cohortingtabel maken:

1. Klik op het pictogram Visualisatie aan de linkerkant en sleep de visualisatie Cohortingtabel naar de werkruimte.
2. Klik op het pictogram Componenten aan de linkerkant en sleep vervolgens het gereedschap **Bezoeken** op zowel de Criteria van de Opname als Criteria van de Terugkeer metrisch.
3. Klik op Samenstellen.

Zie [Cohortanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) in de Analysis Workspace-gebruikershandleiding voor meer informatie over aanvullende aanpassingen aan de cohortvisualisatie.

## Soorten publiek

Het verslag van het publiek in de Google Analytics vereist de instelling van een publiek. Voor het publiek is ook configuratie in Adobe via Adobe Audience Manager vereist. Raadpleeg de gebruikershandleiding van Adobe Audience Manager voor meer informatie.

## Gebruikersverkenner

Het rapport van de Ontdekkingsreiziger van de Gebruiker staat een analist toe om individuele bezoeken door anonymized herkenningstekens te bekijken. Adobe heeft geen oppervlak voor de achterste id&#39;s buiten gegevensfeeds, die onbewerkte gegevensexport op raakniveau zijn.

* Als deze gegevens in Analysis Workspace worden gewenst, is het mogelijk om met een implementatieconsultant samen te werken om de geanonimiseerde waarde voor unieke id-cookies door te geven aan een eVar. Merk op dat dit slechts met kleinere implementaties werkt die uit minder dan 1 miljoen unieke bezoekers per maand bestaan.
* Als deze gegevens binnen gegevensvoer worden gewenst, de samengevoegde kolommen `visid_high` en `visid_low` zijn de meest gebruikelijke manier om unieke bezoekers te identificeren . Meer informatie over [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) in de gebruikershandleiding bij Exporteren.

## Demografische en belangenverslagen

Demografische gegevens en interesses bevatten informatie over leeftijd, geslacht en belangen van gebruikers van de site. Deze gegevens worden door Google verzameld op basis van hun mogelijkheden voor intersite tracering.

Demografische gegevens en interesses worden niet automatisch door Adobe verzameld. Als uw organisatie deze gegevens echter verkrijgt, kunt u Customer Attributes gebruiken, een functie in het Adobe Experience Cloud-Platform. Het maakt volledige controle mogelijk over de organisatie van gegevens op basis van kenmerken, en is niet beperkt tot demografie of belangen.

Raadpleeg de Help voor klantkenmerken voor meer informatie.

## Geo - Taal

Het taalrapport van de geo toont plaatsverkeer door de taal die in browser van de bezoeker plaatst.

Een taalrapport maken:

1. Zoek in het menu Componenten de locatie **Taal** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Taal](/help/components/dimensions/language.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Geo - Locatie

Het geolocatierapport geeft een wereldwijde kaartweergave, waarbij gegevens per land worden uitgesplitst.

Een geografisch locatierapport maken:

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de visualisatie Kaart naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep vervolgens het gereedschap **Unieke bezoekers** In de ruimte met het label Metrisch toevoegen.
3. Klik op Samenstellen.

Als de tabel naast de kaart ook wordt gezocht:

1. Zoek in het menu Componenten de locatie **Landen** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Landen](/help/components/dimensions/countries.md) in de gebruikershandleiding voor componenten voor meer informatie.

## Gedrag - Nieuw vs Terugsturen

Het nieuwe versus het terugsturen rapport geeft een vereenvoudigde mening van eerste zittingen (nieuwe bezoeken) versus volgende zittingen (terugkeerbezoeken).

Een nieuw rapport of een rapport met terugkerende bezoeken maken:

1. Zoek in het optiemenu van de componenten de **Eerste bezoeken** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;. Let op: **Eerste bezoeken** is een segment, terwijl Workspace doorgaans afmetingen gebruikt om rijen te vertegenwoordigen.
2. Zoek de **Retourbezoeken** en sleep deze boven op de rijkop Segmenten. Hierdoor wordt het segment toegevoegd als een dimensie onder First Time Visits, zodat u het eenvoudig kunt vergelijken.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Als een lijngrafiek ook wordt gewenst:

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een lijnvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Gebruik Ctrl+klikken (Windows) of cmd+klikken (Mac) op elke rij in de vrije-vormtabel om deze te markeren. Hierdoor kunnen beide trends in de lijnvisualisatie worden weergegeven.
3. Klik op het kleine ronde punt linksboven in de lijnvisualisatie en klik vervolgens op het selectievakje Selectie vergrendelen.

## Gedrag - Frequentie en Recentie

Het frequentie- en recentierapport is ongeveer gelijk aan **Bezoek nummer** dimensie in Analysis Workspace.

1. Zoek in het optiemenu van de componenten de **Bezoek nummer** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Bezoek nummer](/help/components/dimensions/visit-number.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Gedrag - Betrokkenheid

Het betrokkenheidsrapport is ongeveer gelijk aan het **Tijd besteed per bezoek - Emmerd** dimensie.

1. Zoek in het optiemenu van de componenten de **Tijd besteed per bezoek - Emmerd** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Tijd besteed per bezoek](/help/components/dimensions/time-spent-per-visit.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Technologie - Browser en besturingssysteem

Het rapport Browser &amp; OS bevat meerdere primaire afmetingen.

* De **Browser** De primaire dimensie is ook beschikbaar in Analysis Workspace als dimensie.
* De **Besturingssysteem** De primaire dimensie is ook beschikbaar in Analysis Workspace als dimensie.
* De **Schermresolutie** de primaire dimensie is in Analysis Workspace beschikbaar als de **Monitorresolutie** dimensie.
* De **Schermkleuren** de primaire dimensie is in Analysis Workspace beschikbaar als de **Kleurdiepte** dimensie.
* De **Flash-versie** De primaire dimensie is niet beschikbaar in Adobe Analytics, maar deze gegevens kunnen desgewenst door een eVar worden verzameld.

1. Zoek in het optiemenu de gewenste afmeting die hierboven is vermeld en sleep deze naar het grote tabelgebied in vrije vorm met het label &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de volgende pagina&#39;s in de gebruikershandleiding van Componenten voor meer informatie over hun respectievelijke dimensie:

* [Browser](/help/components/dimensions/browser.md)
* [Besturingssysteem](/help/components/dimensions/operating-systems.md)
* [Monitorresolutie](/help/components/dimensions/monitor-resolution.md)
* [Kleurdiepte](/help/components/dimensions/color-depth.md)

## Technologie - Netwerk

Het netwerkrapport is ongeveer gelijk aan **Domein** dimensie.

1. Zoek in het optiemenu van de componenten de **Domein** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Domein](/help/components/dimensions/domain.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Mobiel - Overzicht

Het mobiele overzichtsrapport is ongeveer gelijk aan **Type mobiel apparaat** dimensie. Merk op dat de waarde &quot;Andere&quot;aan Desktopverkeer gelijkwaardig is.

1. Zoek in het optiemenu van de componenten de **Type mobiel apparaat** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Mobiel apparaattype](/help/components/dimensions/mobile-dimensions.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Mobiele apparaten

Het rapport over mobiele apparaten is ongeveer gelijk aan het **Mobiel apparaat** dimensie.

1. Zoek in het optiemenu van de componenten de **Mobiel apparaat** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Mobiel apparaat](/help/components/dimensions/mobile-dimensions.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Aangepast

Aangepaste rapporten worden per implementatie gedefinieerd. Werk met de Analysebeheerder van uw organisatie en/of de adviseur van de implementatie om deze rapporten te interpreteren. Een organisatie onderhoudt doorgaans een [Document voor oplossingsontwerp](/help/implement/prepare/solution-design.md) om aangepaste variabelewaarden bij te houden en te bepalen hoe deze worden gevuld.

## Benchmarking

Met benchmarkingsrapporten kunt u zien hoe facetten van uw gegevens worden vergeleken met industriële gemiddelden. Adobe deelt momenteel geen benchmarkingsgegevens tussen haar klanten.

## Gebruikersstroom

Het stroomrapport is beschikbaar op beide platforms. Een flowrapport maken:

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Zoek de **Pagina&#39;s** en klikt u op het pictogram Pijl om de paginawaarden weer te geven. Dimension-items zijn gekleurd geel.
3. Zoek de gewenste paginawaarde waarmee moet worden begonnen en sleep deze naar de ruimte met het label &#39;Dimension of item&#39; in het midden
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.
