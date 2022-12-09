---
description: Adobe vereist voorafgaande kennisgeving voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.
title: Vereiste aanlooptijd voor traffic-toename
feature: Traffic Management
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
source-git-commit: 6f7f46b0fee46e572a65f639ea511478c0118f4e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Vereiste aanlooptijd voor traffic-toename

Adobe vereist voorafgaande kennisgeving voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.

De toewijzing van hardware wordt bepaald door waarschuwingen die via de gebruikersinterface voor rapporten en analyses worden verzonden.

>[!IMPORTANT]
>
>Adobe kan geen verzoeken van de &quot;placeholder&quot;verkeersverandering aanpassen. Tenzij anders vermeld, moet u zo nauwkeurig mogelijk de voorgestelde aanlooptijd in acht nemen, inclusief het niet te vroeg verzenden van een waarschuwing. Zie [Plan een verkeerspiek](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md) of [Permanente verkeersverhoging opgeven](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md).

Gebruik de volgende richtlijnen om te bepalen hoe ver van tevoren u een verkeersalarm moet voorleggen:

## Termijnen voor hardwaretoewijzing


<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Type wijziging </th>
   <th colname="col2" class="entry"> Leadtijd vereist </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Nieuwe accountinstellingen </td>
   <td colname="col2"> <ul><li>3 werkdagen</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Verkeerspiek of plotselinge permanente toename van het verkeer met gemiddeld 25% van het dagelijkse volume in vergelijking met de laatste 30 dagen</td>
   <td colname="col2"> <ul><li>Reeksen rapporteren met &lt; 100M hits/dag: Geen melding vereist</li><li>Reeksen rapporteren met &gt; 100M hits/dag: 5 werkdagen</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Verkeerspiek of plotselinge permanente toename van het verkeer met meer dan 25% van het gemiddelde dagelijkse volume in vergelijking met de laatste 30 dagen</td>
   <td colname="col2"> <ul><li>5 werkdagen</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Feiten voor feestdagen oktober - december </td>
   <td colname="col2"> <ul><li>Eén kalendermaand</li></ul> </td>
  </tr>
 </tbody>
</table>

Andere zaken die in overweging moeten worden genomen:

* Als u verscheidene rapportreeksen hebt die beginnen of stijgen die tot de bovengenoemde aantallen optellen, is de loodtijd van toepassing als som verkeer dat voor elk van hen wordt verwacht.
* Beschikbaar zijn van de volgende informatie om een verkeersverandering voor te leggen:

   * Set-id rapporteren
   * Geschatte resultaten per dag
   * Go-live datum

* De Alarm van de cliënt is ook nodig wanneer het verkeer vermindert of een rapportreeks wordt afgekeurd.

## De-Allocatie van de hardware toe te schrijven aan Ongerealiseerd Verkeer

Hardware voor nieuwe rekeningen, verkeersopstoppingen en verkeersstijgingen zullen worden gedesalloceerd als het geprojecteerde verkeer in het cliëntalarm niet binnen 4 weken van de &quot;Go levende datum&quot;bereikt. Als het verkeer nog wordt voorzien, moet een nieuw cliëntalarm als verkeersverhoging worden geproduceerd.
