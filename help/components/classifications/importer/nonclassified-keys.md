---
description: Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.
subtopic: Classifications
title: Niet-geclassificeerde codes
feature: Admin Tools
uuid: b73a9161-0c6f-4c8d-900b-54ab2c36147c
exl-id: 37288c2d-f6f6-4343-87a1-3c3a7b56fe32
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---

# Niet-geclassificeerde codes

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met de naam Geen. Het kan handig zijn de naam Geen te wijzigen in een beschrijvender naam.

## Niet-geclassificeerde codes {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Niet-geclassificeerde sleutels worden in classificatierapporten gegroepeerd als een enkel lijstitem met het label *`None`*. Het kan handig zijn om de naam van *`None`* te wijzigen in een beschrijvender item.

Stel dat uw volgcodes informatie bevatten die het type mobiele campagne aangeeft waaraan de trackingcode is gekoppeld. U gebruikt classificatie (het Type van Mobiele Campagne) om deze het volgen codes in categorieën zoals Mobiel Web, iOS Toepassing, Android Toepassing te groeperen, etc. Sommige campagnes zijn misschien geen mobiele campagnes en worden daarom niet geclassificeerd als een type mobiele campagne. Alle niet-geclassificeerde volgcodes worden in het [!UICONTROL Mobile Campaign Type]-rapport gegroepeerd onder *`None`*.

## De naam van de indelingssleutel Geen wijzigen {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

Stappen die beschrijven hoe te om een niet-gerubriceerde sleutel anders te noemen die als *`none`* in het melden toont.

1. Exporteer classificaties met de importer naar een lokaal bestand.
1. Voeg een rij aan het dossier toe, en typ [!DNL ~none~] in de Belangrijkste kolom.
1. Typ in de rij die u hebt toegevoegd de beschrijvende naam in de desbetreffende classificatiekolom(men).

   Om het voorbeeld in deze documentatie te volgen, zou u &quot;niet-mobiele campagne&quot;in een kolom kunnen typen genoemd [!UICONTROL Mobile Campaign Name].

   Dit item wijzigt de naam *`None`* in *`non-mobile campaign`* in het [!UICONTROL Mobile Campaign Type]-rapport.
1. [Importeer de ](/help/components/classifications/importer/import-file.md) database in het systeem.
