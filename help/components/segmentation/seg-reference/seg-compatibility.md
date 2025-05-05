---
description: Niet zijn alle segmenten die in de Bouwer van het Segment worden gecreeerd compatibel met Data Warehouse. In deze tabel worden de ondersteunde functies weergegeven.
title: Compatibiliteit van Data Warehouse-segmenten
feature: Segmentation
exl-id: 66b86226-ef4c-4a1a-abe1-3c3accf419e5
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '342'
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
   <td>Sleep een dimensie naar de Segment Builder <span class="uicontrol"> Definities</span> voor meer informatie over de compatibiliteit van producten. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Analysis Workspace, Reports &amp; Analytics: 
    <ul> 
     <li>Entry-server </li> 
     <li>Invoercategorie </li> 
     <li>Invoerdatum </li> 
     <li>Alle zoekpaginanummers </li> 
    </ul> </td> 
   <td> Sleep een dimensie naar de Segment Builder <span class="uicontrol"> Definities</span> voor meer informatie over de compatibiliteit van producten. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Data Warehouse: 
    <ul> 
     <li>IP-adres </li> 
     <li>Pagina-URL </li> 
     <li>Bezoekers-id </li> 
     <li>Experience Cloud-bezoeker-id </li> 
    </ul> <p>De volgende afmetingen <b>kan </b>worden gebruikt in Data Warehouse-segmenten: </p> 
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

*Opmerking: Data Warehouse ondersteunt niet alle gevallen van het gebruik van een `exclusion` of `without` container gebruiken `AND/OR`. Wanneer het gebruiken van zulk een combinatie, slechts die segmenten die kunnen worden herschreven zoals `A AND NOT B`, (of **dit kenmerk**&#x200B;en **deze eigenschap uitsluiten**) worden ondersteund in Data Warehouse.*
