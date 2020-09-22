---
description: Veelgestelde vragen over de automatische configuratie van de Adobe Analytics-implementatie. De automatische configuratiemethode beheert de code AppMeasurement voor u.
keywords: Dynamic Tag Management;plug-ins;staging;effect on current settings;revision history;potential pitfalls;report suite id;currency code;tracking server;ssl tracking server;custom code;library management
solution: Experience Cloud,Analytics,Target
title: Veelgestelde vragen over de Adobe Analytics-tool
uuid: 8fcef893-e305-4a95-a033-9066a56b09cd
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 4%

---


# Veelgestelde vragen over de Adobe Analytics-tool

Veelgestelde vragen over de automatische configuratie van de Adobe Analytics-implementatie. De automatische configuratiemethode beheert de [!DNL AppMeasurement] code voor u.

<table id="table_A50D00E2C47A473B92DA800FB08FE640"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Waar moet ik mijn plug-ins plaatsen bij de implementatie van Adobe Analytics via DTM? </p> </td> 
   <td colname="col2"> <p> Als u DTM gebruikt om de toepassing handmatig te hosten, <code> s_code</code>kunnen plug-ins worden toegevoegd in dezelfde editor als de gehoste versie <code> s_code</code>, net als in een standaard Adobe Analytics-implementatie. </p> <p>Het is echter ook een optie om de plug-ins in de editor te plaatsen in de sectie Paginacode <span class="term"></span> aanpassen van de gereedschapsinstellingen. Beide uitvoeringsmethoden moeten even doeltreffend zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als ik configuratieveranderingen in de nieuwe versie van het hulpmiddel aanbreng, kan ik in het opvoeren testen alvorens aan productie te publiceren? </p> </td> 
   <td colname="col2"> <p>Ja. </p> <p>Alle veranderingen kunnen in het opvoeren worden getest enkel zoals u normaal alvorens aan een productiemilieu zou opstellen. Als u ervoor kiest om niet te publiceren, omdat er problemen optreden tijdens het opvoeren, blijft de productiecode functioneren zoals deze is gebeurd voordat de nieuwe integratie is uitgebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als ik van handconfiguratie (het gebrek dat voor bestaande hulpmiddelen plaatst) aan automatische configuratie overschakel, zullen mijn huidige montages worden beïnvloed? </p> </td> 
   <td colname="col2"> <p>Nee. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als ik van manueel bibliotheekbeheer aan Beheerd door Adobe overschakel, zullen mijn huidige montages of code worden beïnvloed? </p> </td> 
   <td colname="col2"> <p>Om het even welke gebruikerscode die u hebt gespecificeerd wordt beschreven met de bibliotheek van de basis <span class="keyword"> AppMeasurement</span> . U moet deze code naar de nieuwe sectie van de Code <span class="wintitle"></span> van de Pagina van de Douane aan het eind van de hulpmiddelconfiguratie verplaatsen zodat de code blijft uitvoeren. Met deze methode kan de <span class="keyword"> AppMeasurement</span> -bibliotheek afzonderlijk van de aangepaste code van de gebruiker worden beheerd (en bijgewerkt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zal de herzieningshistorie van het <span class="keyword"> Adobe Analytics</span> -instrument behouden blijven wanneer de nieuwe integratie wordt vrijgegeven? </p> </td> 
   <td colname="col2"> <p>Ja. </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie Adobe Analytics-gereedschap [](/help/implement/other/dtm/c-aa-tool/analytics-dtm.md) toevoegen voor configuratiegegevens.

## Potentiële valkuilen {#section_201BF9E0EB7D4BC2B72A617543C2030B}

Er is een kleine kans dat de integratie gegevensverzamelingsproblemen kan veroorzaken als u momenteel gebruikt [!DNL Adobe Analytics]. Deze problemen kunnen zich alleen voordoen als u uw bibliotheek naar productie publiceert na de release. (Productiecode blijft intact totdat publicatie plaatsvindt.)

Om deze problemen te voorkomen, moet u ervoor zorgen dat:

* ID&#39;s van rapportsuite worden correct ingevoerd in het gereedschap.
* ID&#39;s van rapportsuite in het gereedschap komen overeen met de id&#39;s in de [!DNL AppMeasurement] code.
* De valutacode, tekenset, trackingserver en SSL-configuratievelden voor trackingservers worden correct ingesteld met ondersteunde waarden.
* Aangepaste code wordt gedefinieerd in [!DNL Library Management].

