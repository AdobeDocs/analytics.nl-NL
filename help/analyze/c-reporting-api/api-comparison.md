---
description: Een vergelijkingstabel voor Analytics die APIs melden. Koppelingen naar de ondersteunende documentatie worden gegeven.
title: Vergelijking Analytics Rapportage-API
uuid: fa533a8e-33c0-42f4-a294-cabee0258c8f
feature: API
role: Developer
exl-id: 924f591d-b6ed-4dae-aa69-72d72217e7bd
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 12%

---

# Vergelijking Analytics Rapportage-API

Een vergelijkingstabel voor Analytics die APIs melden. Koppelingen naar de ondersteunende documentatie worden gegeven.

>[!NOTE]
>
>Wat latentie betreft, combineert Analytics for Target (A4T) Analytics en Target-gegevens op dezelfde hit voor geïntegreerde rapportage. Omdat de Analytics en de vraag van het Doel in verschillende tijden voorkomen, worden de klappen opgeslagen alvorens om het even welke verwerking voorkomt om gegevens van beide oplossingen te verzamelen. Dit proces voegt **een extra 7-10 minuten** latentie aan alle controlepunten toe.

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
   <td colname="col5"> Volledig verwerkte, gefinaliseerde gegevens die worden gebruikt voor het trekken van grote gegevensuitvoer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://experienceleague.adobe.com/docs/analytics/technotes/latency.html"  > Latentie</a> </p> </td> 
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
   <td colname="col1"> <a href="https://experienceleague.adobe.com/docs/analytics/landing/home.html"  > Rapportageinterfaces</a> </td> 
   <td colname="col2"> Analysis Workspace, Reports &amp; Analytics, Report Builder, API </td> 
   <td colname="col3"> Real-time rapport in Reports &amp; Analytics, Report Builder, 1.4 API </td> 
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
   <td colname="col1"> <b>Documentatie</b> </td> 
   <td colname="col2"> <p> <a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html"  > Analytics-API</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://github.com/AdobeDocs/analytics-1.4-apis"  > Real-Time rapporten</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md"  > Overzicht van Livestream</a> </p> </td> 
   <td colname="col5"> <p><a href="https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html"  > Data Warehouse</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Gerelateerde Help**

* [Adobe/IO](https://www.adobe.io/)  - Een uitgebreide bron voor de technische documentatie en hulpmiddelen nodig om de technologieën van de Adobe in uw toepassingen te integreren.
* [Data Workbench Query API](https://marketing.adobe.com/developer/documentation/data-workbench-query-api/c-ins-qry-api)
