---
description: Er zijn meetgegevens voor bezoekers in Adobe Analytics en Adobe Audience Manager die vergelijkbare definities hebben, maar die om verschillende redenen niet volledig zijn uitgelijnd.
title: Verschillen in aantal bezoekers
feature: Audience Analytics
exl-id: be5a935a-c3a2-4ab4-8cd7-ed54a37932c8
source-git-commit: 15f1cd260709c2ab82d56a545494c31ad86d0ab0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 3%

---

# Verschillen in aantal bezoekers

Er zijn meetgegevens voor bezoekers in Adobe Analytics en Adobe Audience Manager die vergelijkbare definities hebben, maar die om verschillende redenen niet volledig zijn uitgelijnd.

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
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html"  > Adobe Audience Manager: Totale segmentpopulatie</a> </p> </td> 
   <td colname="col3"> <p>Aantal apparaten (Experience Cloud IDs) die een lid van uw segment tijdens de raadplegingsperiode waren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html"  > Adobe Audience Manager: Realtime segmentpopulatie</a> </p> </td> 
   <td colname="col3"> <p>Aantal apparaten (Experience Cloud IDs) die een lid van uw segment waren en uw eigenschappen tijdens de raadplegingsperiode bereikten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analyse: Unieke bezoekers </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u het aantal unieke bezoekers weer dat uw eigenschappen tijdens het rapportvenster heeft bereikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analyse: Bezoekers met Experience Cloud-id </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u het aantal unieke bezoekers met een Experience Cloud-id weer die uw eigenschappen tijdens het rapportvenster hebben bereikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Adobe Audience Manager Real-time segment Population and Analytics Visitors with Experience Cloud ID used within Audience Analytics reporting will be the similar. Op korte termijn zullen er echter, vanwege verschillende factoren, kleine verschillen tussen deze factoren zijn. Bijdragende factoren zijn:

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Factor </th> 
   <th colname="col2" class="entry"> Adobe Audience Manager: Realtime segmentpopulatie </th> 
   <th colname="col3" class="entry"> Analyse: Bezoekers met Experience Cloud-id </th> 
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

Zie [Segmenten begrijpen in Analytics en Audience Manager](/help/integrate/c-audience-analytics/aam-analytics-segments.md) voor aanvullende uitleg over de nuances tussen de gegevens van Analytics en Audience Manager en de segmentatie.
