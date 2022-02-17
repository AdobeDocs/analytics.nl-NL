---
description: Bezoekersmigratie is een proces waarbij het cookie van de bezoeker-id van het ene domein naar het andere wordt gemigreerd.
keywords: Analyseimplementatie
title: Migratie van bezoekers
topic-fix: Developer and implementation
feature: Analytics Basics
exl-id: d44628c8-902f-4e60-b819-41d5537407d8
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# Migratie van bezoekers

Bezoekersmigratie is een proces waarbij het cookie van de bezoeker-id van het ene domein naar het andere wordt gemigreerd.

Met de migratie van bezoekers kunt u de identificatie-cookies van bezoekers behouden wanneer u domeinen voor gegevensverzameling wijzigt. Domeinen voor gegevensverzameling kunnen om de volgende redenen worden gewijzigd:

* Verplaatsen van `2o7.net` tot `adobedc.net`.

* U implementeert de [Experience Cloud Bezoeker-id-service](https://experienceleague.adobe.com/docs/id-service/using/home.html) en worden van een CNAME/first-party domein van de gegevensinzameling overgegaan naar `adobedc.net`, `2o7.net` of `omtrdc.net`

* Naar een name-/first-party-gegevensverzameling ( [Eerste cookies)](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html).

* Het bewegen van één CNAME aan een andere (veranderende domeinen).

Nadat de bezoekersmigratie wordt gevormd, wanneer een gebruiker het nieuwe domein zonder een koekje van bezoekersidentiteitskaart bezoekt, leidt de server aan de vorige gegevensinzameling hostname opnieuw, wint om het even welke beschikbare koekjes van bezoekersidentiteitskaart terug, en richt dan terug naar het nieuwe domein. Als een bezoeker-id niet wordt gevonden op de vorige hostnaam, wordt een nieuwe id gegenereerd. Dit gebeurt slechts eenmaal per bezoeker.

## Migratieproces van bezoekers {#section_FF0C5C5CAEF343FFA1892B29311F7160}

In de volgende tabel worden de taken weergegeven die zijn vereist voor bezoekersmigratie:

<table id="table_7B2535FC3E264216A299686415C6B21C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Taak </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Aan de slag:</b> <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"  > Contact opnemen met de klantenservice </a> met de domeinen die u wilt migreren en de migratieperiode die u wilt inschakelen (30, 60 of 90 dagen). Zorg ervoor dat u de niet-beveiligde en beveiligde domeinen opneemt. </p> </td> 
   <td colname="col3"> <p>Maak een lijst met de <i>exact</i> syntaxis voor de domeinen die u wilt migreren naar en migreren. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; metrics.example.com </li> 
    </ul> <p>De namen van de migratiegastheer worden gevormd op de de inzamelingsserver van Gegevens van Adobe. De Zorg van de klant zal u vertellen wanneer de verandering wordt aangebracht zodat kunt u voor de volgende stap plannen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>6+ uur na wijziging van configuratie</b>: Werk de <code> s.trackingServer</code> en <code> s.trackingServerSecure</code> variabelen in uw JavaScript-code Analytics om de nieuwe servers voor gegevensverzameling te gebruiken. </p> </td> 
   <td colname="col3"> <p>Nadat u deze wijziging hebt aangebracht, gebruikt u de opdracht <a href="https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=en"> Experience Cloud debugger</a> om te verifiëren dat het de beeldverzoek van de Analyse naar de bijgewerkte server van de gegevensinzameling gaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Onmiddellijk nadat u de Analysecode hebt bijgewerkt</b>: Test uw plaats om te verifiëren dat redirect aan het vorige domein van de gegevensinzameling voorkomt. </p> </td> 
   <td colname="col3"> <p>Een <a href="../implement/validate/packet-monitor.md"> pakketcontrole</a> om te controleren dat wanneer u uw plaats voor het eerst, of na het ontruimen van koekjes toegang hebt, u twee 302 (omleiding) statuscodes van HTTP vóór de 200 (O.K.) statuscode van HTTP ziet. Als een van deze omleidingen mislukt, neemt u onmiddellijk contact op met de klantenservice om ervoor te zorgen dat de migratie correct is geconfigureerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Voor de gehele migratieperiode</b>: Houd het DNS verslag voor vorige hostname actief. </p> </td> 
   <td colname="col3"> <p>De vorige hostname moet door DNS oplossen of de koekjesmigratie zal niet voorkomen. </p> </td> 
  </tr> 
 </tbody> 
</table>
