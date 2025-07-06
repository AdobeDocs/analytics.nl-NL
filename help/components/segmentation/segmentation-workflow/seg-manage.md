---
description: Begrijp hoe te om de segmentmanager te gebruiken om segmenten, zoals aandeel, filter, markering te beheren, goed te keuren, segmenten te kopiëren, te schrappen, en segmenten als favorieten te merken.
title: Segmenten beheren
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Segmenten beheren


U kunt [ delen, ](t-seg-share.md) segment [, ](t-seg-filter.md) markering [, ](seg-tag.md) goedkeuren [, anders noemen, ](seg-approve.md) exemplaar [, schrappen, de segmenten en merken segmenten als ](seg-copy.md) favoriet [ van een centrale ](t-seg-favorite.md) beheersinterface. [!UICONTROL Segment] Segmenten beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Segments]** .


>[!NOTE]
>
>De snelle segmenten die u binnen een specifiek Workspace-project maakt, worden niet weergegeven in de [!UICONTROL Segment] -manager, tenzij u het segment beschikbaar hebt gemaakt voor al uw projecten.
>

## Segmentbeheer

Segmentbeheer heeft de volgende interface-elementen:

![ interface van het Segment ](assets/segments-manager.png)

### Segmentlijst

In de lijst met segmenten ➊ worden alle segmenten weergegeven die u bezit, de segmenten die binnen het bereik van al uw projecten vallen en de segmenten die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een segment te begunstigen. Zie [ segment van het Teken als favoriet ](t-seg-favorite.md) |
| **[!UICONTROL Title and description]** | Om het segment uit te geven, selecteer de titelverbinding, die de [ bouwer van het Segment ](seg-build.md) opent. Een gedeeld segment wordt vermeld met ![ Aandeel ](/help/assets/icons/ShareAlt.svg). |
| **[!UICONTROL Report suitew]** | De rapportsuite waarop dit segment van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van het segment. Als gebruiker, ziet u slechts de segmenten die u bezit of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Tags]** | De labels voor dit segment. |
| **[!UICONTROL Shared with]** | Hoeveel individuen of groepen u het segment met deelde. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Component]** te openen. Zie [ de segmenten van het Aandeel ](t-seg-share.md) voor meer informatie. |
| **[!UICONTROL Published]** | Of het [ segment ](seg-publish.md) aan Experience Cloud wordt gepubliceerd. |
| **[!UICONTROL Date modified]** | De datum en tijd waarop het segment voor het laatst is gewijzigd. |

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt op segmenten actie ondernemen met de actiebalk ➋ . De actiebalk bevat de volgende handelingen:

| Handeling | Beschrijving |
|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** | Voeg een ander segment toe, gebruikend de [ bouwer van het Segment ](seg-build.md). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) [!UICONTROL *Onderzoek door titel*] | Wanneer er geen segment in de lijst is geselecteerd, zoekt u naar segmenten met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Tag]** | Tags toewijzen aan de geselecteerde segmenten. Selecteer in het dialoogvenster **[!UICONTROL Tag Segment]** de tags voor de geselecteerde segmenten of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde segmenten op te slaan. Zie [ de segmenten van de Markering ](seg-tag.md) voor meer informatie. |
| ![ Aandeel ](/help/assets/icons/ShareAlt.svg) **[!UICONTROL Share]** | Deel de geselecteerde segmenten. In de **[!UICONTROL Share Segment]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde segmenten op te slaan. Zie [ de segmenten van het Aandeel ](t-seg-share.md) voor meer informatie. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** | Verwijder de geselecteerde segmenten. U wordt gevraagd om een bevestiging. |
| ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Rename]** uit | Wijzig de naam van één geselecteerd segment. Als deze optie is geselecteerd, kunt u de naam van het segment inline wijzigen. |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Approve]** | Geef de geselecteerde segmenten goed. Zie [ segmenten ](seg-approve.md) voor meer informatie goedkeuren. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** | Kopieer het geselecteerde segment. Nieuwe segmenten worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** | De segmenten exporteren naar een `Segments List.csv` -bestand. |

### Actieve filterbalk

Op de filterbalk ➌ worden de actieve segmenten weergegeven die van het filterdeelvenster zijn toegepast op de lijst met segmenten (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meerdere filters zijn opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt de lijst van segmenten filtreren gebruikend ![ ](/help/assets/icons/Filter.svg) linkerpaneel van de Filter **[!UICONTROL Filter]** ➍. In het filterdeelvenster worden het type filter en het aantal segmenten weergegeven dat het specifieke filter toepast. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het paneel van de Filter van een knevel te voorzien.

Zie [ de lijst van segmenten ](t-seg-filter.md) voor meer informatie filtreren.


<!--

The Segment manager offers many ways of curating segments, such as sharing, filtering, tagging, approving, copying, deleting, and marking as favorites.

The Analytics Segment manager shows you all the segments you own and that have been shared with you. Admin-level users can see all segments in the organization. This overview presents the user interface and the capabilities of the Segment manager. 

![Segments manager](assets/segments-manager.png)

## Access the Segment manager

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Segments]**.

   Or 

   In an existing report, select the Segments icon ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in the left navigation, then select **[!UICONTROL Manage]**.

## Available actions in the Segment manager

In the Segment manager, you can:

* [Filter segments](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Mark segments as favorites](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Approve segments](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Tag segments](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Share segments](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Export a segment to a CSV file.

* [Copy segments](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Delete segments](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Configure columns

You can configure the information displayed for each segment in the Segment manager by configuring the columns that are displayed.

To configure the visible columns in the Segment manager:

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Segments]**. 

1. In the Segment manager, select the **Customize columns** icon ![Customize columns icon](assets/customize-columns-icon.png), then select the columns that you want to be displayed in the Segment manager.

   The following columns are available:

   | Column title | Description  |
   |---|---|
   | Title and description | These values are provided in the Segment builder. To edit the title and description, select the title link to open the Segment builder.  |
   | Favorites  | Displays star icons next to each segment, allowing you to mark segments as favorites. For more information, see [Mark segments as favorites](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Report suites  | This column indicates in which report suite the segment was last saved.  |
   | Owner  | Indicates who owns the segment. As a non-Admin, you can see only segments you own or those that were shared with you.  |
   | Tags (not checked in column selector, hence column not appearing)  | Tags that were applied to the segment, either by you or by people who shared the segment with you.  |
   | Shared with  | Lists individuals or groups (Admin only) or All (Admin only) that you shared the segment with. <p>When a segment is being shared by you or with you, a share icon displays next to the segment name.</p>|
   | Date modified  | Shows the date that the segment was last modified.  |
   | Used in | Shows where segments are currently being used, and how many times they are being used in each area. <p>For example, if the segment is being used in 40 projects and 2 alerts, then the value of this column shows as [!UICONTROL **42 components**].</p> <p>Select the value in this column to see the breakdown of where the segments are being used (for example, [!UICONTROL **Projects (40)**], [!UICONTROL **Alerts (2)**]). Furthermore, you can view the list of items where the segments are being used. For example, so see the list of projects where they are being used, select the [!UICONTROL **Projects (40)**] link.</p><p>Each of the following areas shows the number of instances of segments being used in that area:</p>  <ul><li>[!UICONTROL **Projects**]<p>Contains segments that were [created in the segment builder](/help/components/segmentation/segmentation-workflow/seg-build.md) and are available for all projects.</p></li><li>[!UICONTROL **Ad hoc components**]<p>Contains segments that were [created as quick segments](/help/analyze/analysis-workspace/components/segments/quick-segments.md) and are available only within a single project.</p></li><li>[!UICONTROL **Scheduled projects**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Annotations**]</li><li>[!UICONTROL **Alerts**]</li><li>[!UICONTROL **Calculated metrics**]</li><li>[!UICONTROL **Report Builder**]<p>Selecting this option downloads a CSV file, with the following columns of data:</p><ul><li>Report Builder Name</li><li>Last accessed</li><li>Last accessed IMS User ID</li><li>Last accessed user name</li></ul><p>When viewing information for Report Builder, usage information is available starting in September 2024.</p></li></ul><p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information is available only to system administrators.</li><li>The [!UICONTROL **Used in**] column does not display by default. [Configure columns](#configure-columns) to display it.</li><li>If a segment includes another segment in its definition, any use of that segment is not shown in the [!UICONTROL **Used in**] column. If a segment is included in the definition of another type of component (such as a calculated metric), then usage is shown in the [!UICONTROL **Used in**] column.</li><li>This information does not include usage from the API or Data Warehouse.</li><li>If there is no data in this column for a given component but it has a [!UICONTROL **Last used**] date, the component might have been used in an analysis without being saved.</li><li>Usage information is available starting in September 2023.</li></ul><p>You can use the [Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization.</p>  |
   | Last used | Shows the date when the segment was last used in any of the following component types: <ul><li>Alerts</li><li>Calculated metrics</li><li>Projects</li><li>Scheduled projects</li><li>Segments</li></ul> <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li><li>This information is available only to system administrators.</li></ul><p>You can use the [Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization. |
   
   {style="table-layout:auto"}

## How-To Video {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

This [Adobe Analytics video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html) gives a short overview of how to use the Segment manager.

-->