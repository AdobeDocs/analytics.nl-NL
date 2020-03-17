---
description: U kunt filteren op afmetingen die u toevoegt aan het raster Rijlabels. Filters beperken de gegevens die door aanvragen worden geretourneerd en kunnen worden toegepast vanuit de indelingen Draaien of Aangepast. Wanneer u dimensie het filtreren van de Lay-out van de Draaiende vormt, kunt u het aantal ingangen van cel extra specificeren.
title: Overzicht van filterafmetingen
topic: Report builder
uuid: c54d5add-f278-476d-8f14-73f1c2e37671
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Overzicht van filterafmetingen

U kunt filteren op afmetingen die u toevoegt aan het raster Rijlabels. Filters beperken de gegevens die door aanvragen worden geretourneerd en kunnen worden toegepast vanuit de indelingen Draaien of Aangepast. Wanneer u dimensie het filtreren van de Lay-out van de Draaiende vormt, kunt u het aantal ingangen van cel extra specificeren.

De geselecteerde filtervorm wordt bevolkt gebaseerd op het element &amp; metrisch dat in het verzoek van de rapportbouwer wordt geselecteerd.

## Filter definiëren - waarden en speciale tekens {#section_15840216A4044C40974945FAA435AD93}

Informatie over filters in het deelvenster **[!UICONTROL Most Popular Filter]** > **[!UICONTROL Define Filter]** .

![](assets/define_filter.png)

De volgende tabellen bevatten voorbeelden en informatie over filters:

<table id="table_8AC3A26FF02143DBA949B30F2A46CF11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Filter </th> 
   <th colname="col02" class="entry"> Beschrijving </th> 
   <th colname="col2" class="entry"> Voorbeeldfilter </th> 
   <th colname="col3" class="entry"> Resultaten afstemmen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bevat alle termen </p> </td> 
   <td colname="col02"> <p>Bevat elke door spaties gescheiden waarde in willekeurige volgorde. </p> </td> 
   <td colname="col2"> <p>a ter </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> a</span>cand <span class="term"> b a c</span>enzovoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bevat een term </p> </td> 
   <td colname="col02"> <p>Bevat ten minste een van de filters (gescheiden door spaties). </p> </td> 
   <td colname="col2"> <p>A B C </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> A1</span>, <span class="term"> B2</span>, <span class="term"> C3</span>, maar niet met <span class="term"> D4</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bevat de woordgroep </p> </td> 
   <td colname="col02"> <p>Bevat het zoekfilter en mogelijk andere termen. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> abc</span> en <span class="term"> abc def</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bevat geen term </p> </td> 
   <td colname="col02"> <p>Retourneert alles tenzij het een waarde bevat die u invoert. </p> </td> 
   <td colname="col2"> <p>a ter </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> d e f</span> , maar niet <span class="term"> c d e f</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bevat niet de uitdrukking </p> </td> 
   <td colname="col02"> <p>Retourneert alles dat je uitdrukking niet bevat. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Omvat niet <span class="term"> abc</span>, <span class="term"> abc def</span> en komt overeen met <span class="term"> def</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gelijk </p> </td> 
   <td colname="col02"> <p>Retourneert een exacte overeenkomst. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p> <span class="term"> abc</span> wordt teruggegeven en niets anders . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Is niet gelijk aan </p> </td> 
   <td colname="col02"> <p>Retourneert alles wat niet exact overeenkomt met uw invoer. </p> </td> 
   <td colname="col2"> <p>a </p> </td> 
   <td colname="col3"> <p>Komt niet overeen met <span class="term"> a</span>. </p> <p>Komt overeen met <span class="term"> a b c</span>. </p> <p>Komt overeen <span class="term"> met abc</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begint met </p> </td> 
   <td colname="col02"> <p>Retourneert resultaten die beginnen met een specifieke waarde. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> abcd</span> maar niet <span class="term"> 1abc</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eindigt met </p> </td> 
   <td colname="col02"> <p>Retourneert resultaten die met de specifieke waarde eindigen. </p> </td> 
   <td colname="col2"> <p>xyz </p> </td> 
   <td colname="col3"> <p>Komt overeen met <span class="term"> wxyz</span> maar niet <span class="term"> wxyz0</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geavanceerd (speciale tekens) </p> </td> 
   <td colname="col02"> <p>Hiermee kunt u tekens regex: </p> <p> <code> "", ^, -, *, $, | </code> </p> </td> 
   <td colname="col2"> <p>"^Home*Page$"| sport </p> </td> 
   <td colname="col3"> <p> Hiermee definieert u een filter dat begint met <span class="term"> Home</span>, vervolgens op nul of meer tekens zoekt en vervolgens eindigt met <span class="term"> Pagina</span>. </p> <p>Ook elke pagina met <span class="term"> sporten</span> erin. </p> <p>Een paar voorbeelden komen overeen: </p> 
    <ul id="ul_72D76C5AFEAF405E8A0E4E3C604D10AE"> 
     <li id="li_4D490059B667450DA8A0103167C7B391">HomePage </li> 
     <li id="li_1351619156274092AEB2771D882AD357">Home en (andere tekens) Pagina </li> 
     <li id="li_940EAA99A8CF49308E8471065EB317B1">Thuissport </li> 
     <li id="li_50A895F14A454BE9BF06EE0F07F99B3B">sportpagina </li> 
     <li id="li_F3CE0D07941D4C2485D2DE0B73E00677">sport </li> 
     <li id="li_E84C15C061824A5D922D9900392F2996">xyz Sport abc </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_8BBB06C8860745DEA41B39673699DC0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Speciale tekens </th> 
   <th colname="col2" class="entry"> Doel </th> 
   <th colname="col3" class="entry"> Notities </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> " " </td> 
   <td colname="col2"> Gelijk </td> 
   <td colname="col3"> <p>Niet ontsnapt tenzij het niet met een ander citaat wordt gepareerd. 17- <span class="term"> inch beeldscherm</span> is bijvoorbeeld geen woordgroep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> * </td> 
   <td colname="col2"> Jokerteken </td> 
   <td colname="col3"> <p>Hetzelfde als de asterisk die wordt gebruikt in een reguliere expressie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ^ </td> 
   <td colname="col2"> Begint met </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> $ </td> 
   <td colname="col2"> Eindigt met </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> - </td> 
   <td colname="col2"> Niet </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> | </td> 
   <td colname="col2"> of </td> 
   <td colname="col3"> <p>Alleen ondersteund in het filter <span class="term"> Geavanceerd (speciale tekens)</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>
