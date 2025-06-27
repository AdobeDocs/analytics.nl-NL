---
description: Leer hoe te om freeform lijst of een gegevensbron aan de overeenkomstige visualisatie te synchroniseren.
keywords: Analysis Workspace;Visualisatie synchroniseren met gegevensbron
title: Gegevensbronnen beheren
feature: Visualizations
role: User, Admin
exl-id: 0500b27a-032e-4dc8-98b7-58519ef59368
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Gegevensbronnen beheren {#manage-data-sources}

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection"
>title="Selectie vergrendelen"
>abstract="Schakel deze instelling in om de visualisatie te vergrendelen op de geselecteerde posities of op de geselecteerde items in de gegevensbron."

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection_showtable"
>title="Tabel tonen"
>abstract="Als u **[!UICONTROL Show table]** selecteert, wordt een nieuwe gegevensbron voor uw huidige visualisatie gegenereerd, los van de oorspronkelijke gegevensbron."

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_showtable"
>title="Tabel tonen"
>abstract="Selecteer **[!UICONTROL Show table]** om een nieuwe gegevensbron voor uw huidige visualisatie te produceren, los van de originele gegevensbron."


Door visualisatie te synchroniseren kunt u bepalen welke vrije-vormtabel of gegevensbron overeenkomt met een visualisatie.


>[!TIP]
>
>U kunt zien welke visualisaties door de kleur van ![ StatusOrange ](/help/assets/icons/StatusOrange.svg) naast de titel van visualisaties verwant zijn. Gelijktijdige kleuren betekenen dat visualisaties zijn gebaseerd op dezelfde gegevensbron.
>

U kunt de gegevensbron tonen of verbergen. U kunt de selectie ook vergrendelen op geselecteerde posities of geselecteerde items. Deze instellingen bepalen hoe de visualisatie verandert (of niet verandert) wanneer er nieuwe gegevens binnenkomen.

![ de de optiesdialoog van Source van Gegevens die de opties tonen in de volgende sectie worden beschreven.](assets/lock-selection.png)

<!--
**Tip:** You can tell which visualizations are related by the color of the dot next to the title. Matching colors mean that visualizations are based on the same data source.

Managing a data source lets you show the data source or lock the selection. These settings determine how the visualization changes (or doesn't change) when new data comes in.

1. [Create a project](/help/analyze/analysis-workspace/home.md) with a data table and a [visualization](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. In the data table, select the cells (data source) you want to associate with the visualization.
1. In the visualization, click the dot next to the title to bring up the **[!UICONTROL Data Source]** dialog. Select **[!UICONTROL Show Data Source]** or **[!UICONTROL Lock Selection]**.

   ![](assets/manage-data-source.png)

   Synchronizing a visualization to a table cell creates a new (hidden) table and color-codes the synchronized visualization with that table.

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Data source settings](https://video.tv.adobe.com/v/23729?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->

| Optie | Beschrijving |
|--- |--- |
| **[!UICONTROL Data source]** | Selecteer in het keuzemenu de gegevensbron waarop de visualisatie is gebaseerd. |
| **[!UICONTROL Linked visualizations]** | Hiermee geeft u alle gekoppelde visualisaties weer. Is van toepassing op de gegevensbron (vrije-vormlijst). |
| **[!UICONTROL Show data source]** | Hiermee kunt u de gegevensbron (vrije-vormentabel) die overeenkomt met de visualisatie, weergeven of verbergen. |
| **[!UICONTROL Lock Selection]** | Selecteer deze optie om visualisatie ![ LockClosed ](/help/assets/icons/LockClosed.svg) aan de gegevens te sluiten die momenteel in de overeenkomstige gegevenslijst worden geselecteerd. Als deze optie is ingeschakeld, selecteert u tussen:  <ul><li>**Geselecteerde Plaatsen**: De visualisatie is gesloten op de **posities** die in de overeenkomstige gegevenslijst worden geselecteerd. Deze posities blijven zichtbaar, zelfs als de specifieke punten in deze posities veranderen (bijvoorbeeld toe te schrijven aan het sorteren of het filtreren). Selecteer deze optie bijvoorbeeld als u de vijf belangrijkste campagnemenamen in de gegevensbron in deze visualisatie altijd wilt weergeven. Geen kwestie welke campagnemenamen verschijnen.</li> <li>**Geselecteerde Punten**: De visualisatie is gesloten op de specifieke **punten** momenteel geselecteerd in de overeenkomstige gegevenslijst. Deze items blijven zichtbaar, zelfs als ze een andere positie innemen onder de items in de tabel. Selecteer deze optie bijvoorbeeld als u altijd dezelfde vijf specifieke campagnemenamen wilt weergeven die in de gegevensbron in deze visualisatie worden vermeld. Hoe die campagnenamen er ook uitzien.</li></ul>Als de visualisatie is vergrendeld voor gegevens die niet meer zichtbaar zijn in de tabel met verbonden gegevens, kunt u een nieuwe tabel genereren. Selecteer **[!UICONTROL Show table]** om een nieuwe gegevensbron voor uw huidige visualisatie, los van de originele gegevensbron te produceren. |
