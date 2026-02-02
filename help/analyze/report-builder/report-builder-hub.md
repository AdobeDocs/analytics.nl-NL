---
title: Report Builder Hub
description: Meer weten over de Report Builder hub?
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: e18381ea-b7d4-4d7a-9ded-23b2d06fa204
source-git-commit: ff1722416fe5062d16c12185d17271ebc2d6b624
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# Report Builder hub


De hub van Report Builder is de juiste ruit die binnen uw werkboek van Excel wordt getoond wanneer u ![ AdobeLogoRedonWhite ](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** van de bar van het lint van Excel selecteert.

Met de Report Builder-hub kunt u gegevensblokken maken, bijwerken, verwijderen en beheren.

De hub van Report Builder bevat ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**, ![ TableManage ](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** en ![ Kalender ](/help/assets/icons/Calendar.svg) **[!UICONTROL Schedule]** knopen, het **[!UICONTROL Commands]** paneel, en het **[!UICONTROL Quick edit]** paneel.

![ hub van Report Builder ](assets/hub51.png){zoomable="yes"}


Selecteren

* ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]** [ creeert nieuwe gegevensblokken ](create-a-data-block.md).
* ![ TableManage ](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** aan [ beheer bestaande gegevensblokken ](manage-reportbuilder.md).
* ![ Kalender ](/help/assets/icons/Calendar.svg) **[!UICONTROL Schedule]** aan [ beheert programma&#39;s om uw werkboek door e-mail ](schedule-reportbuilder.md) te verzenden.

## Opdrachten, deelvenster

Gebruik het deelvenster **[!UICONTROL Commands]** voor toegang tot opdrachten die compatibel zijn met de geselecteerde cellen of een vorige handeling.

| Opdrachten | Beschikbaar als... | Doel |
|------|------------------|--------|
| ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit data block]** uit | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Wordt gebruikt om een gegevensblok te bewerken. |
| ![ verfrissen zich ](/help/assets/icons/Refresh.svg) **[!UICONTROL Refresh data block]** | De selectie bevat ten minste één gegevensblok. Met deze opdracht vernieuwt u alleen de gegevensblokken in de selectie. | Vernieuw een of meer gegevensblokken. |
| ![ DocumentRefresh ](/help/assets/icons/DocumentRefresh.svg) **[!UICONTROL Refresh all data blocks]** | Het werkboek bevat één of meerdere gegevensblokken. | Gebruik om alle gegevensblokken in het werkboek te verfrissen |
| ![ verzend ](/help/assets/icons/Send.svg) **[!UICONTROL Send workbook]** | Het werkboek bevat één of meerdere gegevensblokken. | Gebruik om [ het werkboek als dossier door e-mail ](schedule-reportbuilder.md) te verzenden. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy data block]** | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Wordt gebruikt om een gegevensblok te kopiëren. |
| ![ Besnoeiing ](/help/assets/icons/Cut.svg) **[!UICONTROL Cut data block]** | De geselecteerde cel of het geselecteerde celbereik maakt deel uit van een of meer gegevensblokken. | Zie om een gegevensblok te knippen. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete data block]** | De geselecteerde cel of het geselecteerde celbereik maakt slechts deel uit van één gegevensblok. | Gebruiken om een gegevensblok te verwijderen |

## Deelvenster Snel bewerken

Wanneer u een of meer gegevensblokken in een spreadsheet selecteert, geeft Report Builder het deelvenster **[!UICONTROL Quick edit]** weer. U kunt het deelvenster **[!UICONTROL Quick edit]** gebruiken om parameters in een of meer gegevensblokken tegelijk te wijzigen.

De wijzigingen die u aanbrengt wanneer u de secties **[!UICONTROL Quick Edit]** gebruikt, zijn van toepassing op alle geselecteerde gegevensblokken.

### Reeksen rapporteren

Gegevensblokken trekken gegevens uit een geselecteerde rapportsuite. Als de veelvoudige gegevensblokken in een aantekenvel worden geselecteerd en zij trekken geen gegevens van de zelfde rapportreeks, de **verbindingsvertoningen van de de reeksen van het 0} Rapport** Veelvoud **[!UICONTROL _._]**

Wanneer u de rapportsuite wijzigt, nemen alle gegevensblokken in de selectie de nieuwe rapportsuite aan. De componenten in het gegevensblok worden aangepast aan de nieuwe rapportreeks die op identiteitskaart wordt gebaseerd. Als een component niet in een gegevensblok wordt gevonden, wordt de component verwijderd en met **[!UICONTROL Invalid value]** vervangen of ![ AlertRed ](/help/assets/icons/AlertRed.svg) wordt getoond voor de specifieke component.

Als u de rapportsuite wilt wijzigen, selecteert u een nieuwe rapportsuite in de vervolgkeuzelijst **[!UICONTROL Report suite]** .


### Datumbereik

**waaier van de Datum** toont de datumwaaier voor de geselecteerde gegevensblokken. Als de veelvoudige gegevensblokken met veelvoudige datumwaaiers worden geselecteerd, **[!UICONTROL Date range]** verbindingsvertoningen **[!UICONTROL _Veelvoud_]**.

### Segmenten

De **verbinding van Segmenten** toont een summiere lijst van de segmenten die door de geselecteerde gegevensblokken worden gebruikt. Als de veelvoudige gegevensblokken met veelvoudige toegepaste segmenten worden geselecteerd, de **verbindingsvertoningen van segmenten** Veelvoudig **[!UICONTROL _._]**

>[!MORELIKETHIS]
>
>[Een rapportsuite selecteren](select-report-suite.md)
>[Selecteer een datumbereik ](select-date-range.md)
>[Werken met filters ](work-with-segments.md)
>

<!--

Use the Report Builder hub to create, update, delete, and manage data blocks.

The Report Builder hub contains the Create, Manage, and Schedule buttons, the COMMANDS panel, and The QUICK EDIT panel.

<img src="./assets/hub51.png" alt="Report Builder Hub"/>


## Create, Manage, and Schedule buttons

Use the Create, Manage, and Schedule buttons to create new data blocks, manage existing data blocks, or schedule datablocks.

## COMMANDS panel

Use the COMMANDS panel to access commands that are compatible with the selected cells or a previous action.

### Commands

| Commands displayed      | Available when…   | Purpose          |
|------|------------------|--------|
| Edit data block | The selected cell or cells range is part of one data block only. | Used to edit a data block |
| Refresh data block | The selection contains at least one data block. The command refreshes only the data blocks in the selection. | Used to refresh one or more data blocks |
| Refresh all data blocks | The workbook contains one or more data blocks. | Used to refresh ALL data blocks in the workbook |
| Send workbook |   |  Send a workbook on a schedule. |
| Copy data block   | The selected cell or cell range is part of one or more data blocks. | Used to copy a data block   |
| Cut data block |   | Used to cut a data block |
| Delete data block | The selected cell or cells range is part of one data block only. | Used to delete a data block |

## QUICK EDIT panel

When you select one or more data blocks in a spreadsheet, Report Builder displays the QUICK EDIT panel. You can use the QUICK EDIT panel to change parameters in a single data block or to change parameters in multiple data blocks at the same time.

![The Quick Edit panel in Report Builder](./assets/hub2.png)

The changes made using the Quick Edit sections apply to all selected data blocks.

### Report suites

Data blocks pull data from a selected report suite. If multiple data blocks are selected in a worksheet and they don't pull data from the same report suite, the **Report Suites** link displays *Multiple*.

When you change the report suite, all data blocks in the selection adopt the new report suite. Components in the data block are matched to the new report suite based on ID, for example, matching ```evars```). If a component isn't found in a data block, a warning message is displayed and the component is removed from the data block.

To change the report suite, select a new report suite from the drop-down menu.

![The Report Builder Hub showing the report suite drop-down menu.](./assets/image16.png)

### Date range

**[!UICONTROL Date range]** shows the date range for the selected data blocks. If multiple data blocks are selected with multiple date ranges, the **[!UICONTROL Date range]** link displays *Multiple*. [Learn more](/help/analyze/report-builder/select-date-range.md)

### Segments

The **Segments** link displays a summary list of the segments used by the selected data blocks. If multiple data blocks are selected with multiple segments applied, the **Segments** link displays *Multiple*. [Learn more](/help/analyze/report-builder/work-with-segments.md)

-->