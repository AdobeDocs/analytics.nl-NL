---
title: Gedragrapporten in Adobe Analytics
description: Leer hoe u gedragsrapporten maakt in Adobe Analytics
translation-type: tm+mt
source-git-commit: e1cbdf87140b915dccbb8f64694797bb903d8ab8

---


# Gedragsrapporten

Gedragrapporten bevatten informatie over de manier waarop gebruikers met uw site werken.

Deze pagina veronderstelt de gebruiker een basiskennis van het gebruiken van de Werkruimte van de Analyse heeft. Zie Een basisrapport [maken in de Analyse Workspace voor Google Analytics-gebruikers](create-report.md) als u nog niet bekend bent met het hulpprogramma in Adobe Analytics.

## Gedragingen

Het rapport van de gedragsstroom kan worden ontspannen gebruikend de visualisatie van de Stroom.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Bepaal de plaats van de afmeting van de **Pagina** , dan klik het pictogram van de Pijl om paginawaarden te openbaren. Dimensiewaarden zijn geel.
3. Zoek de gewenste paginawaarde waarmee u wilt beginnen en sleep deze naar de ruimte met het label Dimensie of item in het midden
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

![Stroomrapport](/help/technotes/ga-to-aa/assets/flow.png)

## Site-inhoud - alle pagina&#39;s

Het paginapport geeft de prestaties van afzonderlijke pagina&#39;s op uw site weer.

1. Zoek in het menu Componenten de afmetingen **Pagina** &#39;s en sleep deze naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Als alternatief biedt Adobe diverse vooraf gemaakte werkruimten, sjablonen genoemd. Het malplaatje van het Verbruik van de Inhoud (Web) verstrekt gelijkaardige waarde aan het alle paginapport.

1. Klik op *[!UICONTROL Project]>[!UICONTROL New]*. Hiermee wordt een modaal venster met projectopties geopend.
2. Klik op de sjabloon Inhoudsverbruik (Web) en klik vervolgens op Maken.

## Site-inhoud - Inhoudskeuzelijst

Met het rapport voor de inhoudstramienpagina kunt u naar het paginaverkeer kijken op basis van de URL-structuur. Aanvullende implementatie is vereist voor gebruik in de analysewerkruimte. Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct worden verzameld.

## Site-inhoud - bestemmingspagina&#39;s

Het rapport met bestemmingspagina&#39;s geeft de bovenste bestemmingspagina&#39;s op uw site weer. Landingspagina&#39;s zijn beschikbaar in de Analyse-werkruimte als de **dimensie Pagina** in item.

1. Zoek in het menu Componenten de afmetingen voor de **invoerpagina** en sleep deze naar het grote tabelgebied voor vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de **Visits** -meting voor deze dimensie te gebruiken.

## Site-inhoud - Pagina&#39;s afsluiten

In het rapport Afsluitpagina&#39;s worden de bovenste pagina&#39;s weergegeven die de laatste pagina van het bezoek van een individu werden. Het is beschikbaar in de Werkruimte van de Analyse onder de zelfde naam.

1. Zoek in het menu Componenten de afmetingen Pagina **** afsluiten en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de **Visits** -meting voor deze dimensie te gebruiken.

## Sitesnelheidsrapporten

Sitesnelheidsrapporten laten zien hoe snel pagina&#39;s worden geladen, zodat u de kans krijgt om de laadtijden van de pagina te verlengen.

Voor deze functie is aanvullende implementatie op beide platforms vereist. Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor de analysewerkruimte. De [insteekmodule](/help/implement/vars/plugins/getpageloadtime.md) getPageLoadTime wordt doorgaans aan een eVar toegewezen voor het verkrijgen van prestatiegegevens in Adobe Analytics.

## Sitezoekrapporten

De het onderzoeksrapporten van de plaats verstrekken inzicht in hoe de bezoekers de interne onderzoeksmogelijkheden van uw plaats gebruiken.

Voor deze functie is aanvullende implementatie op beide platforms vereist. Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor de analysewerkruimte. Doorgaans wordt een interne zoekterm uit een parameter van een querytekenreeks opgehaald en in een eVar geplaatst voor rapportage.

## Gebeurtenisrapporten

Er zijn enkele grote structurele verschillen tussen Google en Adobe Analytics. Beide vereisen aanvullende implementatiewijzigingen om naar behoren op hun respectieve platform te kunnen werken.

* In Google Analytics worden gebeurtenissen in uw implementatie gedefinieerd als tekst. Gebeurtenissen hebben categorieën, handelingen en labels.
* In Adobe Analytics worden gebeurtenissen eerst ingesteld in de beheerconsole waaraan een id is toegewezen. Deze id wordt gebruikt in de implementatiecode. Bijvoorbeeld:
   1. U kunt event1 in de beheerconsole instellen als &#39;Registrations&#39;.
   2. In uw implementatie, zou u event1 in de gebeurtenisvariabele op de pagina van de registratiebevestiging omvatten. Telkens wanneer de pagina van de registratiebevestiging wordt getoond, neemt event1 toe.
   3. In de Werkruimte van de Analyse, &quot;Registraties&quot;verschijnt als metrisch voor gebruik in om het even welk rapport.

Omdat voor deze functie implementatiewijzigingen zijn vereist, raadt Adobe aan met een implementatieconsultant te werken om ervoor te zorgen dat gegevens correct zijn geconfigureerd voor de analysewerkruimte.

## Uitgever-rapporten

Net als voor Google is een verbinding met Google Ad Manager vereist, biedt Adobe een speciaal product voor inzicht met de naam Adobe Advertising Cloud. Neem contact op met de accountmanager van uw organisatie als uw organisatie dit product wil gebruiken.
