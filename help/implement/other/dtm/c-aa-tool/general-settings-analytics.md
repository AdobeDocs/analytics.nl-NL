---
description: Veldbeschrijvingen voor de algemene instellingen in dynamisch tagbeheer voor de implementatie van Adobe Analytics.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;general settings;eu compliance;character set;currency code;tracking server;ssl tracking server
title: Algemeen
topic: Developer and implementation
uuid: 93008719-6fb6-4e39-9a75-c937fe3247b9
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Algemeen

Veldbeschrijvingen voor de algemene instellingen in DTM, voor de implementatie van Adobe Analytics.

**[!UICONTROL <Property>]** > ![](assets/settings_gear.png) **[!UICONTROL Edit Tool]** > **[!UICONTROL General]**

<table id="table_DD8DA303698041D296DD5DB080AF7971"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Compatibiliteit met de EU voor <span class="keyword"> Adobe Analytics inschakelen </span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt het bijhouden van gegevens op basis van het privacycookie van de EU in- of uitgeschakeld. </p> <p>Wanneer een pagina wordt geladen, controleert het systeem of wordt een koekje genoemd <span class="filepath"> sat_track geplaatst (of de naam van het douanecookie die op de </span> Edit <span class="wintitle"> </span> pagina van het Bezit wordt gespecificeerd). Overweeg de volgende informatie: </p> 
    <ul id="ul_42A6D728F0BC4FBABB0069EFB66DCB01"> 
     <li id="li_227CB14326344AA3980F20C7EACF2AD2"> <p> Als het cookie niet bestaat of als het cookie bestaat en op iets anders is ingesteld dan <span class="term"> true </span>, wordt het laden van het gereedschap overgeslagen wanneer deze instelling is ingeschakeld. Betekenis, zal om het even welk gedeelte van een regel die het hulpmiddel gebruikt niet van toepassing zijn. </p> <p>Als een regel analyses bevat van EU-conformiteit op en code van derden en het cookie is ingesteld op <span class="term"> false </span>, wordt de code van derden nog steeds uitgevoerd. De analytische variabelen worden echter niet ingesteld. </p> </li> 
     <li id="li_1E74E02D7E4646ACA86D862A1D3C6679"> Als het cookie bestaat maar is ingesteld op <span class="term"> true </span>, wordt het gereedschap normaal geladen. </li> 
    </ul> <p>U bent verantwoordelijk voor het instellen van het cookie <span class="filepath"> sat_track </span> (of aangepaste benoemde cookie) op <span class="term"> false </span> als een bezoeker het cookie uitschakelt. U kunt dit bereiken met behulp van aangepaste code: </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"false"); 
     </code> </p> <p> U moet ook een mechanisme hebben om die cookie in te stellen op <span class="term"> true </span> als u wilt dat een bezoeker zich later kan aanmelden: </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"true"); 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tekenset </p> </td> 
   <td colname="col2"> <p>Geeft de beschikbare tekensets weer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Valutacode </p> </td> 
   <td colname="col2"> <p>Geeft de ondersteunde valutacodes voor selectie weer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Trackingserver </p> </td> 
   <td colname="col2"> <p>Het domein waarop de afbeeldingsaanvraag en het cookie worden geschreven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-traceringsserver </p> </td> 
   <td colname="col2"> <p>Het domein waarop de afbeeldingsaanvraag en het cookie worden geschreven. Wordt gebruikt voor beveiligde pagina's. Als deze niet is gedefinieerd, gaan SSL-gegevens naar <span class="term"> trackingServer </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datacenter </p> </td> 
   <td colname="col2"> <p>Het Adobe-datacenter dat wordt gebruikt voor gegevensverzameling. </p> </td> 
  </tr> 
 </tbody> 
</table>

