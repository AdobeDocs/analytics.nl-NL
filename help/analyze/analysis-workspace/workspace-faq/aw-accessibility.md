---
description: Meer informatie over de toegankelijkheidsfuncties in Analysis Workspace.
title: Toegankelijkheid in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: 2bacbee8-097c-4fc5-8be4-7e4f284db08c
source-git-commit: 70d87e62441f8d5c3c6041721353a07432fef912
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---


# Toegankelijkheid in Analysis Workspace

Meer informatie over toegankelijkheidsondersteuning vindt u in [!UICONTROL Analysis Workspace] , het belangrijkste hulpprogramma voor analyse voor Customer Journey Analytics.

Toegankelijkheid heeft betrekking op het bruikbaar maken van producten voor mensen met een visuele, auditieve, cognitieve, motorische en andere handicap. Voorbeelden van toegankelijkheidsfuncties voor softwareproducten zijn:

* ondersteuning voor schermlezers,
* tekstequivalenten voor afbeeldingen,
* sneltoetsen,
* verandering van de weergavekleuren in hoog contrast,
* en meer.

[!UICONTROL Analysis Workspace] bevat enkele gereedschappen die het programma toegankelijk maken voor gebruik, zoals:

## Toetsenbordnavigatie

Navigatie in [!UICONTROL Analysis Workspace] werkt van boven naar beneden en van links naar rechts. De volgende navigatie-elementen vergemakkelijken de toegankelijkheid:

* Met de toets **[!UICONTROL Tab]** kunt u sneltoetsen gebruiken om markeringen te markeren die zich verplaatsen tussen grotere secties in Workspace. In het linkerdeelvenster kunt u met **[!UICONTROL Tab]** ook van de ene versleepbare optie naar de andere gaan.
* De &rbrace;︎ ◀ en ▶ &rbrace;︎ tussen afzonderlijke elementen gaan nadat met de toets **[!UICONTROL Tab]** een element is gemarkeerd.
* Met de **[!UICONTROL F6]** -toets navigeert u naar het eerste deelvenster in het project en gaat u tussen de visualisaties in dat deelvenster. Vervolgens wordt het naar het volgende deelvenster in het project verplaatst en herhaald.
* Focusindicatoren worden toegepast zodat gebruikers met een waargenomen toetsenbord een duidelijke indicatie hebben van welk interface-element momenteel focus heeft. De indicator is een blauwe rand voor het deelvenster dat focus heeft. En grijze achtergrond voor de onlangs geselecteerde functionaliteit en de selectie binnen de functionaliteit. In het voorbeeld zijn [!UICONTROL Components] en de pagina-dimensie onlangs geselecteerd.

  ![ vrije lijst die een nadrukindicator van een blauwe grens rond de lijst Freeform toont.](assets/focus-indicator.png)

### Toetsenbordnavigatie voor de menubalk

1. Tab totdat u de menubalk hebt bereikt.
1. Gebruik de pijltoetsen om te navigeren tussen menu&#39;s en menu-items.
1. Druk op **[!UICONTROL Enter]** om een menu te openen of een menu-item te selecteren.
1. Gebruik **[!UICONTROL Esc]** om een menu te sluiten.

### Toetsenbordnavigatie voor interactie Slepen en neerzetten

[!UICONTROL Analysis Workspace] is een gebruikersinterface voor slepen en neerzetten. Gebruikers kunnen echter wel componenten toevoegen met het toetsenbord:

1. Tab naar een component in het linkerdeelvenster.
1. Druk op **[!UICONTROL Enter]** om te selecteren.
1. Met de pijltoetsen navigeert u naar het gebied waar u de component wilt neerzetten.
1. Druk op **[!UICONTROL Enter]** om de component te plaatsen.

### Sneltoetsen (sneltoetsen)

[!UICONTROL Analysis Workspace] biedt een rijke reeks [ toetsenbordkortere weg ](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md) voor een naadloze werkschema aan.

## Ondersteuning voor schermlezers en schermvergrotingen

Een schermlezer leest tekst die op het computerscherm wordt weergegeven. Deze leest ook niet-tekstuele informatie, zoals knoplabels of beschrijvingen van afbeeldingen in de toepassing.

## Kleurenpaletten en contrast

[!UICONTROL Analysis Workspace] streeft naar WCAG 2.1 AA-conformiteit, inclusief vereisten voor kleurcontrast.

Bovendien kunnen de gebruikers hun eigen aangewezen kleurenpalet voor een project onder **[!UICONTROL Project]** plaatsen > **[!UICONTROL Project settings]** > [ het kleurenpalet van het Project ](/help/analyze/analysis-workspace/build-workspace-project/color-palettes.md).

## Vereiste validatie

Wanneer u een component, een visualisatie of een deelvenster maakt, worden de vereiste velden gevalideerd tijdens het opslaan. Als een vereist veld de validatie niet doorgeeft, wordt het veld rood weergegeven met een foutpictogram. In een schriftelijke beschrijving wordt uitgelegd wat er moet worden opgelost.

![ de Bouwer van het Segment en de indicator van de foutenbevestiging.](assets/error-validation.png)

## Ondersteuning voor toegankelijkheidsfuncties van besturingssystemen

Analysis Workspace biedt ondersteuning voor ingebouwde toegankelijkheidsfuncties voor Windows en macOS, zoals de modus voor hoog contrast, sticky keys en trage toetsen/filtertoetsen. Het verstrekt ook informatie over het gebruikersinterface aan het werkende systeem om interactie met ondersteunende technologieën, met inbegrip van het schermlezers zoals VoiceOver voor macOS en NVDA op Vensters toe te laten.


<!--

# Accessibility in Analysis Workspace

Learn about accessibility support in [!UICONTROL Analysis Workspace], the premier analysis tool for Adobe Analytics. 

Accessibility refers to making products usable for people with visual, auditory, cognitive, motor, and other disabilities. Examples of accessibility features for software products include screen reader support, text equivalents for graphics, keyboard shortcuts, change of display colors to high contrast, and so on. 

[!UICONTROL Analysis Workspace] provides some tools that make it accessible to use, including:

## Navigate [!UICONTROL Workspace] using the keyboard

Navigation in [!UICONTROL Analysis Workspace] works top > down, and left > right. The following navigational elements facilitate accessibility:

* The `Tab` key enables landmark shortcuts, moving between larger sections within Workspace. In the left rail, `Tab` also enables you to move from one draggable option to the next.
* The `left/right arrows` move between individual elements after `Tab` has highlighted it. 
* The `F6` navigates to the first panel in the project and  moves between the visualizations within that panel. Then, it moves to the next panel in the project and repeats. 
* We apply focus indicators so that sighted keyboard users have a clear indication of which UI element currently has focus. The indicator is a blue border around the selected element.

    ![Focus Indicator](assets/focus-indicator.png)

### Keyboard navigation for the menu bar 

1. Tab until you have reached the menu bar.
1. Use left/right arrow keys to navigate to the menu you want.
1. Press `Enter` to select the menu and show its options.
1. Use up/down arrow keys to navigate to the menu option you want.
1. Press `Enter` to select the option.

### Keyboard navigation for drag & drop interactions 

[!UICONTROL Analysis Workspace] is a drag & drop user interface. However, users can add components using the keyboard instead:

1. Tab to a component in the left rail.
1. Press `Enter` to select.
1. Use arrow keys to navigate to the area where you want to drop the component.
1. Press `Enter` to place the component.

### Keyboard shortcuts (hotkeys) 

[!UICONTROL Analysis Workspace] offers a rich set of [keyboard shortcuts](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.html) for a more seamless workflow. Some common shortcuts for navigation, analysis creation, and insight democratization are listed below. 

#### Navigation

| Shortcut | Action |
| --- | --- |
| `[Alt + Shift + 1 / 2 / 3]` | Jump to different rails: [!UICONTROL Panels], [!UICONTROL Visualizations], or [!UICONTROL Components] | 
| `[Alt + Left / Right]` | Navigate between panels |
| `[Alt + M]` | Collapse/expand all panels |
| `[Alt + Ctrl + M]` | Collapse/expand active panel |
| `[Ctrl + /]` | Search left rail |

#### Analysis creation

| Shortcut | Action |
| --- | --- |
| `[Alt + 1]` | New freeform table |
| `[Ctrl + Shift + C]` | New calculated metric |
| `[Ctrl + Shift + D]` | New date range |
| `[Ctrl + Shift + E]` | New segment |
| `[Ctrl + Z]` | Undo |
| `[Component drag + Shift]` | Create a drop-down filter |

#### Democratization

| Shortcut | Action |
| --- | --- |
| `[Ctrl + S]` | Save |
| `[Ctrl + Shift + G]` | Curate |
| `[Ctrl + G]` | Share |
| `[Alt + Shift + S]` | Schedule |
| `[Alt + L]` | Get link to project |
| `[Ctrl + Shift + B]` | Download PDF |

## Support for screen readers and screen magnifiers

A screen reader reads text that appears on the computer screen. It also reads non-textual information, such as button labels or image descriptions in the application, provided in accessibility tags or attributes.  

## Color palettes & contrast  

[!UICONTROL Analysis Workspace] strives for WCAG 2.1 AA conformance, including requirements for color contrast. 

In addition, users can set their own preferred color palette for a project under **[!UICONTROL Project]** > **[!UICONTROL Project settings]** > [Project color palette](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html). 

## Required field validation in component builders 

When building a component, required fields are validated when you save. If a required field does not pass validation, it will be outlined in red with an error icon. A written description appears of the issue that needs to be fixed.  

Once a component is fully validated, pressing `Save` closes the builder. 

![Error validation](assets/error-validation.png)

## Support for operating system accessibility features  

Analysis Workspace supports built-in MS Windows and macOS accessibility features like high-contrast mode, sticky keys, and slow keys/filter keys. It also provides information about the user interface to the operating system to enable interaction with assistive technologies, including screen readers such as VoiceOver for macOS and NVDA on Windows.

-->