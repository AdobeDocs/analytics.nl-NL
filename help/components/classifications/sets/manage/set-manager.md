---
title: Indelingssetmanager
description: Classificatiesets beheren in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Indelingssetmanager

Met de indelingssetmanager kunt u classificatiesets maken, bewerken of verwijderen.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]**

De reeksen van de classificatie bestaan uit **Abonnementen** (rapportreeks en afmetingscombinaties) en **de namen van de Indeling** (dimensies die classificatiegegevens bevatten). De abonnementen worden gevormd onder [ Montages ](settings.md), terwijl de classificatienamen onder [ Schema ](schema.md) worden gevormd.

## Filterclassificatiesets

De linkerkant van het beheer van classificatiesets biedt filterinstellingen om de gewenste classificatieset te vinden. Door op het filterpictogram te klikken schakelt u de zichtbaarheid van de filterinstellingen in of uit. U kunt classificatiesets filteren op **[!UICONTROL Tags]** of **[!UICONTROL Report suite]** .

![ de vastgestelde filters van de Classificatie ](../../assets/classification-set-filters.png)

1.000 classificatiesets worden vooraf geladen. De filters die in de linkerspoorlijn worden getoond weerspiegelen de opties voor de reeksen die worden vooraf geladen.

## Kolommen met indelingssetbeheer

De volgende kolommen zijn beschikbaar in de het reeksmanager van de Classificatie:

* **[!UICONTROL Classification set]**: De naam van de classificatieset. Het klikken van de naam van een classificatieset geeft zijn [ montages ](settings.md) uit.
* **[!UICONTROL Subscriptions]**: Het aantal abonnementen waarop deze classificatieset van toepassing is.
* **[!UICONTROL Classifications]**: Het aantal classificatieafmetingen dat de classificatieset bevat.
* **[!UICONTROL Automated]**: hiermee wordt bepaald of de classificatieset is geconfigureerd voor het automatisch importeren van gegevens uit een cloudlocatie. De automatisering kan in het schema van de classificatiereeks [ worden gevormd ](schema.md).
* **[!UICONTROL Last Modified]**: De datum en tijd waarop de classificatieset voor het laatst is gewijzigd.

## Opties maken of bewerken

De volgende knoppen zijn beschikbaar in het venster Indelingsensetbeheer:

* **[!UICONTROL Add]**: [ creeer ](create.md) een classificatiereeks.
* **[!UICONTROL Search by title]**: zoek naar classificatiesets op naam.
* **[!UICONTROL Load more]**: In eerste instantie worden maximaal 1000 classificatiesets weergegeven door de classificatiesetmanager. Met deze knop worden 1000 andere classificatiesets geladen.
* **toon/verberg kolommen**: Wissel zicht voor om het even welke kolom naast [!UICONTROL Classification set].

Selecteer een of meer classificatiesets door op het selectievakje naast de gewenste classificatieset te klikken. Als u een classificatieset selecteert, worden de volgende opties weergegeven:

* **[!UICONTROL Tag]**: Voeg een of meer tags toe aan de geselecteerde classificatiesets, zodat u classificatiesets kunt ordenen of groeperen, zodat u deze in de toekomst gemakkelijker kunt vinden.
* **[!UICONTROL Delete]** : hiermee verwijdert u de classificatieset. Indelingsafmetingen op basis van deze classificatieset zijn niet meer beschikbaar. Geplande projecten die de geschrapte classificatiereeks gebruiken blijven het gebruiken van afhankelijke dimensies tot u het geplande project opnieuw opslaat.
* **[!UICONTROL Consolidate]**: Begin een nieuwe [ consolidatie ](../consolidations/process.md).
* **[!UICONTROL Rename]**: wijzig de naam van de geselecteerde classificatieset.
