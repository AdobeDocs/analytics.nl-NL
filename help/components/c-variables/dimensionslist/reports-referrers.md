---
description: Geeft het domein of de URL weer van waar uw bezoekers vandaan kwamen voordat ze bij uw site aankwamen, de methoden die bezoekers gebruiken om uw website te zoeken, en het aantal bezoeken aan uw site dat afkomstig was van deze verwijzingslocaties.
title: Referenties
topic: Reports
uuid: e63b47b4-49f3-43af-8409-3272bec0484e
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Referenties

Geeft het domein of de URL weer van waar uw bezoekers vandaan kwamen voordat ze bij uw site aankwamen, de methoden die bezoekers gebruiken om uw website te zoeken, en het aantal bezoeken aan uw site dat afkomstig was van deze verwijzingslocaties.

Als een bezoeker bijvoorbeeld op een koppeling van Site A klikt en op uw site arriveert, is Site A de referentie als deze niet als onderdeel van uw domein is gedefinieerd. Tijdens de implementatie kan uw implementatieconsultant u helpen de domeinen en URL&#39;s te definiëren die deel uitmaken van uw website. (Deze wijziging kan na de implementatie worden uitgevoerd.)

Domeinen of URL&#39;s die geen deel uitmaken van die gedefinieerde domeinen en URL&#39;s, worden als referentie beschouwd. Webpagina A en webpagina B worden bijvoorbeeld toegevoegd aan het interne URL-filter, maar webpagina C niet. In dit geval wordt webpagina C beschouwd als een referentie.

## Toewijzing, verlopen en speciale waarden {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketingrapporten en -analyses (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad-hocanalyse </th> 
   <th colname="col4" class="entry"> Gegevenspakhuis </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Metrische toewijzing </td> 
   <td colname="col2"> Recentste </td> 
   <td colname="col3"> Recentste </td> 
   <td colname="col4"> Recentste </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waarden vervallen na </td> 
   <td colname="col2"> Bezoek </td> 
   <td colname="col3"> Bezoek </td> 
   <td colname="col4"> Bezoek </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waardelimieten </td> 
   <td colname="col2"> Geen limieten (kan in een toekomstige release veranderen) </td> 
   <td colname="col3"> Geen limieten (kan in een toekomstige release veranderen) </td> 
   <td colname="col4"> none </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Speciale waarden </td> 
   <td colname="col2"> <p>"Geen": totalen voor de hele site die tijdens het bezoek geen referentie hadden. </p> </td> 
   <td colname="col3"> <p>"Geen": totalen voor de hele site die tijdens het bezoek geen referentie hadden. </p> </td> 
   <td colname="col4"> <p> Leeg - equivalent van "Geen", totalen voor de hele site die tijdens het bezoek geen referentie hadden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Notities {#section_B83A3571D64E4E7792712FAF740D7955}

* Het verwijzende, verwijzende type, en verwijzende domein worden geplaatst bij de eerste klap van het bezoek, of tijdens een bezoek wanneer de verwijzende (bijvoorbeeld, als een bezoeker uw plaats verlaat, een onderzoeksmotor gebruikt, dan aan uw plaats terugkeert alvorens het eerste bezoek verloopt). Deze waarden worden tegelijkertijd ingesteld en blijven tijdens het bezoek behouden.
* Interne URL&#39;s worden gefilterd. Dit rapport bevat alleen verwijzingen die niet overeenkomen met de interne URL-filters.
* De overeenkomstige metrische waarde wordt ReferrerInstance genoemd in ad hoc analyse.
* Getypte/bladwijzerwaarden worden niet opgenomen in het rapport Referenties. Dit betekent dat bezoeken voor de hele site niet overeenkomen met bezoeken voor dit rapport.

## Rapportgeschiedenis {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

<table id="table_9DFA79EC6A5A48648F2FB5418E1752DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Wijzigen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1/16/2014 </td> 
   <td colname="col2"> Het pakhuis van gegevens werd bijgewerkt om de logica aan te passen die door marketing rapporten &amp; analyses wordt gebruikt. Vóór deze datum zijn de zoektrefwoorden tijdens het bezoek niet meer aanwezig. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6/19/2012 </td> 
   <td colname="col2"> <p> Vóór juli 2012 omvat "Geen" alle mobiel verkeer, getypt/gemarkeerd als bladwijzer en bezoeken zonder JavaScript. Na juli 2012 bevat "Geen" alleen treffers zonder JavaScript op de eerste pagina van het bezoek. </p> </td> 
  </tr> 
 </tbody> 
</table>

