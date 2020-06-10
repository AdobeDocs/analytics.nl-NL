---
description: Not all segments created in the Segment Builder are compatible with Data Warehouse. This table lists the supported functions.
title: Data Warehouse Segment Compatibility
topic: Segments
uuid: 370258c5-8614-4434-871c-41753ed77f5c
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# Data Warehouse Segment Compatibility

Not all segments created in the Segment Builder are compatible with [!DNL Data Warehouse]. This table lists the supported functions.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis </th> 
   <th> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td > <b>Exclude container</b> </td> 
   <td> Supported at any level </td> 
   <td> Supported only in special cases at the top level </td> 
  </tr> 
  <tr> 
   <td> <b>Sequential segments</b> </td> 
   <td> Supported </td> 
   <td> Niet ondersteund </td> 
  </tr> 
  <tr> 
   <td> <b>AND and OR can be combined without limits</b> </td> 
   <td> Supported </td> 
   <td> Some limitations. See *note* below table. </td> 
  </tr> 
  <tr> 
   <td> <b>Nested containers</b> </td> 
   <td> Supported </td> 
   <td> Sommige beperkingen (ze moeten het bereik verkleinen, bijvoorbeeld bezoekers kunnen hits bevatten, maar niet andersom) </td> 
  </tr> 
  <tr> 
   <td> <b>Dimensies</b> </td> 
   <td>Sleep een dimensie naar het veld <span class="uicontrol"> Definities</span> van Segment Builder om meer te weten te komen over de productcompatibiliteit. Deze dimensies worden bijvoorbeeld alleen ondersteund in Analysatiewerkruimte, Rapporten en Analyse en Ad hoc-analyse: 
    <ul> 
     <li>Entry Server </li> 
     <li>Entry Category </li> 
     <li>Entry Date </li> 
     <li>Alle zoekpaginanummers </li> 
    </ul> </td> 
   <td> Drag and drop a dimension into the Segment Builder's <span class="uicontrol"> Definitions</span> field to find out about its product compatibility. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Data Warehouse: 
    <ul> 
     <li>IP-adres </li> 
     <li>Pagina-URL </li> 
     <li>Bezoeker-id </li> 
     <li>Experience Cloud Visitor ID </li> 
    </ul> <p>De volgende afmetingen <b>kunnen niet in de segmenten van het Pakhuis van Gegevens </b>worden gebruikt: </p> 
    <ul> 
     <li>Alle zoekpaginanummers </li> 
     <li>AM/PM </li> 
     <li>Dag van Maand </li> 
     <li>Weekdag </li> 
     <li>Dag van het Jaar </li> 
     <li>Zakelijke eenheid voor toegang </li> 
     <li>Item (alle afmetingen beginnen met item, behalve invoerpagina) </li> 
     <li>Afsluiten (alle afmetingen die beginnen met Afsluiten, behalve Koppeling afsluiten en Pagina afsluiten) </li> 
     <li>Hiërarchie (alle afmetingen beginnen met hiërarchie) </li> 
     <li>Hit Depth </li> 
     <li>Type hit </li> 
     <li>Uur Dag </li> 
     <li>Maand van jaar </li> 
     <li>Pagina's niet gevonden </li> 
     <li>Betaalde zoekopdracht </li> 
     <li>Kwartaal van jaar </li> 
     <li>Geretourneerde frequentie </li> 
     <li>Bezoeken van één pagina </li> 
     <li>Tijd voorafgaand aan gebeurtenis </li> 
     <li>Tijd besteed op pagina - Emmerd </li> 
     <li>Tijd besteed per bezoek - Emmerd </li> 
     <li>Reden voor reeksspatiëring </li> 
     <li>VS </li> 
     <li>Weekdag/Weekend </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <b>Segmentstapeling</b> </td> 
   <td> Ondersteund </td> 
   <td> Niet ondersteund </td> 
  </tr>
  <tr>
    <td><b>Gelijk aan alle operatoren 'gelijk aan' en 'gelijk aan geen van de operatoren'</b></td>
    <td>Ondersteund</td>
    <td>Niet ondersteund</td>
  </tr>
 </tbody> 
</table>

*Opmerking: Data Warehouse biedt geen ondersteuning voor alle gevallen waarin een`exclusion`of een`without`container wordt gebruikt`AND/OR`. Wanneer het gebruiken van een dergelijke combinatie, slechts die segmenten die als`A AND NOT B`, (of **omvat dit kenmerk**en **sluit dit kenmerk**uit) kunnen worden herschreven worden gesteund in het Pakhuis van Gegevens.*
