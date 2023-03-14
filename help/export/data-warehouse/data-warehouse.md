---
description: Het entrepot van gegevens verwijst naar het exemplaar van de gegevens van Analytics voor opslag en douanerapporten, die u kunt lopen door de gegevens te filtreren. U kunt rapporten vragen om geavanceerde gegevensrelaties van onbewerkte gegevens weer te geven op basis van uw unieke vragen. De rapporten van het gegevenspakhuis worden gemaild of via FTP verzonden, en kunnen tot 72 uren aan verwerking vergen. De verwerkingstijd is afhankelijk van de complexiteit van de query en de hoeveelheid gevraagde gegevens.
title: Overzicht van Data Warehouse
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 1%

---

# Overzicht van Data Warehouse

Data Warehouse verwijst naar de kopie van analysegegevens voor opslag en aangepaste rapporten, die u kunt uitvoeren door de gegevens te filteren. U kunt rapporten vragen om geavanceerde gegevensrelaties van onbewerkte gegevens weer te geven op basis van uw unieke vragen. De rapporten van het gegevenspakhuis worden gemaild of via FTP verzonden, en kunnen tot 72 uren aan verwerking vergen. De verwerkingstijd is afhankelijk van de complexiteit van de query en de hoeveelheid gevraagde gegevens.

Adobe laat Data Warehouse voor beheerder-vlakke gebruikers slechts, voor specifieke rapportreeksen toe. (Het kan voor globale en kindrapportsuites worden toegelaten, maar niet voor rollup rapportsuites.) De beheerder kan een groep tot stand brengen die toegang tot Data Warehouse heeft, en dan gebruikers niet-beheerderniveau aan die groep associëren.

In Data Warehouse wordt elk bestand dat groter is dan 1 MB, automatisch gecomprimeerd. De maximale grootte van e-mailbijlagen is 10 MB.

Data Warehouse kunnen een onbeperkt aantal rijen verwerken in één aanvraag voor afzonderlijke geplande en gedownloade rapporten.

>[!NOTE]
>
>Data Warehouse rapporteert de eerste waarde die in de verslagperiode is aangetroffen.

>[!IMPORTANT]
>
>Bij segmentering op geclassificeerde waarden behandelen Analysis Workspace en Data Warehouse &#39;ongespecificeerde&#39; waarden anders. &#39;Niet opgegeven&#39; in Workspace verwijst naar waarden die niet zijn geclassificeerd, terwijl &#39;Niet opgegeven&#39; in Data Warehouse verwijst naar waarden die u hebt geclassificeerd als &#39;Niet opgegeven&#39;.

## Beschrijvingen van Data Warehouse-aanvragen {#section_F21C78ED36884C389C852E876AF5CDE8}

In deze tabel worden de velden en opties in het dialoogvenster [!UICONTROL Data Warehouse Request] tab.

<table id="table_7325A2466866460E8B0AF7D696152713"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Naam aanvraag</span> </td> 
   <td colname="col2"> Identificeert het verzoek. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Datum van rapportage</span> </td> 
   <td colname="col2"> <p>De datum en granulariteit van het verzoek. </p> 
    <ul id="ul_C00F4529BD9E4113B517A61751B1DD5C"> 
     <li id="li_4D7C26812DF94ED7B64F985309541F46"> <span class="wintitle"> Aangepast</span>: Een datumbereik dat u configureert in de kalender. </li> 
     <li id="li_2B272087006847148A936350D1B2D523"> <span class="wintitle"> Voorinstelling</span>: Een vooraf ingesteld bereik. Het vooraf ingestelde bereik is relatief ten opzichte van de rapportdatum. </li> 
     <li id="li_745989965BB94D489FF7046587E13C42"> <span class="wintitle"> Korreligheid</span>: De tijdsgranulariteit. Geldige waarden zijn None, Hour, Day, Week, Month, Quarter en Year. </li> 
    </ul> <p>Data Warehouse die over virtuele rapportreeksen rapporteert steunt de alternatieve tijdzone die op de virtuele rapportreeks wordt gevormd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Beschikbare segmenten</span> </td> 
   <td colname="col2"> <p>Hiermee kunt u het deel van de bezoekerspopulatie selecteren dat u wilt onderzoeken en complexe segmenten genereren. U kunt pre-gevormde segmenten laden, nieuwe segmenten tot stand brengen, en de componenten van het opslagsegment in een bibliotheek aan gebruik in de bouw van extra segmenten. </p> <p>U kunt nu segmenten stapelen. Wanneer het selecteren van veelvoudige segmenten, tonen het voorproefgebied, de Manager van het Verzoek, en popup van het Detail van het Verzoek een komma-gescheiden lijst van namen (b.v., Segment1, Segment2). </p> <p>Zie de <a href="/help/components/segmentation/seg-home.md"> Segmenteringsgids</a> voor meer informatie . </p> <p>Opmerking: U kunt niet zowel een segmentfilter als een uitsplitsing op hetzelfde segment opnemen, in hetzelfde Data Warehouse-rapport. Dit leidt tot een fout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Uitsplitsingen</span> </td> 
   <td colname="col2"> <p>Hiermee kunt u gegevens categoriseren met behulp van uitsplitsingen. Segmenten en indelingen verschillen in die zin dat een segment gegevens uit een gegevensset filtert, terwijl een indeling gegevens over alle geldige waarden voor de uitsplitsing onderverdeelt. </p> U kunt een rapport door één of meerdere segmenten ook onderverdelen. Nochtans, kunt u niet zowel een segmentfilter als een mislukking op het zelfde segment, in het zelfde rapport van de Data Warehouse omvatten. Dit leidt tot een fout. <p> Gebruik bijvoorbeeld segmenten om een geslacht uit de gegevensset te verwijderen en gebruik een indeling om gegevens te zien gescheiden door geslacht. </p> <p>Wanneer een verzoek van de Data Warehouse met veelvoudige multi-waardedimensies (b.v., diverse Mobiele Rapporten) wordt voorgelegd, kan een exponentieel aantal rijen uit één enkele klap worden geproduceerd. Het aantal rijen dat uit één enkele klap kan worden uitgevoerd wordt beperkt tot 100 (eerder 1.000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Cijfers</span> </td> 
   <td colname="col2">Hiermee kunt u metrische gegevens toevoegen waarop u wilt rapporteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Metrische sortering</span> </td> 
   <td colname="col2">Verstrekt gerangschikte verdelingsrapporten, die door dalende metrische waarde worden gesorteerd, gelijkend op wat in de het gebruikersinterface van Rapporten &amp; van de Analyse, Data Workbench, enz. wordt getoond. <a href="/help/export/data-warehouse/sorting-by-metric.md"  > Meer...</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Levering plannen</span> </td> 
   <td colname="col2"> <p>Hiermee kunt u aanvragen voor automatische levering met geselecteerde intervallen plannen, of als een eenmalig rapport. Als u de standaardindeling gebruikt, wordt het rapport in een e-mail verzonden als CSV-bestand. </p> <p>Als u het datumbereik wilt toevoegen, neemt u <span class="filepath"> %R</span> in de bestandsnaam. Deze waarde vertegenwoordigt de datumwaarden die in het rapport worden gevraagd. Als u bijvoorbeeld gegevens aanvraagt van 1 mei 2013 tot en met 7 mei 2013, <span class="filepath"> %R</span> bevat een bestandsnaam met het datumbereik 20130501 - 20130507. </p> </td> 
  </tr> 
 </tbody> 
</table>
