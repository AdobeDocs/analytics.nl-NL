---
title: Consolidaties van classificatiesets beheren
description: Leer hoe u een of meer classificatiesets samenvoegt tot één classificatieset.
exl-id: 0be97ca4-56c3-4642-9347-924812e88e8c
feature: Classifications
source-git-commit: 2ced7cd61c4119347be2ef0fba9b8d60ee6c4df2
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Classificatieconsolidatie beheren

Als u meerdere classificatiesets hebt die vergelijkbare classificatiegegevens bevatten, kunt u deze samenvoegen tot één classificatieset. Wanneer u twee of meer classificatiesets samenvoegt, genereert Adobe een nieuwe classificatieset die alle classificatiegegevens van elke afzonderlijke classificatieset bevat. Consolidaties zijn handig wanneer u gegevens hebt geüpload naar een groot aantal rapportensuites. Of wanneer u afmetingen hebt die dezelfde classificatiegegevens bevatten en u deze wilt samenvoegen in één workflow.

Adobe Analytics moet toegang hebben tot productbeheer om de consolidatiemanager voor classificatiesets te kunnen bekijken.



Indeling consolideren beheren:

1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Consolidations]** .


## Classification Consolidations Manager

De manager **[!UICONTROL Classification Sets - Consolidations]** heeft de volgende interface-elementen:

![&#x200B; de Reeksen van Classificaties - de Manager van Consolidaties &#x200B;](assets/classifications-sets-consolidations.png)



### Rangschikkingsoverzicht

De lijst ➊ bevat classificatieconsolisies die zijn gemaakt en gevalideerd en die mogelijk worden geconsolideerd. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Consolidation Name]** | De naam van de classificatiesets consolidatie. |
| **[!UICONTROL Current Job]** | De taak die aan de classificatie is gekoppeld, stelt consolidatie in. |
| **[!UICONTROL Status]** | De status van de classificatiesets consolidatie. Mogelijke waarden zijn: **[!UICONTROL Created]**, **[!UICONTROL Canceled]**, **[!UICONTROL Canceling]**, **[!UICONTROL Validating]**, **[!UICONTROL Failed Validation]**, **[!UICONTROL Validated]**, **[!UICONTROL Comparing]**, **[!UICONTROL Comparison Failed]**, **[!UICONTROL Consolidation]**, **[!UICONTROL Submitted]**, **[!UICONTROL Consolidating]**, **[!UICONTROL Consolidation Failed]**, **[!UICONTROL Consolidation Succeeded]**, **[!UICONTROL Waiting for Approval]**, **[!UICONTROL Finalizing]**, **[!UICONTROL Failed]** of **[!UICONTROL Completed]** . |
| **[!UICONTROL Creation time]** | De aanmaaktijd van de classificatie stelt consolidatie in. |
| **[!UICONTROL Completion Time]** | De voltooiingstijd van de classificatieconsolisies. |


Als u de grootte van een kolom in de consolidatielijst wilt wijzigen, kunt u:

* Houd de cursor boven het kolomscheidingsteken en sleep het kolomscheidingsteken naar de gewenste kolombreedte.
* Selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Resize column]**. Met een verticale lijn met de knop voor vergroten/verkleinen kunt u de grootte van de kolom naar wens wijzigen.

Een kolom sorteren in de consolidatielijst

* Selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Sort Ascending]** of **[!UICONTROL Sort Descending]**. Een pijl (↓) geeft aan welke kolom en hoe de kolom wordt gesorteerd.

### Zoeken en knoppen

In het gebied ➋ boven op de lijst met classificatieconsolisies kunt u het volgende doen:

* Onderzoek ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) naar classificatieconsolidatie. De resultaten worden weergegeven in de lijst van classificatieconsolideringen. Selecteer ![&#x200B; CrossSize200 &#x200B;](/help/assets/icons/CrossSize200.svg) om het onderzoek te ontruimen.
* Verwijder een filter dat wordt toegepast op de consolidatielijst van classificatiesets. Selecteer ![&#x200B; CrossSize100 &#x200B;](/help/assets/icons/CrossSize100.svg) om een filter te verwijderen.
* Maak een nieuwe consolidatie van classificatiesets. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]** om de de consolidatiedialoog van classificatiesets te openen en een nieuwe classificatiesets consolidatie te bepalen.
* Definieer de kolommen in de lijst met classificatieconsolisies. Selecteer ![&#x200B; ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg) en in de **[!UICONTROL Customize table]** dialoog selecteren de kolommen onder **[!UICONTROL Select columns to show]** te tonen. Selecteer **[!UICONTROL Apply]** om de kolominstellingen toe te passen.


### Actiebalk

Wanneer u een of meer classificatiesets selecteert in de lijst met classificatiesets, wordt een blauwe actiebalk ➌ weergegeven. De volgende acties zijn beschikbaar in de actiebalk:

| Pictogram | Handeling | Beschrijving |
|---|---|---|
| ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Edit]** | [&#x200B; geef de classificatiesets consolidatie &#x200B;](process.md#edit-a-consolidation) uit |
| ![&#x200B; ViewDetail &#x200B;](/help/assets/icons/ViewDetail.svg) | **[!UICONTROL View]** | Bekijk details van de consolidatie van de classificatieset. Afhankelijk van de status, kunt u [&#x200B; goedkeuren of &#x200B;](process.md#approve) [&#x200B; de consolidatie annuleren.](process.md#cancel) |


### Deelvenster Filter

Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om het filterpaneel ➍ te tonen dat u toestaat om de lijst van classificatieconsolidatie te filtreren. U kunt filteren op:

* **[!UICONTROL Status]**. Selecteer een van de mogelijke waarden om de lijst met classificatieconsolisies op status te filteren. |
* **[!UICONTROL Completion Time]**. Selecteer een van de mogelijke waarden om de lijst met classificatieconsolisies na voltooiing te filteren.
* **[!UICONTROL Creation Time]**. Selecteer een van de mogelijke waarden om de lijst met classificatieconsolisies na voltooiing te filteren.


Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om het filterpaneel te verbergen.

De filters die in het deelvenster Filters worden weergegeven, weerspiegelen de opties voor de classificatieconsolisies die vooraf zijn geladen.


<!--

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]**

Once a consolidation is run, the original classification sets are removed, with the consolidated classification set taking their place. Click **[!UICONTROL Add]** to [Create a consolidation](process.md).

## Filter classification sets

The left side of the Classification set consolidation manager provides filter settings to locate the desired consolidation. Clicking the filter icon toggles the filter settings visibility. You can filter consolidations by **[!UICONTROL Status]**, **[!UICONTROL Completion time]**, or **[!UICONTROL Creation time]**.

![Classification set consolidation filters](../../assets/classification-set-consolidation-filters.png)

Additional filter options are available above the Classification set consolidation manager columns:

* **[!UICONTROL Search by title]**: Search for consolidations by name.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Name].

## Classification set consolidation manager columns

The following columns are available in the Classification set consolidation manager:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Current job]**: The current job. 
* **[!UICONTROL Status]**: The status of the consolidation. 
* **[!UICONTROL Creation date]**: The date and time that the consolidation was created.
* **[!UICONTROL Completion date]**: The date and time that the consolidation completed (or failed).

-->
