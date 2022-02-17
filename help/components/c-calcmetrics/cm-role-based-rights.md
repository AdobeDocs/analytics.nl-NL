---
description: De berekende metrierechten verschillen tussen gebruikers op beheerdersniveau en gebruikers zonder beheerdersrechten.
title: Berekende metrieke op rol-gebaseerde rechten
feature: Calculated Metrics
exl-id: 018d9ef5-5a6f-4ebc-a241-c1291ba6b561
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 2%

---

# Berekende standaard: op rol gebaseerde rechten

De berekende metrierechten verschillen tussen gebruikers op beheerdersniveau en gebruikers zonder beheerdersrechten.

<table id="table_13F72FD90C964B86BD4B51E6F51ED292"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col02" class="entry"> Maken </th> 
   <th colname="col2" class="entry"> Delen </th> 
   <th colname="col3" class="entry"> Weergeven/beheren </th> 
   <th colname="col4" class="entry"> Goedkeuren </th> 
   <th colname="col5" class="entry"> Toepassen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Gebruikers op beheerniveau</b> </td> 
   <td colname="col02"> Beheerders kunnen berekende metriek maken en in de Admin Console productprofielen maken om de rechten van gebruikers om berekende metriek te maken te beperken. </td> 
   <td colname="col2"> Kan met volledig bedrijf, met gebruikersgroepen, en met individuele gebruikers delen. </td> 
   <td colname="col3"> <span class="keyword"> Rapporten en analyses</span>: Kan weergeven/bewerken/verwijderen/enzovoort. hun eigen berekende cijfers en die van andere gebruikers. <p> <span class="keyword"> Report Builder </span>: Kan weergeven/bewerken/verwijderen/enzovoort. haar eigen berekende maatstaven en de maatstaven die ermee worden gedeeld. </p> </td> 
   <td colname="col4"> Kan berekende metriek goedkeuren als canonicaal. </td> 
   <td colname="col5"> Kan berekende waarden toepassen in de hele organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gebruikers op niet-beheerniveau</b> </td> 
   <td colname="col02"> Standaard kunnen gebruikers berekende metriek maken. Deze rechten kunnen echter door beheerders worden beperkt. </td> 
   <td colname="col2"> Kan alleen met individuele gebruikers delen </td> 
   <td colname="col3"> Kan weergeven/bewerken/verwijderen/enzovoort. alleen hun eigen berekende maatstaven. <p>De gebruikers niet-admin moeten toegang tot alle componentengebeurtenissen hebben om gedeelde metriek (de toestemmingen in de console Admin worden nog afgedwongen) te kunnen zien. </p> <p>Als een dashboard of een gepland rapport met een niet-admin gebruiker wordt gedeeld en zij metrisch niet hebben die met hen wordt gedeeld, zal het rapport met metrisch lopen toegepast (veronderstellend zij toestemmingen hebben om de gebeurtenissen te bekijken). Nochtans, zullen zij niet de definitie kunnen zien of metrisch uitgeven. </p> </td> 
   <td colname="col4"> alleen goedgekeurde berekende metriek kunnen gebruiken; kan niet markeren als goedgekeurd. </td> 
   <td colname="col5"> Kan hun eigen berekende metriek en segmenten toepassen die met hen zijn gedeeld. </td> 
  </tr> 
 </tbody> 
</table>
