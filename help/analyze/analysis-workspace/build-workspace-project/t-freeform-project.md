---
description: Maak een project en voeg componenten (afmetingen, metriek, segmenten, datumbereiken) toe aan het deelvenster Vrije vorm.
keywords: Analysis Workspace
title: Een Workspace-project maken
topic: Reports and analytics
uuid: c1def77a-a76e-4699-9feb-1ede5b70b7ba
translation-type: tm+mt
source-git-commit: b952ea84a63cdb73684e8765dde6551785c0d6c1
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 14%

---


# Een Workspace-project maken

Maak een project en voeg componenten (afmetingen, metriek, segmenten, datumbereiken) toe aan het deelvenster Vrije vorm.

Dit artikel vertrouwt u met de de interfaceelementen van Analysis Workspace en toont hoe te om een project tot stand te brengen.

## Een project maken

1. Specificeer gebruikerstoestemming om projecten tot stand te brengen en te leiden.

   Voordat u een Analysis Workspace-project kunt maken of beheren, moeten beheerders u toevoegen aan een groep waarvoor de **[!UICONTROL Create / Curate Projects in Analysis Workspace]** machtiging is ingeschakeld, of aan de **[!UICONTROL All Report Access]** gebruikersgroep. ( **[!UICONTROL Admin]** > **[!UICONTROL User Management]** > [Groups](https://docs.adobe.com/content/help/nl-NL/analytics/admin/user-product-management/user-groups/groups.html)).

1. Klik in het [!DNL Experience Cloud]deelvenster op **[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**.

   ![](assets/analysis_workspace_menu.png)

   Alternatief, ga een voorwaartse schuine streep (/) in om de bar van het rapportonderzoek te openen, dan type *`workspace`*.

   ![](assets/analysis-app-search.png)

1. Klik op **[!UICONTROL Create New Project]**.

   U kunt kiezen of u een project wilt maken van

* Een leeg project (standaard). Zie hieronder voor instructies.
* Een standaardsjabloon. Deze sjablonen worden gemaakt door Adobe en uit de doos te verzenden. Zie [Sjablonen voor instructies](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md)
* Een aangepaste sjabloon. Deze sjablonen worden gemaakt door gebruikers met beheerdersrechten. Zie [Sjablonen voor instructies](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md)

   ![](assets/start_modal.png)

1. Om een project van een leeg project tot stand te brengen, klik **[!UICONTROL Blank Project]**.

   * Klik vervolgens **[!UICONTROL Create]** of
   * Klik gewoon **[!UICONTROL Enter]**.

   Een leeg projectvertoningen, die een freeform paneel en een visualisatie van de gegevenslijst tonen.

   ![](assets/fa_project_new.png)

   >[!NOTE]
   >
   >Soms verschijnt het bericht &quot;Incompatible Report Suite&quot; wanneer een project wordt geladen (of wordt overgeschakeld op een rapportsuite), waarbij niet alle componenten (maateenheden/afmetingen) die in het project zijn opgenomen, in de rapportsuite zijn opgenomen. U kunt een lijst zien van de componenten die niet compatibel zijn, zodat u weet waarom u het bericht krijgt.

<table id="table_3989E45D9D4241CBB2E58B29DA257B2F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/analysis-workspace-components.md"  > Onderdelen</a> </td> 
   <td colname="col2"> <p>Dimension, metriek, segmenten en datumbereiken die u in projecten kunt slepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md"  > Visualisaties</a> </td> 
   <td colname="col2"> <p>Items die u naar het deelvenster of de projectgebieden van de interface kunt slepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md"  > Deelvenster Vrije vorm </a> </td> 
   <td colname="col2"> <p>Het canvas of de werkruimte waarmee u in Analysis Workspace werkt. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla uw project op. Geef het project een naam, geef een beschrijving op (optioneel, maar nuttig) en typ het project (optioneel). Klik vervolgens op **[!UICONTROL Save Project]**.

   ![](assets/save_project.png)

1. Door met de rechtermuisknop te klikken kunt u nu een visualisatie of een deelvenster kopiëren en het gekopieerde element vervolgens op een andere plaats in hetzelfde project of in een ander project plakken.

   Zo kunt u &quot;bouwstenen&quot; (vooraf gedefinieerde visualisaties/deelvensters) maken die naar andere projecten kunnen worden gekopieerd om sneller aan de slag te gaan, met data die specifiek zijn voor uw bedrijf.

   >[!NOTE]
   >
   >Nadat u kopieert/sparen-as, zijn de intra-verbindingen nu met betrekking tot het project zij binnen leven, niet het originele project zij van werden gekopieerd.

## Componenten en visualisaties toevoegen {#task_CDAC9B3007BE4A3790AFAD3746D669B1}

1. Bouw uw project door *`components`* en aan het project *`visualizations`* te slepen.

   **Onderdelen**

   Op de werkbalk Component worden doorzoekbare afmetingen, maateenheden, segmenten en datumbereiken weergegeven die u het meest gebruikt.

<table id="table_4626163E26DE46CB86391868BBA3AD32"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Component </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Dimension (oranje) </td> 
   <td colname="col2"> <p>Toepassen op projectniveau </p> <p><img  src="assets/dimensions.png" id="image_353BAF1A7AC04C7DB5F5CDFDE7614402" align="left" placement="break" width="300px" /> </p> <p>Prop#, eVar#, en gebeurtenis# worden toegevoegd aan de afmetingsnamen, en u kunt op die aantallen zoeken. Voorbeeld: "Interne campagne" wordt in het linkerspoor weergegeven als "Interne campagne (evar2)". </p> <p> De eigenschap, eVar en gebeurtenisnummers worden niet in de tabel weergegeven (om de titels kort te houden). </p> <p>Er is een standaardsorteervolgorde voor bepaalde afmetingen die buiten het vak vallen, wanneer ze naar een vrije-vormtabel worden gesleept of wanneer ze in de linkerrails worden weergegeven. Wanneer 'Uur van Dag' bijvoorbeeld in een tafel wordt neergezet of in de linkerspoorstaaf wordt weergegeven, wordt deze gesorteerd van 12.00 tot 11.00 uur. U kunt de tabel nog steeds sorteren op een kolom met metrics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Statistieken (groen) </td> 
   <td colname="col2"> <p>Toepassen op projectniveau. </p> <p><img  src="assets/metrics.png" id="image_7C874C72992E414CBEE6B90CEF7B9F3C" /> </p> <p> <span class="term"> Voorkomen</span> is standaard metrisch voor de gegevenslijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Segmenten (blauw) </td> 
   <td colname="col2"> <p>Sleepbaar slechts op paneelniveau, maar u kunt gealigneerde segmenten in de gegevenslijst tot stand brengen. </p> <p><img  src="assets/segments.png" id="image_5674B18BC3AB47A2B1FEE584E0FBF47C" /> </p> <p>See <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > Segments </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Datumbereiken en korreligheid (paars) </td> 
   <td colname="col2"> <p>Sleepbaar alleen op deelvensterniveau. U kunt een project van de Kalender tot stand brengen, wanneer het vormen van een datumwaaier. </p> <p><img  src="assets/date-ranges.png" id="image_A1750DA921234AD0BB02166865EB8FCC" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

**[Visualisaties](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)**

Het [!UICONTROL Visualizations] deelvenster bevat standaardgrafieken van Analytics, grafieken, donuts, gegevenstabellen, [cohortabellen](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) , Venn-diagrammen enzovoort. U kunt meerdere visualisaties naar uw project slepen en neerzetten.

![Stap Resultaat](assets/visualizations.png)

![](assets/fa_full_panel.png)

1. Stap

## Met het snelmenu kunt u uw gegevens aanpassen {#concept_8117C300F21843B99F4E1B9AB7B11B6F}

Met het snelmenu kunt u de volgende handelingen uitvoeren, afhankelijk van de cel in een tabel waarop u met de rechtermuisknop klikt.

![Stap Resultaat](assets/fa_data_table_actions.png)

<table id="table_0F84CC5B604D4D41BD0C9668DF525929"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Handeling </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md"  > Kolom voor tijdperiode toevoegen</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md"  > Vergelijk tijdsperiodes</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kopiëren naar klembord </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geselecteerde verwijderen </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-alerts/intellligent-alerts.md"  > Berichtgeving maken van selectie</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md"  > Uitsplitsing</a> 
    <ul id="ul_18C83B8514AD4C1C86C071AA8402CB5C"> 
     <li id="li_6CA84ED293EA4940A7495DA9D9121264">Dimensies </li> 
     <li id="li_EA16EE017B2E4A6998918706938A21BF">Metrics </li> 
     <li id="li_0405D339CD01405DB508A7D8D1A976B4">Segmenten </li> 
     <li id="li_819CE81C552F49BB9C1B83ED3B42C5F7">Tijd </li> 
    </ul> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md"  > Visualiseren</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/curate-share/download-send.md"  > Downloaden als CSV</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/home.md"  > Trend selection</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > Segment maken van selectie</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md"  > Uitvoeren in segmentvergelijking</a> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alleen geselecteerde rijen weergeven </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alle rijen weergeven </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

Zie Interacties met [toetsenborden en muis in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md) voor informatie over het kopiëren en selecteren van rijen.
