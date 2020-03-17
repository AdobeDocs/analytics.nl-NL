---
description: Hiermee geeft u een uitsplitsing weer van zoektrefwoorden.
title: Trefwoorden zoeken
topic: Reports
uuid: db9d477b-b711-4b93-9c25-3aebe5f2ace6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Trefwoorden zoeken

Hiermee geeft u een uitsplitsing weer van zoektrefwoorden.

**Trefwoorden zoeken - Alles**: Hiermee geeft u een uitsplitsing weer van elk zoekwoord dat is gebruikt om uw site te zoeken. U kunt deze lijst sorteren op paginaweergaven of zoektrefwoorden door op de kolomtitel boven de lijst te klikken. Klik op het vergrootglas naast een zoekwoord om de zoekresultaten voor uw site weer te geven.

**Trefwoorden zoeken - Betaald**: Hiermee geeft u een uitsplitsing weer van elk trefwoord dat u voor betaalde zoekopdrachten hebt gebruikt. U kunt deze lijst sorteren op paginaweergaven of zoektrefwoorden door op de kolomtitel boven de lijst te klikken. Klik op het vergrootglas naast een zoekwoord om de zoekresultaten voor uw site weer te geven.

**Trefwoorden zoeken - Natuurlijk**: Hiermee geeft u een uitsplitsing weer van elk natuurlijk zoekwoord dat wordt gebruikt om uw site te zoeken. U kunt deze lijst sorteren op paginaweergaven of zoektrefwoorden door op de kolomtitel boven de lijst te klikken. Klik op het vergrootglas naast een zoekwoord om de zoekresultaten voor uw site weer te geven.

>[!IMPORTANT]
>
>Voor betaalde en natuurlijke zoekopdrachten hebben zoekprogramma&#39;s (in de meeste gevallen) de zoektrefwoorden niet meer opgegeven als onderdeel van de referentie. Als gevolg hiervan classificeert Adobe het Google- (of Bing- of Yahoo-) domein altijd als zoekopdracht. Op basis van de indeling en inhoud van de referentie (zelfs zonder de trefwoorden) kan Adobe vaak vaststellen dat de zoekopdracht het resultaat is van een zoekopdracht, zodat de zoekopdracht wordt geteld bij de trefwoorden die niet beschikbaar zijn. [Meer...](https://helpx.adobe.com/analytics/kb/keyword-unavailable.html)

## Toewijzing, verlopen en speciale waarden {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Werkruimte Analyse </p> <p>Rapporten en analyses </p> </th> 
   <th colname="col3" class="entry"> Ad hoc-analyse </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Metrische toewijzing </td> 
   <td colname="col2"> <p>Oorspronkelijke waarde (standaardwaarde) </p> <p> Kan worden gewijzigd in lineair. </p> </td> 
   <td colname="col3"> Recentste (kan worden veranderd in lineair gebruikend de lineaire versie van een meticum) </td> 
   <td colname="col4"> <p>Oorspronkelijke waarde (standaardwaarde) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Waarden vervallen na </td> 
   <td colname="col2"> Bezoek - kan worden ingekort maar niet worden verlengd </td> 
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
   <td colname="col2"> <p>"Geen": totalen voor de hele site die tijdens het bezoek geen trefwoord hadden. </p> "Sleutelwoord niet beschikbaar"is onderzoeken waar het sleutelwoord uit het onderzoek werd verwijderd en niet naar gegevensinzameling wordt verzonden. Dit gebeurt gewoonlijk wanneer een klant is aangemeld bij een Google-account. Geldt voor betaald en natuurlijk. </td> 
   <td colname="col3"> (laag-verkeer) vertegenwoordigt waarden voorbij eerste 500k die niet genoeg verkeer hebben ontvangen om te worden gemeld. </td> 
   <td colname="col4"> <p> Leeg - equivalent van "Geen", totalen voor de hele site die tijdens het bezoek geen trefwoord hadden. </p> <p>"Sleutelwoord niet beschikbaar"is onderzoeken waar het sleutelwoord uit het onderzoek werd verwijderd en niet naar gegevensinzameling wordt verzonden. Dit gebeurt gewoonlijk wanneer een klant is aangemeld bij een Google-account. Geldt voor betaald en natuurlijk. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rapportgeschiedenis {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

| Datum | Wijzigen |
|---|---|
| 1/16/2014 | Het pakhuis van gegevens werd bijgewerkt om de logica aan te passen die door marketing rapporten &amp; analyses wordt gebruikt. Vóór deze datum zijn de zoektrefwoorden tijdens het bezoek niet meer aanwezig. |

