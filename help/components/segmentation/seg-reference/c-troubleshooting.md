---
description: Los en los kwesties met betrekking tot segmenten problemen op.
title: Probleemoplossing voor segmentering
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
source-git-commit: d85e6990998e3c153ef969d8dc7f3a4835f683bf
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Problemen met segmentering

<!-- Looks like this is not part anymore of the current UI.

## Error: "Incompatible elements in this segment" {#incompatible}

This error occurs when you try to save a segment in the Data Warehouse folder where the segment contains elements not compatible with Data Warehouse. To resolve this error, do one of two things:

* Save the segment in a different folder 
* Remove or change the incompatible portions of the segment.

-->

## Waarom retourneert mijn segment helemaal geen gegevens? {#no-data}

Mogelijke redenen:

* Omgekeerd het nesten - bijvoorbeeld, het nestelen van a ![ Gebruiker ](/help/assets/icons/User.svg) **[!UICONTROL Visitor]** container onder a ![ Bezoek ](/help/assets/icons/Visit.svg) **[!UICONTROL Visit]** container.
* Het rapport ondersteunt segmentatie niet.
* Er zijn geen gegevens die overeenkomen met de segmenteringscriteria.

## Waarom kan ik niet het segment zien dat ik in de manager van het Segment creeerde? {#invisible}

Mogelijke redenen:

* Sommige afmetingen zijn alleen beschikbaar in Data Warehouse en niet in Segmentbeheer.
* Het segment wordt gecontroleerd slechts voor een specifieke rapportreeks.
* Een gedeeld segment kan door een andere gebruiker zijn verwijderd.
* Segmenten konden niet worden geladen vanwege een cacheprobleem in een datacenter of browser.
* Het segment is niet opgeslagen.
* IP adres kan bij het eind van de gebruiker worden geblokkeerd.

## Waarom lijken de gegevens die na het toepassen van een segment worden getoond onjuist? {#page-data}

Mogelijke redenen:

* De regels of operatoren zijn onjuist voor het vereiste resultaat.
* Onjuist gebruik van containers in het segment.
* De variabelen van het verkeer die aan segment worden gebruikt worden niet behoorlijk geplaatst of zijn verlopen.
