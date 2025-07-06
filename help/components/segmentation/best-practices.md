---
title: Aanbevolen procedures
description: Leer enkele best practices voor segmentatie.
feature: Segmentation
exl-id: 4115a804-5063-430a-b9d3-2b64b26ca4d8
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Beste werkwijzen voor segmentering

De complexe segmenten zijn vaak noodzakelijk om gewenste gegevens te verkrijgen. Als complexe segmenten inefficiënt zijn en in een grote rapportsuite worden gebruikt, duurt het aanzienlijk langer om rapporten uit te voeren. Houd rekening met de volgende bronnen wanneer u een segment maakt of bewerkt om de complexiteit te minimaliseren.

## Alleen de operator `Contains` gebruiken als laatste redmiddel

De [**[!UICONTROL Contains]**exploitant ](/help/components/segmentation/seg-reference/seg-operators.md) is één van de meest verwerkings-intensieve eigenschappen in segmentatie, aangezien de exploitant de volledige inhoud van elke waarde moet analyseren. U kunt ook andere operatoren gebruiken, zoals **[!UICONTROL Starts with]**of **[!UICONTROL Ends with]**, als de gewenste waarden zich aan het begin of einde van een tekenreeks bevinden.

Als een **[!UICONTROL Contains]** exploitant in een segment een groot aantal resultaten terugkeert, typisch tijden uit het rapport. Als u bijvoorbeeld een segment hebt gemaakt waarin **[!UICONTROL Referrer]** **[!UICONTROL equals]** `"."` staat, zoekt het segment door de inhoud van elke waarde. Gebruik in plaats hiervan de operator **[!UICONTROL Exists]** .

## Classificaties gebruiken voor items met groepsdimensies

Als u vele segmentvoorwaarden hebt, kunnen zij segmentprestaties snel degraderen. **[!UICONTROL Page]** **[!UICONTROL equals]** `X` **[!UICONTROL OR]** **[!UICONTROL Page]** **[!UICONTROL equals]** `Y` **[!UICONTROL OR]** **[!UICONTROL Page]** **[!UICONTROL equals]** `Z` wordt bijvoorbeeld herhaald met honderden verschillende waarden. In plaats van deze honderden voorwaarden te schrijven, classificeer alle gewenste waarden in een segment, dan gebruik de geclassificeerde waarde in een segment.

1. Maak een classificatie voor de variabele waarmee u werkt.
2. Download het classificatiesjabloon en open het in het gewenste spreadsheet of de gewenste teksteditor.
3. Geef elk dimensie-item dat u in uw segment wilt opnemen dezelfde waarde.
4. De indelingimporter gebruiken om de spreadsheet weer in Adobe Analytics te importeren
5. Wanneer de classificatie klaar is met verwerken, maakt u een segment met de geclassificeerde waarde.

Deze methode verhoogt drastisch prestaties en verstrekt een gemakkelijke manier om segmentvoorwaarden te wijzigen. In plaats van het segment met verschillende waarden te bewerken, kunt u dimensie-items toevoegen aan of verwijderen uit de classificatie.
