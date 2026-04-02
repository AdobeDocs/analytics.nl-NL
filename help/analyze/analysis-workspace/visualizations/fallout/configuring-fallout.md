---
description: Leer hoe u de aanraakpunten configureert en opgeeft om een multidimensionale fallout-reeks te maken.
title: Een Fallout Visualisatie configureren
feature: Visualizations
role: User, Admin
exl-id: 9d2a0163-a5cb-4a1c-97e9-e78a8f99aaee
source-git-commit: 121fac9958dc34be513a23d5c3ad76d5f0e6b665
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Een fallout-visualisatie configureren

U kunt **touchpoints** specificeren om een multi-dimensionale reserveopeenvolging tot stand te brengen. In veel gevallen is een aanraakpunt een pagina op uw site. Aanraakpunten zijn echter niet beperkt tot pagina&#39;s. U kunt bijvoorbeeld gebeurtenissen, zoals eenheden, en unieke personen en terugkeerbezoeken toevoegen. U kunt ook dimensies toevoegen, zoals een categorie, type browser of interne zoekterm.

U kunt zelfs segmenten binnen een aanraakpunt toevoegen. U kunt bijvoorbeeld segmenten vergelijken, zoals iOS- en Android-gebruikers. Sleep de gewenste segmenten naar de bovenkant van de uitval en de informatie over die segmenten wordt toegevoegd aan het uitvalrapport. Als u alleen die segmenten wilt tonen, kunt u de basislijn Alle bezoeken verwijderen.

Voor de valutamogelijkheden geldt geen beperking voor het aantal aanraakpunten dat u kunt toevoegen of het aantal componenten dat u kunt gebruiken.

U kunt op afmetingen, metriek, en segmenten schilderen. Stel dat iemand op de ene pagina naar `shoes, shirt` kijkt en op de volgende pagina naar `shirt, socks` . Het volgende productflowrapport van schoenen is shirt en sokken, NOT shirt.

## Gebruiken

1. Voeg a ![&#x200B; ConversionFunnel &#x200B;](/help/assets/icons/ConversionFunnel.svg) **[!UICONTROL Fallout]** visualisatie toe. Zie [&#x200B; een visualisatie aan een paneel &#x200B;](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.

1. Sleep een component naar het vervolgkeuzemenu **[!UICONTROL Add touchpoint]** .

   >[!TIP]
   >
   >U kunt één pagina aan het reserverapport, eerder dan de volledige afmeting toevoegen. Klik de juiste pijl ![&#x200B; ChevronRight &#x200B;](/help/assets/icons/ChevronRight.svg) op de paginadimensie om een specifieke pagina, zoals **[!UICONTROL home]** te kiezen, aan het rapport van de Vallout toe te voegen.


   ![&#x200B; de homepage van de pagina van het Huis dimensie die aan het Add gebied van het Aanraakpunt wordt gesleept.](assets/fallout-drag.png)

1. Voeg aanraakpunten toe totdat de reeks is voltooid.

   De omcirkelde getallen in het grijze gedeelte van de balk geven de fallout tussen aanraakpunten aan (niet de totale fallout naar dat punt). De omcirkelde getallen in het groene gedeelte van de balk geven aan dat de geslaagde val van het vorige aanraakpunt naar het huidige aanraakpunt is doorgelopen.

   ![&#x200B; visualisatie van de Fallout &#x200B;](assets/fallout-visualization.png)

   Wanneer u aanraakpunten toevoegt, kunt u een van de volgende handelingen uitvoeren:

   * Combineer meerdere componenten door een of meer aanvullende componenten naar één aanraakpunt te slepen.

     >[!NOTE]
     >
     >De veelvoudige segmenten worden aangesloten bij EN, maar de veelvoudige punten zoals afmetingspunten en metriek worden aangesloten bij OF.

   * U wijzigt de volgorde van aanraakpunten door deze naar een ander niveau in de fallouthiërarchie te slepen.

   * Combineer twee aanraakpunten door het ene aanraakpunt naar het andere te slepen. Zet het aanraakpunt neer wanneer u het woord **[!UICONTROL Combine]** ziet.

   * Behoud individuele touchpoints aan de volgende slag (in tegenstelling tot *uiteindelijk*) binnen de weg. Onder elk aanraakpunt bevindt zich een kiezer met de opties **[!UICONTROL Eventual path]** en **[!UICONTROL Next hit]** , zoals u hier ziet:

     | Optie | Beschrijving |
     |---|---|
     | **[!UICONTROL Eventual path]** (standaardwaarde) | Bezoekers worden geteld dat *uiteindelijk* op de volgende pagina in de weg zal landen, maar niet noodzakelijk op het volgende bezoek. |
     | **[!UICONTROL Next hit]** | Bezoekers worden geteld die op de volgende pagina op het pad landen bij de volgende hit. |

   * Houd de muisaanwijzer boven een aanraakpunt om de fallout en andere informatie over dat niveau te zien. De informatie omvat de naam van het aanraakpunt, het aantal personen, en succestarief. U kunt ook de successnelheid vergelijken met andere aanraakpunten.

## Instellingen

De volgende visualisatie-instellingen zijn beschikbaar:

| Fallout container | Beschrijving |
|--- |--- |
| **[!UICONTROL Visits]** of **[!UICONTROL Visitors]** | Schakel tussen [!UICONTROL visits] en [!UICONTROL Visitors] om het plakken van personen te analyseren. De standaardwaarde is [!UICONTROL Visitors] . Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau (verschillende bezoeken) begrijpen of de analyse beperken tot één bezoek. |


## Contextmenu

Als onderdeel van de visualisatie zijn specifieke opties voor contextmenu&#39;s beschikbaar.

### Het contextmenu openen

U kunt het contextmenu op een van de volgende manieren openen:

* Houd de cursor boven een aanraakpunt in de visualisatie en selecteer vervolgens **[!UICONTROL Click to analyze]** .

  ![&#x200B; het contextmenu van de Toegang van hover &#x200B;](assets/fallout-tooltip-analyze.png)

* Klik met de rechtermuisknop op een aanraakpunt in de visualisatie.

  ![&#x200B; opties van de Fallout &#x200B;](assets/fallout-options.png)

### Opties in het contextmenu

De volgende opties voor contextmenu&#39;s zijn beschikbaar:

| Optie | Beschrijving |
|--- |--- |
| **[!UICONTROL Trend touchpoint]** | Zie trendgegevens voor een aanraakpunt in een lijngrafiek, met sommige vooraf gebouwde anomaliedetectiegegevens. |
| **[!UICONTROL Trend touchpoint (%)]** | Hiermee wordt het totale uitvalpercentage verhoogd. |
| **[!UICONTROL Trend all touchpoints (%)]** | Hiermee worden alle aanraakpuntpercentages in de fallout (behalve **[!UICONTROL All Visitors]** als deze is opgenomen) in hetzelfde diagram gekweekt. |
| **[!UICONTROL Breakdown fallthrough at this touchpoint]** | Bekijk wat bezoekers deden tussen twee aanraakpunten (dit aanraakpunt en het volgende aanraakpunt) als ze doorgingen naar het volgende aanraakpunt. Met deze optie maakt u een vrije-vormtabel waarin de afmetingen worden weergegeven. U kunt afmetingen en andere elementen van de tabel vervangen. Bijvoorbeeld, een lijst die **[!UICONTROL Fallthrough: All Visitors > Page equals any of home]** wordt geëtiketteerd en **[!UICONTROL Page]** als afmeting en **[!UICONTROL Unique Visitors]** bevat die door het [&#x200B; project-slechts snelle segment &#x200B;](/help/components/segmentation/segmentation-workflow/seg-quick.md) **[!UICONTROL Fallthrough: All Visitors > Page equals any of home]** als metrisch wordt gesegmenteerd. Inspecteer het segment om te begrijpen hoe het reservesegment wordt bepaald. |
| **[!UICONTROL Breakdown fallout at this touchpoint]** | Bekijk wat bezoekers die dit niet via de funnel deden, direct na de geselecteerde stap deden. Met deze optie maakt u een vrije-vormtabel waarin de afmetingen worden weergegeven. U kunt afmetingen en andere elementen van de tabel vervangen. Bijvoorbeeld, een lijst die **[!UICONTROL Fallout: All Visitors > Page equals any of home]** wordt geëtiketteerd en **[!UICONTROL Page]** als dimensie en **[!UICONTROL Unique Visitors]** bevat die door het [&#x200B; project-enige snelle segment &#x200B;](/help/components/segmentation/segmentation-workflow/seg-quick.md) **[!UICONTROL Fallthrough: All Visitors > Page equals any of home]** segment als metrisch wordt gesegmenteerd. Inspecteer het segment om te begrijpen hoe het reservesegment wordt bepaald. |
| **[!UICONTROL Create segment from touchpoint]** | Maak een nieuw segment van het geselecteerde aanraakpunt. |

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Contextmenu Visualisatie &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

