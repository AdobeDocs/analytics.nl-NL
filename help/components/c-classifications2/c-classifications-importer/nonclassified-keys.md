---
description: Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.
subtopic: Classifications
title: Niet-geclassificeerde sleutels
topic: Admin tools
uuid: b73a9161-0c6f-4c8d-900b-54ab2c36147c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Niet-geclassificeerde sleutels

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.

## Niet-geclassificeerde sleutels {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als één enkel lijstitem met label *`None`*. Het kan handig zijn de naam te wijzigen *`None`* in een beschrijvende naam.

Stel dat uw volgcodes informatie bevatten die het type mobiele campagne aangeeft waaraan de trackingcode is gekoppeld. U gebruikt classificatie (het Type van Mobiele Campagne) om deze het volgen codes in categorieën zoals Mobiel Web, iOS Toepassing, Android Toepassing te groeperen, etc. Sommige campagnes zijn misschien geen mobiele campagnes en worden daarom niet geclassificeerd als een type mobiele campagne. Alle niet-geclassificeerde volgcodes worden onder *`None`* het [!UICONTROL Mobile Campaign Type] rapport gegroepeerd.

## De naam van de indelingssleutel Geen wijzigen {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

Stappen die beschrijven hoe te om een niet-gerubriceerde sleutel anders te noemen die zoals *`none`* in het melden toont.

1. Exporteer classificaties met de importer naar een lokaal bestand.
1. Voeg een rij toe aan het bestand en typ [!DNL ~geen~] rij in de kolom Sleutel.
1. Typ in de rij die u hebt toegevoegd de beschrijvende naam in de desbetreffende classificatiekolom(men).

   Als u het voorbeeld in deze documentatie wilt volgen, typt u &quot;niet-mobiele campagne&quot; in een kolom met de naam [!UICONTROL Mobile Campaign Name].

   Deze ingang hernoemt *`None`* aan *`non-mobile campaign`* in het [!UICONTROL Mobile Campaign Type] rapport.
1. [Importeer de gegevens](/help/components/c-classifications2/c-classifications-importer/import-file.md) weer in het systeem.
