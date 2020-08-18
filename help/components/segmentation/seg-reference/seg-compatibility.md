---
description: Niet zijn alle segmenten die in de Bouwer van het Segment worden gecreeerd compatibel met Data Warehouse. In deze tabel worden de ondersteunde functies weergegeven.
title: Compatibiliteit van Data Warehouse-segmenten
topic: Segments
uuid: 370258c5-8614-4434-871c-41753ed77f5c
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---


# Compatibiliteit van Data Warehouse-segmenten

Niet alle segmenten die in de Segment Builder zijn gemaakt, zijn compatibel met [!DNL Data Warehouse]. In deze tabel worden de ondersteunde functies weergegeven.

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
   <td > <b>Container uitsluiten</b> </td> 
   <td> Ondersteund op elk niveau </td> 
   <td> Alleen in speciale gevallen op het hoogste niveau ondersteund </td> 
  </tr> 
  <tr> 
   <td> <b>Sequentiële segmenten</b> </td> 
   <td> Ondersteund </td> 
   <td> Niet ondersteund </td> 
  </tr> 
  <tr> 
   <td> <b>AND en OR kunnen zonder grenzen worden gecombineerd</b> </td> 
   <td> Ondersteund </td> 
   <td> Enkele beperkingen. Zie *opmerking* onder tabel. </td> 
  </tr> 
  <tr> 
   <td> <b>Geneste containers</b> </td> 
   <td> Ondersteund </td> 
   <td> Sommige beperkingen (ze moeten het bereik verkleinen, bijvoorbeeld bezoekers kunnen hits bevatten, maar niet andersom) </td> 
  </tr> 
  <tr> 
   <td> <b>Dimensies</b> </td> 
   <td>Sleep een dimensie naar het veld <span class="uicontrol"> Definities</span> van Segment Builder om meer te weten te komen over de productcompatibiliteit. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Analysis Workspace, Reports &amp; Analytics en Ad Hoc Analysis: 
    <ul> 
     <li>Entry-server </li> 
     <li>Invoercategorie </li> 
     <li>Invoerdatum </li> 
     <li>Alle zoekpaginanummers </li> 
    </ul> </td> 
   <td> Sleep een dimensie naar het veld <span class="uicontrol"> Definities</span> van Segment Builder om meer te weten te komen over de productcompatibiliteit. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Data Warehouse: 
    <ul> 
     <li>IP-adres </li> 
     <li>Pagina-URL </li> 
     <li>Bezoekers-id </li> 
     <li>Experience Cloud-bezoeker-id </li> 
    </ul> <p>De volgende afmetingen <b>kunnen niet in de segmenten van de Data Warehouse </b>worden gebruikt: </p> 
    <ul> 
     <li>Alle zoekpaginanummers </li> 
     <li>AM/PM </li> 
     <li>Dag van Maand </li> 
     <li>Weekdag </li> 
     <li>Dag van het Jaar </li> 
     <li>Zakelijke eenheid voor toegang </li> 
     <li>Item (alle Dimension die beginnen met Invoer, behalve Itempagina) </li> 
     <li>Afsluiten (alle Dimension die beginnen met Afsluiten, behalve Koppeling afsluiten en Pagina afsluiten) </li> 
     <li>Hiërarchie (alle Dimension beginnen met hiërarchie) </li> 
     <li>Hit Depth </li> 
     <li>Type hit </li> 
     <li>Uur Dag </li> 
     <li>Maand van jaar </li> 
     <li>Pagina's niet gevonden </li> 
     <li>Betaalde zoekopdracht </li> 
     <li>Kwartaal van jaar </li> 
     <li>Retourfrequentie </li> 
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
   <td> Ondersteund </td> 
  </tr>
  <tr>
    <td><b>Gelijk aan alle operatoren 'gelijk aan' en 'gelijk aan geen van de operatoren'</b></td>
    <td>Ondersteund</td>
    <td>Niet ondersteund</td>
  </tr>
 </tbody> 
</table>

*Opmerking: Data Warehouse biedt geen ondersteuning voor alle gevallen waarin een`exclusion`of een`without`container wordt gebruikt`AND/OR`. Wanneer u een dergelijke combinatie gebruikt, worden alleen de segmenten die als`A AND NOT B`herschreven kunnen worden (of deze eigenschap ****opnemen en deze eigenschap **uitsluiten**) ondersteund in de Data Warehouse.*
