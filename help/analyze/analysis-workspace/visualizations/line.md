---
description: Gebruik de lijnvisualisatie om trended (op tijd-gebaseerde) datasets visualiseren.
title: Lijn
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
feature: Visualizations
role: User, Admin
exl-id: d177b39f-add7-4011-977a-1bdf3a9368cb
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Lijn {#line}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_line_button"
>title="Lijn"
>abstract="Creeer een lijnvisualisatie die toont hoe de waarden over een periode veranderen. Een lijnvisualisatie kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Lijn in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [ Lijn ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/line) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

![ GraphTrend ](/help/assets/icons/GraphTrend.svg) **[!UICONTROL Line]** visualisatie vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijnvisualisatie kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

![ visualisatie van de lijn 0&rbrace;](assets/line-viz.png)


## Instellingen

Als deel van de [ visualiseringsmontages ](freeform-analysis-visualizations.md#settings), zijn de specifieke montages van de lijnvisualisatie beschikbaar.

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Granularity]** | Selecteer in het keuzemenu Korreligheid een trendmatige visualisatie van dag naar week, enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel. |
| **[!UICONTROL Show min]** <br/>**[!UICONTROL Show max]** | U kunt een label voor de minimum- en maximumwaarde bedekken om de minimum- en maximumwaarden in een metrische waarde te markeren. De min/max-waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie.<br/>![ een bedekking met het minimum en maximumwaardeetiket.](assets/min-max-labels.png) |
| **[!UICONTROL Show trendline]** | U kunt een regressie of bewegende gemiddelde trendline aan uw lijnreeks toevoegen. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. Selecteer een model in de lijst als u deze optie hebt geselecteerd. Zie [ Modellen ](#models) voor een overzicht en een beschrijving van beschikbare modellen.<br/>![ Lineaire trendline ](assets/show-linear-trendline.png). |

>[!TIP]
>
>Aanbevolen wordt trendlines toe te passen op gegevens die geen heden (gedeeltelijke gegevens) of toekomstige data omvatten. De trendlijn wordt scheefgetrokken door de datum van vandaag of van morgen. Als u echter datums in de toekomst wilt opnemen, verwijdert u nullen uit de gegevens om te voorkomen dat de gegevens gedurende die dagen worden schuingetrokken. Ga naar de gegevensbrontabel van de visualisatie, kies de metrische kolom en schakel vervolgens **[!UICONTROL Column Settings]** > **[!UICONTROL Interpret zero as no value]** in.



### Modellen

Alle trendlines van het regressiemodel zijn geschikt gebruikend gewone minste vierkanten:

| Model | Beschrijving |
| --- | --- |
| **[!UICONTROL Linear]** | Creeer een best-geschikte rechte lijn voor eenvoudige lineaire datasets en is nuttig wanneer de gegevens met een constante snelheid stijgen of verminderen. Vergelijking: `y = a + b * x` |
| **[!UICONTROL Logarithmic]** | Maak een lijn met een curve die het best past en die nuttig is wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: `y = a + b * log(x)` |
| **[!UICONTROL Exponential]** | Maak een gekromde lijn en is handig wanneer gegevens stijgen of dalen met voortdurend stijgende snelheden. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a + e^(b * x)` |
| **[!UICONTROL Power]** | Maak een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a * x^b` |
| **[!UICONTROL Quadratic]** | Zoekt het best-past voor een dataset die als parabola wordt gevormd (naar boven of naar onder bedekken). Vergelijking: `y = a + b * x + c * x^2` |
| **[!UICONTROL Moving average]** | Maak een vloeiende trendline op basis van een set gemiddelden. Bij een voortschrijdend gemiddelde wordt een bepaald aantal gegevenspunten gebruikt (bepaald door uw [!UICONTROL Granularity] -selectie), wordt het gemiddelde genomen en wordt het gemiddelde gebruikt als een punt op de regel. Voorbeelden zijn een voortschrijdend gemiddelde van zeven dagen of een voortschrijdend gemiddelde van vier weken. |

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

