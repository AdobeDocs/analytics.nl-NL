---
description: Adobe vereist voorafgaande kennisgeving voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.
title: Vereiste aanlooptijd voor traffic-toename
feature: Traffic Management
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 4%

---

# Vereiste aanlooptijd voor traffic-toename

Adobe vereist voorafgaande kennisgeving voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.

De toewijzing van hardware wordt bepaald door waarschuwingen die via de gebruikersinterface voor rapporten en analyses worden verzonden.

>[!IMPORTANT]
>
>Adobe kan geen verzoeken van de &quot;placeholder&quot;verkeersverandering aanpassen. Tenzij anders vermeld, moet u zo nauwkeurig mogelijk de voorgestelde aanlooptijd in acht nemen, inclusief het niet te vroeg verzenden van een waarschuwing. Zie [Plan een verkeerspiek](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) of [Permanente verkeersverhoging opgeven](/help/admin/c-traffic-management/t-traffic-permanent.md).

Gebruik de volgende richtlijnen om te bepalen hoe ver van tevoren u een verkeersalarm moet voorleggen:

## Termijnen voor hardwaretoewijzing

<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> DAGELIJKSE verkeersramingen (Hits) </th>
   <th colname="col2" class="entry"> <p>Leadtijd vereist (januari - oktober) </p> </th>
   <th colname="col3" class="entry"> <p>Leadtijd vereist (november - december) </p> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Tot 1.000.000 </td>
   <td colname="col2"> Geen aanlooptijd nodig </td>
   <td colname="col3"> Geen aanlooptijd nodig </td>
  </tr>
  <tr>
   <td colname="col1"> 1.000.000 - 5.000.000 </td>
   <td colname="col2"> Twee BEDRIJFSdagen </td>
   <td colname="col3" morerows="3"> Alle voor november-december beoogde verkeersverhogingen moeten uiterlijk op 1 september worden ingediend. Dit moet tijd toestaan om capaciteit indien nodig aan te kopen om vakantieverkeer op te vangen. </td>
  </tr>
  <tr>
   <td colname="col1"> 5.000.000 - 10.000.000 </td>
   <td colname="col2"> E??n kalenderweek </td>
  </tr>
  <tr>
   <td colname="col1"> 10.000.000 - 25.000.000 </td>
   <td colname="col2"> Twee kalenderweken </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Boven 25.000.000 </p> </td>
   <td colname="col2"> Een of meer maanden </td>
  </tr>
 </tbody>
</table>

Andere zaken die in overweging moeten worden genomen:

* Als u verscheidene rapportreeksen hebt die beginnen of stijgen die tot de bovengenoemde aantallen optellen, is de loodtijd van toepassing als som verkeer dat voor elk van hen wordt verwacht.
* Beschikbaar zijn van de volgende informatie om een verkeersverandering voor te leggen:

   * Set-id rapporteren
   * Geschatte resultaten per dag
   * Go-live datum

* De Alarm van de cli??nt is ook nodig wanneer het verkeer vermindert of een rapportreeks wordt afgekeurd.

## De-Allocatie van de hardware toe te schrijven aan Ongerealiseerd Verkeer

Hardware voor nieuwe rekeningen, verkeersopstoppingen en verkeersstijgingen zullen worden gedesalloceerd als het geprojecteerde verkeer in het cli??ntalarm niet binnen 4 weken van de &quot;Go levende datum&quot;bereikt. Als het verkeer nog wordt voorzien, moet een nieuw cli??ntalarm als verkeersverhoging worden geproduceerd.
