---
description: Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.
title: Welke Adobe Analytics-tool moet ik gebruiken?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 2%

---


# Welke Adobe Analytics-tool moet ik gebruiken?

Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.

Ga [hier](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md)voor meer informatie over Adobe Analytics-productvergelijkingen.

## Adobe Analytics die gebruikersinterfaces rapporteert {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)**moet de gebruikersinterface zijn voor al uw rapportage- en analysebehoeften. Adobe blijft in dit product investeren en maandelijks updates uitbrengen. Als er een taak is die u niet kunt uitvoeren in Analysis Workspace, kunt u de andere interfaces hieronder overwegen.**

**[Rapporten en Analytics](/help/analyze/reports-analytics/overview/report-overview.md)**moeten worden gebruikt:

* Door beginnergebruikers die toegang tot vooraf gebouwde rapportering nodig hebben die gemakkelijker is te navigeren.
* Toegang krijgen tot realtime gegevens in de gebruikersinterface.
* Kalendergebeurtenissen instellen.
* Doelstellingen instellen.
* Bot-rapportage weergeven.
* Unieke videovisualisaties van de Gelijktijdige Kijker, Video Daypart, en de Daling van de Kijker toegang hebben.
* Als u publicatielijsten in geplande rapporten wilt gebruiken.

**[Ad hoc analysis](/help/analyze/ad-hoc-analysis/adhoc-home.md)**dient te worden gebruikt:

* 50.000 rijen gegevens exporteren
* Als taborganisatie van projectwerk gewenst is.
* Om het rapport van de Analyse van de Plaats te gebruiken (3D-het schilderen rapport).

**[Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)**dient te worden gebruikt:

* De meest flexibele Analytics-tool (tot op bezoekersniveau, analyse op raakniveau).
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

* Wanneer u verbinding maakt met een externe provider die een ondersteunde verbinding met Adobe Analytics heeft gemaakt. Gegevensconnectors bevatten doorgaans permanent en automatisch samenvattingsgegevens in Adobe Analytics, op terugkerende basis.

**[De API](/help/import/c-data-insertion-api/c-data-insertion-api.md)**voor gegevensinvoeging moet worden gebruikt:

* Wanneer u gegevens moet uploaden naar Adobe Analytics en u kunt de Adobe AppMeturement- of mobiele SDK-code niet gebruiken.

**[Klantkenmerken](https://docs.adobe.com/content/help/nl-NL/core-services/interface/customer-attributes/attributes.html)**dienen te worden gebruikt:

* Als u gegevens van ondernemingsklanten in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangt en de gegevens aan Experience Cloud wilt uploaden.
* Als u de gegevens van CRM voor diepere analyse in Analytics wilt gebruiken, of als het richten criteria in Adobe Target.

**[Publiek Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**moet worden gebruikt:

* Als u Adobe Audience Manager (AAM) publieksgegevens zoals demografische informatie (bv. geslacht of inkomensniveau), psychografische informatie (bv. interesses en hobby&#39;s), CRM-gegevens of impliciete gegevens in een Analytics-workflow wilt opnemen.
* Als u geüploade CRM-gegevens op tijd wilt laten gebaseerd, omdat deze integratie nieuwe informatie naar een hit in Analytics stuurt.

## Gegevens exporteren uit Adobe Analytics {#section_901C06ABF2014E92B2952906723DF235}

**[De Bouwer](/help/analyze/report-builder/home.md)**van het rapport zou moeten worden gebruikt:

* Als de aangepaste lay-outopties van Werkruimte (om het even wat mogelijk is in de Bouwer van het Rapport, binnen de grenzen van Excel) beperken.
* Om de invoer of offlinegegevensbronnen (impressies, kosten) van een gebruiker los van elkaar te koppelen aan Adobe-gegevens. De duurdere oplossing voor het verbinden in gegevens is Gegevensbronnen (zie het Importeren van Gegevens aan Analytics).
* Gegevens uit verschillende dimensionale rapporten samenvoegen (bv. rapport over promo-impressions wordt gekoppeld aan rapport over promo-click-to-conversion).
* Voor cross-report-suite weergaven.
* Als automatisering via planning gewenst is (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data warehouse](/help/export/data-warehouse/data-warehouse.md)**dient te worden gebruikt:

* Om tot variabelen toegang te hebben die anders verborgen in UI - IP adres, identiteitskaart van Experience Cloud, identiteitskaart van de Bezoeker van Analytics, Pagina URL)
* Om tot meer korrelige gegevens dan UI (gedenormaliseerde lijstmening) toegang te hebben
* Gegevens downloaden in een indeling die geschikt is voor draaitabelinvoer
* Als de client Adobe-gegevens wil invoeren in een programma voor gegevensvisualisatie van derden (enigszins samengevat en niet op raakniveau)
* Om toegang te krijgen tot alle unieke dimensie-items wanneer u werkt met &quot;Low Traffic&quot; in Adobe Analytics

**[Analytics Data Feed](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**dient te worden gebruikt:

* Als u de meest gedetailleerde gegevensinvoer wilt gebruiken die we kunnen opgeven (bezoeker-id, hit).
* Als de client Adobe-gegevens wil opslaan in een clientdatabase, kunnen we deze gegevens op het meest granulaire niveau verzenden.
* Als de client een Business Intelligence-app (BI) wil ontwikkelen of Adobe-gegevens op aanraakniveau wilt invoeren in een hulpprogramma van derden.

**[Het melden van APIs](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)**zou moeten worden gebruikt wanneer de andere visualisatieopties niet aan uw behoeften voldoen. De drie API-opties zijn:

* **Volledig verwerkt**: wanneer u eigenschap-rijke gegevens (met inbegrip van bezoeken, bezoekers, en segmenten) wilt. Dit zijn standaard samengevatte gegevens uit de gebruikersinterface van Analytics, die binnen ~30-90 minuten beschikbaar zijn. Kan door de Bouwer van het Rapport worden gebruikt.
* **Real-time**: wanneer u een paar metriek en afmetingen met seconden van latentie wilt bekijken. Dit zijn beperkte, gedeeltelijk verwerkte, samengevatte gegevens die binnen ~30 seconden beschikbaar zijn. Omvat unieke algoritmen van populairste, aannemers, en verliezers. Kan door de Bouwer van het Rapport worden gebruikt.
* **[!UICONTROL Live Stream]**: als u een stroom van gedeeltelijk-verwerkte klap-niveau Analytics gegevens binnen seconden na inzameling wilt. Dit zijn gedeeltelijk verwerkte gegevens, beschikbaar binnen ~30 seconden. Alleen beschikbaar voor Analytics Premium. Vereist één of andere manier om de gegevens te visualiseren, typisch door een overeenkomst van de Diensten van de Techniek.

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
