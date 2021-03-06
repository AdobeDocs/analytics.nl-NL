---
description: Veelgestelde vragen over Advertising Analytics.
title: Veelgestelde vragen
uuid: 05724f56-cf98-4ad8-ad0d-83a5a4b1944a
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 2%

---


# Veelgestelde vragen

## Toegang/rechten {#section_5F558C5981F747F0AF375A9E4B75C93C}

<table id="table_6713C3B0B6734F768370F974EB5AC5E8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>V: Moet ik een <b>Adobe Advertising Cloud of Adobe Advertising Cloud (AMO) klant</b> zijn om tot deze functionaliteit toegang te hebben? </p> </td> 
   <td colname="col2"> <p>A: Nee, deze functionaliteit is beschikbaar voor niet-Advertising Cloud- en niet-AMO-klanten. </p> <p>AMO-klanten kunnen gebruikmaken van de bestaande integratie tussen Analytics en AMO; ze kunnen Ad Analytics niet gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Welke <b>Adobe Analytics SKU's</b> geeft u het recht om Advertising Analytics te gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics is beschikbaar voor Adobe Analytics <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html"  > Selecteer </a>, <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html"  > Premium </a> en <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html"  > Ultimate </a> SKU's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Moeten we <b>extra</b> betalen om Advertising Analytics te gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Nee, buiten de juiste SKU-provisioning maakt Advertising Analytics geen extra kosten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Zal Advertising Analytics tellen tegen mijn <b>servervraaggebruik</b>? </p> </td> 
   <td colname="col2"> <p>A: Nee, Advertising Analytics gebruikt een speciaal gegevensbrontype dat geen kosten veroorzaakt voor serveraanroepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Als ik <b>al Advertising Cloud/AMO</b> gebruik, kan ik nog de functionaliteit van Advertising Analytics gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Elk compatibel account voor zoekmachines wordt doorgegeven aan Advertising Analytics en wordt weergegeven als alleen-lezen. Alle bewerkingen of updates moeten worden verwerkt in Advertising Cloud/AMO. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Ik bezit de correcte SKU, maar ik <b>kan geen toegang tot</b> Advertising Analytics, waarom is dat? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics is alleen beschikbaar voor Adobe Analytics-beheerders; beheerders kunnen echter toegang verlenen tot niet-beheerders. Neem contact op met uw beheerder voor toegangsrechten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics {#section_3A70C6C4D5A842B2981F0257A01F95FF} gebruiken

<table id="table_4EC69262B7AB4DF49E736CF3B0362302"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>V: Welke <b>zoekprogrammaaccounts</b> zijn opgenomen in Advertising Analytics? </p> </td> 
   <td colname="col2"> <p>A: Zoekmachinerekeningen zijn Google AdWords en Microsoft Bing. </p> <p>Opmerking: Yahoo Gemini werd door Microsoft Bing geabsorbeerd op 31 maart 2019. Als gevolg hiervan is de optie voor een Yahoo Gemini-advertentieaccount niet meer beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Waar ga ik naar <b>access</b> Advertising Analytics? </p> </td> 
   <td colname="col2"> <p>A: Nadat u zich hebt aangemeld bij Adobe Analytics, navigeert u naar het menu <span class="uicontrol"> Beheer </span>. Selecteer vervolgens de nieuwe menuoptie <span class="uicontrol"> Advertising Analytics </span> om uw zoekprogrammaaccounts toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Hoe worden de <b>gegevens verzameld en in Analytics</b> overgegaan? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics gebruikt een reeks aangepaste API's om gegevens van zoekmachines via de Adobe Advertising Cloud door te geven aan Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Wat <b>onderzoeksgegevens</b> krijg ik met deze integratie? </p> </td> 
   <td colname="col2"> <p>A: U krijgt 1) indrukkingen, 2) klikken, 3) kosten, 4) Kwaliteitsscore en 5) Gemiddelde positie rechtstreeks vanuit de zoekmachines en 6) AMO ID-instanties (klik op Exemplaren). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Kan ik mijn Advertising Analytics-gegevens <b>onderbreken</b> met andere Analytics-gegevens (metriek/afmetingen)? </p> </td> 
   <td colname="col2"> <p>A: Nee, de onbewerkte zoekgegevens worden opgenomen als een onafhankelijke gegevensset. Er is echter een versie van Instanties van de klikgegevens die door andere analysegegevens kan worden gesplitst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Wat is de definitie van de verschillende <b>status indicatoren</b> voor mijn rekeningen (In behandeling, Actief, Gepauzeerd, etc.)? </p> </td> 
   <td colname="col2"> <p>A: Elk van deze statusindicatoren identificeert de levenscyclusfase van elk onderzoek motorrekening. </p> 
    <ul id="ul_F68AD377B2F04A47B20355B2FF4CF345"> 
     <li id="li_05F8D7C6D00E4742A65373BE6FAA0448"><b>Het </b> betalingsverkeer betekent dat de account is ingesteld, maar dat de gegevens nog niet worden opgehaald. </li> 
     <li id="li_42B1557A8AEC41008B85AF6E3F625CAB"><b></b> Gepauzeerd betekent dat de account eerder is ingesteld, maar niet actief is. </li> 
     <li id="li_30B72CC171874F308A2B8CE552EA6930"><b>Hiermee </b> activeert u dat de account volledig is ingesteld en aan zoekgegevens begint. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Ik probeer om <b>mijn Advertising Analytics rekeningen aan een specifiek rapportreeks </b> in kaart te brengen, maar het is niet beschikbaar in de Reeks van het Rapport modaal. Waarom? </p> </td> 
   <td colname="col2"> <p>A: Voordat u een rapportsuite aan een Advertising Analytics-account kunt toewijzen, moet de gewenste rapportsuite <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md"  > zijn ingericht voor Advertising Analytics-rapportage </a>. </p> <p>Dit gebeurt via een aparte beheerpagina die toegankelijk is via: <span class="ignoretag"> <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Rapportsuite </span> &gt; <span class="uicontrol"> [select Experience Cloud-enabled report suite] </span> &gt; <span class="uicontrol"> Edit Settings </span> &gt; <span class="uicontrol"> Advertising Analytics Configuration </span> </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Kan een <b>Virtual Report Suite</b> (VRS) worden toegewezen aan een Advertising Analytics-account? </p> </td> 
   <td colname="col2"> <p>A: Met Virtual Report Suites worden geen gegevens verzameld, zodat u een Advertising Analytics-account niet rechtstreeks aan een VRS kunt toewijzen. </p> <p>U kunt de Advertising Analytics-account echter toewijzen aan de bovenliggende rapportsuite van de vrijwillige VRS waarin u gegevens wilt zien. </p> <p>De metriek van de Motor van het Onderzoek (klik/kosten/impressies) kunnen niet in VRS verschijnen tenzij u een "of"voorwaarde in uw segmentlogica opneemt die op AMO ID (of zijn classificatie) wordt gebaseerd. Voorbeeld: Als u "alle resultaten toevoegt waar AMO-id bestaat", worden ook de cijfers van de zoekmachine in het segment opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Zijn Advertising Analytics metriek rapporteerbaar in <b>Marketing Channels</b> rapport? </p> </td> 
   <td colname="col2"> <p>A: Nr, zijn zij niet inbegrepen in het rapport van de Kanalen van de Marketing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: <b>Wanneer</b> worden de onderzoeksgegevens getrokken in Analytics? </p> </td> 
   <td colname="col2"> <p>A: De zoekgegevens worden uit de zoekmachines gehaald rond 6AM (06:00) in de tijdzone van uw datacenter Analytics. Dit is wanneer de gegevens van AMO worden verzameld en in de rapportreeks opgenomen. Het wordt dan omgezet in de tijdzone van de rapportreeks als deel van het opnemen van de gegevens in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Wat kan <b>worden gevangen vóór de klik</b>? Hebben we beelden, kosten, gemiddelde positie, enzovoort? zelfs zonder klik ? </p> </td> 
   <td colname="col2"> <p>A: De AMO-id legt de maatstaven van de zoekmachine vast: Impressies, kosten, klikken, Gemiddelde positie en Gemiddelde kwaliteitsscore. Als er geen kliks zijn, maar er indrukken zijn, dan zullen de beeld/positie/kwaliteitsscore gegevens nog naar Analytics worden verzonden. Doorgaans zijn er ook geen kosten verbonden als er niet wordt geklikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Op welk niveau worden deze gegevens vastgelegd? <b>Bezoeker? Hit?</b> </p> </td> 
   <td colname="col2"> <p>A: De metriek van de motor van het Onderzoek wordt gevangen op het raakniveau en met AMO identiteitskaart (en zijn classificaties) verbonden. Dit zijn gegevens op overzichtsniveau die geen verband houden met bezoeken/bezoekers. Als zodanig kunnen de metriek van de zoekmachine slechts in segmenten worden gebruikt die bereik op raakniveau zijn en op AMO-id (of zijn classificaties) gebaseerd zijn. </p> <p>De AMO-id wordt ook vastgelegd op de bestemmingspagina in de hit voor die pagina (die de id verbindt met het bezoek/de bezoeker) en zal verderop in de stroom blijven staan om krediet te krijgen voor andere analytische gegevens (totdat deze verlopen of door een nieuwe AMO-id wordt overschreven). Net als alle andere eVar is het volledig in de gegevensset opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Hebben we alleen maar google.com of <b>country versions</b> (zoals google.co.uk, google.it, google.fr, of google.de) vastgelegd? </p> </td> 
   <td colname="col2"> <p>A: In de classificatie Platform toevoegen worden de volgende waarden vastgelegd: "Google Adwords" en "Bing Ads". </p> <p>De beste praktijk is om de landcode op te nemen in de naamgeving van campagnes. Vervolgens kunt u naar beneden of naar een segment filteren (bijvoorbeeld als alle campagnes beginnen met landcode_ en u vervolgens een segment maakt waarin Campagnes (AMO ID) beginnen met "UK_", zodat u alleen gegevens voor het Verenigd Koninkrijk krijgt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: De metrische "Kosten AMO"is de kosten die voor elk sleutelwoord/elke advertentie worden betaald zoals die door het onderzoeksmotor worden gemeld. Zijn dit nettokosten of brutokosten? </p> </td> 
   <td colname="col2"> <p>A: "AMO-kosten" zijn alleen de kosten die aan de zoekmachines worden betaald. Hieronder vallen geen kosten voor het optimaliseren van de zoekopdracht of het beheerplatform. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Zijn er plannen om andere reclamekanalen zoals <b>Display</b> of <b>Social</b> op te nemen? </p> </td> 
   <td colname="col2"> <p>A: Nee, op dit moment hebben we geen plannen voor deze andere kanalen op de routekaart. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Automatisch versus handmatig bijhouden {#section_7437C4698A6D482EB7ED94A948390119}

<table id="table_9738FF8459574ED2937A860A665BE739"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>V: Wanneer u mijn advertentieaccount instelt, staat dat<b> Automatisch bijhouden</b> tot ongewenste gevolgen kan leiden. Welke gevolgen kunnen zich voordoen? </p> </td> 
   <td colname="col2"> <p>A: 
     <ul id="ul_59EFF4A2ECE947EBBDB6A9FF6D072FE0"> 
      <li id="li_8731E4B7D6ED4F0996B3630A35D5BAC4">In de modus Automatisch wordt geprobeerd URL-parameters toe te voegen aan het einde van de volgende sjablonen/doel-URL's in de juiste indeling. <b>Het is echter uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina.  </b> </li> 
      <li id="li_1202FE1FC88342378A60E8FE65E5426B">In de modus Automatisch kunnen sleutelwoorden worden ingevoegd in de bestemmings-URL en het is mogelijk dat uw webserver geen trefwoorden met speciale tekens ondersteunt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Als ik eerst Handmatig of Automatisch bijhouden heb ingesteld, <b>kan ik </b> later overschakelen op de andere modus voor bijhouden? Wat zijn de gevolgen? </p> </td> 
   <td colname="col2"> <p>A: Ja kunt u schakelen, maar u zult de oude volgende logica moeten verwijderen alvorens de schakelaar te maken. Dit kan in wat onderbreking van het volgen op de dag resulteren de schakelaar wordt gemaakt (vooral als zich van hand aan automatisch beweegt). Daarom wordt aanbevolen niet over te schakelen, tenzij dit absoluut noodzakelijk is. </p> 
    <ul id="ul_3F3CADD1C97B4947A13837CEE63A599D"> 
     <li id="li_CB9265951FD040388AEAB9EAD790A36E"><b>Overschakelen van Handmatig naar Automatisch</b>: Verwijder de handmatige toevoegingen aan de volgende malplaatjes en schakel dan de knevel in Advertising Analytics UI van hand aan Automatisch en sparen het plaatsen. Het kan tot x uur duren voordat het systeem de automatische volgcodes heeft ingevuld. </li> 
     <li id="li_2B6ED1342E2D443B8AF26D03532AB8E4"><b>Schakelen van Automatisch naar Handmatig</b>: Werk de schakeloptie van handmatig naar automatisch bij in de Advertising Analytics Setup UI en implementeer de handmatige volgcodes zo snel mogelijk. Als u tijdens de implementatie van de handmatige volgcodes de automatische volgcodes in de sjablonen voor zoekprogramma's ziet, verwijdert u deze. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

