---
description: U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.
title: Nieuwe rapportsuite - instellingen
topic: Beheerprogramma's
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 2%

---


# Nieuwe rapportsuite - instellingen

U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.

Beschrijvingen van de elementen die worden gebruikt wanneer [het creëren van een rapportreeks](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md).

>[!NOTE]
>
>De [Virtuele documentatie van de Reeks van het Rapport](/help/components/vrs/c-workflow-vrs/vrs-create.md) toont u hoe te om virtuele rapportreeksen tot stand te brengen.

<table id="table_F739FBD8DB8D409E916F12F61C5953D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Rapportsuite-id </span> </td> 
   <td colname="col2"> <p>Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan ook niet worden gewijzigd. </p> <p>Wanneer het creëren van veelvoudige rapportreeksen, zorg ervoor dat de noemende overeenkomst u gebruikt unieke rapportreeks IDs waarborgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Titel site</span> </td> 
   <td colname="col2">Identificeert de rapportsuite in <span class="wintitle"> Admin Tools</span>. Deze titel wordt ook gebruikt in <span class="wintitle"> de drop-down lijst van de Reeks </span> in de reeksheader van het Rapport. </td> 
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
   <td colname="col2"> <p>(Optioneel) Hiermee wordt de waarde <span class="wintitle"> Standaardpagina</span> doorgehaald uit URL's die worden aangetroffen. Als uw <span class="wintitle"> Popular Pages</span> rapport URLs eerder dan paginanamen bevat, verhindert dit het plaatsen veelvoudige URLs voor de zelfde Web-pagina. </p> <p>Bijvoorbeeld, zijn URLs<span class="filepath"> https://example.com</span> en <span class="filepath"> https://example.com/index.html</span> typisch de zelfde pagina. U kunt externe bestandsnamen verwijderen, zodat beide URL's worden weergegeven als <span class="filepath"> https://example.com</span> in uw rapporten. </p> <p>Als u deze waarde niet instelt, verwijdert Analytics automatisch de volgende bestandsnamen van URL's: <span class="filepath"> index.htm</span>, <span class="filepath"> index.html</span>, <span class="filepath"> index.cgi</span>, <span class="filepath"> index.asp</span>, <span class="filepath"> default.htm</span>, <span class="filepath"> default.html</span> 12/&gt; default.cgi</span>, <span class="filepath"> default.asp</span>, <span class="filepath"> home.htm</span>, <span class="filepath"> home.html</span>, <span class="filepath"> home.cgi&lt;a2 1/&gt;, en<span class="filepath"> home.asp</span>.<span class="filepath"></span> </span></p> <p>Als u het strippen van bestandsnamen wilt uitschakelen, geeft u een standaardpaginawaarde op die nooit voorkomt in uw URL's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Live-datum </p> </td> 
   <td colname="col2">Informeert Adobe van de datum dat u verwacht dat deze rapportsuite actief wordt. Als uw plaatsingsprogramma verandert, verstrek een bijgewerkte verkeersschatting gebruikend <span class="wintitle"> Permanent Verwacht Verkeer</span> hulpmiddel in <a href="/help/admin/c-traffic-management/traffic-management.md"> Verkeersbeheer</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschat aantal paginaweergaven per dag</span> </td> 
   <td colname="col2"> Hiermee wordt het geschatte aantal paginaweergaven aangegeven dat deze rapportsuite per dag moet ondersteunen. Grote verkeersvolumes vereisen een langer goedkeuringsproces. Om vertragingen bij de verwerking te voorkomen, moet u zo nauwkeurig mogelijk met deze schatting omgaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basisvaluta</span> </td> 
   <td colname="col2"> <p>Geeft de standaardvaluta aan die wordt gebruikt om alle monetaire gegevens op te slaan. Analytische rapportage converteert transacties in andere valuta's naar de basisvaluta, waarbij de huidige omrekeningskoers wordt gebruikt op het tijdstip dat de gegevens worden ontvangen. </p> <p> Analytische rapportage gebruikt de JavaScript-variabele <span class="varname"> currencyCode</span> om de valuta van een bepaalde transactie aan te duiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ondersteuning voor multi-byte tekens uitschakelen  </span> </td> 
   <td colname="col2"> <p>Hiermee schakelt u multibyte-tekenondersteuning voor de rapportsuite uit. Als u multibyte-tekenondersteuning uitschakelt, gaat het systeem ervan uit dat de gegevens de ISO-8859-1-indeling hebben. Webpagina's moeten hun tekenset opgeven in de JavaScript-variabele <span class="varname"> charSet</span>. </p> <p>Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. </p> <p>Neem contact op met uw accountmanager of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. </p> </td> 
  </tr>  
 </tbody> 
</table>

