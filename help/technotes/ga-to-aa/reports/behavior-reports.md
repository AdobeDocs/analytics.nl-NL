---
title: Gedragrapporten in Adobe Analytics
description: Leer hoe u gedragsrapporten maakt in Adobe Analytics
feature: Third-party Integration
exl-id: ea441afa-e595-4ffa-b446-d67e87f8a7c9
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 0%

---

# Gedragsrapporten

Gedragrapporten bevatten informatie over de manier waarop gebruikers met uw site werken.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics](create-report.md) als u het gereedschap nog niet kent in Adobe Analytics.

## Gedragingen

Het rapport van de gedragsstroom kan worden ontspannen gebruikend de visualisatie van de Stroom.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Zoek de **Pagina** en klikt u op het pictogram Pijl om de paginawaarden weer te geven. Dimension-items zijn gekleurd geel.
3. Zoek de gewenste paginawaarde waarmee moet worden begonnen en sleep deze naar de ruimte met het label &#39;Dimension of item&#39; in het midden
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

![Stroomrapport](/help/technotes/ga-to-aa/assets/flow.png)

## Site-inhoud - alle pagina&#39;s

Het paginapport geeft de prestaties van afzonderlijke pagina&#39;s op uw site weer.

1. Zoek in het menu Componenten de locatie **Pagina&#39;s** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Als alternatief biedt Adobe verschillende vooraf gemaakte werkruimten, sjablonen genoemd. Het malplaatje van het Verbruik van de Inhoud (Web) verstrekt gelijkaardige waarde aan het alle paginapport.

1. Klikken *[!UICONTROL Project]>[!UICONTROL New]*, waarmee een modaal venster met projectopties wordt geopend.
2. Klik op de sjabloon Inhoudsverbruik (Web) en klik vervolgens op Maken.

## Site-inhoud - Inhoudskeuzelijst

Met het rapport voor de inhoudstraining kunt u naar het paginaverkeer kijken op basis van de URL-structuur. Aanvullende implementatie is vereist voor gebruik in Analysis Workspace. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct worden verzameld.

## Site-inhoud - bestemmingspagina&#39;s

Het rapport met bestemmingspagina&#39;s geeft de bovenste bestemmingspagina&#39;s op uw site weer. Openingspagina&#39;s zijn in Analysis Workspace beschikbaar als de **Itempagina** dimensie.

1. Zoek in het menu Componenten de locatie **Itempagina** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de **Bezoeken** metrisch voor deze afmeting.

## Site-inhoud - Pagina&#39;s afsluiten

In het rapport Afsluitpagina&#39;s worden de bovenste pagina&#39;s weergegeven die de laatste pagina van het bezoek van een individu werden. Het is beschikbaar in Analysis Workspace onder dezelfde naam.

1. Zoek in het menu Componenten de locatie **Pagina afsluiten** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de **Bezoeken** metrisch voor deze afmeting.

## Sitesnelheidsrapporten

Sitesnelheidsrapporten laten zien hoe snel pagina&#39;s worden geladen, zodat u de kans krijgt om de laadtijden van de pagina te verlengen.

Voor deze functie is aanvullende implementatie op beide platforms vereist. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor Analysis Workspace. De [getPageLoadTime plug-in](/help/implement/vars/plugins/getpageloadtime.md) wordt typisch toegewezen aan een eVar om prestatiesgegevens in Adobe Analytics te verkrijgen.

## Sitezoekrapporten

De het onderzoeksrapporten van de plaats verstrekken inzicht in hoe de bezoekers de interne onderzoeksmogelijkheden van uw plaats gebruiken.

Voor deze functie is aanvullende implementatie op beide platforms vereist. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor Analysis Workspace. Doorgaans wordt een interne zoekterm opgehaald uit een querytekenreeksparameter en in een eVar geplaatst voor rapportage.

## Gebeurtenisrapporten

De gebeurtenissen hebben een aantal grote structurele verschillen tussen Google en Adobe Analytics. Beide vereisen aanvullende implementatiewijzigingen om naar behoren op hun respectieve platform te kunnen werken.

* In Google Analytics worden gebeurtenissen in uw implementatie gedefinieerd als tekst. Gebeurtenissen hebben categorieën, handelingen en labels.
* In Adobe Analytics worden gebeurtenissen eerst ingesteld in de Admin Console waaraan een id is toegewezen. Deze id wordt gebruikt in de implementatiecode. Bijvoorbeeld:
   1. U kunt event1 in de Admin Console instellen als &#39;Registrations&#39;.
   2. In uw implementatie, zou u event1 in de gebeurtenisvariabele op de pagina van de registratiebevestiging omvatten. Telkens wanneer de pagina van de registratiebevestiging wordt getoond, neemt event1 toe.
   3. In Analysis Workspace wordt &#39;Registrations&#39; weergegeven als een maatstaf voor gebruik in rapporten.

Omdat deze functie implementatiewijzigingen vereist, raadt Adobe aan met een implementatieconsultant te werken om ervoor te zorgen dat gegevens correct zijn geconfigureerd voor Analysis Workspace.

## Uitgever-rapporten

Net zoals Google een verbinding met Google Ad Manager nodig heeft, biedt Adobe een speciaal product voor inzicht met de naam Adobe Advertising Cloud. Neem contact op met de accountmanager van uw organisatie als uw organisatie dit product wil gebruiken.
