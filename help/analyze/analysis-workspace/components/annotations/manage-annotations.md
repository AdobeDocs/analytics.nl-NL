---
title: Annotaties beheren
description: Leer hoe u annotaties beheert in Analysis Workspace.
role: User, Admin
feature: Annotations
exl-id: 37a538cc-9ea7-4cb1-8ee8-e8e474ad5b08
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Annotaties beheren

U kunt annotaties delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en annotaties markeren als favoriet vanuit een centrale beheerinterface van [!UICONTROL Annotations] . Annotaties beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Annotations]** .


>[!NOTE]
>
>De annotaties die u binnen een specifiek Workspace-project maakt, worden niet weergegeven in de [!UICONTROL Annotations] -manager, tenzij u de annotatie beschikbaar hebt gemaakt voor al uw projecten.
>

## Annotatiebeheer

Het annotatiebeheer heeft de volgende interface-elementen:

![&#x200B; de interface van Annotaties &#x200B;](assets/annotations-manager.png)

### Lijst met annotaties

In de lijst met annotaties ➊ worden alle annotaties weergegeven die u hebt, de annotaties die binnen het bereik van al uw projecten vallen en de annotaties die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- |
| ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) | Selecteer om ![&#x200B; Ster &#x200B;](/help/assets/icons/Star.svg) of niet-gunst ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) een aantekening te begunstigen. |
| **[!UICONTROL Title and description]** | Opgegeven in de Annotations Builder. Om de titel en de beschrijving uit te geven, selecteer de titelverbinding - opent de [&#x200B; bouwer van Annotaties &#x200B;](/help/analyze/analysis-workspace/components/annotations/create-annotations.md#annotation-builder). Een gedeelde annotatie wordt vermeld met ![&#x200B; Aandeel &#x200B;](/help/assets/icons/ShareAlt.svg). |
| **[!UICONTROL Report suite]** | De rapportsuites waarop deze aantekening van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van de aantekening. Als gebruiker ziet u alleen de annotaties die u hebt of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Applied date range]** | De datum of het datumbereik waarop deze aantekening van toepassing is. |
| **[!UICONTROL Tags]** | De codes voor deze aantekening. |
| **[!UICONTROL Shared with]** | De personen of groepen waarmee u de annotatie hebt gedeeld. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Component]** te openen. |
| **[!UICONTROL Date modified]** | Geeft de datum en tijd weer waarop de annotatie voor het laatst is gewijzigd. |

{style="table-layout:auto"}

Gebruik ![&#x200B; ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt actie ondernemen op annotaties met de actiebalk ➋ . De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:--:|---|---|
| ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een andere annotatie toe, gebruikend de [&#x200B; bouwer van de Annotatie &#x200B;](create-annotations.md#annotation-builder). |
| ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen annotatie is geselecteerd in de lijst, zoekt u naar annotaties met dit zoekveld. |
| ![&#x200B; Etiket &#x200B;](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde annotaties. Selecteer in het dialoogvenster **[!UICONTROL Tag Component]** de tags voor de geselecteerde annotaties of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde annotaties op te slaan. |
| ![&#x200B; Aandeel &#x200B;](/help/assets/icons/ShareAlt.svg) | **[!UICONTROL Share]** | Deel de geselecteerde annotaties. In de **[!UICONTROL Share Component]** dialoog, kunt u ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde annotaties op te slaan. Zie [&#x200B; Annotaties van het Aandeel &#x200B;](#share-annotations) voor meer details. |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde annotaties. U wordt gevraagd om een bevestiging. |
| ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerde annotatie. Als deze optie is geselecteerd, kunt u de naam van de annotatie inline wijzigen. |
| ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde annotaties. Nieuwe annotaties worden gemaakt met dezelfde naam en hetzelfde achtervoegsel (kopie) |
| ![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de annotaties naar een `Annotations List.csv` -bestand. |

### Actieve filterbalk

De filterbalk ➌ geeft de actieve filters weer (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt annotaties filteren met het **[!UICONTROL Filter]** linkerdeelvenster ➍ . In het filterdeelvenster worden het type filter en het aantal annotaties weergegeven die het filter respecteren. Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om de vertoning van het filterpaneel van een knevel te voorzien.

De lijst met filters filteren:

1. Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Filters nodig hebt, kunt u ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. U kunt de annotaties filtreren gebruikend om het even welke beschikbare [&#x200B; filtersecties &#x200B;](#filter-sections).

   >[!INFO]
   >
   >*Punten* verwijzen naar de annotatie punten die in de [&#x200B; lijst van Annotaties &#x200B;](manage-annotations.md#annotations-list) worden getoond.
   > 

#### Secties filteren

{{tagfiltersection}}
{{reportsuitefiltersection}}
{{ownerfiltersection}}
{{daterangefiltersection}}
{{otherfiltersfiltersection}}


De [&#x200B; lijst van Annotaties &#x200B;](manage-annotations.md#annotations-list) wordt automatisch bijgewerkt gebaseerd op uw filterconfiguratie. U kunt de gevormde filters in de [&#x200B; Actieve filterbar &#x200B;](manage-annotations.md#active-filter-bar) zien.


## Annotaties bewerken

U kunt een annotatie op twee manieren bewerken:

* In een project van Workspace, gebruik het [&#x200B; pictogram van de Component info &#x200B;](/help/analyze/analysis-workspace/components/use-components-in-workspace.md#component-info).

* Selecteer in de [[!UICONTROL Annotations] lijst &#x200B;](#annotations-list) de titel van de annotatie.

U gebruikt de [&#x200B; bouwer van de Annotatie &#x200B;](/help/analyze/analysis-workspace/components/annotations/create-annotations.md#annotation-builder) om de annotatie uit te geven.

## Annotaties delen

Het volgende is van toepassing wanneer u annotaties deelt of met annotaties werkt die met u worden gedeeld:

* Projectgebonden annotaties in een project dat u met andere gebruikers deelt, worden voor die gebruikers weergegeven. De gebruikers kunnen deze alleen-projectnotities niet bewerken of verwijderen.
* Als u een annotatie opslaat en de annotatie rechtstreeks met een gebruiker deelt, kan die gebruiker de annotatie alleen bewerken en verwijderen als die gebruiker beheerdersrechten heeft.

* Als een project met u wordt gedeeld, verschijnen de annotaties die in dat project worden gecreeerd slechts in dat project. Als een annotatie rechtstreeks met u wordt gedeeld, wordt de annotatie weergegeven in alle projecten waarin die annotatie kan worden weergegeven.

## Aantekeningen en tijdzones

Alle annotaties worden gemaakt met een tijdstempel, maar geen uur- of tijdzonegegevens. Op rapporttijd, wordt de tijdzone van de rapportreeks die voor het paneel wordt gevormd gebruikt.


<!--
# Manage annotations

The [!UICONTROL Annotations manager] shows you all of the annotations that you own or that have been shared with you. Project-specific annotations do not appear here. You can use this interface to share, filter, tag, copy, delete, and favorite your annotations. Administrators can manage and approve annotations.

**[!UICONTROL Components]** > **[!UICONTROL Annotations]**

## Annotations Manager user interface

![](assets/annotation-mgr.png)

| UI Element | Description |
| --- | --- |
| [!UICONTROL Title and Description] | Provided in the Annotations Builder. To edit the title and description, click the title link - this takes you back to the Annotations Builder.  |
| [!UICONTROL Report Suite] | The report suites that this annotation applies to.  |
| [!UICONTROL Owner] | Indicates who owns the annotation. As a non-Admin, you can see only annotations that you own or those that were shared with you. |
| [!UICONTROL Applied Date Range] | The date or date range that this annotation applies to. |
| [!UICONTROL Shared with] | Lists how many individuals or groups that you shared the annotation with. Click for more detail. |
| [!UICONTROL Date Modified] | Shows the date and time that the annotation was last modified. |

{style="table-layout:auto"}

## Edit annotations

Editing an annotation means that you can adjust date ranges, colors, scope, or whether it applies to all report suites or projects. You can edit annotations in two ways:

* In a line chart, hover over the annotation and click the pencil icon within the popover.
* In the [!UICONTROL Annotations Manager], click the title of the annotation.

Both of these options land you back in the [!UICONTROL Annotations Builder]. There, you can make the necessary adjustments and save the new version.

## Share annotations

When sharing annotations or working with annotations that were shared with you, keep this in mind:

* If you create a project with project-only annotations, then share the project with another user, annotations cannot be edited or deleted by anyone that you share the project with.
* If you save an annotation and share it directly with a user, they can edit/delete the annotation only if they have admin rights.
* If a project is shared with you with a project-only annotation, it shows up only in that project. If the annotation is shared directly with you, it shows up in all projects where that annotation can be displayed. 

## Annotations and time zones

All annotations are created with a timestamp, but no hours or timezone information. At report time, the timezone of the panel's report suite is always applied. For example, an annotation created for Christmas Day happens on December 25 no matter what report suite timezone you are in. 

## Other annotation tasks

The Annotations manager lets Administrators edit, add, tag, delete, rename, approve, copy, export, and filter annotations. It is not visible to non-Admin users. 

Additional options are available when you select at least one annotation:

| Task | Description |
| --- | --- |
| [!UICONTROL Add] | Takes you to the Annotations builder where you can create annotations. |
| [!UICONTROL Tag] | All users can create tags for annotations and apply one or more tags to an annotation. However, you can see tags only for annotations that you own. |
| [!UICONTROL Delete] | Deleting an annotation removes it from any project in your organization. |
| [!UICONTROL Rename] | Renaming an annotation renames it in all projects that it was applied to. |
| [!UICONTROL Copy] | Creates a distinct copy with its own annotation ID, but with the same name and definition.|
| [!UICONTROL Export to CSV] | Export the annotation definition to a .csv file.|
| [!UICONTROL Filter] (left rail) | Filter by tags, report suite, owners, and other filters (Mine, Approved, Favorites, Shared with me, and Show All).|

{style="table-layout:auto"}

-->