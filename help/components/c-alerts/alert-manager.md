---
description: Leer hoe waarschuwingen worden beheerd.
title: Waarschuwingen beheren
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 24dd47e995523aedba1385ee8882af5e11c7b128
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---


# Waarschuwingen beheren


U kunt waarschuwingen filteren, labelen, verwijderen, hernoemen, kopiëren, inschakelen, uitschakelen, vernieuwen en exporteren vanuit een centrale beheerinterface van [!UICONTROL Alerts] . Waarschuwingen beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Alerts]** .

De manager van het Alarm is gestructureerd als de [ manager van het Segment ](/help/components/segmentation/segmentation-workflow/seg-manage.md) en [ Berekende metrische manager ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md).


## Waarschuwingenbeheer

De manager van Alarm heeft de volgende interfaceelementen:

![ de interface van Filters ](assets/alerts-manager.png)

### Waarschuwingenlijst

In de lijst met waarschuwingen ➊ worden alle waarschuwingen weergegeven die u hebt, de waarschuwingen die betrekking hebben op al uw projecten en de waarschuwingen die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een alarm te begunstigen. |
| **[!UICONTROL Title and description]** | Om het alarm uit te geven, selecteer de titelverbinding, die de [ bouwer van Alarm ](alert-builder.md#alert-builder) opent. |
| **[!UICONTROL Type]** | Het type waarschuwing: een Adobe Analytics-gegevenswaarschuwing of een waarschuwing voor het gebruik van een serveroproep. |
| **[!UICONTROL Enabled]** | De waarschuwing wordt in- of uitgeschakeld. |
| **[!UICONTROL Report suite]** | De rapportensuites waarop deze waarschuwing van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van de waarschuwing. Als niet-beheerder, ziet u slechts alarm dat u bezit of alarm dat met u wordt gedeeld. |
| **[!UICONTROL Tags]** | De tags voor deze waarschuwing. |
| **[!UICONTROL Expiration Date]** | De datum en tijd waarop de waarschuwing is ingesteld op verlopen. |
| **[!UICONTROL Date modified]** | De datum en het tijdstip waarop de waarschuwing voor het laatst is gewijzigd. |

<!-- 

When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul>

-->

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt actie ondernemen bij waarschuwingen met de actiebalk ➋ . De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een ander alarm toe, gebruikend de [ Waakzame bouwer ](alert-builder.md#alert-builder). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen waarschuwing in de lijst is geselecteerd, zoekt u naar waarschuwingen met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde waarschuwingen. Selecteer in het dialoogvenster **[!UICONTROL Tag Alert]** de tags voor de geselecteerde waarschuwingen of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde waarschuwingen op te slaan. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde waarschuwingen. U wordt gevraagd om een bevestiging. |
| ![ geeft ](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerde waarschuwing. Als deze optie is geselecteerd, kunt u de naam van de waarschuwing inline wijzigen. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde waarschuwing. Nieuwe waarschuwingen worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL Enable]** of **[!UICONTROL Disable]** | Schakel de geselecteerde waarschuwingen in of uit. |
| ![ verfrissen zich ](/help/assets/icons/Refresh.svg) | **[!UICONTROL Renew]** | Hiermee wordt de vervaldatum van de waarschuwing vernieuwd. De vervaldatum begint met 1 jaar vanaf de dag waarop u deze optie selecteert, ongeacht de oorspronkelijke vervaldatum. |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de waarschuwingen naar een `Alerts List.csv` -bestand. |


### Actieve filterbalk

De filterbalk ➌ geeft de actieve filters weer die van het filterdeelvenster zijn toegepast op de lijst met waarschuwingen (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .


### Deelvenster Filter

U kunt de lijst van alarm filtreren gebruikend het ![ Linkerpaneel van de Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** ➍. In het filterdeelvenster worden het type filter en het aantal waarschuwingen weergegeven die aan het specifieke filter voldoen.


1. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Alarm nodig hebt, kunt u ![ Filter ](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. Selecteer filters uit een van de beschikbare filtersecties.


#### Sectie Labels, filter

{{tagfiltersection}}


#### Sectie voor het filter Rapporten

{{reportsuitefiltersection}}


#### Sectie eigenaarfilter

{{ownerfiltersection}}


#### Ingeschakelde sectie voor statusfilter

{{enabledstatusfiltersection}}


#### Sectie Type filter

{{typefiltersection}}


#### Sectie Overige filters

{{otherfiltersfiltersection}}



## Waarschuwingen bewerken

U kunt een waarschuwing bewerken

* Selecteer in de [[!UICONTROL Alert] lijst ](#alerts-list) de titel van de waarschuwing.

U gebruikt de [ Waakzame bouwer ](alert-builder.md#alert-builder) om het alarm uit te geven.

## Een waarschuwing oplossen

Geef Adobe Support het JID-nummer (Job Instance ID) op wanneer u een probleem met een waarschuwing oplost. Het JID-nummer bevindt zich onder aan het e-mailbericht dat u ontvangt.

![ Alert e-mail ](assets/alerts-email.PNG)


<!--

# Manage alerts

You can manage existing alerts in the Alerts manager. You can perform various management tasks on alerts, such as tagging, renaming, deleting, and more.

The Alerts manager is structured very much like the [Segment Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=nl-NL) and the [Calculated Metric Manager](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=nl-NL).

 ![](assets/alert-manager.png)

## Create alerts

To create alerts from the Alerts manager:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select [!UICONTROL **Add**] (or [!UICONTROL **Create new alert**] if you don't have any existing alerts).

1. Select the alert type that corresponds to the alert that you want to create:

   * [!UICONTROL **Analytics data alert**]: An alert to notify you when abnormal events occur in your data. 

     If you select this option, continue with [Create alerts](/help/components/c-alerts/alert-builder.md) for more details about creating alerts.

   * [!UICONTROL **Server call usage alert**]: An alert to notify you of the risk or occurrence of an overage in your server call consumption and commitment data. 

     If you select this option, continue with [Server call usage alerts](/help/admin/admin/c-server-call-usage/scu-alerts.md).

     >[!NOTE]
     >
     >You must be an Analytics administrator or a user with the Server call usage permission in order to have access to server call usage. 

## Manage existing alerts

You can perform various actions on existing alerts, such as tagging, renaming, deleting, and so forth.

To manage existing alerts in the Alerts manager:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select one or more alerts that you want to manage.

   ![](assets/alert-manager-tasks.png)

1. In the action bar, select any of the following options:

   | Action | Function | 
   |---------|----------|
   | [!UICONTROL **Tag**] | Apply a tag to an alert. This helps you to organize alerts for ease of use. | 
   | [!UICONTROL **Delete**] | Deletes the alert. | 
   | [!UICONTROL **Rename**] | Renames the alert. |
   | [!UICONTROL **Approve**] | Mark the alert as Approved. |
   | [!UICONTROL **Copy**] | Creates a copy (duplicate) of the alert. |
   | [!UICONTROL **Disable**] | Disables an alert that is currently enabled. |
   | [!UICONTROL **Enable**] | Enables an alert that is currently disabled. |
   | [!UICONTROL **Renew**] | Renews the alert expiration date. This extends the  expiration date to be 1 year from the day you selected this option, regardless of the original expiration date. |
   | [!UICONTROL **Export to CSV**] | Exports the alert to a .CSV file. |

## Edit an alert

To edit an existing alert:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select the alert name in the [!UICONTROL **Title and description**] column.

1. Edit the alert as desired. 

   Following are some of the things you can do when editing an alert:

   * Add alerts to other report suites
   * Add or modify the description
   * Modify the time granularity
   * Modify the recipients 
   * Modify the expiration date
   * Modify the metrics and filters

1. Select [!UICONTROL **Save**].

## Configure columns 

You can configure the information displayed for each alert in the Alerts manager by configuring the columns that are displayed.

To configure the visible columns in the Alerts manager:

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Alerts]**. 

1. In the Alert manager, select the **Customize columns** icon ![Customize columns icon](assets/customize-columns-icon.png), then select the columns that you want to be displayed in the Alerts manager.

   The following columns are available:

   | Column title  | Description |
   |---|---|
   | Title and description | These values are provided in the Alert builder. To edit the title and description, select the title link to open the Alert builder.  |
   | Favorites  | Displays star icons next to each alert, allowing you to mark alerts as favorites. |
   | Type | Shows whether the alert is an Analytics data alert or a Server call usage alert. |
   | Enabled | Shows whether the alert is currently enabled or disabled. | 
   | Report suite | Indicates in which report suite the alert was last saved.  |
   | Owner | Indicates who owns the alert. As a non-admin, you can see only alerts you own or those that were shared with you.  |
   | Tags | Shows tags that were applied to the alert, either by you or by people who shared the alert with you.  |
   | Expiration date | Shows the date and time when the alert is set to expire. |
   | Date modified | Indicates the date when the alert was last modified.  |

   {style="table-layout:auto"}
   
   
    When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> 
   
-->

