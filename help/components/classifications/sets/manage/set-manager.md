---
title: Indelingssetmanager
description: Classificatiesets beheren in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
source-git-commit: 496b4891d447ed9dd091a6498a792146a2d5aceb
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Indelingssetmanager

Met de indelingssetmanager kunt u classificatiesets maken, bewerken of verwijderen.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]**

Indelingssets bestaan uit **Abonnementen** (rapportsuite en dimensiecombinaties) en **Classificatienamen** (afmetingen met classificatiegegevens). Abonnementen zijn geconfigureerd onder [Instellingen](settings.md), terwijl classificatienamen zijn geconfigureerd onder [Schema](schema.md).

## Filterclassificatiesets

De linkerkant van het beheer van classificatiesets biedt filterinstellingen om de gewenste classificatieset te vinden. Door op het filterpictogram te klikken schakelt u de zichtbaarheid van de filterinstellingen in of uit. U kunt classificatiesets filteren op **[!UICONTROL Tags]**, **[!UICONTROL Report suite]**, of **[!UICONTROL Owner]**.

![Classificatiesetfilters](../../assets/classification-set-filters.png)

## Kolommen met indelingssetbeheer

De volgende kolommen zijn beschikbaar in de het reeksmanager van de Classificatie:

* **[!UICONTROL Classification set]**: De naam van de classificatieset. Op de naam van een classificatieset klikken [bewerkt de instellingen](settings.md).
* **[!UICONTROL Subscriptions]**: Het aantal abonnementen waarop deze classificatieset van toepassing is.
* **[!UICONTROL Owner]**: De eigenaar van het classificatieset.
* **[!UICONTROL Classifications]**: Het aantal classificatieafmetingen dat het classificatieset bevat.
* **[!UICONTROL Automated]**: Hiermee wordt bepaald of de classificatieset is geconfigureerd voor het automatisch importeren van gegevens uit een cloudlocatie. Automatisering kan worden geconfigureerd in de classificatieset [schema](schema.md).
* **[!UICONTROL Last Modified]**: De datum en het tijdstip waarop het classificatieset voor het laatst is gewijzigd.

## Opties maken of bewerken

De volgende knoppen zijn beschikbaar in het venster Indelingssetbeheer:

* **[!UICONTROL Add]**: [Maken](create.md) een classificatieset.
* **[!UICONTROL Search by title]**: Zoeken naar classificatiesets op naam.
* **[!UICONTROL Load more]**: In eerste instantie worden maximaal 1000 classificatiesets weergegeven door de classificatiesetmanager. Met deze knop worden 1000 andere classificatiesets geladen.
* **Kolommen tonen/verbergen**: Zichtbaarheid van elke kolom in-/uitschakelen [!UICONTROL Classification set].

Selecteer een of meer classificatiesets door op het selectievakje naast de gewenste classificatieset te klikken. Als u een classificatieset selecteert, worden de volgende opties weergegeven:

* **[!UICONTROL Tag]**: Voeg een of meer tags toe aan de geselecteerde classificatiesets, zodat u classificatiesets kunt ordenen of groeperen, zodat u deze in de toekomst gemakkelijker kunt vinden.
* **[!UICONTROL Delete]**: Hiermee verwijdert u de classificatieset. Indelingsafmetingen op basis van deze classificatieset zijn niet meer beschikbaar. Geplande projecten die de geschrapte classificatiereeks gebruiken blijven het gebruiken van afhankelijke dimensies tot u het geplande project opnieuw opslaat.
* **[!UICONTROL Consolidate]**: Een nieuwe [consolidatie](../consolidations/process.md).
* **[!UICONTROL Rename]**: Wijzig de naam van de geselecteerde classificatieset.
