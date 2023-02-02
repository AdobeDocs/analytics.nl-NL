---
description: Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.
title: Niet-geclassificeerde codes
feature: Classifications
exl-id: 37288c2d-f6f6-4343-87a1-3c3a7b56fe32
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# Niet-geclassificeerde codes

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.

## Niet-geclassificeerde codes {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met het label *`None`*. Het kan handig zijn de naam te wijzigen *`None`* naar iets beschrijvender.

Stel dat uw volgcodes informatie bevatten die het type mobiele campagne aangeeft waaraan de trackingcode is gekoppeld. U gebruikt classificatie (het Type van Mobiele Campagne) om deze het volgen codes in categorieën zoals Mobiel Web, de Toepassing van iOS, Toepassing Android te groeperen, etc. Sommige campagnes zijn misschien geen mobiele campagnes en worden daarom niet geclassificeerd als een type mobiele campagne. Alle niet-geclassificeerde volgcodes worden gegroepeerd onder *`None`* in de [!UICONTROL Mobile Campaign Type] verslag.

## De naam van de indelingssleutel Geen wijzigen {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

De naam wijzigen van een niet-geclassificeerde sleutel die wordt weergegeven als *`none`* bij de rapportage:

1. Exporteer classificaties met de importer naar een lokaal bestand.
1. Voeg een rij toe aan het bestand en typ `~none~` in de kolom Sleutel.
1. Typ in de rij die u hebt toegevoegd de beschrijvende naam in de desbetreffende classificatiekolom(men).

   Om het voorbeeld in deze documentatie te volgen, zou u &quot;niet mobiele campagne&quot;in een kolom kunnen typen genoemd [!UICONTROL Mobile Campaign Type].

   De naam van dit item wordt gewijzigd *`None`* tot *`non-mobile campaign`* in de [!UICONTROL Mobile Campaign Type] verslag.

   ![Voorbeeld van een niet-geclassificeerde sleutel](/help/components/classifications/importer/assets/non-classified-key.png)

1. [De gegevens importeren](/help/components/classifications/importer/import-file.md) terug naar het systeem.
