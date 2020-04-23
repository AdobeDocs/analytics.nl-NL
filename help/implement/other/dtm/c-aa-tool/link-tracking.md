---
description: Veldbeschrijvingen in Dynamisch tagbeheer voor het bijhouden van koppelingen bij de implementatie van Analytics.
keywords: Dynamic Tag Management;link tracking;enable clickmap;track download links;download extensions;track outbound links;keep url parameters
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Koppeling bijhouden
uuid: 982b744b-5696-4c31-b1d1-410486b0eedd
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# Koppeling bijhouden

Veldbeschrijvingen in Dynamisch tagbeheer voor het bijhouden van koppelingen bij de implementatie van Analytics.

**[!UICONTROL  *`Property`*]** > **[!UICONTROL ![](assets/settings_gear.png)

Gereedschap Bewerken]* > **[!UICONTROL Link Tracking]**

<table id="table_F23FB0B284E74B66A107B1D69D22A51C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Element </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ClickMap inschakelen </td>
   <td colname="col2"> <p>Bepaalt of de bezoeker kaartgegevens klikt wordt verzameld. </p> <p>Zie <a href="../../../vars/config-vars/trackinlinestats.md">trackInlinestats</a>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Download-koppelingen volgen </td>
   <td colname="col2"> <p>Koppelingen naar downloadbare bestanden op uw site bijhouden. </p> <p>Zie <a href="../../../vars/config-vars/trackdownloadlinks.md">trackDownloadLinks</a>.</p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> Extensies downloaden </td> 
   <td colname="col2"> <p>Als uw site koppelingen bevat naar bestanden met een van de vermelde extensies, worden de URL's van deze koppelingen weergegeven in de rapportage. </p>Zie <a href="../../../vars/config-vars/linkdownloadfiletypes.md">linkDownloadFileTypes</a>. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> Uitgaande koppelingen bijhouden </td>
   <td colname="col2"> <p>Bepaalt of om het even welke geklikte verbinding een uitgangsverbinding is. </p> <p>Zie <a href="../../../vars/config-vars/trackexternallinks.md">trackExternalLinks</a>. </p> <p><b>Overwegingen bij toepassing voor één pagina: </b>Wegens de manier sommige websites van het KUUROORD worden gecodeerd, zou een interne verbinding aan een pagina op de plaats van het KUUROORD als het een uitgaande verbinding kunnen kijken. </p> <p>U kunt één van de volgende methodes gebruiken om uitgaande verbindingen van de plaatsen van het KUUROORD te volgen: </p>
    <ul id="ul_A4179633ED0644C3BA5F548A58CA4EC9">
     <li id="li_1959FBF14E42469FA8724B37EB58BC54"> <p>Als u geen uitgaande verbindingen van uw SPA wilt volgen, neem een ingang in <span class="wintitle"> nooit de sectie van het Spoor</span> op. </p> <p>Bijvoorbeeld: <span class="filepath"> https://testsite.com/spa/#</span> </p> <p>Alle #-koppelingen naar deze host worden genegeerd. Alle uitgaande verbindingen aan andere gastheren worden gevolgd, zoals <span class="filepath"> https://www.google.com</span>. </p> </li>
     <li id="li_37DD4D37887243FB928C9C04ACE9D39E"> <p>Als er sommige verbindingen zijn die u op uw SPA wilt volgen, gebruik <span class="wintitle"> altijd de sectie van het Spoor</span> . </p> <p>Als u bijvoorbeeld een <span class="filepath"> pagina met spa/#/about</span> hebt, kunt u "about" plaatsen in de sectie <span class="wintitle"> Altijd bijhouden</span> . </p> <p>De pagina "about" is de enige uitgaande koppeling die wordt bijgehouden. Eventuele andere koppelingen op de pagina (bijvoorbeeld <span class="filepath"> https://www.google.com</span>) worden niet bijgehouden. </p> </li>
    </ul> <p>Deze twee opties sluiten elkaar uit. </p> </td> 
  </tr>
  <tr>
   <td colname="col1"> URL-parameters behouden </td>
   <td colname="col2"> <p>Zoektekenreeksen blijven behouden. </p> <p>Zie <a href="../../../vars/config-vars/linkleavequerystring.md">linkLeaveQueryString</a>. </p> </td>
  </tr>
 </tbody>
</table>
