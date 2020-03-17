---
title: Poortrapporten in Adobe Analytics
description: Leer hoe u op het publiek gebaseerde rapporten kunt maken met gebruik van de analysewerkruimte.
translation-type: tm+mt
source-git-commit: ''

---


# Poortverslagen

De rapporten van het publiek tonen informatie over de types van mensen die uw plaats bezoeken.

Deze pagina veronderstelt de gebruiker een basiskennis van het gebruiken van de Werkruimte van de Analyse heeft. Zie Een basisrapport [maken in de Analyse Workspace voor Google Analytics-gebruikers](create-report.md) als u nog niet bekend bent met het hulpprogramma in Adobe Analytics.

## Actieve gebruikers

Actieve gebruikers laten het totale aantal gebruikers van uw site zien in de voorafgaande 1, 7, 14 of 28 dagen. Hoewel Adobe niet beschikt over de exacte berekening die wordt gebruikt in Google Analytics, kunt u de metrische unieke bezoekers gebruiken om een gededupliceerde telling van gebruikers naar uw site weer te geven op basis van het geselecteerde datumbereik.

Een lijngrafiek van unieke bezoekers verkrijgen:

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de lijnvisualisatie naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep de metrische waarde voor **Unieke bezoekers** naar de kleinere ruimte met het label &#39;Hier een metrisch getal neerzetten&#39;.
3. Als een andere granulariteit gewenst is, sleept u het gewenste datumbereik (bijvoorbeeld **Dag**, **Week**, **Maand**, enz.) boven op de koptekst van de bestaande datumdimensie.

Zie [Unieke bezoekers](/help/components/c-variables/c-metrics/metrics-unique-visitors.md) in de gebruikershandleiding voor componenten voor meer informatie over hoe Adobe unieke bezoekers berekent.

## Lifetime-waarde

De waarde van het leven is een eigenschap die extra gespecialiseerde implementatie op beide platforms vereist. Adobe raadt u aan samen te werken met een implementatieconsultant om deze gegevens te verkrijgen.

## Cohortanalyse

De Analyse van de kabel toont hoe vaak de zelfde gebruikers aan uw plaats terugkeren.

Een cohortingtabel maken:

1. Klik op het pictogram Visualisatie aan de linkerkant en sleep de visualisatie Cohortingtabel naar de werkruimte.
2. Klik op het pictogram Componenten aan de linkerkant en sleep de metrische **bezoekers** naar de criteria voor insluiting en de criteria voor terugkeer.
3. Klik op Samenstellen.

Zie [Codeanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) in de gebruikersgids van de Werkruimte van de Analyse voor details op extra aanpassingen aan de cohortvisualisatie.

## Soorten publiek

In het rapport Soorten publiek in Google Analytics is het opzetten van een publiek vereist. Voor soorten publiek is ook configuratie in Adobe via Adobe Audience Manager vereist. Raadpleeg de gebruikershandleiding van Adobe Audience Manager voor meer informatie.

## Gebruikersverkenner

Het rapport van de Ontdekkingsreiziger van de Gebruiker staat een analist toe om individuele bezoeken door anonymized herkenningstekens te bekijken. Adobe maakt geen oppervlak van de achtergrondidentifiers buiten de gegevensfeeds, die onbewerkte gegevensexport op raakniveau zijn.

* Als deze gegevens in de Werkruimte van de Analyse worden gewenst, is het mogelijk om met een implementatieconsultant samen te werken om de geanonimiseerde waarde van het unieke identificatiekenmerk in een eVar door te geven. Merk op dat dit slechts met kleinere implementaties werkt die uit minder dan 1 miljoen unieke bezoekers per maand bestaan.
* Als deze gegevens binnen gegevensvoer worden gewenst, zijn de samengevoegde kolommen `visid_high` en `visid_low` zijn de gemeenschappelijkste manier om unieke bezoekers te identificeren. Meer informatie over [gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) vindt u in de gebruikershandleiding bij Exporteren.

## Demografische en belangenverslagen

Demografische gegevens en interesses bevatten informatie over leeftijd, geslacht en belangen van gebruikers van de site. Deze gegevens worden door Google verzameld op basis van hun mogelijkheden voor intersite tracering.

Demografische gegevens en interesses worden niet automatisch door Adobe verzameld. Als uw organisatie deze gegevens echter verkrijgt, kunt u gebruik maken van Customer Attributes, een functie in het Adobe Experience Cloud Platform. Het maakt volledige controle mogelijk over de organisatie van gegevens op basis van kenmerken, en is niet beperkt tot demografie of belangen.

Raadpleeg de Help voor klantkenmerken voor meer informatie.

## Geo - Taal

Het taalrapport van de geo toont plaatsverkeer door de taal die in browser van de bezoeker plaatst.

Een taalrapport maken:

1. Zoek in het menu Componenten de dimensie **Taal** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de dimensie van de [Taal](/help/components/c-variables/dimensionslist/reports-languages.md) in de de gebruikersgids van Componenten voor meer informatie.

## Geo - Locatie

Het geolocatierapport geeft een wereldwijde kaartweergave, waarbij gegevens per land worden uitgesplitst.

Een geografisch locatierapport maken:

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de visualisatie Kaart naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep de metrische waarde voor **Unieke bezoekers** naar de ruimte met het label Metrisch toevoegen.
3. Klik op Samenstellen.

Als de tabel naast de kaart ook wordt gezocht:

1. Zoek in het menu Componenten de dimensie **Landen** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie [Geosegmentatie](/help/components/c-variables/dimensionslist/reports-geosegmentation.md) dimensies in de de gebruikersgids van Componenten voor meer informatie.

## Gedrag - Nieuw vs Terugsturen

Het nieuwe versus het terugsturen rapport geeft een vereenvoudigde mening van eerste zittingen (nieuwe bezoeken) versus volgende zittingen (terugkeerbezoeken).

Een nieuw rapport of een rapport met terugkerende bezoeken maken:

1. Zoek in het menu Componenten het segment **Eerste bezoek** en sleep dit naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een afmeting neerzetten&#39;. Merk op dat de **Eerste Bebezoeken** een segment is, terwijl de Werkruimte typisch dimensies gebruikt om rijen te vertegenwoordigen.
2. Zoek het segment **Return Visits** en sleep dit boven op de rijkop Segmenten. Hierdoor wordt het segment toegevoegd als een dimensie onder First Time Visits (Eerste bezoeken), waardoor een eenvoudige vergelijking mogelijk is.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Als een lijngrafiek ook wordt gewenst:

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een lijnvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Gebruik Ctrl+klikken (Windows) of cmd+klikken (Mac) op elke rij in de vrije-vormtabel om deze te markeren. Hierdoor kunnen beide trends in de lijnvisualisatie worden weergegeven.
3. Klik op het kleine ronde punt linksboven in de lijnvisualisatie en klik vervolgens op het selectievakje Selectie vergrendelen.

## Gedrag - Frequentie en Recentie

Het frequentie- en recentierapport is ongeveer gelijk aan de dimensie **Bezoek nummer** in de analysewerkruimte.

1. Zoek in het optiemenu de dimensie **Visit Number** (Nummerbezoeken) en sleep deze naar het grote tabelgebied voor vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de dimensie [Bezoek Aantal](/help/components/c-variables/dimensionslist/reports-visitor-number.md) in de de gebruikersgids van Componenten voor meer informatie.

## Gedrag - Betrokkenheid

Het betrokkenheidsrapport is ongeveer gelijk aan de dimensie **Tijd besteed per bezoek - Afgekort** .

1. Zoek in het optiemenu de afmeting **Tijd besteed per bezoek - Afmetingen met** Emmering en sleep deze naar het grote tabelgebied met vrije vorm met de naam &#39;Afmeting hier neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de afmeting [Tijd per Bezoek](/help/components/c-variables/dimensionslist/reports-time-spent-per-visit.md) in de gebruikersgids van Componenten voor meer informatie.

## Technologie - Browser en besturingssysteem

Het rapport Browser en OS bevat meerdere primaire afmetingen.

* De primaire dimensie van **Browser** is ook beschikbaar in de Werkruimte van de Analyse als afmeting.
* De primaire dimensie van het **besturingssysteem** is ook als dimensie beschikbaar in de analysewerkruimte.
* De primaire dimensie van de **schermresolutie** is beschikbaar in de analysewerkruimte als de dimensie **monitorresolutie** .
* De primaire dimensie van de **Schermkleuren** is beschikbaar in de Werkruimte van de Analyse als dimensie van de Diepte van de **Kleur** .
* De primaire afmeting van de **Flash-versie** is niet beschikbaar in Adobe Analytics. Deze gegevens kunnen desgewenst echter door een eVar worden verzameld.

1. Zoek in het optiemenu de gewenste afmeting die hierboven is vermeld en sleep deze naar het grote tabelgebied in vrije vorm met het label &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de volgende pagina&#39;s in de gebruikershandleiding van Componenten voor meer informatie over hun respectievelijke dimensie:

* [Browser](/help/components/c-variables/dimensionslist/reports-browsers.md)
* [Besturingssysteem](/help/components/c-variables/dimensionslist/reports-operating-system.md)
* [Monitorresolutie](/help/components/c-variables/dimensionslist/reports-technology.md)
* [Kleurdiepte](/help/components/c-variables/dimensionslist/reports-color-depth.md)

## Technologie - Netwerk

Het netwerkrapport is ongeveer gelijk aan de dimensie van het **Domein** .

1. Zoek in het optiemenu de **Domeindimensie** en sleep deze naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de dimensie van het [Domein](/help/components/c-variables/dimensionslist/reports-domains.md) in de de gebruikersgids van Componenten voor meer informatie.

## Mobiel - Overzicht

Het rapport Mobiel overzicht is ongeveer gelijk aan de dimensie Type **** mobiel apparaat. Merk op dat de waarde &quot;Andere&quot;aan Desktopverkeer gelijkwaardig is.

1. Zoek in het optiemenu de afmetingen voor het type **mobiel apparaat** en sleep dit naar het grote tabelgebied voor vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de dimensie Type [](/help/components/c-variables/dimensionslist/reports-device-types.md) mobiel apparaat in de gebruikershandleiding van Componenten voor meer informatie.

## Mobiele apparaten

Het rapport over mobiele apparaten is ongeveer gelijk aan de dimensie **Mobiel apparaat** .

1. Zoek in het menu Componenten de dimensie **Mobiel apparaat** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de dimensie [Mobiel apparaat](/help/components/c-variables/dimensionslist/reports-devices.md) in de gebruikershandleiding van Componenten voor meer informatie.

## Aangepast

Aangepaste rapporten worden per implementatie gedefinieerd. Werk met de analysebeheerder van uw organisatie en/of de implementatieconsultant om deze rapporten te interpreteren. Typisch handhaaft een organisatie een Document [van het Ontwerp van de](/help/implement/prepare/solution-design.md) Oplossing om spoor van douaneveranderlijke waarden te houden en hoe zij bevolkt zijn.

## Benchmarking

Met benchmarkingsrapporten kunt u zien hoe facetten van uw gegevens worden vergeleken met industriële gemiddelden. Adobe deelt momenteel geen benchmarkingsgegevens tussen zijn klanten.

## Gebruikersstroom

Het stroomrapport is beschikbaar op beide platforms. Een flowrapport maken:

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Zoek de afmetingen voor **pagina** &#39;s en klik op het pictogram Pijl om de paginawaarden weer te geven. Dimensiewaarden zijn geel.
3. Zoek de gewenste paginawaarde waarmee u wilt beginnen en sleep deze naar de ruimte met het label Dimensie of item in het midden
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.
