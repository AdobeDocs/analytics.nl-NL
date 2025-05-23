---
description: Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.
title: Welk Adobe Analytics-gereedschap moet ik gebruiken?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 3%

---

# Welk Adobe Analytics-gereedschap moet ik gebruiken?

Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.

Voor meer op de Vergelijking van het Product van Adobe Analytics, zie [ de productvergelijking van Analytics ](/help/analyze/get-started/analytics-product-comparison.md).


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Vergelijking van hulpmiddelen ](https://video.tv.adobe.com/v/27220?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Adobe Analytics die gebruikersinterfaces rapporteert {#user-interfaces}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)** zou het gaan-aan gebruikersinterface voor elk van uw rapportering en analysebehoeften moeten zijn. Adobe blijft investeren in dit product en geeft maandelijks updates voor dit product uit. Als er een taak is die u niet kunt uitvoeren in Analysis Workspace, kunt u de andere interfaces hieronder overwegen.**

**[Adobe Analytics dashboards](/help/analyze/mobile-app/home.md)** staat gebruikers mobiele toegang tot intuïtieve scorecards toe. Scorecards zijn een inzameling van zeer belangrijke metriek en andere componenten die in een tegellay-out worden voorgesteld die u voor meer gedetailleerde onderverdelingen en trended rapporten kunt tikken. De mobiele app wordt ondersteund op zowel iOS- als Android-besturingssystemen.

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** is toe:voegen-binnen voor Microsoft Excel die op Mac, Vensters, en Webbrowsers loopt. Hiermee kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens, die u kunt invoegen in uw Excel-werkbladen. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft.

**[Verouderde Report Builder](/help/analyze/legacy-report-builder/home.md)** is toe:voegen-binnen voor Microsoft Excel die op Vensters slechts loopt. Hiermee kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens, die u kunt invoegen in uw Excel-werkbladen. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft.

**[Activity Map](/help/analyze/activity-map/overview.md)** is een eigenschap binnen Adobe Analytics die een visuele vertegenwoordiging van gebruikersbetrokkenheid op Web-pagina&#39;s en mobiele apps verstrekt. Hiermee kunnen marketers en analisten gebruikersinteracties zoals klikken, aanwijzen en schuiven volgen en analyseren.

## Gegevens importeren in Adobe Analytics {#import}

**[classificaties](/help/components/classifications/classifications-overview.md)** zouden moeten worden gebruikt:

* Als er metagegevens zijn die u aan een verzamelwaarde wilt koppelen (eVar, prop, marketingkanaal). Adobe adviseert het gebruiken van [ reeksen van de Classificatie ](/help/components/classifications/sets/overview.md). De constructor van classificatieregels en de importer van classificatieregels zijn oude methoden om classificatiegegevens naar Adobe Analytics te brengen.

**[Gegevensbronnen](/help/import/data-sources/overview.md)** zouden moeten worden gebruikt:

* Als er offlinegegevens zijn die u permanent in Adobe Analytics wilt schrijven
* Opties:
   * Samenvatting: eenvoudige gegevens worden geüpload, op dag of in beperkte afmetingen
   * Transactie-id: gegevens worden geüpload die een online eindpunt verbinden met offline gegevens en geïmporteerde gegevens volledig koppelen aan een online vastgelegde bezoekersmomentopname (bestellingen worden bijvoorbeeld online voltooid en offline geretourneerd)

**[de integraties van Adobe Exchange ](https://www.adobeexchange.com/experiencecloud.html)** zouden moeten worden gebruikt:

* Wanneer u verbinding maakt met een externe provider die een ondersteunde verbinding met Adobe Analytics heeft gemaakt. Integratie-apps bevatten doorgaans permanent en automatisch samenvattingsgegevens in Adobe Analytics, op terugkerende basis.

**[Bulk de Invoeging API van Gegevens ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* De API voor het invoegen van gegevens in bulk accepteert CSV-bestanden met gebeurtenisgegevens, één gebeurtenis per rij. Adobe raadt u aan de API voor bulkinvoeging te gebruiken voor elke implementatie waarvoor code op de server nodig is of die AppMeasurement of Web SDK anders niet kan gebruiken voor gegevensverzameling.

**[de Invoeging API van Gegevens (Verouderd)](/help/import/c-data-insertion-api/c-data-insertion-api.md)** zou moeten worden gebruikt:

* Wanneer u gegevens naar Adobe Analytics moet brengen en geen AppMeasurement, Web SDK, of de Bulk API van de Invoeging van Gegevens kunt gebruiken.

**[de attributen van de Klant ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=nl-NL)** zouden moeten worden gebruikt:

* Als u gegevens van ondernemingsklanten in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangt en de gegevens aan Experience Cloud wilt uploaden.
* Als u de gegevens van CRM voor diepere analyse in Analytics wilt gebruiken, of als het richten van criteria in Adobe Target.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** zou moeten worden gebruikt:

* Als u gegevens over het Adobe Audience Manager-publiek, zoals demografische informatie (bv. geslacht of inkomensniveau), psychografische informatie (bv. interesses en hobby&#39;s), CRM-gegevens of impliciete gegevens in een analyseworkflow wilt opnemen.
* Als u de geüploade CRM-gegevens op tijd wilt baseren, omdat deze integratie nieuwe informatie stuurt naar Analytics die door een hit zijn getroffen.

## Gegevens exporteren uit Adobe Analytics {#export}

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** zou moeten worden gebruikt:

* Als de aangepaste lay-outopties van Workspace worden beperkt (alles is mogelijk in Report Builder, binnen de grenzen van Excel).
* Om in gebruikersinput of off-line gegevensbronnen (beelden, kosten) los te koppelen aan de gegevens van Adobe. De duurdere oplossing voor het verbinden in gegevens is Gegevensbronnen (zie het Importeren van Gegevens aan Analytics).
* Gegevens uit verschillende dimensionale rapporten samenvoegen (bv. rapport over promo-impressions wordt gekoppeld aan rapport over promo-click-to-conversion).
* Om gegevens van verschillende rapportreeksen samen te voegen, of door samen te vatten of in de zelfde lijst zij aan zij te tonen.
* Als automatisering door het plannen wordt gewenst (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)** zou moeten worden gebruikt:

* Om tot variabelen toegang te hebben die anders in UI - IP adres, identiteitskaart van Experience Cloud, identiteitskaart van de Bezoeker van Analytics, Pagina URL) worden verborgen
* Om tot meer korrelige gegevens dan UI (gedenormaliseerde lijstmening) toegang te hebben
* Gegevens downloaden in een indeling die geschikt is voor draaitabelinvoer
* Als de client Adobe-gegevens wil invoeren in een hulpprogramma voor gegevensvisualisatie van derden (enigszins samengevat en niet op raakniveau)
* Om tot alle unieke afmetingspunten toegang te hebben als u in &quot;Laag Verkeer&quot;in Adobe Analytics loopt

**[Diervoer van de Gegevens van Analytics](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)** zou moeten worden gebruikt:

* Als u de meest gedetailleerde gegevensinvoer wilt gebruiken die we kunnen opgeven (bezoeker-id, hit).
* Als de client Adobe-gegevens wil opslaan in een client-side database, kunnen we deze gegevens op het meest granulaire niveau verzenden.
* Als de client een Business Intelligence (BI)-tool wil ontwikkelen of Adobe-gegevens op aanraakniveau wil invoeren in een hulpprogramma van derden.

**[Meldend APIs ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** zou moeten worden gebruikt wanneer de andere visualisatieopties niet aan uw behoeften voldoen. De drie API-opties zijn:

* **volledig Verwerkt**: wanneer u eigenschap-rijke gegevens (met inbegrip van bezoeken, bezoekers, en segmenten) wilt. Dit zijn standaard samengevatte gegevens uit de analysefunctie, beschikbaar binnen ~30-90 minuten. Kan via Report Builder worden gebruikt.
* **Echt - tijd**: wanneer u een paar metriek en dimensies met seconden van latentie wilt bekijken. Dit zijn beperkte, gedeeltelijk verwerkte, samengevatte gegevens die binnen ~30 seconden beschikbaar zijn. Omvat unieke algoritmen van populairste, grainers, en verliezers. Kan via Report Builder worden gebruikt.
* **[!UICONTROL Live Stream]**: wanneer u binnen seconden na de verzameling een stream wilt van gedeeltelijk verwerkte analysegegevens op raakniveau. Dit zijn gedeeltelijk verwerkte gegevens, beschikbaar binnen ~30 seconden. Alleen beschikbaar voor Analytics Premium. Vereist één of andere manier om de gegevens te visualiseren, typisch door een overeenkomst van de Diensten van de Techniek.

## Aangepaste oplossingen {#custom-solutions}

De Diensten van de techniek zouden moeten worden gebruikt wanneer:

* De andere Adobe-tools voldoen niet aan uw behoeften.
* U wilt een aangepaste ervaring.
* U wilt een volledig geautomatiseerde oplossing.
* U wilt vele apparaten bereiken.
* U hebt meerdere gegevensbronnen.
* U hebt complexe ETL-vereisten (Extract-Transform-Load) voor gegevens.
* U wilt aangepaste branding.
* U wilt [!UICONTROL Analytics Live Stream] visualiseren.
