---
description: Leer de basisbeginselen van het maken van een project in Analysis Workspace
title: Projecten maken
feature: Workspace Basics
role: User, Admin
exl-id: 24193013-1361-43fc-b129-c44f207d9101
source-git-commit: 2bfc9c1d38957c997e78ee7d6a9550d173063109
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---

# Projecten maken {#create-projects}


[ Projecten ](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) in Analysis Workspace staan u toe om zaken-kritieke analyses tot stand te brengen en te bekijken.  Deze analyses kunnen worden gedeeld met belanghebbenden binnen of buiten uw organisatie.

1. Selecteer **[!UICONTROL Workspace]** in Adobe Analytics.

1. Selecteer **[!UICONTROL Projects]** in het linkerdeelvenster en selecteer vervolgens **[!UICONTROL Create project]** .

1. Selecteer **Leeg project van Workspace** om uw project van Workspace tot stand te brengen gebruikend browser.

   Zie [ Lege mobiele scorecard ](/help/analyze/mobile-app/curator.md) voor meer informatie over hoe te om een Mobiel scorecard project tot stand te brengen dat u met andere belanghebbenden kunt delen gebruikend mobiele app.

1. Selecteer [!UICONTROL **creeer**].


Nu u een Leeg project van Workspace hebt gecreeerd, zorg ervoor u met het [ Analysis Workspace ](/help/analyze/analysis-workspace/home.md) gebruikersinterface vertrouwd bent. Zodra u bent, kunt u uw project bouwen. Daartoe:

![ Project van het Voorbeeld ](assets/example-project.png)

* Voeg [ panelen ](/help/analyze/analysis-workspace/c-panels/panels.md) aan uw project toe. De lus **[!DNL Example Panel]** ➊ .

* Voeg [ visualisaties ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) aan uw panelen toe. Bijvoorbeeld:
   * **[!DNL Line]** [ lijn ](/help/analyze/analysis-workspace/visualizations/line.md) visualisatie ➋
   * **[!DNL US States]** [ Freeform lijst ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) visualisatie ➌
* Voeg [ componenten ](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) aan uw visualisaties toe. Bijvoorbeeld:
   * **[!DNL US States]** [ afmeting ](/help/components/dimensions/overview.md) ➍
   * **[!DNL Unique Visitors]** [ metrisch ](/help/analyze/analysis-workspace/components/apply-create-metrics.md) ➎
   * **[!DNL Average Revenue Per Order]** [ berekende metrisch ](/help/components/c-calcmetrics/cm-overview.md) ➏
   * **[!DNL Visits from Mobile Devices]** [ segment ](/help/components/segmentation/seg-overview.md) ➐
   * **[!DNL Last Month]** [ datumwaaier ](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md) ➑
   * **[!DNL Example]** [ annotation ](/help/analyze/analysis-workspace/components/annotations/overview.md) ➒


## Projectinfo en -instellingen {#project-info-settings}

>[!CONTEXTUALHELP]
>id="workspace_project_countrepeatinstances"
>title="Herhalingsinstanties tellen"
>abstract="Geeft aan of herhalingsinstanties worden geteld in rapporten.<br/><br/> Nota: dit het plaatsen is niet op Stroom of Vallout visualisaties van toepassing."

>[!CONTEXTUALHELP]
>id="workspace_project_repeatinstances"
>title="Herhalingsinstanties tellen"
>abstract="Geeft aan of herhalingsinstanties worden geteld in rapporten.<br/> Nota: dit het plaatsen is niet op Stroom of Vallout visualisaties van toepassing."


>[!CONTEXTUALHELP]
>id="workspace_project_commenting"
>title="Opmerkingen toestaan"
>abstract="Als deze optie is ingeschakeld, is er een opmerkingsgebied beschikbaar in de rechterspoorlijn van het project in Analysis Workspace."


De montages van het project verstrekken project-vlakke informatie over het momenteel actieve project.

![ het venster van Info &amp; van Montages van het Project.](./assets/projectinfo.png)

Voorbeelden van instellingen:

| Instelling | Beschrijving |
|---|---|
| Projectnaam | De naam die aan het project is gegeven. U kunt dubbelklikken op de naam om deze te bewerken. |
| Eigenaar | Naam eigenaar project |
| Laatst gewijzigd | Datum van laatste wijziging van het project. |
| Tags | Hiermee geeft u alle tags weer die op een project zijn toegepast om het eenvoudiger te categoriseren. |
| Beschrijving | Een beschrijving is nuttig om het doel van een project te verduidelijken. U kunt dubbelklikken op de beschrijving om deze te bewerken. |
| Herhalingsinstanties tellen | Geef op of herhalingsinstanties worden geteld in rapporten. Opmerking: deze instelling is niet van toepassing op Wisselstroomvisualisaties of Fallout-visualisaties. |
| Annotaties tonen | Geef op of er annotaties worden weergegeven voor dit project. |
| [ het kleurenpalet van het Project ](/help/analyze/analysis-workspace/build-workspace-project/color-palettes.md) | U kunt het categorische kleurenpalet veranderen dat in Workspace wordt gebruikt, door uit paletten te kiezen die uit-van-de-doos die voor kleurenblindheid zijn geoptimaliseerd, of door uw douanepalet te specificeren. Deze functie is van invloed op veel dingen in Workspace, waaronder de meeste visualisaties. |
| [Dichtheid weergeven](/help/analyze/analysis-workspace/build-workspace-project/view-density.md) | Hiermee kunt u meer gegevens op het scherm zien door de verticale opvulling van het linkerdeelvenster, vrije-vormtabellen en coderingstabellen te verminderen. |



<!--
# Create projects in Analysis Workspace

[Projects](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) in Analysis Workspace allow you to view business-critical analyses that can be shared with stakeholders inside or outside your organization. 

For general information about how to get started using Analysis Workspace, see [Analysis Workspace overview](/help/analyze/analysis-workspace/home.md).

The following sections describe how to create a project and start adding the key building blocks for any Analysis Workspace project: panels, visualizations, and components.

## Create a project from a blank project or a report

1. In Adobe Analytics, select [!UICONTROL **Workspace**].

1. Choose whether to create a blank project or to create a project from a report:

   +++Create a blank project

   1. On the [!UICONTROL **Workspace**] tab, select the [!UICONTROL **Projects**] tab on the left side of the page, then select [!UICONTROL **Create project**].

   1. Choose whether to create a blank project or a blank mobile scorecard

      * **Blank project** if you plan to share your analysis from the browser 
      * [**Blank mobile scorecard**](/help/analyze/mobile-app/curator.md) if you plan to share your analysis from the Adobe Analytics dashboards mobile app.

   1. Select [!UICONTROL **Create**].

   +++

   +++Create a project from a report
   
      1. On the [!UICONTROL **Workspace**] tab, select the [!UICONTROL **Reports**] tab on the left side of the page.

      1. Search for or navigate to the report you want to use, then select it when it appears.

          A set of standard reports is available by default. In addition, your organization might have created custom reports for you to choose from.
          
      1. Select [!UICONTROL **Project**] > [!UICONTROL **Save**] to save the report as a new project.

          For more information about reports, see "Navigate the Reports tab" in [Adobe Analytics landing page](/help/analyze/landing.md).

   +++

1. Next, you need to add panels, visualizations, and components to your project. First, add panels to your project in Analysis Workspace, as described in [Add panels to the project](#add-panels-to-the-project). You can then add visualizations to any panels. Finally, you can add components to any panels or visualizations.

## Add panels to the project {#panels}

[Panels](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=nl-NL) are the foundation to any project in Analysis Workspace. Panels are used to organize the content (visualizations and components) of a project. 

Many of the panels provided in Analysis Workspace generate a full set of analyses based on a few user inputs. 

To add a panel:

1. Select the [!UICONTROL **Panels**] icon in the left rail.

   ![](assets/build-panels.png)

1. Search for the panel you want to add. When it appears in the left rail, drag it into your project.

1. Add visualizations to your panel, as described in [Add visualizations to the project](#add-visualizations-to-the-project). 

   Alternatively, you can add components directly to a panel, as described in [Add components to the project](#add-components-to-the-project).

## Add visualizations to the project

[Visualizations](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=nl-NL) (such as a freeform table, a bar chart, or a line chart) can be used to visually bring data to life. 

>[!TIP]
>
>Freeform tables are the most common type of visualization, and are the foundation for interactive data analysis. For more details about how to work with Freeform tables in Analysis Workspace, see [Freeform table](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md).

To add a visualization:

1. Select the **[!UICONTROL Visualizations]** icon in the left rail.

   ![](assets/build-visualizations.png)

1. Search for the visualization you want to add. When it appears in the left rail, drag it to a panel within your project. 

1. Add components to the visualization, as described in [Add components to the project](#add-components-to-the-project).

## Add components to the project

[Components](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) make up the actual data of any project. You can add components to visualizations or to panels.

>[!TIP]
>
>For information about each component, select the Info icon next to a component's name in the left rail, or see the [Analytics Components Guide](/help/components/home.md).

Following is basic information about how to add a component to a project in Analysis Workspace. For more detailed information about adding the various types of components (dimensions, metrics, segments, and date ranges), see [Use components in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

To add a component to a project in Analysis Workspace:

1. Select the **[!UICONTROL Components]** icon in the left rail.

   ![](assets/build-components.png)

1. Scroll to or search for the component you want to add, then drag it to a panel or visualization within your project. 

   For example, you can drag a segment to the segment drop zone in a panel header.

   ![drop a segment in the drop zone](assets/segment-dropzone.png)

   For more information about adding components to projects, see [Use components in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

1. (Optional) Share the project as described in [Save and share the project](#save-and-share-the-project).

## Save and share the project

As you create an analysis in Analysis Workspace, your work is [automatically saved](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md). 

When you finish building out the project and it's gathering actionable insights, the project is ready to be consumed by others. You can share the project with users and groups in your organization, or even with people outside your organization. For information about sharing a project, see [Share projects](/help/analyze/analysis-workspace/curate-share/share-projects.md).
-->