---
description: Los en los kwesties met betrekking tot segmenten problemen op.
title: Probleemoplossing voor segmentering
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Probleemoplossing voor segmentering

## Fout: &quot;Niet-compatibele elementen in dit segment&quot; {#incompatible}

Deze fout treedt op wanneer u een segment probeert op te slaan in de map Data Warehouse waarin het segment elementen bevat die niet compatibel zijn met Data Warehouse. Voer een van de volgende twee handelingen uit om deze fout op te lossen:

* Het segment opslaan in een andere map
* Verwijder of verander de incompatibele gedeelten van het segment.

## Waarom retourneert mijn segment helemaal geen gegevens? {#no-data}

Mogelijke redenen:

* Omgekeerd nesten - bijvoorbeeld het nesten van een bezoekercontainer onder een Visit-container.
* Het rapport ondersteunt segmentatie niet.
* Er zijn geen gegevens die overeenkomen met de segmenteringscriteria.

## Waarom kan ik niet het segment zien dat ik in de Manager van het Segment creeerde? {#invisible}

Mogelijke redenen:

* Sommige afmetingen zijn alleen beschikbaar in Data Warehouse en niet in Segmentbeheer.
* Het segment wordt gecontroleerd slechts voor een specifieke rapportreeks.
* Een gedeeld segment kan door een andere gebruiker zijn verwijderd.
* Segmenten konden niet worden geladen vanwege een probleem met het datacenter of de browsercache.
* Het segment is niet opgeslagen.
* IP adres kan bij het eind van de gebruiker worden geblokkeerd.

## Waarom lijken de gegevens van de Pagina die na het toepassen van een segment worden getoond onjuist? {#page-data}

Mogelijke redenen:

* De regels/de exploitanten zijn onjuist voor het vereiste resultaat.
* Onjuiste toepassing van containers op het segment.
* De variabelen van het verkeer die aan segment worden gebruikt worden niet behoorlijk geplaatst of zijn verlopen.
