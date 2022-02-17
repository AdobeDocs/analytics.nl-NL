---
description: De categorieën van de gegevensbron identificeren verschillende gegevensbrontypes die gelijkaardige functionaliteit verstrekken.
subtopic: Data sources
title: Overzicht van gegevenstypen en categorieën
topic-fix: Developer and implementation
feature: Data Sources
exl-id: d459fd06-a0fe-49e6-8624-b42f0c60ee6e
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 6%

---

# Overzicht van gegevenstypen en categorieën

De categorieën van de gegevensbron identificeren verschillende gegevensbrontypes die gelijkaardige functionaliteit verstrekken.

Categorieën bieden een manier om gegevensbronnen vanuit het perspectief van de gebruiker te groeperen. Wanneer u een gegevensbron maakt via de [!DNL Data Sources] UI, selecteer eerst een gegevensbroncategorie, dan een specifiek gegevensbrontype. Elke categorie bevat typen gegevensbronnen die vergelijkbare typen gegevens ondersteunen. [!DNL Data Sources] bevat de volgende gegevensbroncategorieën:

## Websitegebruik {#web-usage}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Web Server Log Files] | [Weblog](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md) | De meeste servers van het Web produceren logboekdossiers die elke gediende pagina registreren. Gebruikend deze gegevensbron, kunt u de logboekdossiers van de meeste de servergegevens van het Web verwerken en deze gegevens toevoegen aan uw rapporten. |
| [!UICONTROL Advertising Cloud Bulk Upload] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Biedt handmatige en Excel-geautomatiseerde bulkuploads in [!DNL Advertising Cloud]. |
| [!UICONTROL Site-level Traffic Data Source] | [Verkeer](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | De gegevens van het Verkeer van de invoer voor uw volledige Website. Bijvoorbeeld, [!UICONTROL Page Views]. |
| [!UICONTROL Breakdown Traffic Data Source] | [Verkeer](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | De gegevens van het Verkeer van de invoer die door een andere variabele van de Website worden verdeeld. Bijvoorbeeld: [!UICONTROL Page Views] uitgesplitst naar [!UICONTROL Product]. |

## Campagnes toevoegen {#ad-campaigns}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Generic Ad Server] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u afbeeldingen en andere meetgegevens van het hoogste niveau over uw advertentieactiviteiten vanaf uw advertentieserver integreren in marketingrapporten. Dit is de algemene gegevensbron en de gegevensbron van de server en zou moeten worden gebruikt als uw specifieke advertentieserver niet wordt gesteund. |
| [!UICONTROL Generic Email Campaign Server] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u metrische gegevens van uw e-mailcampagnemeserver integreren in marketingrapporten.  Veelvoorkomende ingebouwde meetgegevens zijn het aantal verzonden berichten, geleverde berichten en gelezen berichten. Dit is de algemene gegevensbron voor de e-mailcampagne en moet worden gebruikt als uw specifieke e-mailcampagnemeserver niet wordt ondersteund. |
| [!UICONTROL Generic Pay-Per-Click Service] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u gegevens importeren over de prestaties per muisklik, zoals afbeeldingen, klikken en kosten.  Dit is de generische pay-per-click gegevensbron en moet worden gebruikt als uw specifieke pay-per-click-service niet wordt ondersteund. |

## Customer Relationship Management (CRM) {#crm}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Generic Call Center] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Laat u informatie over uw callcenter in marketing rapporten integreren. De metriek meer algemeen ingevoerd omvat het aantal vraag, tijd op de telefoon, de agent, en totale verkoop.  Deze gegevensbron is de generische gegevensbron van het vraagcentrum en zou moeten worden gebruikt als uw specifieke software van het vraagcentrum niet wordt gesteund. |
| [!UICONTROL Generic Customer Support Application] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u informatie van uw klantenondersteuningssoftware integreren in marketingrapporten. Het omvat meetgegevens zoals het aantal nieuwe incidenten, het aantal opgeloste incidenten en de tijd die is besteed aan het oplossen van incidenten.  Dit is de generische bron van de klantensteun en zou moeten worden gebruikt als uw specifieke toepassing van de klantendienst niet wordt gesteund. |

## Klanttevredenheid {#csat}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Generic Survey Data] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u enquêteresultaten uit een hulpprogramma van derden integreren in marketingrapporten en laten zien hoe tevreden klanten zijn over hun interacties met uw site.  Dit is de generische bron van onderzoeksgegevens en zou moeten worden gebruikt als uw specifieke dienst van onderzoeksgegevens niet wordt gesteund. |

## Siteprestaties {#performance}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Generic Site Download Speed] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u gegevens integreren van een toepassing of service die de downloadsnelheid bijhoudt met uw gegevens. Dit is de algemene gegevensbron van de downloadsnelheid en zou moeten worden gebruikt als uw specifieke software of de dienst van de downloadsnelheid niet wordt gesteund. |

## Algemeen {#generic}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Generic Data Source (Summary Data Only)] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Gebruik deze gegevensbron als er geen betere overeenkomst is met het type gegevens dat u in marketing reports and analytics wilt importeren. |
| [!UICONTROL Generic Data Source (Full Processing)] | Volledige verwerking | Adobe heeft volledige verwerkingsgegevensbronnen vervangen op 31 januari 2022. [Meer informatie](/help/import/c-data-sources/c-datasrc-types/datasrc-fullproc-eol.md). Adobe raadt u aan de [BDIA (Bulk Data Insertion API)](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) in plaats daarvan. |
| [!UICONTROL Generic Data Source (Transaction ID)] | <ul><li>Transactie-id</li><li>Bezoekers-id</li></ul> | Hiermee kunt u elke offlinegebeurtenis koppelen aan een online gebeurtenis. De [!UICONTROL Transaction ID] fungeert als sleutel tussen de gebeurtenissen offline en online. |

## Online aankopen {#purchases}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Product Returns] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u terugkerende gegevens van een product importeren die u aan een aankoop-id kunt koppelen, zodat u zoekprogramma&#39;s, trefwoorden, campagnes en andere kenmerken kunt identificeren die meer kans maken op het genereren van resultaten. |
| [!UICONTROL Product Cost] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Laat u de daadwerkelijke kosten van producten verstrekken die van uw Website worden gekocht en worden verscheept door kosten of winst met individuele producten te associëren zodat kunt u op de meest winstgevende campagnes, sleutelwoorden en interne bevorderingen voor uw Website nauwkeurig rapporteren. |
| [!UICONTROL Order Status] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u metrische gegevens gebruiken om de status van elke uitgevoerde bestelling te identificeren, inclusief geannuleerde, verzonden, voltooide of als frauduleus beschouwde bestellingen. De rapportage van de status van de order kan bepalen welke verwervingsmethoden het hoogste voltooiingspercentage van de order genereren. |

## Leads en aanhalingstekens {#leads}

| Gegevensbron | Verwerkingstype | Beschrijving |
| --- | --- | --- |
| [!UICONTROL Lead Generation] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Laat u informatie over de resultaten van de lood voor elke lood uploaden die op uw Website, met inbegrip van daadwerkelijke geproduceerde opbrengst wordt geproduceerd.  Nadat de opbrengst correct aan lood IDs wordt toegeschreven, kunt u uw meest winstgevende campagnes en promoties identificeren. |
| [!UICONTROL Online Quote] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Laat u informatie over de resultaten van de lood voor elke lood uploaden die op uw Website, met inbegrip van daadwerkelijke geproduceerde opbrengst wordt geproduceerd.  Nadat de opbrengst correct aan lood IDs wordt toegeschreven, kunt u uw meest winstgevende campagnes en promoties identificeren. |
| [!UICONTROL Call Center Data] | [Conversie](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Hiermee kunt u callcentertransacties uploaden, zodat u de tactiek (campagnes, promoties, enzovoort) kunt identificeren. die klanten ertoe aanzetten de telefoon op te halen. |
