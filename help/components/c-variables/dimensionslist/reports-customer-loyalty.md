---
description: De Loyalty van de klant onthult aankooppatronen van klanten.
title: Loyalty van klant
topic: Reports
uuid: 7dc30b57-7b18-4228-a6ab-6eb66b3d9402
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Loyalty van klant

De Loyalty van de klant onthult aankooppatronen van klanten.

Het rapport toont aankooppatronen van klanten die op vier categorieën loyaliteit worden gebaseerd:

* Geen klant
* Nieuwe klant
* Klant terugsturen
* Klante

Hoewel niet-aankoopcijfers in dit rapport kunnen worden weergegeven (zoals aangepaste gebeurtenissen, winkelwagenevenementen, enzovoort), zijn de categorieën altijd gebaseerd op het aantal geplaatste bestellingen. Een bezoeker kan bijvoorbeeld een aangepaste gebeurtenis genaamd Interne zoekopdrachten toevoegen aan het rapport. Het [!UICONTROL Return Customer] regelitem geeft het aantal interne zoekopdrachten weer dat bezoekers hebben uitgevoerd die eerder twee aankopen hebben gedaan, niet het aantal bezoekers dat twee interne zoekopdrachten heeft uitgevoerd.

**Loyaliteitsverwerking van klanten**

De volgende lijsten bepalen hoe de Werkruimte van de Analyse, Rapporten &amp; Analyse, Ad hoc Analyse en het Pakhuis van Gegevens momenteel de Loyalty van de Klant verwerken:

<table id="table_E6A5CA96BE5C47F29F09688A4D41BC60"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Na 19 mei 2016 </p> </th> 
   <th colname="col3" class="entry"> <p>Tussen 21 april en 19 mei 2016 </p> <p>(niet van toepassing op Data Warehouse) </p> </th> 
   <th colname="col4" class="entry"> <p>Vóór 21 april 2016 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Geen klant </p> </td> 
   <td colname="col2"> <p>Bezoekers die nog nooit hebben gekocht </p> </td> 
   <td colname="col3"> <p>Bezoekers die tot het einde van een bezoek 0 aankopen hebben gedaan. </p> </td> 
   <td colname="col4"> <p>Niet beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe klant </p> </td> 
   <td colname="col2"> <p>Bezoekers die één aankoop hebben gedaan </p> </td> 
   <td colname="col3"> <p>Bezoekers die 1 aankoop hebben gedaan tot het einde van dat bezoek. </p> <p>(Als er een aankoop is gedaan, is de status van de klant bijgewerkt bij het volgende bezoek na die aankoop.) </p> </td> 
   <td colname="col4"> <p>Bezoekers die tot het einde van dat bezoek 0 aankopen hebben gedaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klant terugsturen </p> </td> 
   <td colname="col2"> <p>Bezoekers die 2 aankopen hebben gedaan </p> </td> 
   <td colname="col3"> <p>Bezoekers die twee aankopen deden tot het einde van het bezoek waar ze de tweede aankoop deden. </p> <p>(Als er een aankoop is gedaan, is de status van de klant bijgewerkt bij het volgende bezoek na die aankoop.) </p> </td> 
   <td colname="col4"> <p>Bezoekers die 1 aankoop hebben gedaan tot het einde van het bezoek waar ze die aankoop hebben gedaan. </p> <p>(Als er een aankoop is gedaan, is de status van de klant bijgewerkt bij het volgende bezoek na die aankoop.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klante </p> </td> 
   <td colname="col2"> <p>Bezoekers die 3+ aankopen hebben gedaan </p> </td> 
   <td colname="col3"> <p>Bezoekers die 3+ aankopen deden tot het einde van het bezoek waar ze de meest recente aankoop deden. </p> <p>(Als er een aankoop is gedaan, is de status van de klant bijgewerkt bij het volgende bezoek na die aankoop.) </p> </td> 
   <td colname="col4"> <p>Bezoekers die meer dan 2 aankopen hebben gedaan tot het einde van het bezoek waar ze de meest recente aankoop hebben gedaan. </p> <p>(Als er een aankoop is gedaan, is de status van de klant bijgewerkt bij het volgende bezoek na die aankoop.) </p> </td> 
  </tr> 
 </tbody> 
</table>

| versie 14 Klantengarantie (huidig) |
|---|
| Nieuwe klant | 1 bezoek en 1 aankoop |
| Klant terugsturen | Meer dan 1 bezoek en 2 aankopen |
| Klante | Meer dan één bezoek en meer dan drie aankopen |

De status van de loyaliteit verandert direct na de aankoopgebeurtenis binnen hetzelfde bezoek. Een nieuwe klant (1 aankoop) doet bijvoorbeeld een aankoop en registreert zich vervolgens voor een nieuwsbrief na die aankoop tijdens hetzelfde bezoek. De gebeurtenis van de nieuwsbrief registratie wordt beschouwd als een interactie van de Klant van de Terugkeer, omdat de staat van de klantenloyaliteit van de bezoeker onmiddellijk na de aankoop veranderde.
