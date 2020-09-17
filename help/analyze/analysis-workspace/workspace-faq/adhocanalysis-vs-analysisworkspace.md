---
description: Vergelijkt Ad Hoc Analysis-terminologie en -taken met Analysis Workspace.
title: Analysis Workspace vergeleken met Ad Hoc Analysis
uuid: e4b3e40f-2b08-49a0-95f1-384d85c1640d
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 2%

---


# Analysis Workspace vergeleken met Ad Hoc Analysis

>[!IMPORTANT]
>
>Adobe verplaatst Ad Hoc Analysis naar het einde van zijn leven op 1 maart 2021. [Meer informatie](https://adobe.ly/discoverworkspace)

Vergelijkt Ad Hoc Analysis-terminologie en -taken met Analysis Workspace.

Analysis Workspace haalt veel van de Ad Hoc Analysis-functionaliteit naar de browserworkflow. Hoewel sommige terminologie en kenmerken tussen de producten hetzelfde blijven, zijn er in Analysis Workspace enkele nieuwe termen en benaderingen voor analyse ingevoerd.

Voor een technische vergelijking van de belangrijkste kenmerken en systeemvereisten tussen deze twee producten, ga [hier](https://docs.adobe.com/content/help/en/analytics/admin/admin-overview/analytics-product-comparison.html).

## Vergelijking van sleutelterminologie {#section_6109406B83B043A18E46D38F130B1D2E}

| Ad Hoc Analysis | Analysis Workspace |
|--- |--- |
| Project | Werkruimte of project |
| Werkruimte | Deelvenster |
| Rapport | Vrije-vormentabel |
| Grafiek/grafiek | Visualisatie |
| Hiërarchie: Project > Werkruimten > Rapporten | Hiërarchie: Project > Deelvensters > Tabellen |
| Sjablonen voor gerangschikte, trended- en totalen-rapporten | Visualisatie vrije-tabellen |
| Stroomsjabloon | Stroomvisualisatie |
| Uitval | Uitvalvisualisatie |

## Vergelijking van sleuteltaken {#section_F31446F1DFA742D794A30D713E223440}

<table id="table_90D4461F04F34D70844C5E3FBB0BBE44"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ad Hoc Analysis-taak </th> 
   <th colname="col2" class="entry"> Analysis Workspace-taak </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Afmetingen en segmenten toevoegen aan metrische kolommen </p> </td> 
   <td colname="col2"> <p>U kunt dimensionale items of segmenten als kolomkoppen opnemen om op eenvoudige wijze vergelijkende weergaven van metriek te maken. <a href="https://www.youtube.com/watch?v=P9W0hhIHhCs"  > Video: Werken met Dimension</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Segmenten toepassen </p> </td> 
   <td colname="col2"> <p>De segmenten zijn beschikbaar onder het de componentenmenu van het Segment, en kunnen op 3 plaatsen in Analysis Workspace worden toegepast: </p> 
    <ol id="ol_800D81FE2C84459B94B085C51E140330"> 
     <li id="li_F2E050902F9A4831BBA57F466E07DEAE">Op <b>paneelniveau</b>, dat op vele visualisaties in het paneel van toepassing is. Dit is vergelijkbaar met het toepassen van een segment op een werkruimte in ad-hoc. </li> 
     <li id="li_2D88E43E0161485C95B08DC3C593EFD9">As <b>rows in a table</b>. Dit is gelijkaardig aan het toevoegen van segmenten aan de sectie van de Bouwer van de Lijst "Rijen/Breedtes"in Ad Hoc. </li> 
     <li id="li_102E1A1DAA9247C08FC46C5AB3D78113">Als <b>kolommen van een tabel</b>. Dit is gelijkaardig aan het toevoegen van segmenten aan de sectie van de Bouwer van de Lijst "Kolommen"in Ad Hoc Analysis, of het toepassen van een segment op het rapportniveau in Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=QlUCdQDnni4"  > Video: Segmenten gebruiken in werkruimte</a> </p> <p><a href="https://www.youtube.com/watch?v=YjaRlJoQqRA"  > Video: Segmenten toepassen op een deelvenster</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijdelijke segmenten ("ad-hoc") maken </p> </td> 
   <td colname="col2"> <p>U kunt onmiddellijke, tijdelijke ("ad hoc") segmenten <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > in Analysis Workspace</a> tot stand brengen door afmetingspunten in de sectie van de segmentdaling bij de bovenkant van het paneel te slepen. Bovendien kunnen vervolgkeuzefilters worden toegevoegd aan de neerzetzone van het deelvenster om veel tijdelijke segmenten tegelijk te maken, waardoor beheerste projectinteracties mogelijk zijn. </p> <p><a href="https://www.youtube.com/watch?v=NKm7Rj23TtE"  > Video: Ad-hocsegmenten in Analysis Workspace</a> </p> <p><a href="https://www.youtube.com/watch?v=vpJywtsFVPI"  > Video: Vervolgfilters in Analysis Workspace</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumbereik en korreligheid kiezen </p> </td> 
   <td colname="col2"> <p>Datumbereiken en granulariteiten zijn beschikbaar in het menu van de component Time en kunnen op drie manieren worden gebruikt: </p> 
    <ol id="ol_8B57C8A840694A879B22B809C58E7482"> 
     <li id="li_58FAE6A87B494A5C9007CD35BB101608">Datumbereiken kunnen worden toegepast op kolommen/rijen en het geselecteerde datumbereik van het deelvenster overschrijven. Dit is gelijkaardig aan de waaiers van de het niveaudatum van het Rapport. </li> 
     <li id="li_85BB89EFF9C8466A992815BB7804EA37">Met Toepassen past u een datumbereik toe op alle visualisaties in een deelvenster. Dit is vergelijkbaar met een datumbereik voor Workspace in Ad Hoc Analysis. </li> 
     <li id="li_BC18564A8FBB48F4A522BCAC60838759">Met Toepassen op alle deelvensters past u een datumbereik toe op alle deelvensters in een Workspace-project. Dit is vergelijkbaar met een datumbereik van Project in Ad Hoc Analysis. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=ybmv6EBmhn0"  > Video: Werken met datums in Analysis Workspace</a> </p> <p><a href="https://www.youtube.com/watch?v=L4FSrxr3SDA"  > Video: Aangepaste datumbereiken</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fallout- en conversietrechter gebruiken </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md"  > In Analysis Workspace vindt u een overzicht van de valutamogelijkheden</a> in het menu van de component Visualisatie. Vergelijkbaar met Ad Hoc Analysis: </p> 
    <ol id="ol_625FF45AED4E403DBEE1A906282E8531"> 
     <li id="li_7B6C5F2682774641B82D2021786AE5C4">Bij een vlucht kan een bezoek of bezoeker worden doorgebracht. U kunt desgewenst ook "Alle bezoeken" opnemen. U kunt de uitval snel corrigeren door met de rechtermuisknop op het menu te klikken. </li> 
     <li id="li_CFBDDAB8E96A445DB0624640AEB25994">Dimensionele items kunnen worden aangesloten door een OR-operator (vergelijkbaar met groepen) en gebeurtenissen kunnen worden gebruikt in de trechter. </li> 
     <li id="li_6638E6A62C744A27B2C066E5F9EC62C0">De volgende stappen voor doorvallen en uitvallen kunnen ook worden weergegeven via het snelmenu. </li> 
    </ol> <p>Daarnaast biedt Fallout in Analysis Workspace ruimte voor <a href="/help/analyze/analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md"  > gemengde dimensies</a> in stappen, een verbetering ten opzichte van Ad Hoc Analysis. Gemengde afmetingen binnen stappen worden behandeld met een exploitant AND. </p> <p><a href="https://www.youtube.com/watch?v=VcrfHSyIoj8"  > Video: Uitvallen en trechters</a> </p> <p><a href="https://www.youtube.com/watch?v=EeLV366pQag"  > Video: Meerdere Dimension voor uitvallen gebruiken</a> </p> <p><a href="https://www.youtube.com/watch?v=H-oT3QZlyZQ"  > Video: Segmenten vergelijken in Fallout</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Stroom controleren (tekenen) </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/c-flow/flow.md"  > Stroomvisualisaties</a> zijn beschikbaar in Analysis Workspace onder het menu van de component Visualisatie. Vergelijkbaar met Ad Hoc Analysis: </p> 
    <ul id="ul_42D259310823496499F7D1474E1639AF"> 
     <li id="li_5DE6980EF66A49E58B8946A0422BC02C">De stroom kan een bezoek of een bezoeker overspannen. </li> 
     <li id="li_70A692266D32416BA3D70C1F8999F837">De belangrijkste statistieken worden getoond in termen van % wegmeningen. </li> 
    </ul> <p>Bovendien, staat de stroom voor <a href="/help/analyze/analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md"  > gemengde dimensies</a> toe en de capaciteit om een segment met de rechtermuisknop aan te klikken en te creëren, een verbetering ten opzichte van Ad Hoc Analysis. </p> <p>Op dit moment <b>kunnen gebruikers met Flow in Analysis Workspace geen</b> succesgebeurtenis kiezen. </li> 
    </ul> <p><a href="https://www.youtube.com/watch?v=3R1HTM7y_RM"  > Video: Overzicht van de Visualisatie van de Stroom</a> </p> <p><a href="https://www.youtube.com/watch?v=m1Wa6inC1rQ"  > Video: Multidimensionale stroom</a> </p> <p><a href="https://www.youtube.com/watch?v=XrJoNQy6RaQ"  > Video: Segmenten maken van stroom</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Oneindige uitsplitsingen uitvoeren </p> </td> 
   <td colname="col2"> <p>Met Analysis Workspace kunt u naar oneindig veel lager in de browser gaan. Segmenten en afmetingen kunnen worden gemengd. Items met meerdere dimensies kunnen tegelijk worden uitgesplitst door meerdere instellingen te selecteren en vervolgens naar een afbrekingsdimensie te slepen </p> <p><a href="https://www.youtube.com/watch?v=3mQ2HN7-lIc"  > Video: Verbeterde uitsplitsingen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Snel trendgegevens </p> </td> 
   <td colname="col2"> <p>Gegevens kunnen snel worden weergegeven door op het grafiekpictogram in de rapportrij te klikken. Bovendien worden deze snelle visualisaties gekoppeld aan de brontabel, zodat u van de ene waarde naar de andere in de tabel kunt klikken en de grafiek automatisch kunt bijwerken. </p> <p><a href="https://www.youtube.com/watch?v=kzlPjsBVYFQ"  > Video: Actieve koppeling met Dimension-grafiek</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportsets selecteren </p> </td> 
   <td colname="col2"> <p>U kunt meerdere rapportsuites toevoegen aan één project in Analysis Workspace.  </p> <p><a href="https://www.youtube.com/watch?v=kRPTBDNLJKk"  > Video: Meerdere rapportsets in werkruimte</a> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attribution IQ </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/attribution/overview.md"  > Met Attribution IQ</a> in Analysis Workspace kunt u vele nieuwe typen attributiemodellen toevoegen aan Vrije-vormtabellen, Visualisaties en Berekende metriek. Het omvat 10+ regel-gebaseerde en algoritmische modellen. </p>  <p><a href="https://www.youtube.com/watch?v=aYbGcQvAN1E"  > Video: Attribution IQ in Freeform-tabellen</a> </p> </td> 
  </tr>  
 </tbody> 
</table>

