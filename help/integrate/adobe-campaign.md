---
description: 'null'
title: Adobe-campagnerapportage
uuid: 0919ae9f-84eb-43a5-8282-6cd6dec63dc1
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Adobe-campagnerapportage

Raadpleeg de documentatie [bij](https://helpx.adobe.com/campaign/standard/integrating/using/about-campaign-analytics-integration.html)Adobe Campagne voor meer informatie over het configureren van deze integratie.

Deze integratie tussen Adobe Analytics en Adobe Campaign

* Hiermee kunt u uw KPI-gegevens (Key Performance Indicator) van Adobe Campaign Standard delen met Adobe Analytics.
* Verrijkt trackingformules met Adobe Analytics-parameters.
* Hiermee voegt u een nieuw rapport toe onder **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** > **[!UICONTROL Adobe Campaign.]**
* Hiermee voegt u vijf nieuwe Adobe Campagne-classificaties toe.
* 10 nieuwe maateenheden voor Adobe Campaign toevoegen.
* Hiermee voegt u zes nieuwe Adobe-campagnedimensies toe.
* Hiermee synchroniseert u gegevens naar Analytics elke 15 minuten.

## Stap 1. Adobe-campagnerapportage inschakelen {#section_C685EF10505045708A6536BB13F6CD58}

Als u Campagne-gegevens wilt weergeven in Analytics, moet u eerst Campagne-rapportage inschakelen.

1. Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL <select report suite>]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Adobe Campaign Reporting]** .
1. Klik op **[!UICONTROL Enable Campaign Reporting]**.

   ![](assets/enable-campaign.png)

## Stap 2. Adobe-campagnerapporten weergeven {#section_9C18A29F3CC54BD4AC5EA96417F17B33}

De integratie tussen Adobe Campagne Standard en Adobe Analytics voegt het volgende rapport toe onder **[!UICONTROL Analytics]** > **[!UICONTROL Reports]**

<table id="table_3627F40DC90646A7B5E217A88B6FD630"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Rapport </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Leverings-id voor Adobe Campagne uitgevoerd </p> </td> 
   <td colname="col2"> <p>Toont gegevens die uit Adobe Campaign zijn geïmporteerd over e-mailberichten die vanuit Adobe Campaign zijn verzonden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Stap 3. Adobe Campagnerclassificaties gebruiken {#section_74A28AF3F4CA4091943789DE4D8B2B63}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL <select report suite>]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Adobe Campaign Classifications]**

Zodra uw rapportsuite is ingeschakeld voor Adobe Campaign, zijn de volgende classificaties beschikbaar:

* Leverings-id (interne leveringsnaam die u ziet in campagne)
* Leveringslabel (Aflevering in campagne - Aflevering/Herhaling aflevering/Transactie Aflevering)
* Campagne-id (interne naam voor campagne die u in de campagne ziet)
* Campagnelabel (campagne in Adobe-campagne)
* Uitvoerd leveringslabel (lijst van afzonderlijke uitgevoerde leveringen)

## Adobe Campagne Dimensions en Metrics beschikbaar in Adobe Analytics {#section_F33385C9660644AF84172EC39601469B}

De volgende **meetgegevens** zijn beschikbaar in Campagne in de rapportsuite van Adobe Analytics:

* Adobe-campagne verzonden
* Adobe-campagne geopend
* Adobe-campagne geklikt
* Adobe-campagne verwerkt
* Adobe-campagne geleverd
* Unieke open Adobe-campagne
* Unieke klik op Adobe-campagne
* Adobe Campagne Unsubscribed
* Totale Bounces voor Adobe-campagne
* Instanties van leverings-id voor Adobe Campagne

De volgende **afmetingen** zijn beschikbaar in de categorieën Campagne in het rapport Adobe Analytics:

| Naam dimensie | Definitie |
|--- |--- |
| Campagne-id | Id van alle campagnes waarvoor tijdens de duur KPI&#39;s zijn verzonden |
| Campagnelabel | Labels voor campagne-id&#39;s |
| Leverings-id | Id van alle leveringen waarvoor tijdens de duur KPI’s zijn verzonden. Omvat ook IDs van hoofdleveringen van terugkomende levering en transactielevering. Voorbeeld: Een terugkomende levering DM1 was gepland en DM2, DM3, DM4 en DM5 waren kindleveringen van de terugkomende levering.  De leverings-id geeft de resultaten voor alle leveringen weer, DM1 tot en met DM5. |
| Afleveringslabel | Labels van levering-id&#39;s |
| Uitvoerde leverings-id | Id&#39;s van alleen uitgevoerde leveringen. Geen id van terugkerende/transactionele hoofdlevering. Voorbeeld: Een terugkomende levering DM1 was gepland en DM2, DM3, DM4 en DM5 waren kindleveringen van de terugkomende levering. Uitvoerde identiteitskaart van de Levering toont resultaten voor alle leveringen die van DM2 aan DM5 beginnen - de leveringen die eigenlijk zijn uitgevoerd. |
| Uitvoerd leveringslabel | Labels van uitgevoerde leverings-id&#39;s |
