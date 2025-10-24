---
title: Classificatiesets beheren
description: Classificatiesets beheren in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: 015a5556b4de38c142e1f7f861b73eae3d186ada
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Classificatiesets beheren

U kunt classificatiesets maken, hernoemen, bewerken, consolideren, verwijderen en coderen in de interface van het classificatiesets. U kunt ook filteren op en zoeken naar specifieke classificatiesets.

Classificatiesets beheren:

1. Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .

## Manager voor classificatiesets

De manager **[!UICONTROL Classification Sets]** heeft de volgende interface-elementen:

![&#x200B; de plaatsingsmanager van de Classificatie &#x200B;](assets/classification-sets-manage.png)


### Lijst met classificatiesets

In de **[!UICONTROL Classification Sets]** lijst ➊ worden alle classificatiesets weergegeven. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Classification Set]** | De titel van het classificatieset. Selecteer de titel om [&#x200B; uit te geven classificatiereeks &#x200B;](create.md#edit-a-classification-set). |
| **[!UICONTROL Subscriptions]** | Het aantal abonnementen waarop de classificatieset van toepassing is. |
| **[!UICONTROL Classifications]** | Het aantal classificatieafmetingen dat het classificatieset bevat. |
| **[!UICONTROL Automated]** | Is de classificatieset automatisch geconfigureerd voor het importeren van gegevens uit een cloudlocatie? Deze automatisering kan als deel van het [&#x200B; schema van classificatiesets &#x200B;](schema.md) worden gevormd. |
| **[!UICONTROL Last modified]** | Het tijdstempel van de laatste wijziging van de classificatieset. |

Als u de grootte van een kolom wilt wijzigen in de lijst met classificatiesets, kunt u:

* Houd de cursor boven het kolomscheidingsteken en sleep het kolomscheidingsteken naar de gewenste kolombreedte.
* Selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Resize column]**. Met een verticale lijn met de knop voor vergroten/verkleinen kunt u de grootte van de kolom naar wens wijzigen.

Een kolom sorteren in de lijst met classificatiesets

* Selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Sort Ascending]** of **[!UICONTROL Sort Descending]**. Een pijl (↓) geeft aan welke kolom en hoe de kolom wordt gesorteerd.

### Zoeken en knoppen

In het gebied ➋ boven op de lijst met classificatiesets kunt u het volgende doen:

* Onderzoek ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) naar classificatiereeksen. De resultaten worden weergegeven in de lijst met classificatiesets. Selecteer ![&#x200B; CrossSize200 &#x200B;](/help/assets/icons/CrossSize200.svg) om het onderzoek te ontruimen.
* Verwijder alle filters die op de lijst met classificatiesets zijn toegepast. Selecteer ![&#x200B; CrossSize100 &#x200B;](/help/assets/icons/CrossSize100.svg) om een filter te verwijderen.
* Selecteer ![&#x200B; MoreCircle &#x200B;](/help/assets/icons/MoreCircle.svg) om een toevoeging 1000 classificatiereeksen te laden. In eerste instantie worden in de lijst met classificatiesets maximaal 1000 classificatiesets weergegeven.
* Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]** om [&#x200B; een nieuwe classificatiereeks &#x200B;](create.md#create-a-classification-set) tot stand te brengen.
* Definieer de kolommen in de lijst met classificatiesets. Selecteer ![&#x200B; ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg) en in de **[!UICONTROL Customize table]** dialoog selecteren de kolommen onder **[!UICONTROL Select columns to show]** te tonen. Selecteer **[!UICONTROL Apply]** om de kolominstellingen toe te passen.


### Actiebalk

Wanneer u een of meer classificatiesets selecteert in de lijst met classificatiesets, wordt een blauwe actiebalk ➌ weergegeven. De volgende acties zijn beschikbaar in de actiebalk:

| Pictogram | Handeling | Beschrijving |
|---|---|---|
| ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Edit]** | [&#x200B; geeft de classificatiereeks &#x200B;](create.md#edit-a-classification-set) in de bouwer van de classificatieset uit. |
| ![&#x200B; anders noemen &#x200B;](/help/assets/icons/Rename.svg) | **[!UICONTROL Rename]** | Wijzig de naam van een classificatieset.<br/> in de **[!UICONTROL Rename: _classificatiereeks_]** dialoog gaat een nieuwe naam in en selecteert **[!UICONTROL Rename]**. |
| ![&#x200B; Fusie &#x200B;](/help/assets/icons/Merge.svg) | **[!UICONTROL Consolidate]** | [&#x200B; consolideer classificatiesets &#x200B;](/help/components/classifications/sets/consolidations/manage.md). |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Een classificatieset verwijderen.<br/> de **[!UICONTROL Delete _classificatiereeks _?]**&#x200B;wordt weergegeven. Het verwijderen van een classificatieset kan niet ongedaan worden gemaakt. Voor alle geplande projecten of consolidatie waarvoor deze classificatie wordt gebruikt, blijft de definitie van deze classificatieset worden gebruikt totdat u de geplande projecten opnieuw opslaat of de geplande consolidaties opnieuw valideert. Selecteer **[!UICONTROL Delete]**&#x200B;om de classificatieset te verwijderen. |
| ![&#x200B; Etiket &#x200B;](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label het classificatieset.<br/> in de **[!UICONTROL Tag: _classificatiereeks_]** dialoog, selecteer één of meerdere markeringen van het **[!UICONTROL Tags]** drop-down menu om markeringen toe te voegen. Of voer een of meer nieuwe tags in. Gebruik ![&#x200B; CrossSize100 &#x200B;](/help/assets/icons/CrossSize100.svg) om een markering te verwijderen. <br/> Uitgezocht **[!UICONTROL Save]** om de markeringen te bewaren. |


### Deelvenster Filter

Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om het filterpaneel ➍ te tonen dat u toestaat om de lijst van de classificatieset te filtreren. U kunt filteren op:

* **[!UICONTROL Tags]**. Selecteer een of meer tags om de lijst met classificatiesets op labels te filteren.
* **[!UICONTROL Report Suite]**. Selecteer een of meer rapportsuites om de lijst met classificatiesets op rapportsuites te filteren.

Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om het filterpaneel te verbergen.

De filters in het deelvenster Filters weerspiegelen de opties voor de classificatiesets die vooraf zijn geladen.


<!-- old content

The Classification set manager allows you to create, edit, or delete classification sets.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]**

Classification sets consist of **Subscriptions** (report suite and dimension combinations) and **Classification names** (dimensions containing classification data). Subscriptions are configured under [Settings](settings.md), while classification names are configured under [Schema](schema.md).

## Filter classification sets

The left side of the Classification set manager provides filter settings to locate the desired classification set. Clicking the filter icon toggles the filter settings visibility. You can filter classification sets by **[!UICONTROL Tags]** or **[!UICONTROL Report suite]**.

![Classification set filters](../../assets/classification-set-filters.png)

Note that 1,000 classification sets are preloaded at a time. The filters shown in the left rail reflect the options for the sets that are preloaded.

## Classification set manager columns

The following columns are available in the Classification set manager:

* **[!UICONTROL Classification set]**: The classification set name. Clicking a classification set name edits its [settings](settings.md).
* **[!UICONTROL Subscriptions]**: The number of subscriptions that this classification set applies to.
* **[!UICONTROL Classifications]**: The number of classification dimensions that the classification set contains.
* **[!UICONTROL Automated]**: Determines if the classification set is configured to automatically import data from a cloud location. Automation can be configured in the classification set's [schema](schema.md).
* **[!UICONTROL Last Modified]**: The date and time that the classification set was last modified.

## Create or edit options

The following buttons are available in the Classification set manager:

* **[!UICONTROL Add]**: [Create](create.md) a classification set.
* **[!UICONTROL Search by title]**: Search for classification sets by name.
* **[!UICONTROL Load more]**: The Classification set manager initially displays up to 1000 classification sets. This button loads 1000 more classification sets.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Classification set].

Select one or more classification sets by clicking the checkbox next to the desired classification set. Selecting a classification set reveals the following options:

* **[!UICONTROL Tag]**: Add one or more tags to the selected classification sets, which allows you to organize or group classification sets to make them easier to locate in the future.
* **[!UICONTROL Delete]**: Deletes the classification set. Classification dimensions based on this classification set are no longer available. Scheduled projects using the deleted classification set continue using dependent dimensions until you resave the scheduled project.
* **[!UICONTROL Consolidate]**: Start a new [consolidation](../consolidations/process.md).
* **[!UICONTROL Rename]**: Rename the selected classification set.

-->