---
description: Op de pagina Methoden zoeken wordt aangegeven hoe verschillende rapporten over zoekmethoden kredieten ontvangen voor conversiesuccesgebeurtenissen op uw site. Als een zoekmachine bijvoorbeeld een bezoeker doorverwijst naar uw site die een aankoop doet, kunt u met Methoden zoeken opgeven hoe het zoekprogramma krediet voor de doorverwijzing ontvangt.
title: Zoekmethoden
feature: Admin Tools
uuid: 1053993e-7fc4-4874-84fa-367ecdcd7b45
exl-id: 58c4510c-2343-4b0a-9c09-5583f6d4250f
source-git-commit: 21029930b5cae6acb6bc6a59836ddc1ca33cb27e
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 2%

---

# Zoekmethoden

Op de pagina Methoden zoeken wordt aangegeven hoe verschillende rapporten over zoekmethoden kredieten ontvangen voor conversiesuccesgebeurtenissen op uw site. Als een zoekmachine bijvoorbeeld een bezoeker doorverwijst naar uw site die een aankoop doet, kunt u met Methoden zoeken opgeven hoe de zoekfunctie de verwijzingsvergoeding ontvangt.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Finding Methods]**

## Beschrijving van methoden zoeken {#section_8B6278DB75224EAB9F49D89A86274E8A}

<table id="table_8ABC1C9BD63F419082E4C4C69E401526"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De zoekmethode die u wilt wijzigen </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toewijzing </td> 
   <td colname="col2"> Geeft aan hoe een verwijzingsverzoek moet worden vergoed. Tot de ondersteunde toewijzingsopties behoren: <p> <span class="uicontrol"> Recentste (laatste): </span> Hiermee krijgt de laatste referentie alle krediet (wanbetaling). </p> <p> <span class="uicontrol"> Oorspronkelijke waarde: </span> Hiermee krijgt de eerste referentie alle krediet. </p> <p> <span class="uicontrol"> Lineair: </span>Verdeelt de kredietverlening gelijkelijk over alle referentie-instanties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verlopen na </td> 
   <td colname="col2"> 
    <ul id="ul_95EB224CAD164E9997B148E08AFA5F9B"> 
     <li id="li_C240460C21E14AA498D2EA62B9354710"> <span class="uicontrol"> Bezoek: </span> na een bepaalde periode van inactiviteit; gewoonlijk ongeveer 30 minuten. </li> 
     <li id="li_A3AE5438919E44B68DF99BEEA60C44EE"> <span class="uicontrol"> Paginaweergave: </span> Zodra een pagina op uw site wordt geopend. </li> 
     <li id="li_D5E20FEF313E4C5B99E7097CA175761A"> <span class="uicontrol"> Minuut: </span> Na 1 minuut inactiviteit. </li> 
     <li id="li_7315AA3EDDBB47A2BEA3C173881378A1"> <span class="uicontrol"> Aankoop: </span> Op het moment van aankoop. </li> 
     <li id="li_C0CF07581654472C9C9EC944E6F18164"> <span class="uicontrol"> Productweergave: </span> Wanneer een bezoeker een productwebpagina weergeeft. </li> 
     <li id="li_A1B04065150B407491D2EC78EC0DBDF5"> <span class="uicontrol"> Open winkelwagentje: </span> Wanneer een bezoeker een nieuwe online winkelwagentje opent. </li> 
     <li id="li_2AA50C6B9CB14500B67909CDF2AA700C"> <span class="uicontrol"> Afhandeling van winkelwagentje: </span> Wanneer een bezoeker uitcheckt met een online winkelwagentje. </li> 
     <li id="li_F58CE6FB8DCE4BE4927FFCB35A6D8E31"> <span class="uicontrol"> Winkelwagentje toevoegen: </span> Wanneer een bezoeker een product aan een online winkelwagentje toevoegt. </li> 
     <li id="li_AD7C846F46604FC48E0919ACB7515E14"> <span class="uicontrol"> Winkelwagentje verwijderen: </span> Wanneer een bezoeker een product uit een online winkelwagentje verwijdert. </li> 
     <li id="li_EB66E0563F564C9F985BE922DABD0A56"> <span class="uicontrol"> Open winkelwagentje: </span> Wanneer een bezoeker de inhoud van een online winkelwagentje weergeeft. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Alle zoekmethoden verlopen wanneer het bezoek eindigt. Als u ervoor kiest om te vervallen na een andere gebeurtenis (bijvoorbeeld Afhandeling starten), verloopt de zoekmethode wanneer Afhandeling starten plaatsvindt tijdens het bezoek. Als er tijdens het bezoek geen uitchecken van winkelwagentjes plaatsvindt, verloopt de zoekmethode nog steeds wanneer het bezoek afloopt.
