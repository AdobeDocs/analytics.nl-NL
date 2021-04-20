---
description: Niet zijn alle segmenten die in de Bouwer van het Segment worden gecreeerd compatibel met Data Warehouse. In deze tabel worden de ondersteunde functies weergegeven.
title: Compatibiliteit van Data Warehouse-segmenten
feature: Segmentation
uuid: 370258c5-8614-4434-871c-41753ed77f5c
exl-id: 66b86226-ef4c-4a1a-abe1-3c3accf419e5
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 6%

---

# Compatibiliteit van Data Warehouse-segmenten

Niet alle segmenten die in de Segment Builder zijn gemaakt, zijn compatibel met [!DNL Data Warehouse]. In deze tabel worden de ondersteunde functies weergegeven.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Analysis Workspace, rapporten en analyses </th> 
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
   <td>Sleep en laat vallen een afmeting in <span class="uicontrol"> Definities </span> gebied van de Bouwer van het Segment om over zijn productverenigbaarheid te weten te komen. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Analysis Workspace, Reports &amp; Analytics: 
    <ul> 
     <li>Entry-server </li> 
     <li>Invoercategorie </li> 
     <li>Invoerdatum </li> 
     <li>Alle zoekpaginanummers </li> 
    </ul> </td> 
   <td> Sleep en laat vallen een afmeting in <span class="uicontrol"> Definities </span> gebied van de Bouwer van het Segment om over zijn productverenigbaarheid te weten te komen. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Data Warehouse: 
    <ul> 
     <li>IP-adres </li> 
     <li>Pagina-URL </li> 
     <li>Bezoekers-id </li> 
     <li>Experience Cloud-bezoeker-id </li> 
    </ul> <p>De volgende afmetingen <b>kunnen niet </b>worden gebruikt in Data Warehouse segmenten: </p> 
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

*Opmerking: Data Warehouse biedt geen ondersteuning voor alle gevallen waarin een  `exclusion` of een  `without` container wordt gebruikt  `AND/OR`. Wanneer u een dergelijke combinatie gebruikt, worden alleen de segmenten die opnieuw kunnen worden geschreven als `A AND NOT B` (of **deze eigenschap opnemen**en **dit kenmerk uitsluiten**) ondersteund in de Data Warehouse.*
