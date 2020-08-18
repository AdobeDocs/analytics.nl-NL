---
description: 'null'
title: Segmentproblemen oplossen
uuid: 8476d617-4b44-4ff2-9b3a-02685f666afc
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Segmentproblemen oplossen

## Fout: &quot;Niet-compatibele elementen in dit segment&quot; {#section_B167EE10A0844E649DD7E14D0BAEDA17}

Deze fout treedt op wanneer u een segment probeert op te slaan in de map Data Warehouse waarin het segment elementen bevat die niet compatibel zijn met Data Warehouse. Voer een van de volgende twee handelingen uit om deze fout op te lossen:

* Het segment opslaan in een andere map
* Verwijder of verander de incompatibele gedeelten van het segment.

## Waarom retourneert mijn segment helemaal geen gegevens? {#section_999749CBBE984142AEA49A6E68E6730A}

Mogelijke redenen:

* Omgekeerd nesten - bijvoorbeeld het nesten van een Visitor-container onder een Visit-container.
* Het rapport ondersteunt segmentatie niet.
* Er zijn geen gegevens die overeenkomen met de segmenteringscriteria.

## Waarom kan ik niet het segment zien dat ik in de Manager van het Segment creeerde? {#section_BE0A0930A2694A23BB32DA71696D52CE}

Mogelijke redenen:

* Sommige afmetingen zijn alleen beschikbaar in Data Warehouse en niet in Segmentbeheer.
* Segment is niet compatibel met Rapporten &amp; Analytics.
* Het segment wordt gecontroleerd slechts voor een specifieke rapportreeks.
* Een gedeeld segment kan door een andere gebruiker zijn verwijderd.
* Segmenten konden niet worden geladen vanwege een probleem met het datacenter of de browsercache.
* Het segment is niet opgeslagen.
* IP adres kan bij het eind van de gebruiker worden geblokkeerd.

## Waarom lijken de gegevens van de Pagina die na het toepassen van een segment worden getoond onjuist? {#section_B226AF69FE06463A8BC5337FDA8D4949}

Mogelijke redenen:

* De regels/de exploitanten zijn onjuist voor het vereiste resultaat.
* Onjuiste toepassing van containers op het segment.
* De variabelen van het verkeer die aan segment worden gebruikt worden niet behoorlijk geplaatst of zijn verlopen.

