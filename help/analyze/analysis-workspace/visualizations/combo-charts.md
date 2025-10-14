---
description: Leer hoe u vergelijkingsgegevens in Analysis Workspace visualiseert, zoals het maken van vergelijkingen met vorige maand, vorig jaar enzovoort.
title: Combo
feature: Visualizations
role: User, Admin
exl-id: 08e49857-aa58-4527-bdfd-b1663a75a02b
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Combo {#combo}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_combo_button"
>title="Combo"
>abstract="Maak snel een combografievisualisatie zonder eerst een vrije-vormtabel te hoeven maken."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_Dit artikel documenteert Combo visualization in_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._

_zie [&#x200B; Combo &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/combo-charts) voor_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


De ![&#x200B; kaart Combo &#x200B;](/help/assets/icons/ComboChart.svg) **[!UICONTROL Combo]** visualisatie maakt het gemakkelijk om een vergelijkingsvisualisatie snel te bouwen zonder het moeten eerst een lijst bouwen. U kunt tendensen in uw gegevens in een lijn gemakkelijk bekijken/bar combinatie.

Een [!UICONTROL Combo] gebruiken om:

* Vergelijk de bestellingen van deze week met bestellingen op hetzelfde tijdstip in vorige maand (en vorig jaar).
* Analyseer en vergelijk snel meerdere meetgegevens (zoals [!UICONTROL Persons] en [!UICONTROL Revenue] ) met elkaar op hetzelfde diagram.
* Analyseer metrisch tegen een functie (zoals [!UICONTROL Cumulative Average]) over een tijdshorizon.

Houd er rekening mee dat:

* U kunt meerdere vergelijkingen toevoegen in één [!UICONTROL Combo chart] .
* Als u een of meer vergelijkingen toevoegt, moeten deze van hetzelfde type zijn, zoals [!UICONTROL Time comparison] .
* U kunt maximaal vijf vergelijkingen maken.
* U kunt maximaal drie filters toepassen op een metrische waarde.
* Berekende metriek worden niet ondersteund in Combo-diagrammen.

## Gebruiken

1. Voeg a ![&#x200B; Commentaar &#x200B;](/help/assets/icons/ComboChart.svg) [!UICONTROL Combo] visualisatie toe. Zie [&#x200B; een visualisatie aan een paneel &#x200B;](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen

1. Selecteer in de vervolgkeuzelijsten een afmeting voor de X-as en een afmeting voor de Y-as.

1. Selecteer het type [!UICONTROL Line comparison] dat u wilt gebruiken.

   | Het vergelijkingstype Lijn | Definitie |
   | --- | --- |
   | **[!UICONTROL Time comparison]** | Het meest voorkomende type vergelijking: deze periode wordt bijvoorbeeld vergeleken met 4 weken geleden. Als u [!UICONTROL Time comparison] selecteerde, maak een secundaire selectie over welke tijdspanne u wilt vergelijken.<p>![&#x200B; LIne vergelijking met de geselecteerde periode van de Tijd en het secundaire selectiegebied voor de periode van de Tijd.](assets/combo-time-period.png) |
   | **[!UICONTROL Function]** | U kunt een functie als [!UICONTROL Average] in de vergelijking introduceren. Zie de lijst van [&#x200B; gesteunde functies &#x200B;](#supported-functions).<p>![&#x200B; LIne vergelijkingsdrop-down menu die Functies tonen en een lijst van beschikbare gesteunde functies.](assets/combo-functions.png) |
   | **[!UICONTROL Secondary metric]** | U kunt bijvoorbeeld [!UICONTROL Revenue] met een andere metrische waarde vergelijken.<p>![&#x200B; een Combo grafiek die twee metriek vergelijkt.](assets/combo-2metrics-settings.png) |

   {style="table-layout:auto"}

1. Selecteer **[!UICONTROL Build]** .

   De uitvoer ziet er ongeveer als volgt uit:

   ![&#x200B; een Combo grafiek die de huidige periode in een grafiek van de bar en vergelijkingsperiode in de lijngrafiek toont &#x200B;](assets/combo-output.png)

   De huidige periode wordt weergegeven in het staafdiagram. Het lijndiagram geeft de vergelijkingsperiode weer. De punten op het lijndiagram zijn gekend als *balken*.

## Ondersteunde functies

Wanneer u **[!UICONTROL Function]** als [!UICONTROL Line comparison type] selecteert, wordt een functie van de gekozen metrische waarde geretourneerd.

| Functie | Definitie |
| --- | --- |
| **[!UICONTROL Column Sum]** | Hiermee worden alle numerieke waarden toegevoegd voor een metrische waarde in een kolom (over de elementen van een dimensie) |
| **[!UICONTROL Cumulative Average]** | Retourneer het gemiddelde van de laatste N rijen. |
| **[!UICONTROL Median]** | Retourneert de mediaan voor een metrische waarde in een kolom. De mediaan is het getal in het midden van een reeks getallen. De helft van de getallen heeft waarden die groter zijn dan of gelijk zijn aan de mediaan, en de helft van het getal heeft waarden die kleiner zijn dan of gelijk zijn aan de mediaan. |
| **[!UICONTROL Cumulative]** | De cumulatieve som van N rijen. |
| **[!UICONTROL Column Maximum]** | Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. |
| **[!UICONTROL Mean]** | Retourneert het rekenkundig gemiddelde (of gemiddelde) voor een metrische waarde. |
| **[!UICONTROL Column Minimum]** | Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. |

{style="table-layout:auto"}

Hier is een voorbeeld van het cumulatieve gemiddelde van de metrische inkomsten:

![&#x200B; een Combo grafiek die het cumulatieve gemiddelde &#x200B;](assets/combo-cumul-avg.png) toont

Hier is een voorbeeld van een combo grafiek met zowel Cumulatieve gemiddelde als Gemiddelde functies:

![&#x200B; A Combo grafiek die zowel cumulatieve gemiddelde als gemiddelde functies tonen.](assets/combo-three-functions.png)

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>
