---
description: Meer informatie over het inschakelen van Adobe Campaign-rapporten in Adobe Analytics
title: Hoe integreer ik Adobe Campaign Reporting in Adobe Analytics?
translation-type: tm+mt
source-git-commit: 84337e8112b63859927d31568010ef0f0d604333
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 95%

---


# Adobe Campaign-rapportage

Raadpleeg de [Adobe Campaign-documentatie](https://helpx.adobe.com/nl/campaign/standard/integrating/using/about-campaign-analytics-integration.html) voor meer informatie over het configureren van deze integratie.

Met deze integratie tussen Adobe Analytics en Adobe Campaign is het volgende mogelijk:

* U kunt uw KPI-data (Key Performance Indicator) van Adobe Campaign Standard delen met Adobe Analytics.
* Trackingformules worden aangevuld met Adobe Analytics-parameters.
* Voegt een nieuw rapport toe onder **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** > **[!UICONTROL Adobe Campaign.]**
* Voegt vijf nieuwe Adobe Campaign-classificaties toe.
* Voegt 10 nieuwe cijfers voor Adobe Campaign toe.
* Voegt zes nieuwe Adobe Campaign-dimensies toe.
* Synchroniseert elke 15 minuten data met Analytics.

## Stap 1. Adobe Campaign-rapportage inschakelen {#section_C685EF10505045708A6536BB13F6CD58}

Als u Campaign-data wilt weergeven in Analytics, moet u eerst Campaign-rapportage inschakelen.

1. Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Adobe Campaign Reporting]**.
1. Klik op **[!UICONTROL Enable Campaign Reporting]**.

   ![](assets/enable-campaign.png)

## Stap 2. Adobe Campaign-rapporten weergeven {#section_9C18A29F3CC54BD4AC5EA96417F17B33}

De integratie tussen Adobe Campaign Standard en Adobe Analytics voegt het volgende rapport toe onder **[!UICONTROL Analytics]** > **[!UICONTROL Reports]**

| Rapport | Definitie |
|--- |--- |
| Uitgevoerde levering-id van Adobe Campaign | Toont data die zijn geïmporteerd uit Adobe Campaign over e-mailberichten die vanuit Adobe Campaign zijn verzonden. |

## Stap 3. Adobe Campaign-classificaties gebruiken {#section_74A28AF3F4CA4091943789DE4D8B2B63}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Adobe Campaign Classifications]**

Zodra uw rapportsuite is ingeschakeld voor Adobe Campaign, zijn de volgende classificaties beschikbaar:

* Leverings-id (interne leveringsnaam die u ziet in campagne)
* Leveringslabel (levering in Campaign - individuele levering/terugkerende levering/transactielevering)
* Campagne-id (interne naam voor campagne die u in Campaign ziet)
* Campagnelabel (campagne in Adobe Campaign)
* Uitgevoerd leveringslabel (lijst van individuele uitgevoerde leveringen)

## Beschikbare Adobe Campaign-dimensies en -cijfers in Adobe Analytics {#section_F33385C9660644AF84172EC39601469B}

De volgende **cijfers** van Campaign zijn beschikbaar in de rapportsuite van Adobe Analytics:

* Adobe Campaign verzonden
* Adobe Campaign geopend
* Op Adobe Campaign geklikt
* Adobe Campaign verwerkt
* Adobe Campaign geleverd
* Adobe Campaign eenmalig geopend
* Eenmalig op Adobe Campaign geklikt
* Lidmaatschap op Adobe Campaign opgezegd
* Totaal aantal bounces voor Adobe Campaign
* Instanties van uitgevoerde levering-id&#39;s van Adobe Campaign

De volgende **dimensies** van Campaign zijn beschikbaar in de rapportsuites van Adobe Analytics:

| Naam dimensie | Definitie |
|--- |--- |
| Campagne-id | Id van alle campagnes waarvoor tijdens de duur KPI&#39;s zijn verzonden. |
| Campagnelabel | Labels voor campagne-id&#39;s |
| Leverings-id | Id van alle leveringen waarvoor tijdens de duur KPI’s zijn verzonden. Omvat ook id’s van hoofdleveringen van terugkerende leveringen en transactieleveringen. Voorbeeld: Er is een terugkerende levering DM1 gepland en DM2, DM3, DM4 en DM5 zijn onderliggende leveringen van de terugkerende levering.  De levering-id geeft de resultaten weer voor alle leveringen, DM1 tot en met DM5. |
| Leveringslabel | Labels van levering-id&#39;s |
| Uitgevoerde levering-id | Id&#39;s van alleen uitgevoerde leveringen. Geen id van terugkerende/transactionele hoofdlevering. Voorbeeld: Er is een terugkerende levering DM1 gepland en DM2, DM3, DM4 en DM5 zijn onderliggende leveringen van de terugkerende levering. Uitgevoerde levering-id geeft resultaten weer voor alle leveringen vanaf DM2 tot en met DM5 - de leveringen die daadwerkelijk zijn uitgevoerd. |
| Uitgevoerd leveringslabel | Labels van uitgevoerde leverings-id&#39;s |
