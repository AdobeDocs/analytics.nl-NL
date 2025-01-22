---
description: Wijzig de instellingen en eigenschappen voor alle typen overlayvisualisaties in Activity Map.
title: Activity Map-instellingen configureren
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: User, Admin
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
source-git-commit: 13ad9d40ad74a8dffe05d899db54f4d77cbcc34c
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Activity Map-instellingen configureren

Met het instellingenvenster Activity Map kunt u de instellingen en eigenschappen voor alle typen overlayvisualisaties wijzigen.

**[!UICONTROL Activity Map overlay]** > **toon montages (tandwielpictogram)** > **[!UICONTROL Settings]**

## Algemene instellingen

Wijzig de algemene instellingen voor de extensie en de bedekkingen.

* **[!UICONTROL Companies]**: geeft de huidige organisatie Analytics weer, waaraan u bent aangemeld.
* **[!UICONTROL Page name]** - Geeft de naam van de huidige pagina weer.
* **[!UICONTROL Language]**: hiermee wijzigt u de taal voor extensielabels voor Activity Mappen. Met deze instelling wijzigt u de inhoud van uw website en de namen van koppelingen in rapporten niet. Tot de ondersteunde talen behoren Engels, Frans, Chinees (vereenvoudigd), Chinees (traditioneel), Duits, Japans, Koreaans, Spaans en Portugees.
* **[!UICONTROL Label overlays with]** - Hiermee wordt bepaald wat de bubbel- of verlooptekst is. De standaardinstelling is [!UICONTROL Rank] . U kunt onder andere de volgende opties kiezen:
   * **[!UICONTROL No label]**: Geen tekst binnen de labels, waardoor deze gekleurde vakken krijgen
   * **[!UICONTROL Value]**: Toont het aantal verbinding klikt ([ Voorkomen ](/help/components/metrics/occurrences.md))
   * **[!UICONTROL Percent]**: geeft het aandeel van klikken op koppelingen weer in verhouding tot het totale aantal klikken op koppelingen op de pagina
   * **[!UICONTROL Rank]**: De numerieke positie van de koppeling op basis van het aantal koppelingen waarop wordt geklikt.
* **[!UICONTROL Label font size]** - Hiermee bepaalt u de grootte van de tekst binnen de bel of het verloop.
* **[!UICONTROL Gradient color]**: hiermee kunt u de verloopkleur wijzigen wanneer het visualisatietype [!UICONTROL Gradient] is.
* **[!UICONTROL Bubble color]**: hiermee kunt u de belkleur wijzigen wanneer het visualisatietype [!UICONTROL Bubble] is.
* **[!UICONTROL Color gradient based on]** - Hiermee wordt bepaald op welke metrische waarde de kleurintensiteit van een koppeling is gebaseerd wanneer het visualisatietype [!UICONTROL Gradient] is.
   * **[!UICONTROL Top 30 rankings]**: de kleurintensiteit wordt genormaliseerd voor de bovenste 30 koppelingen.
   * **[!UICONTROL Absolute metric value]**: de kleurintensiteit is een functie van de absolute metrische waarde.
* **[!UICONTROL Gradient transparency]** - Hiermee bepaalt u de transparantie van verloopbedekkingen wanneer het visualisatietype [!UICONTROL Gradient] is. Met deze schuifregelaar kunt u de kleurbedekking volledig transparant, volledig ondoorzichtig of ergens tussenin maken.

## Standaardinstellingen

Pas de instellingen voor de standaardweergave aan.

* **[!UICONTROL Dynamic data filtering]**: hiermee kunt u wijzigen welke koppelingen worden weergegeven.
   * **[!UICONTROL Top]**: geeft de populairste koppelingen weer. Gebruik de numerieke vervolgkeuzelijst aan de rechterkant om het aantal bovenste koppelingen te bepalen dat moet worden weergegeven. U kunt kiezen uit 1, 10, 50 en 100.
   * **[!UICONTROL Bottom]**: geeft de minst populaire koppelingen weer op basis van de vervolgkeuzelijst met nummers. Gebruik de numerieke vervolgkeuzelijst aan de rechterkant om het aantal onderliggende koppelingen te bepalen dat moet worden weergegeven. U kunt kiezen uit 1, 10, 50 en 100.
   * **[!UICONTROL All links]**: pas geen dynamische gegevensfiltering toe. De numerieke vervolgkeuzelijst is niet van toepassing als deze optie is geselecteerd.
* **[!UICONTROL Hide overlays for links that received no hits]**: koppelingen op de pagina met een klik op de koppeling nul tonen geen bedekking. Deze koppelingen zijn uitgesloten van dynamische gegevensfiltering.

## Live-instellingen

* **[!UICONTROL Display top]**: geef het bovenste aantal guminatoren of verliezers weer op basis van de numerieke vervolgkeuzelijst aan de linkerkant.
* **[!UICONTROL Exclude bottom (%)]**: filter het onderste percentage van koppelingswijzigingen uit om alleen de koppelingen met voldoende gegevens weer te geven om relevante winsten of verliezen weer te geven. Het percentage wordt berekend op basis van het aantal koppelingen op die pagina. Als u bijvoorbeeld de onderste 10% van een lijst met 200 koppelingen verwijdert, worden de onderste 20 koppelingen verwijderd.
* **[!UICONTROL Auto update data]** - Hiermee wordt bepaald of de analysegegevens die in de overlay worden weergegeven, automatisch worden bijgewerkt wanneer een nieuwe periode wordt berekend.
* **[!UICONTROL Auto update period]**: Als deze optie is ingeschakeld, wordt de pagina vernieuwd met elke nieuwe gegevensophaling, zodat de koppelingen op de pagina nauwer worden gesynchroniseerd met verzamelde gegevens.
