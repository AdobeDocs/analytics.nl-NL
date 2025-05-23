---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Bouw een rapport voor een verzoek van de Data Warehouse
feature: Data Warehouse
exl-id: 34e84e39-e3b1-4184-898a-3fd222ff4d38
source-git-commit: 6a7bbf5103eb6e7f8a3738d27d1fbb189d951a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Bouw een rapport voor een verzoek van de Data Warehouse

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om een rapport voor het verzoek te bouwen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [ een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

Om een rapport voor een verzoek van de Data Warehouse te bouwen:

1. Als u niet reeds hebt, begin creërend een verzoek in Adobe Analytics door te selecteren **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [ een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe pagina van het de verzoekverzoek van de Data Warehouse, selecteer [!UICONTROL **Bouw uw rapport**] tabel.

   ![ bouwt rapportlusje ](assets/build-report.png)

1. Kies in de linkerbovenhoek de rapportsuite die u wilt gebruiken bij het samenstellen van het rapport van de Data Warehouse.

   Niet zijn alle segmenten die in de Bouwer van het Segment worden gecreeerd compatibel met Data Warehouse. Er wordt een fout weergegeven als u een virtuele rapportsuite met incompatibele segmenten kiest.

   Voor een lijst van gesteunde functies binnen een segment, zie {de verenigbaarheid van het 0} Data Warehouse segment [&#128279;](/help/components/segmentation/seg-reference/seg-compatibility.md).

1. Sleep om het even welke segmenten, metriek, en afmetingen in de bouwer. Het rapport u bouwt bepaalt welke gegevens in het verzoek van de Data Warehouse inbegrepen zijn.

1. Ga verder het vormen van uw verzoek van de Data Warehouse op het [!UICONTROL **doel van het Rapport**] lusje. Voor meer informatie, zie [ een rapportbestemming voor een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) vormen.

<!--

Keep any of this? It was in the Overview article:

The following table describes the fields and options on the [!UICONTROL Data Warehouse Request] tab.

<table id="table_7325A2466866460E8B0AF7D696152713"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Request Name</span> </td> 
   <td colname="col2"> Identifies the request. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Reporting Date</span> </td> 
   <td colname="col2"> <p>The date and granularity of the request. </p> 
    <ul id="ul_C00F4529BD9E4113B517A61751B1DD5C"> 
     <li id="li_4D7C26812DF94ED7B64F985309541F46"> <span class="wintitle"> Custom</span>: A date range you configure in the calendar. </li> 
     <li id="li_2B272087006847148A936350D1B2D523"> <span class="wintitle"> Preset</span>: A preset range. The preset range is relative to the report date. </li> 
     <li id="li_745989965BB94D489FF7046587E13C42"> <span class="wintitle"> Granularity</span>: The time granularity. Valid values are None, Hour, Day, Week, Month, Quarter, and Year. </li> 
    </ul> <p>Data Warehouse reporting on virtual report suites supports the alternative time zone configured on the virtual report suite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Available Segments</span> </td> 
   <td colname="col2"> <p>Lets you select the part of the visitor population you want to examine and generate complex segments. You can load pre-configured segments, create new segments, and store segment components in a library to use in building additional segments. </p> <p>You can now stack segments. When selecting multiple segments, the preview area, the Request Manager, and the Request Detail popup show a comma-separated list of names (e.g., Segment1, Segment2). </p> <p>See the <a href="/help/components/segmentation/seg-home.md"> Segmentation Guide</a> for more information. </p> <p>Note:  You cannot include both a segment filter and a breakdown on the same segment, in the same Data Warehouse report. Doing so will result in an error. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Breakdowns</span> </td> 
   <td colname="col2"> <p>Lets you categorize data using breakdowns. Segments and breakdowns differ in that a segment filters data out of a data set, while a breakdown compartmentalizes data across all valid values for the breakdown. </p> You can also break down a report by one or more segments. However, you cannot include both a segment filter and a breakdown on the same segment, in the same Data Warehouse report. Doing so will result in an error. <p> For example, use segments to remove a gender from the data set, and use a breakdown to see data separated by gender. </p> <p>When a Data Warehouse request is submitted with multiple multi-value dimensions (e.g., various Mobile Reports), an exponential number of rows can be generated from a single hit. The number of rows that can be output from a single hit is capped at 100 (previously 1,000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Metrics</span> </td> 
   <td colname="col2">Lets you add metrics that you want to report on. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Metrics Sort</span> </td> 
   <td colname="col2">Provides ranked breakdown reports, sorted by descending metric value, similar to what is displayed in the Reports &amp; Analytics user interface, Data Workbench, etc. <a href="/help/export/data-warehouse/sorting-by-metric.md"  > More...</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Schedule Delivery</span> </td> 
   <td colname="col2"> <p>Lets you schedule requests for automatic delivery at selected intervals, or as a one-time report. If you use the default format, the report arrives in an email as a .csv file. </p> <p>To add the date range, include <span class="filepath"> %R</span> in the filename. This value represents the date values requested in the report. For example, if you request data from May 1, 2013 through May 7, 2013, the <span class="filepath"> %R</span> shows a filename including the date range of 20130501 - 20130507. </p> </td> 
  </tr> 
 </tbody> 
</table>

-->
