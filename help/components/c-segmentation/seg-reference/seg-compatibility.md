---
description: Niet zijn alle segmenten die in de Bouwer van het Segment worden gecreeerd compatibel met het Pakhuis van Gegevens. In deze tabel worden de ondersteunde functies weergegeven.
title: Verenigbaarheid van gegevensopslagsegment
topic: Segments
uuid: 370258c5-8614-4434-871c-41753ed77f5c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verenigbaarheid van gegevensopslagsegment

Niet alle segmenten die in de Segment Builder zijn gemaakt, zijn compatibel met [!DNL Data Warehouse]. In deze tabel worden de ondersteunde functies weergegeven.

<table id="table_BBB1DAFDF85041598FA4AF869172CF7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> De Werkruimte van de analyse, Rapporten &amp; Analyse, Ad hoc Analyse </th> 
   <th colname="col3" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Exclusief</b> </td> 
   <td colname="col2"> Ondersteund op elk niveau </td> 
   <td colname="col3"> Alleen in speciale gevallen op het hoogste niveau ondersteund </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Sequentiële segmenten</b> </td> 
   <td colname="col2"> Ondersteund </td> 
   <td colname="col3"> Niet ondersteund </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>AND en OR kunnen zonder grenzen worden gecombineerd</b> </td> 
   <td colname="col2"> Ondersteund </td> 
   <td colname="col3"> Enkele beperkingen. Zie *opmerking* onder tabel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geneste containers</b> </td> 
   <td colname="col2"> Ondersteund </td> 
   <td colname="col3"> Sommige beperkingen (ze moeten het bereik verkleinen, bijvoorbeeld bezoekers kunnen hits bevatten, maar niet andersom) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Afmetingen</b> </td> 
   <td colname="col2">Sleep een dimensie naar het veld <span class="uicontrol"> Definities</span> van Segment Builder om meer te weten te komen over de productcompatibiliteit. Deze dimensies worden bijvoorbeeld alleen ondersteund in Analysatiewerkruimte, Rapporten en Analyse en Ad hoc-analyse: 
    <ul id="ul_BD708CC3A16743F49F998D1046EC70A3"> 
     <li id="li_240DA619D50B4336ACD9117BF59AF10A">Entry-server </li> 
     <li id="li_222D4D4116674EF8A52945CCB9C78719">Invoercategorie </li> 
     <li id="li_5A43C846E2EA4EFCB892DE9E0607C68C">Invoerdatum </li> 
     <li id="li_8E9CABBE04FC4A7A9A5D2BDD34AD3C87">Alle zoekpaginanummers </li> 
    </ul> </td> 
   <td colname="col3"> Sleep een dimensie naar het veld <span class="uicontrol"> Definities</span> van Segment Builder om meer te weten te komen over de productcompatibiliteit. Deze afmetingen worden bijvoorbeeld alleen ondersteund in Data Warehouse: 
    <ul id="ul_61A5B314CCCF497DB0385324E3309E22"> 
     <li id="li_1254089BDFAE4E0F8E51CB1511BBBF53">IP-adres </li> 
     <li id="li_D8E040F77A8C46A084547F4FE685CB10">Pagina-URL </li> 
     <li id="li_4C79AE900CF6458780C124143DC6FA5B">Bezoeker-id </li> 
     <li id="li_4EC10645DE9740609D8DDFD4F668FE67">Experience Cloud Visitor ID </li> 
    </ul> <p>De volgende afmetingen <b>kunnen niet in de segmenten van het Pakhuis van Gegevens </b>worden gebruikt: </p> 
    <ul id="ul_FE143F6D1ABF45DAA444E1B5691C7D4F"> 
     <li id="li_E77F3CC45BA04674B857FE5AB19D56F1">Alle zoekpaginanummers </li> 
     <li id="li_95E1549C13F14BA0B32686401EE78E31">AM/PM </li> 
     <li id="li_6F1C8FC2E7674A0CA14B70B65784D896">Dag van Maand </li> 
     <li id="li_79D1A91D741D4CCC937D07906D71F964">Weekdag </li> 
     <li id="li_4008565353084611BD782B98D50C0611">Dag van het Jaar </li> 
     <li id="li_F87D78F125874087BFF74FAAE2BA46F5">Zakelijke eenheid voor toegang </li> 
     <li id="li_53DA4E64C6714CFF90D164245D01C16A">Item (alle afmetingen beginnen met item, behalve invoerpagina) </li> 
     <li id="li_7F26B0E54A4A48319F31D8FC499D1CF2">Afsluiten (alle afmetingen die beginnen met Afsluiten, behalve Koppeling afsluiten en Pagina afsluiten) </li> 
     <li id="li_1877D2D8A95B43F29CAA426BF2FE4996">Hiërarchie (alle afmetingen beginnen met hiërarchie) </li> 
     <li id="li_DF0BCC63ED274ABEA1C5A28274936310">Hit Depth </li> 
     <li id="li_98BE56213E1A4FD28D4858D53C46D23E">Type hit </li> 
     <li id="li_52ECB31657DF4180BDB9C8D21CC74313">Uur Dag </li> 
     <li id="li_93716207F2614822ACB84100B35D27BC">Maand van jaar </li> 
     <li id="li_FFC8E1F7092C4876A7E9F2365CC234B9">Pagina's niet gevonden </li> 
     <li id="li_7A070C8E0F664F5AB554555B17D0E4E6">Betaalde zoekopdracht </li> 
     <li id="li_12228C18BF90463C8D8394FB810843D3">Kwartaal van jaar </li> 
     <li id="li_1833B6E2011C4757A60CAA2C98B35AFA">Geretourneerde frequentie </li> 
     <li id="li_39154CD74A534D9AA09C701FE1E2C521">Bezoeken van één pagina </li> 
     <li id="li_84BDE34DD577488881E8842D2DE72D3C">Tijd voorafgaand aan gebeurtenis </li> 
     <li id="li_552BE3414CC949B3B24BE99298945874">Tijd besteed op pagina - Emmerd </li> 
     <li id="li_33D815E04CB3493C82BE33E958C2D7B9">Tijd besteed per bezoek - Emmerd </li> 
     <li id="li_76F2BB88B8CD456DB50D04F36BB7854B">Reden voor reeksspatiëring </li> 
     <li id="li_07345E08D0584CEC99128A0542587019">VS </li> 
     <li id="li_3D6BD9E927334B9BBC29E602D1103F7A">Weekdag/Weekend </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Segmentstapeling</b> </td> 
   <td colname="col2"> Ondersteund </td> 
   <td colname="col3"> Niet ondersteund </td> 
  </tr> 
 </tbody> 
</table>

*Opmerking: Data Warehouse biedt geen ondersteuning voor alle gevallen waarin een`exclusion`of een`without`container wordt gebruikt`AND/OR`. Wanneer het gebruiken van een dergelijke combinatie, slechts die segmenten die als`A AND NOT B`, (of **omvat dit kenmerk**en **sluit dit kenmerk**uit) kunnen worden herschreven worden gesteund in het Pakhuis van Gegevens.*
