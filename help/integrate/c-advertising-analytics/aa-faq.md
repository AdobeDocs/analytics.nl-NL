---
description: Veelgestelde vragen over Advertising Analytics.
title: Veelgestelde vragen voor reclameanalyses
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '1419'
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
   <td colname="col1"> <p>Q: Moet ik een <b>Adobe Advertising Cloud- of Adobe Advertising Cloud-klant (AMO)</b> toegang te krijgen tot deze functionaliteit? </p> </td> 
   <td colname="col2"> <p>A: Nee, deze functionaliteit is beschikbaar voor niet-Advertising Cloud- en niet-AMO-klanten. </p> <p>AMO-klanten kunnen gebruikmaken van de bestaande integratie tussen Analytics en AMO; ze kunnen Ad Analytics niet gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: welke <b>Adobe Analytics SKU's</b> Je het recht geven om Advertising Analytics te gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics is beschikbaar voor Adobe Analytics <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html"  > Selecteren </a>, <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html"  > Eerste </a>, en <a href="https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html"  > Ultieme </a> SKU's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Moeten we <b>betaal extra</b> om Advertising Analytics te gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Nee, buiten de juiste SKU-provisioning maakt Advertising Analytics geen extra kosten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Zal Advertising Analytics tellen voor mijn <b>serveroproepgebruik</b>? </p> </td> 
   <td colname="col2"> <p>A: Neen, Advertising Analytics gebruikt een speciaal gegevensbrontype dat geen kosten van de servervraag veroorzaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Als I <b>Advertising Cloud/AMO wordt al gebruikt</b>, kan ik nog steeds de Advertising Analytics-functionaliteit gebruiken? </p> </td> 
   <td colname="col2"> <p>A: Alle compatibele accounts van zoekprogramma's worden doorgegeven naar Advertising Analytics en worden weergegeven als alleen-lezen. Alle bewerkingen of updates moeten worden verwerkt in Advertising Cloud/AMO. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Ik bezit de juiste SKU, maar ik <b>heeft geen toegang</b> Advertising Analytics, waarom is dat? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics is alleen beschikbaar voor Adobe Analytics-beheerders; beheerders kunnen echter toegang verlenen aan niet-beheerders. Neem contact op met uw beheerder voor toegangsrechten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics gebruiken {#section_3A70C6C4D5A842B2981F0257A01F95FF}

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
   <td colname="col1"> <p>Q: welke <b>zoekprogrammaaccounts</b> zijn ze opgenomen in Advertising Analytics? </p> </td> 
   <td colname="col2"> <p>A: Zoekmachinerekeningen bevatten Google AdWords en Microsoft Bing. </p> <p>Opmerking: Yahoo Gemini werd op 31 maart 2019 door Microsoft Bing geabsorbeerd. Als gevolg hiervan is de optie voor een Yahoo Gemini-advertentieaccount niet meer beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Waar ga ik naar <b>toegang</b> Advertising Analytics? </p> </td> 
   <td colname="col2"> <p>A: Navigeer na het aanmelden naar Adobe Analytics naar de <span class="uicontrol"> Beheerder </span> -menu. Selecteer vervolgens de nieuwe menuoptie <span class="uicontrol"> Advertising Analytics </span> om je zoekprogrammaaccounts toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Hoe is het? <b>gegevens verzameld en doorgegeven aan Analytics</b>? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics gebruikt een reeks aangepaste API's om gegevens van zoekmachines via de Adobe Advertising Cloud door te geven aan Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Wat <b>zoekgegevens</b> kom ik bij deze integratie? </p> </td> 
   <td colname="col2"> <p>A: U krijgt 1) indrukkingen, 2) klikken, 3) kosten, 4) Kwaliteitsscore en 5) Gemiddelde positie rechtstreeks vanuit de zoekmachines en 6) AMO ID-instanties (klik op Exemplaren). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Mag ik <b>Advertising Analytics-gegevens onderbreken</b> door andere analytische gegevens (metriek/afmetingen)? </p> </td> 
   <td colname="col2"> <p>A: Neen, de ruwe onderzoeksgegevens zullen binnen als onafhankelijke gegevensreeks komen. Nochtans, is er een versie van Instanties van de klikgegevens die door andere gegevens van Analytics kunnen worden verdeeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Wat is de definitie van de verschillende <b>statusindicatoren</b> voor mijn accounts (In behandeling, Actief, Gepauzeerd, enzovoort)? </p> </td> 
   <td colname="col2"> <p>A: Elk van deze statusindicatoren identificeert de levenscyclusfase van elke rekening van de onderzoeksmotor. </p> 
    <ul id="ul_F68AD377B2F04A47B20355B2FF4CF345"> 
     <li id="li_05F8D7C6D00E4742A65373BE6FAA0448"><b>In behandeling</b> betekent dat de account is ingesteld, maar dat de gegevens nog niet zijn opgehaald. </li> 
     <li id="li_42B1557A8AEC41008B85AF6E3F625CAB"><b>Gepauzeerd</b> betekent dat de rekening eerder is ingesteld, maar niet is geactiveerd. </li> 
     <li id="li_30B72CC171874F308A2B8CE552EA6930"><b>Actief</b> betekent dat de rekening volledig is opgezet en aan zoekgegevens voldoet. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Ik probeer <b>Mijn Advertising Analytics-accounts toewijzen aan een specifieke rapportsuite</b>, maar deze optie is niet beschikbaar in de rapportsuite modal. Waarom? </p> </td> 
   <td colname="col2"> <p>A: Voordat u een rapportsuite aan een Advertising Analytics-account kunt toewijzen, moet de gewenste rapportsuite <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md"  > voorzien voor Advertising Analytics-rapportage </a>. </p> <p>Dit gebeurt via een aparte beheerpagina die toegankelijk is via: <span class="ignoretag"> <span class="uicontrol"> Beheerder </span>  &gt; <span class="uicontrol"> Rapportageopties </span>  &gt; <span class="uicontrol"> [selecteer Experience Cloud-toegelaten rapportreeks] </span>  &gt; <span class="uicontrol"> Instellingen bewerken </span>  &gt; <span class="uicontrol"> Advertising Analytics-configuratie </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Is het mogelijk een <b>virtuele rapportsuite</b> op een Advertising Analytics-account? </p> </td> 
   <td colname="col2"> <p>A: Met virtuele rapportsuite worden geen gegevens verzameld, zodat u een Advertising Analytics-account niet rechtstreeks kunt toewijzen aan een Virtual Report-suite. </p> <p>U kunt de Advertising Analytics-account echter toewijzen aan de bovenliggende rapportsuite van de Virtual Report Suite waarin u gegevens wilt zien. </p> <p>De metriek van de Motor van het Onderzoek (klik/kosten/impressies) kunnen niet in de Virtuele rapportreeks verschijnen tenzij u een "of"voorwaarde in uw segmentlogica opneemt die op AMO ID (of zijn classificatie) wordt gebaseerd. Voorbeeld: het toevoegen van "alle treffers waar AMO ID bestaat" zou de metriek van de onderzoeksmotor in het segment omvatten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Zijn Advertising Analytics-meetgegevens te rapporteren in de <b>Marketingkanalen</b> rapporteren? </p> </td> 
   <td colname="col2"> <p>A: Nr, zij zijn niet inbegrepen in het rapport van de Kanalen van de Marketing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: <b>Wanneer</b> worden de zoekgegevens naar Analytics opgehaald? </p> </td> 
   <td colname="col2"> <p>A: De zoekgegevens worden rond 6.00 uur (06.00 uur) uit de zoekmachines gehaald in de tijdzone van het datacenter Analytics. Dit is wanneer de gegevens van AMO worden verzameld en in de rapportreeks opgenomen. Het wordt dan omgezet in de tijdzone van de rapportreeks als deel van het opnemen van de gegevens in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Wat kan er gebeuren? <b>vastgelegd voor klik</b>? Zien we indrukken, kosten, gemiddelde positie, enzovoort? zelfs zonder klik ? </p> </td> 
   <td colname="col2"> <p>A: De AMO-id legt de metriek van de zoekmachine vast: Impressies, Kosten, Klikken, Gemiddelde positie en Gemiddelde kwaliteitsscore. Als er geen kliks zijn, maar er indrukken zijn, dan zullen de beeld/positie/kwaliteitsscore gegevens nog naar Analytics worden verzonden. Doorgaans zijn er ook geen kosten verbonden als er niet wordt geklikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V: Op welk niveau worden deze gegevens vastgelegd? <b>Bezoeker? Hit?</b> </p> </td> 
   <td colname="col2"> <p>A: De meetgegevens van de zoekmachine worden vastgelegd op raakniveau en aangesloten op de AMO-id (en de classificaties). Dit zijn gegevens op overzichtsniveau die geen verband houden met bezoeken/bezoekers. Als zodanig kunnen de metriek van de zoekmachine slechts in segmenten worden gebruikt die bereik op raakniveau zijn en op AMO-id (of zijn classificaties) gebaseerd zijn. </p> <p>De AMO-id wordt ook vastgelegd op de bestemmingspagina in de hit voor die pagina (die de id verbindt met het bezoek/de bezoeker) en zal verderop in de stroom blijven staan om krediet te krijgen voor andere analytische gegevens (totdat deze verlopen of door een nieuwe AMO-id wordt overschreven). Net als elke andere eVar wordt het volledig in de gegevensset opgenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: vangen wij slechts google.com of <b>landversies</b> (zoals google.co.uk, google.it, google.fr, of google.de) eveneens? </p> </td> 
   <td colname="col2"> <p>A: De classificatie van het Platform van de Advertentie vangt deze waarden: "Google Adwords", en "Bing Ads". </p> <p>De beste praktijk is om de landcode op te nemen in de naamgeving van campagnes. Vervolgens kunt u naar beneden of naar een segment filteren (bijvoorbeeld als alle campagnes beginnen met landcode_ en u vervolgens een segment maakt waarin Campagnes (AMO ID) beginnen met "UK_", zodat u alleen gegevens voor het Verenigd Koninkrijk krijgt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: De metrische "AMO Cost" is de kosten die voor elk trefwoord/advertentie worden betaald, zoals opgegeven door het zoekprogramma. Zijn dit nettokosten of brutokosten? </p> </td> 
   <td colname="col2"> <p>A: "AMO-kosten" zijn alleen de kosten die aan de zoekmachines worden betaald. Hieronder vallen geen kosten voor het optimaliseren van de zoekopdracht of het beheerplatform. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Zijn er plannen om andere reclamekanalen op te nemen, zoals <b>Weergave</b> of <b>Sociaal</b>? </p> </td> 
   <td colname="col2"> <p>A: Nee, we hebben momenteel geen plannen voor deze andere kanalen op de routekaart. </p> </td> 
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
   <td colname="col1"> <p>Q: Bij het instellen van mijn advertentieaccount staat het volgende:<b> Automatisch bijhouden</b> kan leiden tot onbedoelde gevolgen. Welke gevolgen kunnen zich voordoen? </p> </td> 
   <td colname="col2"> <p>A: 
     <ul id="ul_59EFF4A2ECE947EBBDB6A9FF6D072FE0"> 
      <li id="li_8731E4B7D6ED4F0996B3630A35D5BAC4">In de modus Automatisch wordt geprobeerd URL-parameters toe te voegen aan het einde van de volgende sjablonen/doel-URL's in de juiste indeling. <b>Het is echter uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina. </b> </li> 
      <li id="li_1202FE1FC88342378A60E8FE65E5426B">In de modus Automatisch kunnen sleutelwoorden worden ingevoegd in de bestemmings-URL en het is mogelijk dat uw webserver geen trefwoorden met speciale tekens ondersteunt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q: Als ik eerst handmatig of automatisch bijhouden heb ingesteld, <b>kan ik schakelen</b> op de andere volgmodus later? Wat zijn de gevolgen? </p> </td> 
   <td colname="col2"> <p>A: Ja u kunt schakelen, maar u zult de oude volgende logica moeten verwijderen alvorens de schakelaar te maken. Dit kan in wat onderbreking van het volgen op de dag resulteren de schakelaar wordt gemaakt (vooral als zich van hand aan automatisch beweegt). Daarom wordt aanbevolen niet over te schakelen, tenzij dit absoluut noodzakelijk is. </p> 
    <ul id="ul_3F3CADD1C97B4947A13837CEE63A599D"> 
     <li id="li_CB9265951FD040388AEAB9EAD790A36E"><b>Overschakelen van Handmatig naar Automatisch</b>: Verwijder de handmatige toevoegingen aan de volgsjablonen en schakel de schakeloptie in de gebruikersinterface van Advertising Analytics van handmatig naar Automatisch in en sla de instelling op. Het kan tot x uur duren voordat het systeem de automatische trackingcodes heeft ingevuld. </li> 
     <li id="li_2B6ED1342E2D443B8AF26D03532AB8E4"><b>Schakelen van Automatisch naar Handmatig</b>: Werk de schakeloptie van handmatig naar automatisch bij in de Advertising Analytics-instellingsinterface en implementeer de handmatige volgcodes zo snel mogelijk. Als u tijdens de implementatie van de handmatige volgcodes de automatische volgcodes in de sjablonen voor zoekprogramma's ziet, verwijdert u deze. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
