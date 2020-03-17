---
description: De metriek worden berekend gebruikend norm, participatie, recente, en lineaire toewijzingsmethodes. Elke methode berekent waarden op basis van formules.
title: Metrische berekeningen
topic: Metrics
uuid: 2af58f1e-12c5-4828-ae39-c9aeaef6b705
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Metrische berekeningen

De metriek worden berekend gebruikend norm, participatie, recente, en lineaire toewijzingsmethodes. Elke methode berekent waarden op basis van formules.

<table id="table_6F81A12174D84124B7FD81FBBEDF18A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Metrische berekening </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Origineel </td> 
   <td colname="col2"> <p>De eerste variabele die aan de succesgebeurtenis is gekoppeld, krijgt een volledig krediet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recent </td> 
   <td colname="col2"> <p>De laatste variabele die aan de succesgebeurtenis is gekoppeld, wordt volledig vergoed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lineair </td> 
   <td colname="col2"> <p>Wanneer lineaire toewijzing is geselecteerd, worden succesgebeurtenissen gelijkmatig verdeeld over alle variabelewaarden die tijdens het bezoek worden gezien. Voor numerieke gebeurtenissen en gebeurtenissen in valuta zoals <span class="term"> Inkomsten</span>, wordt het monetaire bedrag gedeeld. Voor tegengebeurtenissen zoals <span class="term"> Orders</span>, wordt een fractie van de gebeurtenis toegekend aan elke veranderlijke waarde in het bezoek. Deze breuken in de rapportage worden opgeteld en vervolgens afgerond naar het dichtstbijzijnde gehele getal in de rapportage. </p> <p>Als bijvoorbeeld vier pagina's worden bezocht voordat een geslaagde gebeurtenis plaatsvindt, krijgt elke pagina een krediet voor 25% van de gebeurtenis. Als tijdens hetzelfde bezoek twee waarden voor de <span class="varname"> campagne</span> zouden worden gebruikt, zou elke campagnewaarde 50% van de kredieten voor het evenement ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Deelname </td> 
   <td colname="col2"> <p>Wijst volledig krediet aan elke veranderlijke waarde toe die tot een succesgebeurtenis binnen een bezoek bijdroeg. Deze berekening kan ook van toepassing zijn op bezoekerssessies, als u statistieken voor deelname tussen bezoekers gebruikt. </p> <p>Zie <a href="/help/components/c-variables/c-metrics/metrics-participation.md"  > Deelname</a> voor meer informatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld - Metrische berekening {#section_4CE01DA35108418D9909823A7ECC4B45}

Stel dat uw site een interne zoekopdracht heeft die wordt bijgehouden met behulp van een conversievariabele (eVar). De bezoeker voert verschillende interne zoekopdrachten uit voordat hij een aankoop van $100 doet:

*`Pet`* > *`Feline`* > *`Cat`* > *`Kitten`* > Aankoop $100

Bij de rapportage is de krediettoewijzing als volgt:

<table id="table_91A7244E77854838A8392B49366FB445"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar-waarde </th> 
   <th colname="col2" class="entry"> Eerste </th> 
   <th colname="col3" class="entry"> Laatste </th> 
   <th colname="col4" class="entry"> Lineair </th> 
   <th colname="col5" class="entry"> Deelname </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Huisdier </p> </td> 
   <td colname="col2"> <p>$100 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feline </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kat </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kitten </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$100 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
 </tbody> 
</table>

