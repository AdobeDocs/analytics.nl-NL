---
description: U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.
title: Nieuwe rapportsuite - instellingen
topic: Admin tools
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Nieuwe rapportsuite - instellingen

U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.

Beschrijvingen van de elementen die bij het [creëren van een rapportreeks](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)worden gebruikt.

> [!NOTE] De documentatie [van de](/help/components/vrs/c-workflow-vrs/vrs-create.md) Virtuele Reeks van het Rapport toont u hoe te om virtuele rapportreeksen tot stand te brengen.

<table id="table_F739FBD8DB8D409E916F12F61C5953D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> ID van rapportsuite </span> </td> 
   <td colname="col2"> <p>Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan dit ook niet wijzigen. </p> <p>Wanneer het creëren van veelvoudige rapportreeksen, zorg ervoor dat de noemende overeenkomst u gebruikt unieke rapportreeks IDs waarborgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Titel site</span> </td> 
   <td colname="col2">Identificeert de rapportsuite in <span class="wintitle"> Admin Tools</span>. Deze titel wordt ook gebruikt in de vervolgkeuzelijst <span class="wintitle"> Report Suite</span> in de reeksheader. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Tijdzone</span> </td> 
   <td colname="col2"> Hiermee plant u gebeurtenissen en tijdstempelgegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basis-URL</span> </td> 
   <td colname="col2"> (Facultatief) bepaalt het basisdomein voor de rapportreeks. Deze URL werkt als een intern filter URL als u niet uitdrukkelijk interne filters URL voor de rapportreeks bepaalt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Standaardpagina</span> </td> 
   <td colname="col2"> <p>(Optioneel) De standaardwaarde voor de pagina <span class="wintitle"></span> wordt doorgehaald bij URL's die worden aangetroffen. Als uw rapport met de <span class="wintitle"> meest populaire pagina</span> 's URL's bevat in plaats van paginanamen, voorkomt u met deze instelling dat er meerdere URL's voor dezelfde webpagina zijn. </p> <p>De URL<span class="filepath"> 's https://mysite.com</span> en <span class="filepath"> https://mysite.com/index.html</span> zijn bijvoorbeeld doorgaans dezelfde pagina. U kunt externe bestandsnamen verwijderen, zodat deze URL's in uw rapporten worden weergegeven als <span class="filepath"> https://mysite.com</span> . </p> <p>Als u deze waarde niet instelt, verwijdert Analytics automatisch de volgende bestandsnamen van URL's: <span class="filepath"> index.htm</span>, <span class="filepath"> index.html</span>, <span class="filepath"> .cgi</span>, <span class="filepath"> index.asp</span>, <span class="filepath"> default.htm</span><span class="filepath"></span><span class="filepath"></span><span class="filepath"></span><span class="filepath"></span><span class="filepath"></span><span class="filepath"></span><span class="filepath"></span>, default.html, default.cgi, default.asp.htm.htm, home.htm.home.cgi.aspp. </p> <p>Als u het strippen van bestandsnamen wilt uitschakelen, geeft u een standaardpaginawaarde op die nooit voorkomt in uw URL's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Live-datum </p> </td> 
   <td colname="col2">Informeert Adobe over de datum die u verwacht dat deze rapportsuite actief wordt. Als uw plaatsingsprogramma verandert, verstrek een bijgewerkte verkeersschatting gebruikend het <span class="wintitle"> Permanente Verwachte hulpmiddel van het Verkeer</span> in <a href="/help/admin/c-traffic-management/traffic-management.md"> Verkeersbeheer</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschat aantal paginaweergaven per dag</span> </td> 
   <td colname="col2"> Hiermee wordt het geschatte aantal paginaweergaven aangegeven dat deze rapportsuite per dag moet ondersteunen. Grote verkeersvolumes vereisen een langer goedkeuringsproces. Om vertragingen bij de verwerking te voorkomen, moet u zo nauwkeurig mogelijk met deze schatting omgaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basisvaluta</span> </td> 
   <td colname="col2"> <p>Geeft de standaardvaluta aan die wordt gebruikt om alle monetaire gegevens op te slaan. Analytische rapportage converteert transacties in andere valuta's naar de basisvaluta, waarbij de huidige omrekeningskoers wordt gebruikt op het tijdstip dat de gegevens worden ontvangen. </p> <p> Analytische rapportage gebruikt de JavaScript-variabele <span class="varname"> currencyCode</span> om de valuta van een bepaalde transactie te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ondersteuning voor multi-byte tekens uitschakelen </span> </td> 
   <td colname="col2"> <p>Hiermee schakelt u multibyte-tekenondersteuning voor de rapportsuite uit. Als u multibyte-tekenondersteuning uitschakelt, gaat het systeem ervan uit dat de gegevens de ISO-8859-1-indeling hebben. Webpagina's moeten hun tekenset opgeven in de JavaScript-variabele <span class="varname"> charSet</span> . </p> <p>Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. </p> <p>Neem contact op met uw accountmanager of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ad hoc analyse voor deze suite activeren</span> </td> 
   <td colname="col2"> Hiermee kunt u deze rapportsuite weergeven wanneer u een ad-hocanalyse uitvoert. </td> 
  </tr> 
 </tbody> 
</table>

