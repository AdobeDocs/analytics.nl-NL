---
description: Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk hulpprogramma van Adobe Analytics. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.
title: Welk hulpprogramma van Adobe Analytics moet ik gebruiken?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: b4e17f7aad73af250c89cb8117f741f7eed89b7e

---


# Welk hulpprogramma van Adobe Analytics moet ik gebruiken?

Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk hulpprogramma van Adobe Analytics. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.

Ga [hier](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md)voor meer informatie over productvergelijkingen van Adobe Analytics.

## Adobe Analytics Reporting User Interfaces {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[De Werkruimte](/help/analyze/analysis-workspace/analysis-workspace-features.md)**van de analyse zou de go-aan gebruikersinterface voor al uw rapportering en analysebehoeften moeten zijn. Adobe blijft in dit product investeren en maandelijks updates uitbrengen. Als er een taak is u niet in de Werkruimte van de Analyse kunt doen, overweeg de andere hieronder interfaces.**

**[Rapporten en analyses](/help/analyze/reports-analytics/overview/report-overview.md)**moeten worden gebruikt:

* Door beginnergebruikers die toegang tot vooraf gebouwde rapportering nodig hebben die gemakkelijker is te navigeren.
* Om inzicht te krijgen in de doelactiviteit (Analytics for Target/A4T): lift en vertrouwen.
* Toegang krijgen tot realtime gegevens in de gebruikersinterface.
* Kalendergebeurtenissen instellen.
* Doelstellingen instellen.
* Bot-rapportage weergeven.
* Om veelvoudige rapportreeksen in één enkel dashboard UI te bekijken.
* Unieke videovisualisaties van de Gelijktijdige Kijker, Video Daypart, en de Daling van de Kijker toegang hebben.
* Als u publicatielijsten in geplande rapporten wilt gebruiken.

**[Gebruikersinterface](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)**voor mobiele services moet worden gebruikt:

* Als u een gesiloade weergave van de gegevens van de Mobile App wilt.
* De implementatie van de SDK van uw mobiele app beheren.
* Mobiele reclame instellen, zoals berichten in de app, pushberichten en het opgeven van locaties.
* Als u meer interactieve visualisaties wilt gebruiken voor App-gegevens (Zonneexplosie).
* Om aandachtspunten op een kaart te visualiseren.
* Voor waarden van de Lifetime-waarde.

**[Er moet gebruik worden gemaakt van ad-hocanalyse](/help/analyze/ad-hoc-analysis/adhoc-home.md)**:

* 50.000 rijen gegevens exporteren
* Als taborganisatie van projectwerk gewenst is.
* Om het rapport van de Analyse van de Plaats te gebruiken (3D-het schilderen rapport).

**[Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)**dient te worden gebruikt:

* De meest flexibele optie voor Analytics (tot op bezoekersniveau, analyse op raakniveau).
* Om een multi-kanaaldataset van online en off-line interactie van CRM aan POS aan Web tot stand te brengen.
* Voor geavanceerde attributie (op regels gebaseerde &amp; algoritmische modellen).
* Voor voorspellende, statistische modellering (prospectie, clustering, correlaties, enz.).
* Voor Latentie-analyse (tijd voor / sinds een gebeurtenis).
* Voor identificatie en export van complexe segmenten in de gehele Adobe Experience Cloud.

## Gegevens importeren in Adobe Analytics {#section_B42B998D6E3E4357B024AEFA4EC69A23}

**[Classificaties](/help/components/c-classifications2/c-classifications.md)**moeten worden gebruikt:

* Als er metagegevens zijn die u aan een verzamelwaarde wilt koppelen (eVar, prop, marketing channel)
* Opties:

   * Regelbouwer: gebruiken wanneer u voorspelbare opgemaakte waarden hebt die voor een variabele worden verzameld, bijvoorbeeld waarden met scheidingstekens. Op deze manier kunt u regels voor een keer instellen, grotendeels &quot;instellen en vergeten&quot;.
   * Browser importeren: gebruiken wanneer u geen voorspelbare waarden hebt, of wanneer u een eindige lijst van waarden hebt die een eenmalig update vereist. Deze aanpak vereist dat u de classificaties voortdurend controleert op nieuwe waarden.

**[Gegevensbronnen](/help/import/c-data-sources/datasrc-home.md)**moeten worden gebruikt:

* Als er offlinegegevens zijn die u permanent in Adobe Analytics wilt schrijven
* Opties:

   * Overzicht: eenvoudige gegevens uploaden, op dag of beperkte afmetingen
   * Transactie-id: gegevens uploaden die een online eindpunt met off-line gegevens verbinden, en ingevoerde gegevens volledig associëren aan een bezoekersmomentopname die online wordt gevangen (b.v. orden volledig online, en worden teruggekeerd off-line)
   * Volledige verwerking: gegevensbronnen met tijdstempels, verwerkt alsof deze zijn verzameld door Adobe-servers. Dat wil zeggen dat gegevens rechtstreeks in de bezoekersreis worden ingevoerd.

**[Gegevensconnectors](https://www.adobeexchange.com/experiencecloud.html)(voorheen Genesis genoemd)**moeten worden gebruikt:

* Wanneer u verbinding maakt met een externe provider die een ondersteunde verbinding heeft gemaakt met Adobe Analytics. Gegevensconnectors gebruiken doorgaans permanent en automatisch samenvattingsgegevens in Adobe Analytics, op terugkerende basis.

**[De API](https://marketing.adobe.com/developer/documentation/data-insertion/c-data-insertion-api)**voor gegevensinvoeging moet worden gebruikt:

* Wanneer u gegevens moet uploaden naar Adobe Analytics en u kunt de Adobe AppMeasurement- of mobiele SDK-code niet gebruiken.

**[Klantkenmerken](/help/components/c-variables/dimensionslist/reports-customer-attributes.md)**dienen te worden gebruikt:

* Als u gegevens van ondernemingsklanten in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangt en de gegevens aan de Wolk van de Ervaring wilt uploaden.
* Als u de gegevens van CRM voor diepere analyse in Analytics wilt gebruiken, of als het richten criteria in Adobe Doel.

**[Analyse](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**van het publiek moet worden gebruikt:

* Als u de publieksgegevens van de Manager van de Audience van Adobe (AAM) zoals demografische informatie (b.v. geslacht of inkomensniveau), psychografische informatie (b.v. interesses en hobby&#39;s), CRM-gegevens, of impliciete gegevens in om het even welke analysewerkschema wilt opnemen.
* Als u de geüploade CRM-gegevens op tijd wilt baseren, omdat deze integratie nieuwe informatie stuurt naar Analytics die door een hit zijn getroffen.

## Gegevens exporteren uit Adobe Analytics {#section_901C06ABF2014E92B2952906723DF235}

**[De Bouwer](/help/analyze/report-builder/home.md)**van het rapport zou moeten worden gebruikt:

* Als de aangepaste lay-outopties van Werkruimte (om het even wat mogelijk is in de Bouwer van het Rapport, binnen de grenzen van Excel) beperken.
* Om de invoer of offlinegegevensbronnen (impressies, kosten) van een gebruiker los van elkaar te koppelen aan Adobe-gegevens. De duurdere oplossing voor het verbinden in gegevens is Gegevensbronnen (zie het Importeren van Gegevens aan Analytics).
* Gegevens uit verschillende dimensionale rapporten samenvoegen (bv. rapport over promo-impressions wordt gekoppeld aan rapport over promo-click-to-conversion).
* Voor cross-report-suite weergaven.
* Als automatisering via planning gewenst is (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)**dient te worden gebruikt:

* Om tot variabelen toegang te hebben die anders in UI - IP adres, de identiteitskaart van de Wolk van de Ervaring, de Bezoeker van de Analyse, identiteitskaart van de Bezoeker, Pagina URL) worden verborgen
* Om tot meer korrelige gegevens dan UI (gedenormaliseerde lijstmening) toegang te hebben
* Gegevens downloaden in een indeling die geschikt is voor draaitabelinvoer
* Als de client Adobe-gegevens wil invoeren in een programma voor gegevensvisualisatie van derden (enigszins samengevat en niet op raakniveau)
* Als u toegang wilt tot alle waarden van unieke dimensies, gaat u naar &quot;Laag verkeer&quot; in Adobe Analytics

**[Gegevensinvoer](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**voor analyse moet worden gebruikt:

* Als u de meest gedetailleerde gegevensinvoer wilt gebruiken die we kunnen opgeven (bezoeker-id, hit).
* Als de client Adobe-gegevens wil opslaan in een clientdatabase, kunnen we deze gegevens op het meest granulaire niveau verzenden.
* Als de client een Business Intelligence-hulpprogramma (BI) wil ontwikkelen of Adobe-gegevens op hit-niveau wil invoeren in een hulpprogramma van derden.

**[Het melden van APIs](https://marketing.adobe.com/developer/get-started/introduction/c-introduction)**zou moeten worden gebruikt wanneer de andere visualisatieopties niet aan uw behoeften voldoen. De drie API-opties zijn:

* **Volledig verwerkt**: wanneer u eigenschap-rijke gegevens (met inbegrip van bezoeken, bezoekers, en segmenten) wilt. Dit zijn standaard samengevatte gegevens uit de analysefunctie, beschikbaar binnen ~30-90 minuten. Kan door de Bouwer van het Rapport worden gebruikt.
* **Real-time**: wanneer u een paar metriek en afmetingen met seconden van latentie wilt bekijken. Dit zijn beperkte, gedeeltelijk verwerkte, samengevatte gegevens die binnen ~30 seconden beschikbaar zijn. Omvat unieke algoritmen van populairste, aannemers, en verliezers. Kan door de Bouwer van het Rapport worden gebruikt.
* **[!UICONTROL Live Stream]**: als u binnen seconden na de verzameling een stream wilt van gedeeltelijk verwerkte analysegegevens op raakniveau. Dit zijn gedeeltelijk verwerkte gegevens, beschikbaar binnen ~30 seconden. Alleen beschikbaar voor Analytics Premium. Vereist één of andere manier om de gegevens te visualiseren, typisch door een overeenkomst van de Diensten van de Techniek.

## Aangepaste oplossingen {#section_4A212F26A15947599DFB0399A0440CB6}

De Diensten van de techniek zouden moeten worden gebruikt wanneer:

* De andere Adobe-gereedschappen voldoen niet aan uw wensen.
* U wilt een aangepaste ervaring.
* U wilt een volledig geautomatiseerde oplossing.
* U wilt vele apparaten bereiken.
* U hebt meerdere gegevensbronnen.
* U hebt complexe ETL-vereisten (Extract-Transform-Load) voor gegevens.
* U wilt aangepaste branding.
* U wilt visualiseren [!UICONTROL Analytics Live Stream].
