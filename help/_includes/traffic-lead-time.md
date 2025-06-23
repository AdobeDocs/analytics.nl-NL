---
description: Adobe heeft een voorafgaande kennisgeving nodig voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.
title: Vereiste aanlooptijd voor verkeersstijgingen
feature: Report Suite Settings
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Vereiste aanlooptijd voor verkeersstijgingen

Adobe heeft een voorafgaande kennisgeving nodig voor nieuwe accountinstellingen, verkeerspikes en verkeersverhogingen. Hardware moet vooraf worden toegewezen om latentie en mogelijke negatieve effecten voor het gehele systeem tot een minimum te beperken.

>[!IMPORTANT]
>
>Adobe kan geen aanvragen voor plaatsaanduidingswijzigingen verwerken. Tenzij anders vermeld, moet u zo nauwkeurig mogelijk de voorgestelde aanlooptijd in acht nemen, inclusief het niet te vroeg verzenden van een waarschuwing.

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
   <td colname="col2"> <ul><li>Reeksen rapporteren met &lt; 100M hits/dag: geen melding vereist</li><li>Reeksen rapporteren met &gt; 100M hits/dag: 5 werkdagen</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Verkeerspiek of plotselinge permanente toename van het verkeer met meer dan 25% gemiddeld dagelijks volume in vergelijking met de laatste 30 dagen</td>
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

   * Reeks-id rapporteren
   * Geschatte resultaten per dag
   * Go-live datum

* De Alarm van de cliënt is ook nodig wanneer het verkeer vermindert of een rapportreeks wordt afgekeurd.

## De-Allocatie van de hardware toe te schrijven aan Ongerealiseerd Verkeer

Hardware voor nieuwe rekeningen, verkeersopstoppingen en verkeersstijgingen zullen worden gedesalloceerd als het geprojecteerde verkeer in het cliëntalarm niet binnen 4 weken van de &quot;Go levende datum&quot;bereikt. Als het verkeer nog wordt voorzien, moet een nieuw cliëntalarm als verkeersverhoging worden geproduceerd.
