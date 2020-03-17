---
description: 'null'
title: Segmentproblemen oplossen
uuid: 8476d617-4b44-4ff2-9b3a-02685f666afc
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Segmentproblemen oplossen

## Fout: &quot;Niet-compatibele elementen in dit segment&quot; {#section_B167EE10A0844E649DD7E14D0BAEDA17}

Deze fout komt voor wanneer u probeert om een segment in de omslag van het Pakhuis van Gegevens te bewaren waar het segment elementen bevat niet compatibel met het Pakhuis van Gegevens. Voer een van de volgende twee handelingen uit om deze fout op te lossen:

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

