---
title: Real-time rapporten in Adobe Analytics
description: Leer hoe u real-time rapporten kunt genereren in Adobe Analytics, gericht op gebruikers die meer vertrouwd zijn met Google Analytics.
translation-type: tm+mt
source-git-commit: 3ce18f3f222286aed08c81dd2c958dab7e443df3

---


# Real-time rapporten

Real-time rapporten laten zien wat er momenteel op uw site gebeurt. Deze typen rapporten zijn vooral handig als u direct resultaten wilt zien van updates die u op uw site uitvoert. Bijvoorbeeld, kan een bedrijf dat een verkoop op Zwarte Vrijdag in werking stelt verkeer aan specifieke pagina&#39;s meten en bepalen welke verkoop om voorrang te geven op prestaties op dat ogenblik.

![Rapport in realtime](/help/technotes/ga-to-aa/assets/realtime.png)

Real-time rapporten zijn één van de weinige eigenschappen die nog niet aan de Werkruimte van de Analyse zijn geïntroduceerd. Gebruik Rapporten en Analyses om deze gegevens te verkrijgen. Zij vereisen één of andere eenvoudige configuratie beginnen gegevens te verzamelen.

Om de pagina van de rapportconfiguratie in real time (vereiste toestemmingen Admin) te bereiken:

1. Klik op [!UICONTROL Reports] de koptekstnavigatie Adobe Analytics.
2. Klik in het linkermenu op *[!UICONTROL Site Metrics]* > *[!UICONTROL Real-Time]*.
3. Als de rapportreeks nog niet toegelaten real time heeft, wordt een bericht getoond met een verbinding om de rapportreeks te vormen. Als de rapportreeks in real time toegelaten heeft, klik [!UICONTROL Configure] dichtbij de titel van het rapport in real time.

Met Adobe kunnen maximaal drie realtime rapporten tegelijkertijd gegevens verzamelen. Elk moet worden gevormd alvorens zij beginnen gegevens in real time te verzamelen.

![Real-time rapportconfiguratie](/help/technotes/ga-to-aa/assets/realtime_config.png)

## Locaties in realtime

In real time plaatsen vertelt u waar de bezoekers verblijven terwijl het bezoeken van uw plaats op het huidige ogenblik. Om één van uw drie rapporten in real time te vormen om plaatsgegevens te tonen:

1. Klik [!UICONTROL Configure] dichtbij de titel van het rapport in real time.
2. Onder één van de rapportgroeven in real time:
   * Geef uw real-time rapport een naam; bijvoorbeeld &quot;Locations&quot;.
   * Instanties worden doorgaans gebruikt als de metrische waarde. Gebruikers/unieke bezoekers zijn momenteel niet beschikbaar in realtime-rapporten.
   * Voor de primaire dimensie wordt doorgaans GeoSegmentation-land gebruikt. GeoSegmentation Region, GeoSegmentation US DMA, en GeoSegmentation City zijn ook beschikbaar.
   * Voor de twee secundaire dimensies, gebruik de aangewezen extra gegevens die u voor dit verkeer wilt zien. Secundaire afmetingen hoeven niet specifiek te zijn voor de locatie.
3. Klik op [!UICONTROL Save and View Report].

## Real-time verkeersbronnen

In real time verkeersbronnen vertellen u waar de bezoekers van kwamen terwijl het bezoeken van uw plaats op het huidige ogenblik. Om één van uw drie rapporten in real time te vormen om verkeersbrongegevens te tonen:

1. Klik &quot;vormen&quot;dichtbij de titel van het rapport in real time.
2. Onder één van de rapportgroeven in real time:
   * Geef uw real-time rapport een naam; bijvoorbeeld &quot;Verkeersbronnen&quot;.
   * Instanties worden doorgaans gebruikt als de metrische waarde. Gebruikers/unieke bezoekers zijn momenteel niet beschikbaar in realtime-rapporten.
   * Voor Primaire afmeting wordt het verwijzende domein typisch gebruikt. Zoekengine en Trefwoord zoeken zijn ook beschikbaar.
   * Voor de twee secundaire dimensies, gebruik de aangewezen extra gegevens die u voor dit verkeer wilt zien. Secundaire afmetingen hoeven niet specifiek te zijn voor verkeersbronnen.
3. Klik op [!UICONTROL Save and View Report].

## Inhoud in realtime

In real time inhoud vertelt u welke pagina&#39;s uw bezoekers momenteel bekijken. Om één van uw drie rapporten in real time te vormen om inhoudsgegevens te tonen:

1. Klik [!UICONTROL Configure] dichtbij de titel van het rapport in real time.
2. Onder één van de rapportgroeven in real time:
   * Geef uw real-time rapport een naam; bijvoorbeeld &quot;Inhoud&quot;.
   * Instanties worden doorgaans gebruikt als de metrische waarde. Gebruikers/unieke bezoekers zijn momenteel niet beschikbaar in realtime-rapporten.
   * Voor de primaire afmeting wordt de pagina doorgaans gebruikt. De Sectie van de plaats en de Server zijn ook beschikbaar als uw implementatie deze variabelen bepaalt.
   * Voor de twee secundaire dimensies, gebruik de aangewezen extra gegevens die u voor dit verkeer wilt zien. Secundaire afmetingen hoeven niet specifiek te zijn voor de inhoud.
3. Klik op [!UICONTROL Save and View Report].

## Gebeurtenissen in realtime

Gebeurtenissen in real time vertellen u welke gebeurtenissen het meest op uw plaats gebeuren. In Google Analytics legt een gebeurtenis vast hoe vaak een specifieke actie (meestal een actie die geen verband houdt met een paginaweergave) is uitgevoerd. GA-gebeurtenissen worden verzonden met een categorie, label en handeling. In Adobe Analytics zijn aangepaste gebeurtenissen metriek met vriendelijke namen in de beheerconsole die naast elke gewenste dimensie kan worden geanalyseerd. Als u op zoek bent naar een dimensie in Adobe Analytics die vergelijkbaar is met Google Analytics-gebeurtenissen, kunt u de dimensie Aangepaste koppeling toepassen. Deze wordt vaak gebruikt als een &#39;catch-all&#39; voor het verzamelen van gegevens die geen verband houden met paginaweergaven (naast Koppelingen afsluiten - voor Afsluiten - en Koppelingen downloaden - voor Downloads).

> [!NOTE] Wanneer het gebruiken van douanegebeurtenissen in rapporten in real time, moet de afmetingswaarde in de zelfde klap worden bepaald zoals de douanegebeurtenis. Als u bijvoorbeeld een aangepaste gebeurtenis &#39;Registrations&#39; weergeeft voor de dimensie &#39;Referring Domain&#39;, worden er geen gegevens geretourneerd zonder aanvullende implementatie. Aangezien het verwijzende domein slechts op de eerste slag verschijnt, en een douanegebeurtenis typisch later in het bezoek zou verschijnen, kunnen de gegevens niet in rapporten in real time worden geassocieerd. Deze gegevens zijn beschikbaar met Analyse-werkruimte met standaardverwerkingslatentie (doorgaans 30-90 minuten).

## Conversies in realtime

In real time omzettingen presenteren gegevens verschillend tussen platforms. De doelen in Google Analytics zijn te vergelijken met metriek- en succesgebeurtenissen in Adobe Analytics. U kunt de meeste metriek in de Analytics van Adobe (zowel douanemetriek zoals succesgebeurtenissen als standaardmetriek zoals opbrengst) in Echte - tijd Rapporten gebruiken. Net als bij Google Analytics kunt u ook dimensies zoals productnaam, trackingcode en campagneprestaties toepassen in real-time rapporten.

1. Klik [!UICONTROL Configure] dichtbij de titel van het rapport in real time.
2. Onder één van de rapportgroeven in real time:
   * Geef uw real-time rapport een naam; bijvoorbeeld Conversies.
   * Instanties worden doorgaans gebruikt als de metrische waarde. Gebruikers/unieke bezoekers zijn momenteel niet beschikbaar in realtime-rapporten.
   * Voor de primaire dimensie wordt doorgaans trackingcode gebruikt. De dimensie Producten is ook beschikbaar als uw implementatie het gebruikt.
   * Voor de twee secundaire dimensies, gebruik de aangewezen extra gegevens die u voor dit verkeer wilt zien. Secundaire afmetingen hoeven niet specifiek te zijn voor conversies.
3. Klik op [!UICONTROL Save and View Report].

> [!NOTE] Als het gebruiken van gebeurtenissen buiten Instanties, zoals Orders, zorg ervoor dat uw implementatie de dimensie en de gebeurtenis op de zelfde klap bepaalt. Als de afmetingen en de gebeurtenissen niet op de zelfde klap in brand steken, zijn die gegevens beschikbaar in de Werkruimte van de Analyse gebruikend standaardverwerkingslatentie, die typisch 30-90 minuten is.
