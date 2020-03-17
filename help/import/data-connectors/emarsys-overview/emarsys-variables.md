---
description: De integratie van Verbindingen van Gegevens voor emarsys gebruikt variabelen van de Analyse om diverse metriek te volgen.
title: Variabelen voor analyse
uuid: 4d5e087c-f495-4aab-9ad1-9b901d34a254
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Variabelen voor analyse{#analytics-variables}

De integratie van Verbindingen van Gegevens voor emarsys gebruikt variabelen van de Analyse om diverse metriek te volgen.

Na het identificeren van de Gebeurtenis en eVars om met de externe systeemintegratie te gebruiken, laat hen in de Console [](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/c-admin-tools.html)Admin toe.

**Vereiste variabelen**

<table id="table_5B8F3A1EB55D4BB48F669FB84C857256"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type variabele </th> 
   <th colname="col2" class="entry"> Naam </th> 
   <th colname="col3" class="entry"> Populatiemethode </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> gebeurtenis (numeriek) </td> 
   <td colname="col2"> Totaal Bounces </td> 
   <td colname="col3"> <p>Automatisch geïmporteerd uit emarsys </p> </td> 
   <td colname="col4"> <p>Met de gebeurtenis Total Bounces kunt u het aantal e-mailberichten zien dat niet aan ontvangers is bezorgd vanwege een leveringsprobleem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> gebeurtenis (numeriek) </td> 
   <td colname="col2"> Geklikt </td> 
   <td colname="col3"> <p>Automatisch geïmporteerd uit emarsys </p> </td> 
   <td colname="col4"> <p>Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> gebeurtenis (numeriek) </td> 
   <td colname="col2"> Geopend </td> 
   <td colname="col3"> <p>Automatisch geïmporteerd uit emarsys </p> </td> 
   <td colname="col4"> <p>Met de gebeurtenis Geopend kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> gebeurtenis (numeriek) </td> 
   <td colname="col2"> Verzonden </td> 
   <td colname="col3"> <p>Automatisch geïmporteerd uit emarsys </p> </td> 
   <td colname="col4"> <p>Met de gebeurtenis Verzenden kunt u het aantal e-mailberichten zien dat is verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> gebeurtenis (numeriek) </td> 
   <td colname="col2"> Abonnement opgezegd </td> 
   <td colname="col3"> <p>Automatisch geïmporteerd uit emarsys </p> </td> 
   <td colname="col4"> <p>Met de gebeurtenis Unsubscribed kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend, maar vervolgens op de koppeling Unsubscribe klikken om toekomstige e-mailberichten van uw organisatie af te melden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Ontvanger-id </td> 
   <td colname="col3"> <p>Verzameld van vraagparameters in e-mailverbindingen door de geautomatiseerde inzamelingsmethode of een elektrisch toestel JavaScript. </p> </td> 
   <td colname="col4"> Ontvanger-id </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar of s.campagne </td> 
   <td colname="col2"> Bericht-id </td> 
   <td colname="col3"> <p>Verzameld van vraagparameters in e-mailverbindingen door de geautomatiseerde inzamelingsmethode of een elektrisch toestel JavaScript. </p> </td> 
   <td colname="col4"> Deze waarde wordt vaak opgeslagen in de campagnevariabele. </td> 
  </tr> 
 </tbody> 
</table>

