---
description: Veldbeschrijvingen voor de algemene instellingen voor cookies die worden gebruikt voor de implementatie van dynamisch tagbeheer in Adobe Analytics.
keywords: Dynamic Tag Management;cookies;visitor id;visitor namespace;domain periods;fp domain periods;transaction id;cookie lifetime
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Cookies
uuid: 9c81ecbb-0f02-4c1a-a5a5-426cdea57f38
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Cookies

Veldbeschrijvingen voor de algemene instellingen voor cookies die worden gebruikt voor implementatie [!UICONTROL Dynamic Tag Management] in Adobe Analytics.

*`Property`* > Bewerken > Cookies

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bezoeker-id </td> 
   <td colname="col2"> <p>Unieke waarde die een klant in zowel de online als off-line systemen vertegenwoordigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naamruimte van bezoeker </td> 
   <td colname="col2"> <p>Variabele waarmee het domein wordt geïdentificeerd waarmee cookies worden ingesteld. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> Domeinperioden </td> 
   <td colname="col2"> <p>Het domein waarop het cookie Analytics <code> s_cc</code> en <code> s_sq</code> worden ingesteld door het aantal punten in het domein van de pagina-URL te bepalen. Deze variabele wordt ook gebruikt door bepaalde plug-ins voor het bepalen van het juiste domein voor het instellen van het cookie van de plug-in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Domeinperioden van het FP </td> 
   <td colname="col2"> <p>De <span class="term"> fpCookieDomainPeriods</span> variabele is voor koekjes die door JavaScript (<code> s_sq</code>, <code> s_cc</code>, stop-ins) worden geplaatst die inherent eerste-partijkoekjes zijn, zelfs als uw implementatie de derde <span class="filepath"> 2o7.net</span> of <span class="filepath"> omtr domeinen dc.net</span> gebruikt. </p> <p>Zie <a href="/help/implement/vars/config-vars/fpcookiedomainperiods.md"  > s.fpCookieDomainPeriods</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transactie-id </td> 
   <td colname="col2"> <p>De unieke waarde die een online transactie vertegenwoordigt die in off-line activiteit resulteerde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Cookie Lifetime </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de levensduur van een cookie. </p> </td> 
  </tr> 
 </tbody> 
</table>

