---
description: Hier worden gegevens over de locatie van de bezoeker weergegeven. GeoSegmentation-rapporten omvatten Landen, Regio's, Steden, Staten van de V.S., en DMA van de V.S. (digitaal marketing gebied). GeoSegmentation-rapporten worden voor alle klanten ingeschakeld.
title: GeoSegmentation
topic: Reports
uuid: 66aa22c4-dcbc-491a-b23c-0c3d87444d23
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# GeoSegmentation

Hier worden gegevens over de locatie van de bezoeker weergegeven. GeoSegmentation-rapporten omvatten Landen, Regio&#39;s, Steden, Staten van de V.S., en DMA van de V.S. (digitaal marketing gebied). GeoSegmentation-rapporten worden voor alle klanten ingeschakeld.

Alle metriek die elders aan u in Rapporten &amp; Analytics beschikbaar zijn zijn automatisch inbegrepen in de Landen, de Regio&#39;s, Steden, de Staten van de V.S., en DMA- rapporten: conversie- en op bezoeken gebaseerde meetgegevens en berekende meetwaarden. Zie dit [blogbericht](https://blogs.adobe.com/digitalmarketing/analytics/introducing-new-metrics-in-geosegmentation-and-more/) van Adobe voor meer informatie.

<table id="table_566CFFC82E1149D8BAFE6641627FCF1F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Rapport </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Landen </td> 
   <td colname="col2"> <p> De grootste geografische divisie. Naast de standaard Rangschikte en Gedetailleerde meningen beschikbaar op de meeste rapporten, is er ook een mening van de Kaart die de landen volgens hun relatieve bijdrage aan uw totale verkeer kleuren-codeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Regio's </td> 
   <td colname="col2"> <p> Een geografisch gebied dat kleiner is dan een land maar groter dan een stad. In sommige landen is een regio een staat, provincie of prefectuur. In andere gebieden is het een deelland, afdeling of metropolitane regio. Rechts van elke getoonde regio wordt ook het land van de regio tussen haakjes weergegeven. </p> <p>Klik in de tabeldetails op Een stadsrapport voor dit gebied (het vergrootglas) uitvoeren om een rapport uit te voeren waarin wordt aangegeven hoe de steden in een geselecteerde regio hebben gepresteerd ten opzichte van andere steden in de regio. </p> <p>Zie <a href="/help/components/c-variables/dimensionslist/reports-geosegmentation-reference.md"  > GeoSegmentation Regions and Postcode usage by Country</a> om te zien welke landen regio's gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plaatsen </td> 
   <td colname="col2"> <p> De kleinste geografische indeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Amerikaanse staten </td> 
   <td colname="col2"> <p> Een warmtekaart waarop bezoekers van elke staat van de Verenigde Staten worden getoond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> U.S. DMA </td> 
   <td colname="col2"> <p> (Digitaal marketinggebied) Afdelingen van de mediamarkt voor radio en televisie in de Verenigde Staten. U kunt het rapport filteren zodat alleen marketinggebieden in een bepaalde status worden weergegeven. Deze gegevens worden verstrekt via een partnerschap tussen Adobe en Nielsen Media Research, Inc. </p> <p>Opmerking:  Het niet gespecificeerde punt in het rapport van DMA van de V.S. wijst op bezoekers die niet met een specifieke DMA konden worden geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nauwkeurigheid van rapport </td> 
   <td colname="col2"> <p>Adobe heeft samengewerkt met Digital Envoy, een toonaangevende leverancier van IP-oplossingen voor intelligentie en verificatie, om GeoSegmentation aan te bieden, een geografische meetmogelijkheid die is gebaseerd op IP-adressen van eindgebruikers. Hoewel de nauwkeurigheid op basis van individuele gegevenssets kan variëren, biedt Digital Envoy doorgaans meer dan 99% nauwkeurigheid op landniveau, meer dan 97% nauwkeurigheid op regionaal niveau en meer dan 90% nauwkeurigheid op stadsniveau. </p> <p>Opmerking: Deze aantallen veronderstellen dat <a href="/help/admin/admin/general-acct-settings-admin.md">het plaatsen</a> om het laatste octet van het IP adres te verwijderen NIET wordt toegelaten. </p> <p>IP de adressen worden in kaart gebracht aan postcodes, en elke stad wordt bepaald door de postcodes die de "lokale autoriteit"als deel van die stad bepaalt. Zo vallen de voorsteden van Berlijn niet onder de definitie van Berlijn, maar wordt elke stad afzonderlijk vermeld, ervan uitgaande dat de IP-adressen nauwkeurig kunnen worden toegewezen aan een postcode in een van deze steden. </p> <p>Enkele factoren die invloed kunnen hebben op GeoSegmentation-gegevens zijn: </p> 
    <ul id="ul_1B05024AD5174232A8DB8145753FB09B"> 
     <li id="li_C3A21E7C1186490EB9A236634DB45E7F">IP adressen die collectieve volmachten vertegenwoordigen. Deze kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat eigenlijk een verschillende plaats kan zijn als de gebruiker ver werkt. </li> 
     <li id="li_56FC36B3598C420F9246D4E8772822A7">Mobiele IP-adressen. Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale POPs. </li> 
     <li id="li_C1EED854AE584489BCBC2A7AA20B8EF1">IP adressen die tot gebruikers van satelliet ISPs behoren. Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de locatie van de uplink afkomstig lijken te zijn. </li> 
     <li id="li_A735756F39554DF19E05D251CA614F02">IP's van militaire en overheidsinstellingen. Vaak gaat het hier om personeel dat over de hele wereld reist en dat door zijn thuislocatie komt, in plaats van de basis of het kantoor waar ze momenteel zijn gestationeerd. </li> 
     <li id="li_ACFF1B8094684173B8325A44304CA32B">Onze GeoSegmentation/IP-gegevens worden door een externe leverancier verstrekt en worden regelmatig bijgewerkt op basis van informatie die door ISP's en andere netwerkbronnen wordt verstrekt. IP raadplegingen zijn inherent volatiel, omdat zij over de hele wereld worden gekocht en verkocht. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

