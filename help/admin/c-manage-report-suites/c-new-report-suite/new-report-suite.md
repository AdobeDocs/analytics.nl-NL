---
description: U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.
title: Nieuwe rapportsuite - instellingen
feature: Report Suite Settings
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 2%

---

# Nieuwe rapportsuite - instellingen

U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.

Beschrijvingen van de elementen die worden gebruikt wanneer [een rapportenpakket maken](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md).

>[!NOTE]
>
>De [Documentatie van Virtual Report Suite](/help/components/vrs/c-workflow-vrs/vrs-create.md) toont u hoe te om virtuele rapportseries tot stand te brengen.

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
   <td colname="col2">Identificeert de rapportsuite in <span class="wintitle"> Admin Tools</span>. Deze titel wordt ook gebruikt in het dialoogvenster <span class="wintitle"> Rapportsuite</span> vervolgkeuzelijst in de koptekst van de suite. </td> 
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
   <td colname="col2"> <p>(Optioneel) Er wordt aantekening gemaakt van de <span class="wintitle"> Standaardpagina</span> waarde van URLs het ontmoet. Als uw <span class="wintitle"> Meest populaire pagina's</span> rapport bevat URL's in plaats van paginanamen. Met deze instelling worden meerdere URL's voor dezelfde webpagina voorkomen. </p> <p>De URL's<span class="filepath"> https://example.com</span> en <span class="filepath"> https://example.com/index.html</span> zijn doorgaans dezelfde pagina. U kunt externe bestandsnamen verwijderen, zodat beide URL's worden weergegeven als <span class="filepath"> https://example.com</span> in uw rapporten. </p> <p>Als u deze waarde niet instelt, verwijdert Analytics automatisch de volgende bestandsnamen van URL's: <span class="filepath"> index.htm</span>, <span class="filepath"> index.html</span>, <span class="filepath"> index.cgi</span>, <span class="filepath"> index.asp</span>, <span class="filepath"> default.htm</span>, <span class="filepath"> default.html</span>, <span class="filepath"> default.cgi</span>, <span class="filepath"> default.asp</span>, <span class="filepath"> home.htm</span>, <span class="filepath"> home.html</span>, <span class="filepath"> home.cgi</span>, en<span class="filepath"> home.asp</span>. </p> <p>Als u het strippen van bestandsnamen wilt uitschakelen, geeft u een standaardpaginawaarde op die nooit voorkomt in uw URL's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Live-datum </p> </td> 
   <td colname="col2">Informeert Adobe van de datum dat u verwacht dat deze rapportsuite actief wordt. Als uw plaatsingsprogramma verandert, verstrek een bijgewerkte verkeersschatting gebruikend <span class="wintitle"> Permanent verwacht verkeer</span> in <a href="/help/admin/c-traffic-management/traffic-management.md"> Verkeersbeheer</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschat aantal paginaweergaven per dag</span> </td> 
   <td colname="col2"> Hiermee wordt het geschatte aantal paginaweergaven aangegeven dat deze rapportsuite per dag moet ondersteunen. Grote verkeersvolumes vereisen een langer goedkeuringsproces. Om vertragingen bij de verwerking te voorkomen, moet u zo nauwkeurig mogelijk met deze schatting omgaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basisvaluta</span> </td> 
   <td colname="col2"> <p>Geeft de standaardvaluta aan die wordt gebruikt om alle monetaire gegevens op te slaan. Analytische rapportage converteert transacties in andere valuta's naar de basisvaluta, waarbij de huidige omrekeningskoers wordt gebruikt op het tijdstip dat de gegevens worden ontvangen. </p> <p> Voor analyserapportage worden de <span class="varname"> currencyCode</span> JavaScript-variabele om de valuta van een bepaalde transactie te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ondersteuning voor multi-byte tekens uitschakelen </span> </td> 
   <td colname="col2"> <p>Hiermee schakelt u multibyte-tekenondersteuning voor de rapportsuite uit. Als u multibyte-tekenondersteuning uitschakelt, gaat het systeem ervan uit dat de gegevens de ISO-8859-1-indeling hebben. Webpagina's moeten hun tekenset opgeven in het dialoogvenster <span class="varname"> charSet</span> JavaScript-variabele. </p> <p>Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken. </p> <p>Neem contact op met uw accountmanager of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. </p> </td> 
  </tr>  
 </tbody> 
</table>
