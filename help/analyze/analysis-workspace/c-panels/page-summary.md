---
description: Leer hoe u het deelvenster Paginaoverzicht kunt gebruiken om overzichtsgegevens voor een geselecteerde pagina weer te geven.
title: Deelvenster Paginaoverzicht
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: 19c2c1abd7f1799598597c0e696d0b001c1ef0ea
workflow-type: tm+mt
source-wordcount: '598'
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
>abstract="Bekijk snel enkele maatstaven op hoog niveau en de verplaatsing van en naar een specifieke pagina.<br/><br/>**Parameters &#x200B;**<br/>**voegen een punt van de paginadimensie** toe: Open de componentenspoorstaaf, bepaal de plaats van de dimensie van de Pagina en breid het door op de wortel te klikken om de afmetingspunten te zien. Vervolgens sleept u de specifieke pagina waarover u meer wilt weten naar de builder. Zodra u hebt gesleept en het afmetingspunt gelaten vallen, bevolkt het rapport automatisch met zeer belangrijke informatie over de pagina."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert het summiere paneel van de Pagina in_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_er is geen gelijkwaardig paneel in_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**._

>[!ENDSHADEBOX]

In een deelvenster **[!UICONTROL Page summary]** kunt u belangrijke statistieken over specifieke pagina&#39;s bekijken.

## Gebruiken

Een deelvenster **[!UICONTROL Page summary]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Page summary]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [&#x200B; een paneel &#x200B;](panels.md#create-a-panel) creëren.

1. Specificeer de [&#x200B; input &#x200B;](#panel-input) voor het paneel.

1. Neem de [&#x200B; output &#x200B;](#panel-output) voor het paneel waar.



U kunt het deelvenster openen vanuit [!UICONTROL Reports] of vanuit [!UICONTROL Workspace] .

| Toegangspunt | Beschrijving |
| --- | --- |
| [!UICONTROL Reports] | <ul><li>Het deelvenster is al neergezet in een project.</li><li>De linkerspoorstaaf is samengevouwen.</li><li>Alleen de pagina-afmeting wordt ondersteund.</li><li>Een gebrek die reeds plaatsen is toegepast, in dit geval, de hoogste bezochte pagina voor de [!UICONTROL Page] dimensie. U kunt deze instelling wijzigen.</li></ul> |
| Workspace | Maak een nieuw project en selecteer het deelvensterpictogram in de linkerspoorstaaf. Sleep het deelvenster [!UICONTROL Page summary] boven de tabel voor vrije vorm. Het veld Pagina [!UICONTROL Dimension Item] blijft leeg. Selecteer een dimensie-item in de vervolgkeuzelijst. |

### Deelvensterinvoer {#panel-input}

U kunt het deelvenster [!UICONTROL Page summary] configureren met de volgende invoerinstellingen:

![&#x200B; overzicht van de de inputinvoer van de Pagina &#x200B;](assets/page-summary-input.png)

| Invoer | Beschrijving |
| --- | --- |
| **[!UICONTROL Page]** | Selecteer een pagina-dimensie waarvoor u de belangrijkste statistieken wilt bekijken. **[!UICONTROL home]** bijvoorbeeld om statistieken voor de startpagina te bekijken. Gebruik het vervolgkeuzemenu om een pagina te selecteren of te beginnen te typen (bijvoorbeeld `home` ) om snel naar pagina&#39;s te zoeken. |

{style="table-layout:auto"}


Selecteer **[!UICONTROL Build]** om het deelvenster te maken.

### Deelvensteruitvoer {#panel-output}

Het deelvenster [!UICONTROL Page summary] retourneert een uitgebreide set metrische gegevens en visualisaties om u te helpen statistieken over specifieke pagina&#39;s beter te begrijpen.

![&#x200B; het summiere paneel van de Pagina &#x200B;](assets/page-summary-output.png)

| Visualisatie | Beschrijving |
| --- | --- |
| **[!UICONTROL Page views]- Huidige maand (tot nu toe)** | A [&#x200B; Summiere aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) visualisatie die het aantal paginameningen voor deze pagina voor de huidige maand toont. |
| **[!UICONTROL Page views]- 4 weken eerder** | A [&#x200B; Summiere aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) visualisatie die het aantal paginameningen voor deze pagina over de laatste maand toont. |
| **[!UICONTROL Page views]- 52 weken eerder** | A [&#x200B; Summiere aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) visualisatie die het aantal paginameningen voor deze pagina over het laatste jaar toont. |
| **[!UICONTROL Trend]** | Een trended [&#x200B; visualisatie van de Lijn &#x200B;](/help/analyze/analysis-workspace/visualizations/line.md) voor paginameningen voor deze maand, 4 weken voorafgaand, en 52 weken voorafgaand. |
| **[!UICONTROL Percentage of all page views]** | Een samenvattingsnummer voor het percentage van alle paginaweergaven die naar deze pagina zijn gegaan. |
| **[!UICONTROL Time spent on page]** | A [&#x200B; Horizontale bar &#x200B;](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md) visualisatie die de tijd toont die aan deze pagina wordt doorgebracht. |
| **[!UICONTROL Single page visits]** | A [&#x200B; Summiere aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) dat het aantal paginameningen toont waar deze pagina de enige bezochte pagina was. |
| **[!UICONTROL Reloads]** | A [&#x200B; Samenvattend aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) dat toont het aantal tijden een afmetingspunt tijdens een herlading aanwezig was. Een bezoeker die zijn browser vernieuwt, is de meest gebruikelijke manier om een nieuwe laadbewerking te starten. |
| **[!UICONTROL Entries]** | A [&#x200B; Samenvattend aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) dat toont het aantal tijden een bepaald afmetingspunt wordt gevangen als eerste waarde in een bezoek. |
| **[!UICONTROL Exits]** | A [&#x200B; Samenvattend aantal &#x200B;](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) dat toont het aantal tijden een bepaald afmetingspunt wordt gevangen als laatste waarde in een bezoek. |
| **[!UICONTROL Flow]** | A [&#x200B; stroom &#x200B;](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) visualisatie met de geselecteerde pagina als brandpunt. U kunt verder in de gegevens enkel als in om het even welke [&#x200B; Stroom &#x200B;](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) visualisatie boren. |

{style="table-layout:auto"}

Het gebruik ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) uit om het paneel opnieuw te vormen en te bouwen.
