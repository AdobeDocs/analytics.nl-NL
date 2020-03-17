---
description: Adobe Analytics en Adobe Audience Manager bevatten statistieken voor bezoekers met vergelijkbare definities die om verschillende redenen niet voor 100% zijn uitgelijnd.
title: Verschillen in aantal bezoekers
uuid: c3bbb887-bd02-4c1c-9a2b-64811c0ef56a
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Verschillen in aantal bezoekers

Adobe Analytics en Adobe Audience Manager bevatten statistieken voor bezoekers met vergelijkbare definities die om verschillende redenen niet voor 100% zijn uitgelijnd.

De cijfers voor de bezoeker zijn:

<table id="table_F9FE107A89934C3B854C55D7D76AC6E8"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Metrisch </th> 
   <th colname="col3" class="entry"> Definitie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html"  > AAM: Totale segmentpopulatie</a> </p> </td> 
   <td colname="col3"> <p>Aantal apparaten (de Identiteitskaart van de Wolk van de Ervaring) die een lid van uw segment tijdens de raadplegingsperiode waren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html"  > AAM: Realtime segmentpopulatie</a> </p> </td> 
   <td colname="col3"> <p>Aantal apparaten (geledingen van de Wolk van de Ervaring) die een lid van uw segment waren en uw eigenschappen tijdens de raadplegingsperiode bereikten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analyse: Unieke bezoekers </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u het aantal unieke bezoekers weer dat uw eigenschappen tijdens het rapportvenster heeft bereikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analyse: Bezoekers met Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u het aantal unieke bezoekers met een Experience Cloud-id weer die uw eigenschappen hebben bereikt tijdens het rapportagevenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

De Bezoekers van het segment van AAM in real time Bevolking en van Analytics met de identiteitskaart van de Wolk van de Ervaring die binnen de rapportering van de Analytics van het Publiek wordt gebruikt zal het meest gelijkaardig zijn. Op korte termijn zullen er echter, vanwege verschillende factoren, kleine verschillen tussen deze factoren zijn. Bijdragende factoren zijn:

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Factor </th> 
   <th colname="col2" class="entry"> AAM: Realtime segmentpopulatie </th> 
   <th colname="col3" class="entry"> Analyse: Bezoekers met Experience Cloud ID </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tijdzone </p> </td> 
   <td colname="col2"> <p>UTC (Coordinated Universal Time) </p> </td> 
   <td colname="col3"> <p>Opgegeven per rapportsuite </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste filters </p> </td> 
   <td colname="col2"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Ja, bijvoorbeeld IP-filters, beide filters </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limiet voor 150 segmenten </p> </td> 
   <td colname="col2"> <p>Nee </p> </td> 
   <td colname="col3"> <p>Ja - Het aantal analytische gegevens kan tot 5% worden beïnvloed door de integratielimiet van 150 segmenten. De "grens van het publiek bereikte"zal in de dimensie van de Naam van het publiek verschijnen als de beknotting is voorgekomen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie Segmenten [begrijpen in Analytics en Audience Manager](/help/integrate/c-audience-analytics/aam-analytics-segments.md) voor meer uitleg over de nuances tussen de gegevens en segmentatie van Analytics en Audience Manager.
