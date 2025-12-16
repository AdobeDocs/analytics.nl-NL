---
title: Classificatiesets maken
description: Leer hoe u Beschikbare velden en beschrijvingen kunt gebruiken bij het maken van een classificatieset.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: 0f80bb314c8e041a98af26734d56ab364c23a49b
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Classificatiesets maken en bewerken

U [ creeert ](#create-a-classification-set) en [ geeft ](#edit-a-classification-set) classificatiereeksen van de manager van de Reeksen van de Classificatie uit.

## Een classificatieset maken

Een classificatieset maken:

1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]**.
1. In het dialoogvenster **[!UICONTROL Add New Classification Set]** :

   ![ de Reeksen van de Classificatie - voeg Nieuwe Reeks van de Classificatie toe ](assets/classifications-sets-new.png)

   1. Voer een **[!UICONTROL Name]** in. Bijvoorbeeld: `Classification Set Example` .
   1. Voer een **[!UICONTROL Description (optional)]** in. Bijvoorbeeld `Example classification set` .
   1. Voer een of meer e-mailadressen (gescheiden door komma&#39;s) in **[!UICONTROL Notify of issues]** in. E-mailmeldingen worden naar deze gebruikers verzonden bij problemen.
   1. Selecteer de **[!UICONTROL Type]** classificatieset. Mogelijke typen zijn:
      * **[!UICONTROL Primary]**. Een primair classificatieset is van toepassing op in Adobe Analytics verzamelde afmetingen. Primaire classificaties zijn een manier om waarden van korreldimensies te groeperen (classificeren) in zinvollere niveaus van gegevens. U kunt bijvoorbeeld interne zoektrefwoorden groeperen in interne zoekcategorieën om de thema&#39;s in uw zoekgegevens te begrijpen. Of classificeer product SKUs door kleur of categorie.
         * Voer een of meer **[!UICONTROL Subscriptions]** in.  U kunt meerdere combinaties **[!UICONTROL Report Suite]** en **[!UICONTROL Dimension]** definiëren voor een classificatieset.

         * Selecteer ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om een **[!UICONTROL Report Suite]** en **[!UICONTROL Key Dimension]** combinatie te schrappen.

        Als u een combinatie **[!UICONTROL Report Suite]** en **[!UICONTROL Key Dimension]** toevoegt die al in een andere classificatieset bestaat, wordt een rood gekleurd bericht weergegeven.
U kunt:
         * Selecteer **[!UICONTROL Add to existing]** om de andere classificatiereeks te openen en [ classificaties aan het schema ](schema.md) voor die andere classificatiereeks toe te voegen.
         * Wijzig **[!UICONTROL Report Suite]** en **[!UICONTROL Key Dimension]** in een combinatie die niet is geabonneerd op een andere classificatieset.
      * **[!UICONTROL Lookup]**. Een opzoektabel wordt meestal aangeduid als onderliggende of subclassificaties en is een classificatie van een primaire classificatie. Een zoekopdracht bestaat uit metagegevens over een classificatiewaarde in plaats van de oorspronkelijke dimensie. Bijvoorbeeld, zou de dimensie van het a *Product* een primaire classificatie van *Code van de Kleur* kunnen hebben. Een raadplegingslijst van *naam van de Kleur* kon dan aan de *code van de Kleur* worden vastgemaakt om elke kleurencode te verklaren.
1. Selecteer **[!UICONTROL Save]** om de classificatieset op te slaan. Selecteer **[!UICONTROL Cancel]** om de definitie te annuleren.
1. Om het schema voor de classificatiereeks te bepalen, selecteer uw onlangs gecreeerde classificatiereeks van de **[!UICONTROL Classification Sets]** manager om [ de classificatiereeks ](#edit-a-classification-set) uit te geven.


## Een classificatieset bewerken

Een classificatieset bewerken:

1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .
1. Selecteer de naam van de classificatieset.
1. In de **[!UICONTROL Classification Set: _dialoog van de classificatiereeks naam_]**, kunt u de [ montages ](settings.md) en het [ schema ](schema.md) voor de classificatiereeks bepalen.
1. Als u klaar bent, selecteert u **[!UICONTROL Save]** om de wijzigingen op te slaan. Selecteer **[!UICONTROL Cancel]** om te annuleren.


<!--


### Schema

In the Schema tab 





You can use the Classification set manager to create a classification set.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > **[!UICONTROL Add]**

When creating a classification set, the following fields are available.

* **[!UICONTROL Name]**: A text field used to identify the classification set. This field cannot be edited upon creation, but can be renamed later.
* **[!UICONTROL Column Name]**: The name of the first classification dimension that you want to create. This field is the dimension name used in Analysis Workspace, and the column name when exporting classification data. You can add more column names after the classification set is created.
* **[!UICONTROL Type]**: Radio buttons that indicate the type of classification.
  * **[!UICONTROL Primary]**: Apply to dimensions collected in Analytics. They are a way to group (classify) granular dimension values into more meaningful levels of data. For example, you might want to group internal search keywords into internal search categories, to better understand themes in your search data.
  * **[!UICONTROL Lookup]**: Commonly referred to as child or subclassifications, a lookup table is a classification of a primary classification. It is metadata about a classification value, rather than the original dimension. For example, the Product variable might have a primary classification of 'Color code'. A lookup table of 'Color name' could then be attached to 'Color code' to further explain what each code means.
* **[!UICONTROL Subscriptions]** The report suites and dimensions that this classification set applies to. You can add multiple report suite and dimension combinations to a classification set.

![Create a Classification set](../../assets/classification-set-create.png)

If a classification set exists for a given report suite + variable, the classification is added to the schema instead. A given report suite + variable combination cannot belong to multiple classification sets.

-->