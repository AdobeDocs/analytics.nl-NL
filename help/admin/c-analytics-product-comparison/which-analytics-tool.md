---
description: Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.
title: Welke Adobe Analytics-tool moet ik gebruiken?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: 12d2391e2429f80648ca674540e65ecd224b1b02
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 4%

---


# Welke Adobe Analytics-tool moet ik gebruiken?

Deze Help-pagina bevat aanbevolen gebruiksgevallen voor elk Adobe Analytics-hulpprogramma. De hulpmiddelen zouden in de orde moeten worden overwogen zij worden vermeld. Als een bepaald hulpmiddel niet aan de behoefte voldoet, ga naar volgende voor overweging.

Voor meer informatie over de Vergelijking van het Product van Adobe Analytics, ga [hier](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md).

## Adobe Analytics Reporting User Interfaces {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[De](/help/analyze/analysis-workspace/home.md)** Werkruimten van de analyse zouden de go-aan gebruikersinterface voor al uw rapportering en analysebehoeften moeten zijn. Adobe blijft in dit product investeren en maandelijks updates uitbrengen. Als er een taak is die u niet kunt uitvoeren in Analysis Workspace, kunt u de andere interfaces hieronder overwegen.**

**[Rapporten en](/help/analyze/reports-analytics/overview/report-overview.md)** analyses moeten worden gebruikt:

* Door beginnergebruikers die toegang tot vooraf gebouwde rapportering nodig hebben die gemakkelijker is te navigeren.
* Toegang krijgen tot realtime gegevens in de gebruikersinterface.
* Kalendergebeurtenissen instellen.
* Doelstellingen instellen.
* Bot-rapportage weergeven.
* U krijgt toegang tot unieke videovisualisaties van Video Daypart en Viewer Drop-off.
* Als u publicatielijsten in geplande rapporten wilt gebruiken.

**[Er moet gebruik worden gemaakt van ad-](/help/analyze/ad-hoc-analysis/adhoc-home.md)** hocanalyse:

>[!IMPORTANT]
>
>Adobe verplaatst Ad Hoc Analysis naar het einde van zijn leven op 1 maart 2021. [Meer informatie](https://adobe.ly/discoverworkspace)

* Als taborganisatie van projectwerk gewenst is.
* Om het rapport van de Analyse van de Plaats te gebruiken (3D-het schilderen rapport).

**[Gegevenswerkbenchmark ](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)** moet worden gebruikt:

* De meest flexibele optie voor Analytics (tot op bezoekersniveau, analyse op raakniveau).
* Om een multi-kanaaldataset van online en off-line interactie van CRM aan POS aan Web tot stand te brengen.
* Voor geavanceerde attributie (op regels gebaseerde &amp; algoritmische modellen).
* Voor voorspellende, statistische modellering (prospectie, clustering, correlaties, enz.).
* Voor Latentie-analyse (tijd voor / sinds een gebeurtenis).
* Voor de identificatie en uitvoer van complexe segmenten in Adobe Experience Cloud.

## Gegevens importeren in Adobe Analytics {#section_B42B998D6E3E4357B024AEFA4EC69A23}

**[Er moeten](/help/components/classifications/c-classifications.md)** classificaties worden gebruikt:

* Als er metagegevens zijn die u aan een verzamelwaarde wilt koppelen (eVar, prop, marketingkanaal)
* Opties:

   * Regelbouwer: gebruiken wanneer u voorspelbare opgemaakte waarden hebt die voor een variabele worden verzameld, bijvoorbeeld waarden met scheidingstekens. Op deze manier kunt u regels voor een keer instellen, grotendeels &quot;instellen en vergeten&quot;.
   * Browser importeren: gebruiken wanneer u geen voorspelbare waarden hebt, of wanneer u een eindige lijst van waarden hebt die een eenmalig update vereist. Deze aanpak vereist dat u de classificaties voortdurend controleert op nieuwe waarden.

**[Gegevensbronnen](/help/import/c-data-sources/datasrc-home.md)** moeten worden gebruikt:

* Als er offlinegegevens zijn die u permanent in Adobe Analytics wilt schrijven
* Opties:

   * Overzicht: eenvoudige gegevens uploaden, op dag of beperkte afmetingen
   * Transactie-id: gegevens uploaden die een online eindpunt met off-line gegevens verbinden, en ingevoerde gegevens volledig associëren aan een bezoekersmomentopname die online wordt gevangen (b.v. orden volledig online, en worden teruggekeerd off-line)
   * Volledige verwerking: gegevensbronnen met tijdstempels, verwerkt alsof deze zijn verzameld door Adobe-servers. Dat wil zeggen dat gegevens rechtstreeks in de bezoekersreis worden ingevoerd.

**[Gegevensverbindingen ](https://www.adobeexchange.com/experiencecloud.html)** moeten worden gebruikt:

* Wanneer u verbinding maakt met een externe provider die een ondersteunde verbinding met Adobe Analytics heeft gemaakt. Gegevensconnectors bevatten doorgaans permanent en automatisch samenvattingsgegevens in Adobe Analytics, op terugkerende basis.

**[De](/help/import/c-data-insertion-api/c-data-insertion-api.md)** API voor gegevensinvoeging moet worden gebruikt:

* Wanneer u gegevens naar Adobe Analytics moet uploaden en u kunt de Adobe AppMeasurement- of mobiele SDK-code niet gebruiken.

**[API voor data-invoer in bulk](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* API voor gegevensinvoeging en API voor bulkgegevensinvoeging zijn beide methoden om verzamelingsgegevens op de server naar Adobe Analytics te verzenden. API-aanroepen voor het invoegen van gegevens worden één gebeurtenis tegelijk uitgevoerd. De API voor het invoegen van bulkgegevens accepteert CSV-bestanden met gebeurtenisgegevens, één gebeurtenis per rij. Als u aan een nieuwe implementatie van server-zijinzameling werkt, adviseren wij gebruikend de Invoeging API van de Gegevens van het Bulk.

**[Klantkenmerken ](https://docs.adobe.com/content/help/nl-NL/core-services/interface/customer-attributes/attributes.html)** dienen te worden gebruikt:

* Als u gegevens van ondernemingsklanten in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangt en de gegevens aan Experience Cloud wilt uploaden.
* Als u de gegevens van CRM voor diepere analyse in Analytics wilt gebruiken, of als het richten van criteria in Adobe Target.

**[Er moeten](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** analyses van het publiek worden gebruikt:

* Als u gegevens over het Adobe Audience Manager-publiek (AAM), zoals demografische informatie (bv. geslacht of inkomensniveau), psychografische informatie (bv. interesses en hobby&#39;s), CRM-gegevens of impliciete gegevens in een analyseworkflow wilt opnemen.
* Als u de geüploade CRM-gegevens op tijd wilt baseren, omdat deze integratie nieuwe informatie stuurt naar Analytics die door een hit zijn getroffen.

## Gegevens exporteren uit Adobe Analytics {#section_901C06ABF2014E92B2952906723DF235}

**[Report](/help/analyze/report-builder/home.md)** Buildershould be used:

* Als de aangepaste layoutopties van Workspace worden beperkt (alles is mogelijk in Report Builder, binnen de grenzen van Excel).
* In gebruikersinvoer of offlinegegevensbronnen (impressies, kosten) losjes koppelen aan Adobe-gegevens. De duurdere oplossing voor het verbinden in gegevens is Gegevensbronnen (zie het Importeren van Gegevens aan Analytics).
* Gegevens uit verschillende dimensionale rapporten samenvoegen (bv. rapport over promo-impressions wordt gekoppeld aan rapport over promo-click-to-conversion).
* Voor cross-report-suite weergaven.
* Als automatisering via planning gewenst is (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Er](/help/export/data-warehouse/data-warehouse.md)** dient gebruik te worden gemaakt van gegevenspaden:

* Om tot variabelen toegang te hebben die anders in UI - IP adres, Experience Cloud ID, Analytics Visitor ID, Pagina URL) worden verborgen
* Om tot meer korrelige gegevens dan UI (gedenormaliseerde lijstmening) toegang te hebben
* Gegevens downloaden in een indeling die geschikt is voor draaitabelinvoer
* Als de client Adobe-gegevens wil invoeren in een hulpprogramma voor gegevensvisualisatie van derden (enigszins samengevat en niet op raakniveau)
* Om tot alle unieke afmetingspunten toegang te hebben als u in &quot;Laag Verkeer&quot;in Adobe Analytics loopt

**[Gegevensfeedback voor analyse](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)** moet worden gebruikt:

* Als u de meest gedetailleerde gegevensinvoer wilt gebruiken die we kunnen opgeven (bezoeker-id, hit).
* Als de cliënt Adobe gegevens wil die in een cliënt-zijgegevensbestand worden opgeslagen, op het meest korrelige niveau kunnen wij verzenden.
* Als de client een Business Intelligence-app (BI) wil ontwikkelen of Adobe-gegevens op raakniveau in een hulpprogramma van derden wil invoeren.

**[Rapportage ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** van APIs zou moeten worden gebruikt wanneer de andere visualisatieopties niet aan uw behoeften voldoen. De drie API-opties zijn:

* **Volledig verwerkt**: wanneer u eigenschap-rijke gegevens (met inbegrip van bezoeken, bezoekers, en segmenten) wilt. Dit zijn standaard samengevatte gegevens uit de analysefunctie, beschikbaar binnen ~30-90 minuten. Kan via Report Builder worden gebruikt.
* **Real-time**: wanneer u een paar metriek en afmetingen met seconden van latentie wilt bekijken. Dit zijn beperkte, gedeeltelijk verwerkte, samengevatte gegevens die binnen ~30 seconden beschikbaar zijn. Omvat unieke algoritmen van populairste, aannemers, en verliezers. Kan via Report Builder worden gebruikt.
* **[!UICONTROL Live Stream]**: als u binnen seconden na de verzameling een stream wilt van gedeeltelijk verwerkte analysegegevens op raakniveau. Dit zijn gedeeltelijk verwerkte gegevens, beschikbaar binnen ~30 seconden. Alleen beschikbaar voor Analytics Premium. Vereist één of andere manier om de gegevens te visualiseren, typisch door een overeenkomst van de Diensten van de Techniek.

## Aangepaste oplossingen {#section_4A212F26A15947599DFB0399A0440CB6}

De Diensten van de techniek zouden moeten worden gebruikt wanneer:

* De andere Adobe-gereedschappen voldoen niet aan uw behoeften.
* U wilt een aangepaste ervaring.
* U wilt een volledig geautomatiseerde oplossing.
* U wilt vele apparaten bereiken.
* U hebt meerdere gegevensbronnen.
* U hebt complexe ETL-vereisten (Extract-Transform-Load) voor gegevens.
* U wilt aangepaste branding.
* U wilt [!UICONTROL Analytics Live Stream] visualiseren.
