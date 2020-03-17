---
description: Tips en aanbevolen procedures voor nieuwe gebruikers van virtuele rapportsuites.
keywords: Virtual Report Suite
title: VRS Veelgestelde vragen
topic: Reports and analytics
uuid: 91225743-765a-4145-9ce5-4268e80ea7e8
translation-type: tm+mt
source-git-commit: 444a2b93a39cad0d2f62a4bf8d889b71ba726092

---


# VRS Veelgestelde vragen

Tips en aanbevolen procedures voor nieuwe gebruikers van virtuele rapportsuites.

<table id="table_4D9DE70984674B65AD7D40E3D1479CD2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Moet ik mijn implementatie van veelvoudige rapportreeksen in één enkele "globale"rapportreeks consolideren en dan virtuele rapportreeksen gebruiken om verschillende segmenten gegevens aan mijn gebruikers bloot te stellen?</b> </td> 
   <td colname="col2"> <p>Misschien. Hier volgen enkele situaties waarin u kunt <b>overwegen om door te gaan met individuele rapportreeksen</b>: </p> 
    <ul> 
     <li>Als u variabelen/dimensies met een groot aantal unieke waarden hebt, kan het consolideren in één enkele rapportreeks ertoe leiden dat u maandelijkse unieke waardemaxima in deze globale reeks overschrijdt, leidend tot beknotting ("Laag Verkeer"als lijnpunt in rapporten). </li> 
     <li>Als u real-time of "Huidige gegevens" rapportage voor afzonderlijke segmenten nodig hebt (bijvoorbeeld merken, bedrijfseenheden, enz.) van uw gegevens. </li> 
     <li>Als uw verschillende rapportsuites elk unieke vereisten voor het bijhouden hebben (d.w.z., als zij de variabelen en gebeurtenissen van de Analyse van Adobe zeer verschillend gebruiken), merk op dat het consolideren aan een globale rapportreeks u geen extra variabelen of gebeurtenissen voor het volgen zal verlenen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Welke montages op virtuele rapportsuites worden geërft van de reeks van het ouderrapport? </b> </td> 
   <td colname="col2"> <p>Een virtuele rapportsuite (VRS) neemt de meeste serviceniveaus van de bovenliggende rapportsuite over, zoals eVar-instellingen, verwerkingsregels, classificaties, enzovoort. </p> <p>De volgende instellingen worden <b>NIET</b> overgeërfd: </p> 
    <ul> 
     <li>Set-id rapporteren </li> 
     <li>Naam rapportsuite </li> 
     <li>Machtigingsgroepen (virtuele rapportsuites kunnen worden toegewezen aan hun eigen machtigingsgroepen) </li> 
    </ul> <p>Opmerking:  De meeste door de gebruiker gemaakte entiteiten, zoals Bladwijzers, dashboards, Geplande rapporten, enz., vallen hier niet onder.; deze items worden niet overgenomen van het bovenliggende element en kunnen specifiek worden gemaakt en gebruikt tegen de vrijwillige VUT-regeling (meer details in de volgende vraag). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Hoe verschilt het werken met een virtuele rapportsuite van het werken met een basisrapportsuite in de gebruikersinterface van Analytics?</b> </td> 
   <td colname="col2"> <p>Zodra gecreeerd, wordt een virtuele rapportreeks behandeld enkel als een reeks van het basisrapport door UI en over het algemeen gesteund voor de meeste uitgebreide eigenschappen. Bijvoorbeeld: </p> 
    <ul> 
     <li>Virtuele rapportsuites verschijnen in de selecteur van de Reeks van het Rapport en kunnen individueel worden geselecteerd enkel als een andere reeks van het basisrapport. </li> 
     <li>DL-rapporten, bladwijzers, dashboards, doelen, waarschuwingen, segmenten, berekende cijfers, enz. kunnen allen tegen een virtuele rapportreeks worden gecreeerd en zich onafhankelijk van de ouder gedragen. </li> 
     <li>De virtuele rapportsuites kunnen individueel aan de Groepen van Toestemmingen worden toegevoegd enkel als een andere rapportreeks. </li> 
     <li>Segmenten kunnen nog steeds worden toegepast bij het uitvoeren van rapporten in het kader van een vrijwillige VUT-regeling; deze worden automatisch gestapeld met het segment(en) van de virtuele rapportsuite wanneer de rapportgegevens worden opgehaald. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Hoe worden virtuele rapportsuites behandeld in de Admin Console en Admin API? Kan ik eigenschappen tegen hen zoals de koffers van het basisrapport bewaren? </b> </td> 
   <td colname="col2"> <p>Nee, virtuele rapportsuites worden <b>niet ondersteund voor de meeste beheerfuncties</b>. Zoals hierboven vermeld, erft VRS de meeste de dienstniveaus en eigenschappen van de ouder (bijvoorbeeld, eVar montages, de Regels van de Verwerking, Classificaties, enz.), zodat om een veranderingen in deze geërfte montages op VRS aan te brengen, moet u de ouderrapportreeks veranderen. </p> <p>Dientengevolge, worden de virtuele rapportsuites getoond in UI <b>slechts hier</b>: </p> 
    <ul> 
     <li>De virtuele Manager van de Reeks van het Rapport, waar u VRSs creeert en uitgeeft. <p>( <span class="ignoretag"><span class="uicontrol"> Analytics </span> &gt; <span class="uicontrol"> Components </span> &gt; <span class="uicontrol"> Virtual Report Suites </span> </span>) </p> </li> 
     <li id="li_E2B3F61A3013402697DCF6E0D32A62DC"> De gebruikersbeheerinterface waarin u groepen met aangepaste machtigingen bewerkt. Dit staat VRS rekeningen toe om aan een toestemmingengroep worden toegevoegd en zou kunnen worden gebruikt om een groep tot stand te brengen die slechts toegang tot virtuele rapportsuites heeft (als Admin toegang tot de ouder wilde ontkennen en slechts gebruikers toegang tot specifieke segmenten toestaat). <p>( <span class="ignoretag"> Admin <span class="uicontrol"> &gt; </span> Gebruikersbeheer <span class="uicontrol"> </span> </span>) </p> </li> 
    </ul> <p>Opmerking:  Wanneer u de API van de Diensten van het Web gebruikt en probeert om de montages van de Eigenschap tegen VRS te bewaren, zal een uitzondering worden geworpen. Functies kunnen alleen worden ingesteld op basis van een basisrapportsuite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Ik controleerde "begin nieuw bezoek bij lancering." Waarom zie ik bezoeken die nog veel hoger zijn dan lanceringen?</b> </td> 
   <td colname="col2"> <p> Als het selectievakje 'Nieuw bezoek starten bij starten' is ingeschakeld, geldt de time-out nog steeds. Dus als een gebruiker de app tien minuten gebruikt met een pauze van één minuut tussen elke actie, begint een nieuw bezoek bij het starten en worden negen extra bezoeken gemaakt wanneer het bezoek uitvalt. Als u het starten en bezoeken zo dicht mogelijk wilt houden wanneer u de optie "Nieuw bezoek starten bij starten" gebruikt, moet u een time-out gebruiken die langer is dan de sessietime-out die in de SDK is ingesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Ik stel "nieuw bezoek starten bij starten" in en stel een langere time-out in dan mijn SDK. Waarom zijn mijn lanceringen nog veel lager dan bezoeken?</b> </td> 
   <td colname="col2"> <p> Als de time-out hoger is dan de waarde die is ingesteld in de SDK, wordt er waarschijnlijk op de achtergrond in uw app hits verzonden en worden deze resultaten geregistreerd als nieuwe bezoeken. Controleer of dit het geval is door de dimensie hit type op de bovenliggende rapportsuite te gebruiken om te kijken of er achtergrondtreffers zijn. </p> <p> <p>Opmerking: Achtergrond- en voorgrondresultaten worden alleen gedifferentieerd in versie 4.13.6 en hoger van de SDK. Als u op een lagere versie werkt, worden alle treffers als voorgrond weergegeven. Als u op de juiste versie van de SDK werkt, schakelt u de instelling 'Achtergrondhits voorkomen bij een nieuw bezoek' in. </p> </p> <p> <p>Opmerking: Als u oudere verwerking voor achtergrondklappen in de admin console hebt onbruikbaar gemaakt, zullen zij niet in de ouderrapportreeks verschijnen maar in de virtuele rapportreeks. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Welke versie van SDK moet ik achtergrondopdrachten bijhouden?</b> </td> 
   <td colname="col2"> <p> U moet versie 4.13.6 of hoger van de SDK zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

