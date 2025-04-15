---
description: Deze Help-pagina bevat aanbevolen gebruiksscenario's voor elke Adobe Analytics-tool. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.
title: Welk Adobe Analytics-gereedschap moet ik gebruiken?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
source-git-commit: 9a2d4c582b6a3946b658924851e5b5ada2f5a7ee
workflow-type: tm+mt
source-wordcount: '1214'
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

**[Adobe Analytics dashboards](/help/analyze/mobile-app/home.md)** staat gebruikers mobiele toegang tot intuïtieve scorecards toe. Scorekaarten zijn een verzameling belangrijke statistieken en andere componenten die worden gepresenteerd in een tegelindeling waarop u kunt tikken voor meer gedetailleerde uitsplitsingen en trendrapporten. De mobiele app wordt ondersteund op zowel iOS- als Android-besturingssystemen.

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** is toe:voegen-binnen voor Microsoft Excel die op Mac, Vensters, en Webbrowsers loopt. Hiermee kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens, die u kunt invoegen in uw Excel-werkbladen. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft.

**[Verouderde Report Builder](/help/analyze/legacy-report-builder/home.md)** is toe:voegen-binnen voor Microsoft Excel die op Vensters slechts loopt. Hiermee kunt u aangepaste aanvragen maken van Adobe Analytics-gegevens, die u kunt invoegen in uw Excel-werkbladen. De aanvragen kunnen dynamisch verwijzen maar cellen binnen uw werkblad, en u kunt bijwerken en aanpassen hoe Report Builder de data weergeeft.

**[Activity Map](/help/analyze/activity-map/overview.md)** is een functie binnen Adobe Analytics die een visuele weergave biedt van de betrokkenheid van gebruikers op webpagina&#39;s en mobiele apps. Hiermee kunnen marketers en analisten gebruikersinteracties zoals klikken, aanwijzen en schuiven volgen en analyseren.

## Gegevens importeren in Adobe Analytics {#import}

**[Classificaties](/help/components/classifications/c-classifications.md)** moeten worden gebruikt:

* Wanneer er metadata zijn die u wilt koppelen aan een verzamelwaarde (eVar, prop, marketingkanaal)
* Opties:

   * De bouwer van de regel: gebruik wanneer u voorspelbare formatted-values hebt die voor een variabele, b.v. afgebakende waarden worden verzameld. Op deze manier kunt u regels voor een keer instellen, grotendeels &quot;instellen en vergeten&quot;.
   * Browser het invoeren: gebruik wanneer u geen voorspelbare waarden hebt, of wanneer u een eindige lijst van waarden hebt die een eenmalig update vereist. Deze aanpak vereist dat u de classificaties voortdurend controleert op nieuwe waarden.

**[Gegevensbronnen](/help/import/data-sources/overview.md)** zouden moeten worden gebruikt:

* Als er offlinegegevens zijn die u permanent in Adobe Analytics wilt schrijven
* Opties:

   * Samenvatting: eenvoudige gegevens worden geüpload, op dag of in beperkte afmetingen
   * Transactie-id: gegevens worden geüpload die een online eindpunt verbinden met offline gegevens en geïmporteerde gegevens volledig koppelen aan een online vastgelegde bezoekersmomentopname (bestellingen worden bijvoorbeeld online voltooid en offline geretourneerd)
   * Volledige verwerking: gegevensbronnen met tijdstempels, verwerkt alsof deze zijn verzameld door Adobe-servers. Dat wil zeggen dat gegevens rechtstreeks in de bezoekersreis worden ingevoerd.

**[de integraties van Adobe Exchange ](https://www.adobeexchange.com/experiencecloud.html)** zouden moeten worden gebruikt:

* Wanneer u verbinding maakt met een externe provider die een ondersteunde verbinding met Adobe Analytics heeft gemaakt. Integratie-apps nemen doorgaans permanent en automatisch gegevens op samenvattingsniveau op in Adobe Analytics, op terugkerende basis.

**[de Invoeging API van Gegevens](/help/import/c-data-insertion-api/c-data-insertion-api.md)** zou moeten worden gebruikt:

* Wanneer u gegevens naar Adobe Analytics moet uploaden en u kunt de Adobe AppMeasurement- of SDK-code niet gebruiken. We raden u aan de API voor het invoegen van gegevens in bulk te gebruiken (zie hieronder).

**[Bulk de Invoeging API van Gegevens ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* API voor gegevensinvoeging en API voor bulkgegevensinvoeging zijn beide methoden om verzamelingsgegevens op de server naar Adobe Analytics te verzenden. API-aanroepen voor het invoegen van gegevens worden één gebeurtenis tegelijk uitgevoerd. De API voor het invoegen van bulkgegevens accepteert CSV-bestanden die gebeurtenisgegevens bevatten, één gebeurtenis per rij. Als u aan een nieuwe implementatie van server-zijinzameling werkt, adviseren wij gebruikend de Invoeging API van de Gegevens van het Bulk.

**[Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html)** moeten worden gebruikt:

* Als u klantgegevens van ondernemingen vastlegt in een CRM-database (Customer Relationship Management) en de gegevens wilt uploaden naar de Experience Cloud.
* Als u CRM-gegevens wilt gebruiken voor diepere analyse in Analytics of als targetingcriteria in Adobe Target.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** moet worden gebruikt:

* Als u gegevens over het Adobe Audience Manager-publiek, zoals demografische informatie (bv. geslacht of inkomensniveau), psychografische informatie (bv. interesses en hobby&#39;s), CRM-gegevens of impliciete gegevens in een analyseworkflow wilt opnemen.
* Als u de geüploade CRM-gegevens op tijd wilt baseren, omdat deze integratie nieuwe informatie stuurt naar Analytics die door een hit zijn getroffen.

## Gegevens exporteren uit Adobe Analytics {#export}

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** zou moeten worden gebruikt:

* Als de aangepaste lay-outopties van Workspace worden beperkt (alles is mogelijk in Report Builder, binnen de grenzen van Excel).
* Om in gebruikersinput of off-line gegevensbronnen (beelden, kosten) los te koppelen aan de gegevens van Adobe. Een meer permanente oplossing voor het koppelen van gegevens is Gegevensbronnen (zie Gegevens importeren in Analytics).
* Gegevens uit verschillende dimensionale rapporten samenvoegen (bv. rapport over promo-impressions wordt gekoppeld aan rapport over promo-click-to-conversion).
* Om gegevens van verschillende rapportreeksen samen te voegen, of door samen te vatten of in de zelfde lijst zij aan zij te tonen.
* Als automatisering door het plannen wordt gewenst (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)** zou moeten worden gebruikt:

* Om tot variabelen toegang te hebben die anders in UI - IP adres, identiteitskaart van Experience Cloud, identiteitskaart van de Bezoeker van Analytics, Pagina URL) worden verborgen
* Om tot meer korrelige gegevens dan UI (gedenormaliseerde lijstmening) toegang te hebben
* Gegevens downloaden in een indeling die geschikt is voor een draaitabelinvoer
* Als de klant Adobe-gegevens wil invoeren in een 3rd-party tool voor gegevensvisualisatie (enigszins samengevat en niet op trefferniveau)
* Toegang krijgen tot alle unieke dimensie-items als u &quot;Weinig verkeer&quot; tegenkomt in Adobe Analytics

**[De Analytics-gegevensfeed](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)** moet worden gebruikt:

* Als u de meest gedetailleerde gegevensinvoer wilt gebruiken die we kunnen opgeven (bezoeker-id, hit).
* Als de client Adobe-gegevens wil opslaan in een client-side database, kunnen we deze gegevens op het meest granulaire niveau verzenden.
* Als de client een Business Intelligence (BI)-tool wil ontwikkelen of Adobe-gegevens op aanraakniveau wil invoeren in een hulpprogramma van derden.

**[Meldend APIs ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** zou moeten worden gebruikt wanneer de andere visualisatieopties niet aan uw behoeften voldoen. De drie API-opties zijn:

* **volledig Verwerkt**: wanneer u eigenschap-rijke gegevens (met inbegrip van bezoeken, bezoekers, en segmenten) wilt. Dit zijn standaard samengevatte gegevens uit de analysefunctie, beschikbaar binnen ~30-90 minuten. Kan via Report Builder worden gebruikt.
* **Echt - tijd**: wanneer u een paar metriek en dimensies met seconden van latentie wilt bekijken. Dit zijn beperkte, gedeeltelijk verwerkte, samengevatte gegevens die binnen ~30 seconden beschikbaar zijn. Omvat unieke algoritmen van populairste, grainers, en verliezers. Kan via Report Builder worden gebruikt.
* **[!UICONTROL Live Stream]**: wanneer u binnen seconden na de verzameling een stream wilt van gedeeltelijk verwerkte analysegegevens op raakniveau. Dit zijn gedeeltelijk verwerkte gegevens, beschikbaar binnen ~30 seconden. Alleen beschikbaar voor Analytics Premium. Vereist één of andere manier om de gegevens te visualiseren, typisch door een overeenkomst van de Diensten van de Techniek.

## Oplossingen op maat {#custom-solutions}

De Diensten van de techniek zouden moeten worden gebruikt wanneer:

* De andere Adobe-tools voldoen niet aan uw behoeften.
* U wilt een aangepaste ervaring.
* U wilt een volledig geautomatiseerde oplossing.
* Je wilt veel apparaten bereiken.
* U beschikt over meerdere gegevensbronnen.
* Je hebt complexe data ETL (Extract-Transform-Load) vereisten.
* U wilt een aangepaste branding.
* U wilt visualiseren [!UICONTROL Analytics Live Stream].
