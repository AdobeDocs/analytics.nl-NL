---
description: 'null'
title: Veelgestelde vragen over projectconversie
uuid: 8e1bf0e9-ce0f-443a-bcfe-45d3e2c82b1c
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 3%

---


# Veelgestelde vragen over projectconversie

>[!IMPORTANT]
>
>Adobe verplaatst Ad Hoc Analysis naar het einde van zijn leven op 1 maart 2021. [Meer informatie](https://adobe.ly/discoverworkspace)

## Veelgestelde vragen over projectconversie {#topic_8231595303AD403E9322645A63632D57}

* [Bekende omzettingsproblemen](/help/analyze/ad-hoc-analysis/c-aha-project-converter/aha2aw-converter-faq.md#section_39C922A58B2E49C9877B363042801361)
* [Veelgestelde vragen over conversie](/help/analyze/ad-hoc-analysis/c-aha-project-converter/aha2aw-converter-faq.md#section_1E53FE373AF045978F939916124E194E)

## Bekende omzettingsproblemen {#section_39C922A58B2E49C9877B363042801361}

| Probleem | Beschrijving |
|--- |--- |
| Korreligheid bij minuten met onderverdelingen of kolommen | Wanneer er op kleine granulariteit onderbrekingen zijn toegepast of als er kolommen met kleine granulariteit voorkomen, kan het project niet naar Analysis Workspace worden geconverteerd.  Als tijdelijke oplossing kunt u de afbraak verwijderen bij kleine granulariteit en deze verwijderen uit kolommen en vervolgens het project omzetten. Vervolgens kunt u in Analysis Workspace indelingen toepassen op de kleinste granulariteit. |
| Interne berekende metrische waarde die samen met een kolomsegment wordt gebruikt | Als u intern berekende metrisch samen met een kolomsegment gebruikt, kan het project niet in Analysis Workspace worden omgezet. Om rond deze kwestie te werken, verwijder de interne berekende metriek uit het project vóór omzetting, dan voeg hen in Analysis Workspace opnieuw toe. |


## Veelgestelde vragen over conversie {#section_1E53FE373AF045978F939916124E194E}

<table id="table_48CC119236C94835A6A512E989BE4200"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>V: Worden Ad Hoc Analysis-functies niet ondersteund in Analysis Workspace?</b> </p> </td> 
   <td colname="col2"> <p>A: Het rapport Site-analyse wordt niet ondersteund in Analysis Workspace. Er zijn ook enkele kleine verschillen tussen andere visualisaties in Ad Hoc Analysis en Workspace. Raadpleeg de onderstaande vragen voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden tabelinstellingen geconverteerd?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_A645A004FB094A1593439A6607FE9A6B"> 
     <li id="li_033CA771F08A4BC3B0BC52CDCCA03FF4"><b>Aantal weergegeven</b>rijen: De werkruimte is gepagineerd om slechts 10 rijen (aanpasbaar om tot 400 rijen tegelijkertijd te tonen) te tonen, terwijl ad hoc tot 50.000 rijen op een pagina zal tonen. Merk op dat de gegevens nog in Werkruimte zijn, enkel gepagineerd aan een gebrek van 10 rijen. </li> 
     <li id="li_A8B8890149334032A56D8D1C0F8691EA"><b>Geavanceerd zoeken: </b>Meerdere opties voor gelijktijdig zoeken worden niet ondersteund, maar één zoekoptie (zoals <span class="wintitle"> Al deze woorden</span>, <span class="wintitle"> De exacte woordgroep</span>, <span class="wintitle"> Een van deze woorden</span>of <span class="wintitle"> Geen van deze woorden</span>) wordt omgezet in Analysis Workspace. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden grafieken/grafieken omgezet?</b> </p> </td> 
   <td colname="col2"> <p>A: Grafieken en grafieken worden in Workspace 'visualisaties' genoemd. </p> 
    <ul id="ul_597F5AB826EF434295D0CABD0313CAD5"> 
     <li id="li_AFB2805418034721A9519D999128C0A8"><b>Instellingen</b>: Visualisatie-instellingen zoals "Aantal items" of "Aantal balken" worden niet ondersteund in Workspace. </li> 
     <li id="li_D5C7EA8815344EDB8585CBB8E1AF583E"><b>Cirkeldiagram</b>: Geëxporteerd als een <a href="https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/donut.html"  > Donut</a> -visualisatie. Deze visualisatie in Workspace is beperkt tot 19 secties. </li> 
     <li id="li_91659FBFD77C4B3393D78447D658B7B4"><b>Bubbeldiagram</b>: Geëxporteerd als een <a href="https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/scatterplot.html"  > verstrooiingsperceel</a> . Standaard tekent het beelddiagram de eerste metrische waarde op de x-as en de tweede metrische waarde op de y-as. Als er slechts één metrische waarde is, zullen de borstelgrafieken in de visualisaties van de Lijn worden omgezet. </li> 
     <li id="li_FA05085FFB1747EBAF63616AC2B8D59C"><b>Histogram</b>: Biedt ondersteuning voor een andere emaillogica in Workspace dan in Ad Hoc Analysis. Daarom wordt het omgezet in een <a href="https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/bar.html"  > Bar</a> visualisatie. </li> 
     <li id="li_959499D20796459CA0F6BBC8F0A8D808"><b>Spreidingsperceel</b>: Bij geëxporteerde projecten in Analysis Workspace wordt de Y-as ingesteld als de eerste kolom, de X-as als de tweede kolom en de diameter als de derde kolom. </li> 
     <li id="li_14E06D7A5106405A89A07B44FFD9A92D"><b>Uitvaltabellen</b>: Als u doorhalings- of uitvaltabellen wilt weergeven, klikt u met de rechtermuisknop op het controlepunt en selecteert u een uitsplitsingsoptie. </li> 
     <li id="li_240F43C386F04111A7632A8FCA37832C"><b>Datumbereiken</b>op rapportniveau: De aangepaste waaiers van de rapportdatum zijn niet toegepast op de visualisaties van de Uitval. </li> 
     <li id="li_1FF5B3FD9E424E7190AF03FD4DD9D654"><b>Stroomrapport</b>: De stroom wordt naar een apart deelvenster verplaatst om datumbereiken en segmentatie te behouden. </li> 
     <li id="li_BE8F8F6EC2EA49E18EF52539BC1700E0"><b>Conversietrechter</b>: Wordt omgezet in een vrije-vormtabel omdat deze niet wordt ondersteund in Analysis Workspace. De Fallout-visualisatie is een aanbevolen vervanging voor de Conversie-trechter, maar het gedraagt zich op een iets andere manier. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden segmenten omgezet?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_15D5B17461E2402DB07DF8B0A10AAC37"> 
     <li id="li_CF9C3D235A664B15B21D9F89DC5EF7D3">De segmenten zijn intern aan het omgezette project (niet openbaar). U kunt ervoor kiezen om ze openbaar te maken, zoals u hier ziet: <p><img placement="inline"  src="assets/internal_segment.png" id="image_5942392F18E845A5B41C3DED59374E89" width="300px" /> </p> </li> 
     <li id="li_AE61DAEC5C0047349DD192EFEEDB0BF9">Ad Hoc Analysis-segmenten op werkruimteniveau worden toegepast op project-/werkruimteniveau in Workspace. </li> 
     <li id="li_B1559E2C18724FE189AF87D0BEF16811">Ad Hoc Analysis-segmenten op rapportniveau worden toegepast op het niveau van de tabelkolom in Workspace. </li> 
     <li id="li_0E6DF6D44EA448A4A212BA2BB8E342CF">Ad Hoc Analysis-tabelsegmenten worden toegepast op kolomniveau in Workspace. </li> 
    </ul> <p>U kunt segmenten bewerken in de <a href="https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html"  > Segment Builder</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden datumbereiken geconverteerd?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_A24AB597F3CE4847AF00D49A9A72A395"> 
     <li id="li_24FD18AF64114445939C4FBC03F2D406">De datumbereiken 'Laatste X dag' in Ad Hoc Analysis <i>sluiten</i> vandaag niet uit, terwijl Analysis Workspace <i>vandaag de dag wel van toepassing</i> is. Datumbereiken als 'laatste 90 dagen' komen dus mogelijk niet precies overeen tussen de gereedschappen. Gebruik aangepaste datumbereiken om dezelfde tijdsperiode op te halen in Analysis Workspace. </li> 
     <li id="li_AA4390470C494748B4B12030B1226720">Het datumbereik op werkruimteniveau van Ad Hoc Analysis wordt toegepast op project-/werkruimteniveau in Workspace. </li> 
     <li id="li_B8F0CDD413154856A315D087FEC4D418">Het rapport-vlakke de datumwaaier van Ad Hoc Analysis wordt toegepast op het niveau van de lijstkolom in Werkruimte. </li> 
    </ul> <p>U kunt uw aangepaste datumbereiken bewerken via <span class="uicontrol"> Analytics</span> &gt; <span class="uicontrol"> Components</span> &gt; <span class="uicontrol"> Date Ranges</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden berekende metriek omgezet?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_ADA380D5D09B4223AAE4853D4C64F679"> 
     <li id="li_010572F793F54680ABE64117DAB7E800">De berekende metriek zijn intern aan het uitgevoerde project (niet openbaar). U kunt ervoor kiezen om ze openbaar te maken door met de rechtermuisknop op de metrische waarde te klikken en op Openbaar <span class="uicontrol"></span>maken te klikken. <p><img placement="inline"  src="assets/calc_metric_internal.png" id="image_EA19BA55B161499CBDB9275A5C94BA90" width="200px" /> </p> </li> 
     <li id="li_930546EC8FEB432C8810FAF93556FC9A">Alle soorten berekende metriek worden gesteund voor de uitvoer. </li> 
     <li id="li_DFF7C6F8BB2344928D49194DA0F6EC38"><b>Toewijzingstypen</b>: Hoewel Analysis Workspace niet expliciet het toewijzingstype van een berekende metrische waarde weergeeft, wordt bij het exporteren het toewijzingstype gemaakt en aangepast dat in Ad Hoc Analysis aanwezig was. </li> 
    </ul> <p>U kunt het toewijzingstype in de <a href="https://docs.adobe.com/content/help/nl-NL/analytics/components/calculated-metrics/cm-overview.html"  > Berekende Metrische Bouwer</a> uitgeven door het Edit (potlood) pictogram te klikken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe worden de Globale Montages van Gegevens in Ad Hoc toegepast op omgezette projecten?</b> </p> </td> 
   <td colname="col2"> <p>Algemene gegevensinstellingen kunnen ertoe leiden dat hetzelfde tweemaal geëxporteerde project zich anders gedraagt: </p> 
    <ul id="ul_E3827883DD8045FAAB359D7E85E3EEFA"> 
     <li id="li_1056CA4813C44638BEB070228AE6914C"><b>Aantal herhalingsinstanties.</b> Wat op het moment van de export ook is ingesteld, wordt toegepast op het geëxporteerde project in Analysis Workspace. </li> 
     <li id="li_D5405E2862CF434CA82AA9DE000F4BBC"><b>Databronnen.</b> In Analysis Workspace worden alle analysegegevens weergegeven, inclusief gegevensbronnen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Als mijn Ad Hoc Analysis-project gepland is, wordt het programma dan omgezet naar Analysis Workspace?</b> </p> </td> 
   <td colname="col2"> <p>Nee, schema's worden niet omgezet. Open in Analysis Workspace het project dat u wilt plannen en ga naar <span class="uicontrol"> Delen</span> &gt; Bestand verzenden volgens schema <span class="uicontrol"></span> om een nieuw schema in te stellen. Vergeet niet uw geplande project in Ad Hoc Analysis te annuleren. </p> </td> 
  </tr> 
 </tbody> 
</table>

