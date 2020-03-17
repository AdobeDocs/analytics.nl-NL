---
description: Een vergelijkingstabel voor Analytics die APIs melden. Koppelingen naar de ondersteunende documentatie worden gegeven.
title: Analytics Reporting API Comparison
uuid: fa533a8e-33c0-42f4-a294-cabee0258c8f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Analytics Reporting API Comparison

Een vergelijkingstabel voor Analytics die APIs melden. Koppelingen naar de ondersteunende documentatie worden gegeven.

> [!NOTE] Wat latentie betreft, combineert Analytics for Target (A4T) Analytics en Target-gegevens op dezelfde hit voor geïntegreerde rapportage. Omdat de Analytics en de vraag van het Doel in verschillende tijden voorkomen, worden de klappen opgeslagen alvorens om het even welke verwerking voorkomt om gegevens van beide oplossingen te verzamelen. Hierbij wordt **een extra wachttijd van 7 tot 10 minuten** toegevoegd aan alle controlepunten.

<table id="table_7AF4FD678D494063ADF459B3CBC3EF3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> API-type </th> 
   <th colname="col2" class="entry"> Volledig verwerkt </th> 
   <th colname="col3" class="entry"> Real-time </th> 
   <th colname="col4" class="entry"> Livestream </th> 
   <th colname="col5" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Beschrijving</b> </td> 
   <td colname="col2"> Volledig verwerkte, voltooide gegevens die in alle interfaces van Analytics beschikbaar zijn. </td> 
   <td colname="col3"> Gedeeltelijk verwerkte, beperkte metriek beschikbaar binnen seconden van inzameling. </td> 
   <td colname="col4"> Gedeeltelijk verwerkte raakgegevens beschikbaar binnen seconden na verzameling. </td> 
   <td colname="col5"> Volledig verwerkte, afgeronde gegevens die worden gebruikt om grote gegevensuitvoer te trekken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://marketing.adobe.com/resources/help/en_US/analytics/whitepapers/analytics-data-availability.pdf"  > Latentie</a> </p> </td> 
   <td colname="col2"> 30-90 minuten </td> 
   <td colname="col3"> * Seconden -10 minuten </td> 
   <td colname="col4"> Seconden -10 minuten </td> 
   <td colname="col5"> 90 minuten + </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerking voltooid</b> </td> 
   <td colname="col2"> Volledig </td> 
   <td colname="col3"> Gedeeltelijk </td> 
   <td colname="col4"> Gedeeltelijk </td> 
   <td colname="col5"> Volledig </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="https://marketing.adobe.com/resources/help/en_US/reference/"  > Rapportageinterfaces</a> </td> 
   <td colname="col2"> Rapporten en analyses, Report Builder, API </td> 
   <td colname="col3"> Rapport in realtime in Rapporten &amp; Analytics, Report Builder, API </td> 
   <td colname="col4"> Alleen API </td> 
   <td colname="col5"> Data Warehouse en API </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Korreligheid gegevens</b> </td> 
   <td colname="col2"> Samengevat </td> 
   <td colname="col3"> Samengevat </td> 
   <td colname="col4"> Niveau aanpassen </td> 
   <td colname="col5"> Samengevat </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Bezoekerprofiel verwerken</b> </td> 
   <td colname="col2"> Ja </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Nee </td> 
   <td colname="col5"> Ja </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ondersteunt segmenten</b> </td> 
   <td colname="col2"> Ja </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Nee </td> 
   <td colname="col5"> Ja (maar alleen met Data Warehouse compatibele segmenten) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Analytics SKU</b> </td> 
   <td colname="col2"> Standaard+ </td> 
   <td colname="col3"> Standaard+ </td> 
   <td colname="col4"> Premium Complete of Predictive Intelligence </td> 
   <td colname="col5"> Standaard+ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Documentatie</b> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/get-started%E2%80%8B"  > Webservices</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/real-time"  > Real-Time rapporten</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1%E2%80%8B"  > Overzicht van Livestream</a> </p> </td> 
   <td colname="col5"> <p><a href="https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse.html"  > Data Warehouse</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Gerelateerde Help**

* [Adobe/IO](https://www.adobe.io/) - Een uitgebreide bron voor de technische documentatie en gereedschappen die nodig zijn om Adobe-technologieën in uw toepassingen te integreren.
* [API voor gegevenswerkbench](https://marketing.adobe.com/developer/documentation/data-workbench-query-api/c-ins-qry-api)

