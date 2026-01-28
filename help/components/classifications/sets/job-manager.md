---
title: Indelingstaakbeheer
description: Leer hoe u huidige en voltooide classificatietaken bekijkt die zijn gegenereerd op basis van classificatiesets.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
feature: Classifications
source-git-commit: cfa8335008548254786e46dfe634229edad5bd54
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Classificatietaken bekijken en volgen

De manager van de banen van de Classificatie toont huidige en voltooide classificatietaken die voor classificatiereeksen worden geproduceerd. U kunt de manager ook gebruiken om classificatiegegevens of malplaatjes voor een bepaalde baan te downloaden.

Om classificatietaken te bekijken en te volgen:


1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Jobs]** .

## Taakmanager classificeren

De manager **[!UICONTROL Classification Sets - Jobs]** heeft de volgende interface-elementen:

![ de Reeksen van Classificaties - de Manager van de Baan ](manage/assets/classifications-sets-jobs.png)



### Lijst met classificatieopdrachten

De **[!UICONTROL Classification Jobs]** list ➊ geeft classificatietaken weer. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Job Id]** | De id van de classificatietaak. |
| **[!UICONTROL Classification Set]** | Het classificatieset dat aan de classificatietaak is gekoppeld. |
| **[!UICONTROL Size]** | De grootte van het bestand dat is geëxporteerd of geïmporteerd als onderdeel van de classificatietaak. |
| **[!UICONTROL Status]** | De status van de classificatietaak. Mogelijke waarden zijn: **[!UICONTROL Created]**, **[!UICONTROL Queued]**, **[!UICONTROL Validated]**, **[!UICONTROL Failed validation]**, **[!UICONTROL Processing]**, **[!UICONTROL Done processing]**, **[!UICONTROL Failed processing]** , **[!UICONTROL Completed]** of **[!UICONTROL Progress]** . Indien getoond, houd over waakzaam ![ Alarm ](/help/assets/icons/Alert.svg) om extra informatie te tonen. |
| **[!UICONTROL File Name]** | Identificeert de naam of functionaliteit die wordt gebruikt om het bestand te importeren of exporteren als onderdeel van de classificatietaak. Mogelijke waarden zijn: <ul><li>*geen waarde*</li><li>De naam van het bestand dat wordt verwerkt als onderdeel van de classificatietaak.</li><li>**[!UICONTROL SAINT Export]**: De baan is een uitvoer van de [ interface van erfenisclassificaties ](/help/components/classifications/importer/c-working-with-saint.md).</li><li>**[!UICONTROL export for _classificatiereeks _bij_ timestamp_]**: De baan is een download van de [ schema ](manage/schema.md#download) interface.</li></ul> |
| **[!UICONTROL Job Type]** | Het type classificatietaak. Mogelijke waarden zijn: **[!UICONTROL Import]** of **[!UICONTROL Export]** . |
| **[!UICONTROL Source]** | De bron van de classificatietaak. Mogelijke waarden zijn: **[!UICONTROL Web API]** , **[!UICONTROL Direct API Upload]** , **[!UICONTROL Adobe]** , **[!UICONTROL SAINT]** of **[!UICONTROL Unknown]** . |
| **[!UICONTROL Modified Lines]** | Het aantal gewijzigde regels dat de classificatietaak heeft gewijzigd. |
| **[!UICONTROL Total Lines]** | Het aantal totale lijnen dat de classificatiebaan verwerkte. |
| **[!UICONTROL Completion Time]** | De voltooiingstijd van de classificatietaak. |
| **[!UICONTROL File Download]** | Het gebruik ![ Download ](/help/assets/icons/Download.svg) om het dossier (malplaatje of gegevens) te downloaden verbonden aan de classificatietaak. |

Als u de grootte van een kolom in de lijst met classificatietaken wilt wijzigen, kunt u:

* Houd de cursor boven het kolomscheidingsteken en sleep het kolomscheidingsteken naar de gewenste kolombreedte.
* Selecteer ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Resize column]**. Met een verticale lijn met de knop voor vergroten/verkleinen kunt u de grootte van de kolom naar wens wijzigen.

Een kolom sorteren in de lijst met classificatietaken

* Selecteer ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) en selecteer **[!UICONTROL Sort Ascending]** of **[!UICONTROL Sort Descending]**. Een pijl (↓) geeft aan welke kolom en hoe de kolom wordt gesorteerd.


### Zoeken en knoppen

In het gebied ➋ boven op de lijst met classificatietaken kunt u het volgende doen:

* Onderzoek ![ Onderzoek ](/help/assets/icons/Search.svg) naar classificatietaken. De resultaten worden weergegeven in de lijst met classificatietaken. Selecteer ![ CrossSize200 ](/help/assets/icons/CrossSize200.svg) om het onderzoek te ontruimen.
* Verwijder een filter dat is toegepast op de lijst met classificatietaken. Selecteer ![ CrossSize100 ](/help/assets/icons/CrossSize100.svg) om een filter te verwijderen.
* Selecteer ![ MoreCircle ](/help/assets/icons/MoreCircle.svg) om een toevoeging 1000 classificatietaken te laden. In eerste instantie worden in de lijst met classificatiesets maximaal 1000 classificatietaken weergegeven.
* Definieer de kolommen in de lijst met classificatiesets taken. Selecteer ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) en in de **[!UICONTROL Customize table]** dialoog selecteren de kolommen onder **[!UICONTROL Select columns to show]** te tonen. Selecteer **[!UICONTROL Apply]** om de kolominstellingen toe te passen.



### Deelvenster Filter

Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om het filterpaneel ➌ te tonen dat u toestaat om de lijst van classificatietaken te filtreren. U kunt filteren op:

* **[!UICONTROL Classification Set]**. Selecteer een of meer classificatiesets om de lijst met classificatietaken te filteren.
* **[!UICONTROL Completion Time]**. Selecteer een van de mogelijke waarden om de lijst met classificatietaken na voltooiing te filteren.
* **[!UICONTROL Status]**. Selecteer een van de mogelijke waarden om de lijst met classificatietaken op status te filteren.
* **[!UICONTROL Job Type]**. Selecteer een van de mogelijke waarden om de lijst met classificatietaken op het taaktype te filteren.
* **[!UICONTROL Source]**. Selecteer een van de mogelijke waarden om de lijst met classificatietaken op de bron te filteren.


Selecteer ![ Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om het filterpaneel te verbergen.

De filters die worden weergegeven in het deelvenster Filters weerspiegelen de opties voor de classificatietaken die zijn voorgeladen.
