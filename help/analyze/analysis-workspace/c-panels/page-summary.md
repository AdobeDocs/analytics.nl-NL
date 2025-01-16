---
description: In het deelvenster Paginaoverzicht staan overzichtsgegevens voor een door u gekozen pagina.
title: Het deelvenster Paginaoverzicht
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: 33fdd685de21736964d0cbfbc479794a9154e8a3
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Het deelvenster Paginaoverzicht {#page-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_button"
>title="Overzicht van pagina"
>abstract="Bekijk snel enkele maatstaven op hoog niveau en de verplaatsing van en naar een specifieke pagina."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_panel"
>title="Het deelvenster Paginaoverzicht"
>abstract="Bekijk snel enkele maatstaven op hoog niveau en de verplaatsing van en naar een specifieke pagina.<br/><br/>**Parameters **<br/>**voegen een punt van de paginadimensie** toe: Open de componentenspoorstaaf, bepaal de plaats van de dimensie van de Pagina en breid het door op de wortel te klikken om de afmetingspunten te zien. Vervolgens sleept u de specifieke pagina waarover u meer wilt weten naar de builder. Zodra u hebt gesleept en het afmetingspunt gelaten vallen, zal het rapport automatisch met zeer belangrijke informatie over de pagina bevolken."

<!-- markdownlint-enable MD034 -->


In dit deelvenster kunt u eenvoudig belangrijke statistieken over specifieke pagina&#39;s bekijken.

## Het deelvenster openen

U kunt het deelvenster openen vanuit [!UICONTROL Reports] of vanuit [!UICONTROL Workspace] .

| Toegangspunt | Beschrijving |
| --- | --- |
| [!UICONTROL Reports] | <ul><li>Het deelvenster is al neergezet in een project.</li><li>De linkerspoorstaaf is samengevouwen.</li><li>Alleen de pagina-afmeting wordt ondersteund.</li><li>Een gebrek die reeds plaatsen is toegepast, in dit geval de hoogste bezochte pagina voor de [!UICONTROL Page] dimensie. U kunt deze instelling wijzigen.</li></ul> |
| Workspace | Maak een nieuw project en selecteer het deelvensterpictogram in de linkerspoorstaaf. Sleep het deelvenster [!UICONTROL Page summary] boven de tabel voor vrije vorm. Het veld Pagina [!UICONTROL Dimension Item] blijft leeg. Selecteer een dimensie-item in de vervolgkeuzelijst. |

## Deelvensterinvoer {#Input}

U kunt het deelvenster [!UICONTROL Page summary] configureren met de volgende invoerinstellingen:

| Instelling | Beschrijving |
| --- | --- |
| Segment (of andere component) dropzone | U kunt segmenten of andere componenten slepen en neerzetten om de resultaten van het deelvenster verder te filteren. |
| Pagina-dimensie-item | Selecteer in de vervolgkeuzelijst het item Paginadimensie waarvan u de belangrijkste statistieken wilt bekijken. |

{style="table-layout:auto"}

Klik op **[!UICONTROL Build]** om het deelvenster te maken.

## Deelvensteruitvoer {#output}

Het deelvenster [!UICONTROL Page summary] retourneert een uitgebreide set metrische gegevens en visualisaties om u te helpen statistieken over specifieke pagina&#39;s beter te begrijpen.

| Metrisch/visualisatie | Beschrijving |
| --- | --- |
| [!UICONTROL Page views] - Huidige maand, tot nu toe | Aantal paginaweergaven voor deze pagina voor de huidige maand. |
| [!UICONTROL Page views] - 4 weken eerder | Aantal paginaweergaven voor deze pagina in de afgelopen maand. |
| [!UICONTROL Page views] - 52 weken eerder | Aantal paginaweergaven voor deze pagina in het afgelopen jaar. |
| [!UICONTROL Trend] | Een overzicht met trendpaginaweergaven voor deze maand, 4 weken eerder en 52 weken daarvoor. |
| [!UICONTROL Percentage of all page views] | Een samenvattingsnummer voor het percentage van alle paginaweergaven die naar deze pagina zijn gegaan. |
| [!UICONTROL Time spent on page] | Een horizontaal staafdiagram waarin de tijd wordt weergegeven die aan deze pagina is besteed. |
| [!UICONTROL Single page visits] | Een samenvattingsnummer met het aantal paginaweergaven waarop dit de enige bezochte pagina was. |
| [!UICONTROL Reloads] | De metrische waarde [!UICONTROL Reloads] geeft het aantal keren weer dat een dimensie-item aanwezig was tijdens het opnieuw laden. Een bezoeker die zijn browser vernieuwt, is de meest gebruikelijke manier om een nieuwe laadbewerking te starten. |
| [!UICONTROL Entries] | De [!UICONTROL Entries] -meting geeft het aantal keren weer dat een bepaald dimensie-item als eerste waarde in een bezoek wordt vastgelegd. |
| [!UICONTROL Exits] | De [!UICONTROL Exits] -meting geeft het aantal keren weer dat een bepaald dimensie-item als laatste waarde in een bezoek wordt vastgelegd. |
| [!UICONTROL Flow] | Een stroomdiagram met de geselecteerde pagina als brandpunt. U kunt verder in de gegevens enkel als in om het even welk [ diagram van de Stroom ](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) boren. |

{style="table-layout:auto"}

![ het summiere paneel van de Pagina ](assets/page-sum1.png)

![ Metriek en stroom ](assets/page-sum2.png)
