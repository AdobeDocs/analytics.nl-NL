---
description: Voert de pagina's op uw plaats opnieuw samen die op de pagina's wordt gebaseerd die het meeste verkeer ontvangen. Als uw bedrijfsvraag kwantitatieve gegevens voor pagina's behandelt, kunt u dit rapport gebruiken om die vraag te beantwoorden, door de juiste metriek toe te voegen.
title: Pagina's
topic: Reports
uuid: 6435e262-e734-4c15-af5b-173799d5cc43
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Pagina&#39;s

Voert de pagina&#39;s op uw plaats opnieuw samen die op de pagina&#39;s wordt gebaseerd die het meeste verkeer ontvangen. Als uw bedrijfsvraag kwantitatieve gegevens voor pagina&#39;s behandelt, kunt u dit rapport gebruiken om die vraag te beantwoorden, door de juiste metriek toe te voegen.

## Toewijzing, verlopen en speciale waarden {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

Merk op dat in Rapporten &amp; Analytics, de metriek op het Rapport van Pagina&#39;s lineaire toewijzing gebruikt. Zo worden de inkomsten gesplitst tussen alle pagina&#39;s die vóór een aankoopgebeurtenis zijn weergegeven. Dit kan verwarring veroorzaken voor sommige metriek die u zou kunnen verwachten om slechts op één pagina voor te komen, zoals een het winkelwagentje toevoeging.

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry">Rapporten &amp; <p>Analyse </p> </th> 
   <th colname="col3" class="entry"> Ad hoc-analyse </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
   <th colname="col5" class="entry"> Werkruimte Analyse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Metrische toewijzing </td> 
   <td colname="col2"> Lineair </td> 
   <td colname="col3"> Toewijzing is specifiek voor elke dimensie. De standaardinstelling is Last Touch-toewijzing, maar de dimensie 'pagename' vormt een uitzondering. Als u een aangepaste gebeurtenis toepast op 'pagename', is dit de exacte toewijzing voor Actief. </td> 
   <td colname="col4"> <p>Waarden ingesteld op dezelfde paginaweergave </p> </td> 
   <td colname="col5"> <p>Waarden ingesteld op dezelfde paginaweergave </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waarden vervallen na </td> 
   <td colname="col2"> Paginaweergave </td> 
   <td colname="col3"> Paginaweergave </td> 
   <td colname="col4"> Paginaweergave </td> 
   <td colname="col5"> Paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waardelimieten </td> 
   <td colname="col2"> <p>Eerste unieke 500 k per maand + nieuwe waarden met verkeer </p> </td> 
   <td colname="col3"> <p>Eerste unieke 500 k per maand + nieuwe waarden met verkeer </p> </td> 
   <td colname="col4"> Geen </td> 
   <td colname="col5"> <p>Eerste unieke 500 k per maand + nieuwe waarden met verkeer </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Speciale waarden </td> 
   <td colname="col2"> <p>(laag-verkeer) vertegenwoordigt waarden voorbij eerste 500k die niet genoeg verkeer hebben ontvangen om te worden gemeld. </p> </td> 
   <td colname="col3"> <p>(laag-verkeer) vertegenwoordigt waarden voorbij eerste 500k die niet genoeg verkeer hebben ontvangen om te worden gemeld. </p> </td> 
   <td colname="col4"> none </td> 
   <td colname="col5"> <p>(laag-verkeer) vertegenwoordigt waarden voorbij eerste 500k die niet genoeg verkeer hebben ontvangen om te worden gemeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Als u in Rapporten &amp; Analytics een aangepaste gebeurtenis als metrisch toepast in een rapport Pagina&#39;s, wordt lineaire toewijzing toegepast.

Dit betekent dat zelfs als de gebeurtenis met een s.tl () vraag werd verzonden, het de lineaire toewijzing van om het even welke vorige s.t () vraag zal krijgen. Voorbeeld:

| Paginanaam | Page_event | Gebeurtenissen |
|---|---|---|
| Page1 | **s.t()** |  |
| Page1 | s.tl() | Event1 |
| Page1 | s.tl() | Event1 |
| Page1 | s.tl() | Event1 |
| Page2 | **s.t()** |  |
| Page2 | **s.t()** |  |
| Page2 | s.tl() | Event1 |

Voor dit scenario krijgen we de volgende toewijzing in het verslag Pagina&#39;s:

| Pagina&#39;s | Pageviews | Gebeurtenis 1 |
|---|---|---|
| Pagina 1 | 1 | 1+1+1+1/3 = 3.33 |
| Pagina 2 | 2 | 2/3 = 0.67 |

Zelfs als de gebeurtenis op een s.tl vraag wordt verzonden, zal de pagina die voorafgaand aan de gebeurtenis wordt bekeken die (s.t () vraag) werd verzonden gedeeltelijke krediet krijgen.

## Notities {#section_47B0F4746D4847AC9E8697127063F4D0}

* Als er geen paginanaam bestaat, wordt de URL gebruikt.
* Als u een hit hebt zonder paginanaam, pagina-URL of gebeurtenislijst (geen handelsgebeurtenis), wordt de hit uitgesloten.
* Onderverdelingen op pagina&#39;s geven alle pagina&#39;s weer waarvoor een waarde behouden bleef.

