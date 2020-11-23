---
description: Functies voor toegankelijkheidsondersteuning in Analysis Workspace
title: Toegankelijkheid in Analysis Workspace
translation-type: tm+mt
source-git-commit: 97309a5be19912432ca75c7029999085c45ba353
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 2%

---


# Toegankelijkheid in Analysis Workspace

Meer informatie over toegankelijkheidsondersteuning in [!UICONTROL Analysis Workspace]de belangrijkste tool voor Adobe Analytics.

Toegankelijkheid heeft betrekking op het bruikbaar maken van producten voor mensen met een visuele, auditieve, cognitieve, motorische en andere handicap. Voorbeelden van toegankelijkheidsfuncties voor softwareproducten zijn ondersteuning voor schermlezers, tekstequivalenten voor afbeeldingen, sneltoetsen, wijziging van weergavekleuren in hoog contrast, enzovoort.

[!UICONTROL Analysis Workspace] bevat enkele gereedschappen die het programma toegankelijk maken voor gebruik, zoals:

## Navigeren [!UICONTROL Workspace] met het toetsenbord

Navigatie in [!UICONTROL Analysis Workspace] werkt boven > omlaag en links > rechts. De volgende navigatie-elementen vergemakkelijken de toegankelijkheid:

* Met de `Tab` toets kunt u zoeken naar sneltoetsen voor landmarkeringen, waarbij u kunt schakelen tussen grotere secties in Workspace. In het linkerspoor, laat u `Tab` ook toe om zich van één draggable optie aan volgende te bewegen.
* De `left/right arrows` beweging tussen afzonderlijke elementen nadat deze `Tab` is gemarkeerd.
* De gebruiker `F6` navigeert naar het eerste deelvenster in het project en beweegt tussen de visualisaties in dat deelvenster. Vervolgens wordt het naar het volgende deelvenster in het project verplaatst en herhaald.
* We passen focusindicatoren toe zodat gebruikers met een waargenomen toetsenbord een duidelijke indicatie hebben van welk interface-element momenteel focus heeft. De indicator is een blauwe rand rondom het geselecteerde element.

   ![Focusindicator](assets/focus-indicator.png)

### Toetsenbordnavigatie voor de menubalk

1. Tab totdat u de menubalk hebt bereikt.
1. Gebruik de pijltoetsen naar links en rechts om naar het gewenste menu te navigeren.
1. Druk op `Enter` om het menu te selecteren en de opties ervan weer te geven.
1. Gebruik de pijltoetsen omhoog en omlaag om naar de gewenste menuoptie te navigeren.
1. Druk op `Enter` om de optie te selecteren.

### Toetsenbordnavigatie voor interactie Slepen en neerzetten

[!UICONTROL Analysis Workspace] is een gebruikersinterface voor slepen en neerzetten. Gebruikers kunnen echter wel componenten toevoegen met het toetsenbord:

1. Tab naar een component in de linkerspoorstaaf.
1. Druk `Enter` om te selecteren.
1. Met de pijltoetsen navigeert u naar het gebied waar u de component wilt neerzetten.
1. Druk op `Enter` om de component te plaatsen.

### Sneltoetsen (sneltoetsen)

[!UICONTROL Analysis Workspace] biedt een uitgebreide set [sneltoetsen](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.html) voor een naadloze workflow. Hieronder worden enkele algemene sneltoetsen voor navigatie, het maken van analyses en democratisering van inzichten weergegeven.

#### Navigatie

| Sneltoets | Handeling |
|---|---|
| Alt + Shift + 1 / 2 / 3 | Naar verschillende rails springen: [!UICONTROL Panels], [!UICONTROL Visualizations]of [!UICONTROL Components] |
| Alt + Pijl-links/Pijl-rechts | Navigeren tussen deelvensters |
| Alt + M | Alle deelvensters samenvouwen/uitvouwen |
| Alt+ Ctrl + M | Actief deelvenster samenvouwen/uitvouwen |
| Ctrl + / | Zoeken in linkerrail |

#### Analyse maken

| Sneltoets | Handeling |
|---|---|
| Alt + 1 | Nieuwe vrije-vormlijst |
| Ctrl + Shift + C | Nieuwe berekende metrisch |
| Ctrl + Shift + D | Nieuw datumbereik |
| Ctrl + Shift + E | Nieuw segment |
| Ctrl + Z | Ongedaan maken |
| Houd Shift ingedrukt (in de dropzone van het deelvenstersegment) | Een [vervolgkeuzefilter maken](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) |

#### democratisering

| Sneltoets | Handeling |
|---|---|
| Ctrl + S | Opslaan |
| Ctrl + Shift + G | Curate |
| Ctrl + G | Delen |
| Alt + Shift + S | Schema |
| Alt + L | Koppeling naar project ophalen |
| Ctrl + Shift + B | PDF downloaden |

## Ondersteuning voor schermlezers en schermvergrotingen

Een schermlezer leest tekst die op het computerscherm wordt weergegeven. De pagina leest ook niet-tekstuele informatie, zoals knoplabels of beschrijvingen van afbeeldingen in de toepassing, die in toegankelijkheidstags of -kenmerken wordt aangeboden.

## Kleurenpaletten en contrast

[!UICONTROL Analysis Workspace] streeft naar WCAG 2.1 AA-conformiteit, inclusief vereisten voor kleurcontrast.

Bovendien kunnen gebruikers hun eigen voorkeurskleurenpalet voor een project instellen onder **[!UICONTROL Project]** > **[!UICONTROL Project settings]** > [Kleurenpalet](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html)Project.

## Vereiste veldvalidatie in componentbuilders

Wanneer u een component maakt, worden de vereiste velden gevalideerd tijdens het opslaan. Als een vereist veld de validatie niet doorgeeft, wordt het veld rood weergegeven met een foutpictogram. Er verschijnt een schriftelijke beschrijving van het probleem dat moet worden opgelost.

Wanneer een component volledig is gevalideerd, wordt de builder `Save` gesloten wanneer u op de component drukt.

![Foutvalidatie](assets/error-validation.png)

## Ondersteuning voor toegankelijkheidsfuncties van besturingssystemen

Analysis Workspace biedt ondersteuning voor ingebouwde toegankelijkheidsfuncties van MS Windows en macOS, zoals de modus voor hoog contrast, sticky keys en slow keys/filters. Het verstrekt ook informatie over het gebruikersinterface aan het werkende systeem om interactie met ondersteunende technologieën, met inbegrip van het schermlezers zoals VoiceOver voor macOS en NVDA op Vensters toe te laten.
