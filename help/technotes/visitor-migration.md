---
description: Bezoekersmigratie is een proces waarbij het cookie van de bezoeker-id van het ene domein naar het andere wordt gemigreerd.
keywords: Analyseimplementatie
title: Migratie van bezoekers
topic-fix: Developer and implementation
uuid: af31928c-85d7-407f-a583-0c8f2852ceb3
exl-id: d44628c8-902f-4e60-b819-41d5537407d8
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# Migratie van bezoekers

Bezoekersmigratie is een proces waarbij het cookie van de bezoeker-id van het ene domein naar het andere wordt gemigreerd.

Met de migratie van bezoekers kunt u de identificatie-cookies van bezoekers behouden wanneer u domeinen voor gegevensverzameling wijzigt. Domeinen voor gegevensverzameling kunnen om de volgende redenen worden gewijzigd:

* Overstappen van `2o7.net` naar `adobedc.net`.

* U implementeert de [Experience Cloud Bezoeker ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) en gaat van een CNAME/first-party gegevensverzamelingsdomein naar `adobedc.net`, `2o7.net` of `omtrdc.net`

* Het bewegen naar een naam/de inzameling van de eerste-partijgegevens ( [Eerste-partijCookies)](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html).

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
   <td colname="col1"> <p> <b>Ga aan de slag:</b> <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"  > Neem contact op met de klantenservice  </a> met de domeinen die u wilt migreren en met de migratieperiode die u wilt inschakelen (30, 60 of 90 dagen). Zorg ervoor dat u de niet-beveiligde en beveiligde domeinen opneemt. </p> </td> 
   <td colname="col3"> <p>Maak een lijst met de syntaxis <i>exact</i> voor de domeinen die u wilt migreren naar en migreren. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; metrics.example.com </li> 
    </ul> <p>De namen van de migratiegastheer worden gevormd op de de inzamelingsserver van Gegevens van Adobe. De Zorg van de klant zal u vertellen wanneer de verandering wordt aangebracht zodat kunt u voor de volgende stap plannen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>6+ uur na configuratiewijziging</b>: Werk de  <code> s.trackingServer</code> en de  <code> s.trackingServerSecure</code> variabelen in uw code van JavaScript van Analytics bij om de nieuwe servers van de gegevensinzameling te gebruiken. </p> </td> 
   <td colname="col3"> <p>Nadat u deze verandering aanbrengt, gebruik <a href="https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=en"> debugger van de Experience Cloud </a> om te verifiëren dat het de beeldverzoek van de Analyse naar de bijgewerkte server van de gegevensinzameling gaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Onmiddellijk na het bijwerken van uw Analysecode</b>: Test uw plaats om te verifiëren dat redirect aan het vorige domein van de gegevensinzameling voorkomt. </p> </td> 
   <td colname="col3"> <p>Gebruik een <a href="../implement/validate/packet-monitor.md"> pakketmonitor</a> om te verifiëren dat wanneer u tot uw plaats voor het eerst toegang hebt, of na het ontruimen van koekjes, u twee 302 (omleiding) de statuscodes van HTTP vóór de 200 (O.K.) statuscode van HTTP ziet. Als een van deze omleidingen mislukt, neemt u onmiddellijk contact op met de klantenservice om ervoor te zorgen dat de migratie correct is geconfigureerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Voor de gehele migratieperiode</b>: Houd het DNS verslag voor vorige hostname actief. </p> </td> 
   <td colname="col3"> <p>De vorige hostname moet door DNS oplossen of de koekjesmigratie zal niet voorkomen. </p> </td> 
  </tr> 
 </tbody> 
</table>
