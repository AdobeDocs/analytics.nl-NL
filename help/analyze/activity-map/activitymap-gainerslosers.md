---
description: Met bedekkingen kunt u op meerdere manieren gegevensvisualisatie configureren, zodat u de populariteit van koppelingen op een pagina gemakkelijk kunt zien en begrijpen.
title: Aanpasbare overlays
uuid: c1e56480-c1df-4a81-8a2a-42ea1362175c
feature: Activity Map
role: User, Admin
exl-id: 1e83d470-36e4-47bb-a262-ac12472b21c3
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---

# Aanpasbare overlays

Met bedekkingen kunt u op meerdere manieren gegevensvisualisatie configureren, zodat u de populariteit van koppelingen op een pagina gemakkelijk kunt zien en begrijpen.

Met bedekkingen kunt u rechtstreeks op de pagina op gegevens klikken. Dit is wat een visueel analysehulpmiddel zoals Activity Map van en vooral tabelvormige en grafische hulpmiddelen zoals Rapporten &amp; Analytics scheidt.

Activity Map biedt drie typen overlays:

* Verloopbedekking (Heatmap)
* Bubble Overlay
* Bedekking voor tussenruimten en Losers

U kunt [bedekkende rendering ook configureren voor dynamische inhoud](/help/analyze/activity-map/activitymap-link-tracking/activitymap-stl-track-custom-elements.md).

Als u overlays wilt wijzigen, opent u het [deelvenster Overlayinstellingen](/help/analyze/activity-map/activitymap-overlay-settings.md) en bewerkt u de beschikbare opties.

Als u de bedekking boven een bedekking plaatst, worden de [details](/help/analyze/activity-map/activitymap-overlay-details.md) weergegeven.

## Verloopbedekking (Heatmap) {#section_06AF13DE05A1454D960176CD0DA921A6}

Met de verloopbedekking is de kleurintensiteit gebaseerd op de populariteit van de koppeling. Deze intensiteit kan worden genormaliseerd voor de bovenste 30 waarderingen, of een functie van de absolute metrische waarde.

Deze meetgegevens worden boven op de pagina-koppelingen geplaatst als een soort &#39;warmtekaart&#39; voor het beantwoorden van kritieke vragen, waaronder de volgende:

* Wat is de waarde van een afzonderlijke pagina?
* Wat is de waarde van een afzonderlijk element op een pagina?
* Wat is het meest waardevolle &#39;digitale onroerend goed&#39; op een pagina?

![](assets/gradient.png)

## Bubbelbedekking {#section_A657AB3F64CB47F881BBFFD72B37D9D4}

De bedekking van de Bubbel toont de bedekkingsinhoud (metrisch, percentage, of rang) in een kleine callout bel.

Bubbelbedekkingen worden weergegeven wanneer u deze bedekking selecteert in Overlaytype op de werkbalk. . Bubble-overlays worden weergegeven voor alle koppelingen die overeenkomen met de selectie in [Activity Map-instellingen](/help/analyze/activity-map/activitymap-overlay-settings.md) (bovenste 30, bovenste 50, alle..). Verloopbedekkingen worden weergegeven als deze optie niet is geselecteerd.

![](assets/bubble_overlay.png)

>[!NOTE]
>
>Bubble-overlays voor submenu&#39;s worden alleen weergegeven wanneer u het submenu weergeeft:
>
>![](assets/bubbles_submenu.png)>

## Bedekkingen voor tussenpersonen en verliezers {#section_EE80278E20C14824869BF5A27A4634C8}

**[!UICONTROL Gainers and losers overlays]** zijn alleen beschikbaar in de live modus. Zij melden veranderingen in real time in verbindingsactiviteit door de metriek van de huidige periode met metriek van de laatste periode te vergelijken. Ze geven je een visueel aantrekkelijke manier om trending in real-time te bekijken.

Deze overlayranks in real time worden gebaseerd op veranderingen in de metrische waarde tussen de vorige en huidige periodes geklikt die.

![](assets/gainers_losers.png)
