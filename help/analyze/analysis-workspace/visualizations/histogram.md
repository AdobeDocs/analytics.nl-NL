---
description: Leer hoe u een histogram gebruikt, dat lijkt op een staafdiagram, maar getallen groepeert in bereiken (emmers).
title: Histogram
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
feature: Visualizations
role: User, Admin
exl-id: f3dd7507-db2c-495c-b6b9-6c770c7c7ddc
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 2%

---

# Histogram {#histogram}

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="Histogram"
>abstract="Maak een histogramvisualisatie om de distributie van numerieke gegevens in groepen bereiken weer te geven."


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Histogram in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [ Histogram ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/histogram) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


De ![ visualisatie van de Histogram ](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** is gelijkaardig aan a [!UICONTROL Bar] visualisatie, maar het groepeert aantallen in waaiers (emmers). De analyse automatiseert het &quot;knippen&quot;van aantallen in waaiers, maar u kunt de montages in [ Geavanceerde Montages ](#advanced-settings) veranderen.

## Gebruiken

Een histogram maken:

1. Voeg a ![ Histogram ](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogram]** visualisatie toe. Zie [ een visualisatie aan een paneel ](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.
1. Sleep metrisch van de **[!UICONTROL Metrics]** componentenlijst, of selecteer metrisch van [!UICONTROL *een metrisch*] drop-down menu toevoegen.
1. (optioneel) Selecteer **[!UICONTROL Show advanced settings]** . Zie [ Geavanceerde montages ](#advanced-settings).
1. Selecteer **[!UICONTROL Build]** .

>[!NOTE]
>
>Histogrammen ondersteunen alleen standaardmeetwaarden, geen berekende meetwaarden.

In het onderstaande voorbeeld wordt een histogram gebruikt om sessies voor het aantal personen te emmeren. Uit het histogram blijkt dat de meeste personen tussen de 16 en 21 sessies hebben voor het geselecteerde datumbereik.

![](assets/histogram.png)

## Geavanceerde instellingen

Als onderdeel van de visualisatie zijn specifieke histograminstellingen beschikbaar.

| Histograminstellingen | Beschrijving |
|---|---|
| **[!UICONTROL Starting bucket]** | Hiermee bepaalt u met welk emmertje het histogram begint. &quot;1&quot; is de standaardwaarde. U kunt begingetallen instellen van 0 tot oneindig (geen negatieve getallen). |
| **[!UICONTROL Metric buckets]** | Hiermee kunt u het aantal gegevensbereiken (emmers) vergroten/verkleinen. Het maximumaantal emmers is 50. |
| **[!UICONTROL Metric bucket size]** | Hiermee kunt u de grootte van elk emmertje instellen. U kunt bijvoorbeeld de emmergrootte wijzigen van de paginaweergave 1 in de weergave van 2 pagina&#39;s. |
| **[!UICONTROL Counting method]** | Selecteer uit **[!UICONTROL Person]**, **[!UICONTROL Session]** of **[!UICONTROL Event]** . Bijvoorbeeld paginaweergaven per sessie, of paginaweergaven per persoon of paginaweergaven per gebeurtenis. |

<!--Russ or Meike - Check Hit Type link above. -->

**Voorbeelden**:

| Beginemmer | Metrische emmers | Grootte van metrische emmer | Resultaat |
|:----:|:--:|:--:|:--|
| 1 | 5 | 2 | ![ Histogram, beginnend emmer 1, metrische emmers 5, metrische emmer grootte 2 ](assets/histogram-1-5-2.png) |
| 0 | 3 | 5 | ![ Histogram, beginnend emmer 0, metrische emmers 3, metrische emmer grootte 5 ](assets/histogram-0-3-5.png) |

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>&#x200B;>[Histogrammen gebruiken om onverwachte gegevenswaarden te identificeren ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168)

