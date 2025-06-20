---
description: Berekende en Geavanceerde berekende metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.
keywords: Berekende waarden;Geavanceerde berekende waarden
title: Berekende en geavanceerde berekende statistieken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 9714863374052e257e1d6349c442fc74182a0a2f
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 4%

---

# Berekende en geavanceerde berekende metriek

Berekende en geavanceerde berekende metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.

Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Zo kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u de [!DNL Analytics] -implementatie hoeft te wijzigen. De aangepaste meetgegevens die beschikbaar zijn in elk [!DNL Analytics] -pakket zijn:

* Adobe [!DNL Analytics] Foundation: berekend
* [ Uitgezochte Adobe Analytics ](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html): Berekend + Geavanceerd Berekend
* [ Adobe Analytics Prime ](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html): Berekend + Geavanceerd Berekend
* [ Adobe Analytics Ultimate ](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html): Berekend + Geavanceerd Berekend

Hier is een vergelijking van berekende metriek en geavanceerde berekende metriekmogelijkheden:

| Builder-opties | Berekende cijfers | Geavanceerde berekende meetwaarden |
|---|---|---|
| [ types van Formaat (decimaal, tijd, percenten, munt) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | Ja | Ja |
| [ veranderingen van de Attributie (gebrek, lineair, participatie, enz.) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| [ Metrische types (standaard, totaal) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| [ pas segmenten ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) toe | Nee | Ja |
| [ Basisfuncties (telling, abs waarde, gemiddelde, enz.) ](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | Nee | Ja |
| [ Geavanceerde functies (regressie, als/toen, t-score, enz.) ](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | Nee | Ja |

## Mogelijkheden {#section_A0A5C275B68A4D628950BBB0B1EE631F}

U kunt

* Maak metrische gegevens over [!UICONTROL Analysis Workspace] , [!UICONTROL Report Builder] , [!UICONTROL Anomaly Detection] en [!UICONTROL Contribution Analysis] .
* Creeer gesegmenteerde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op segmenten.

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Berekende metriek ](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

* De metriek van het aandeel over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.
* (Alleen geavanceerde berekende maatstaven) Segment op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.

* (Alleen geavanceerde berekende maatstaven) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.


## Beperkingen

Met sommige functies van [!DNL Analytics] kunt u wel gebeurtenissen gebruiken, maar geen berekende meetwaarden:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Cohort Analysis] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segments]
* [!DNL Analytics] for [!DNL Target]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Berekende metriek ](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Gesegmenteerde berekende metriek in segmenten ](https://video.tv.adobe.com/v/25409?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

<!--

Here is a short overview of the [!UICONTROL Calculated metrics] tools: 

|Tool|Capabilities|
|--- |--- |
| [Calculated metric builder](c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)| The capabilities are: <ul><li>Create calculated and advanced calculated metrics using advancmd allocation models.</li><li>Add segments inline to metric formulas</li><li>Compare segments in the same report. For example, compare local visitors vs. international visitors.</li><li>Use statistical functions</li><li>Provide detailed metric descriptions (show what it does, where to use it, where NOT to use it)</li><li>Copy definitions into new metrics</li><li>Provide an inline metric preview</li><li>Set metric polarity, which indicates whether it's good or bad if a given custom event (metric) goes up</li><li>Tag metrics</li></ul>|
|Calculated Metric Manager|<ul><li>Share metrics with others</li<li>Approve and curate metrics</li><li>Organize (tag) your metrics so people can find them</li><li>Delete metrics</li><li>Rename metrics</li></ul>|
|Metric Selector rail|Lets you search for and add/apply metrics to the report. You can also change the  sort order (options are: alphabetical, recommended, frequently used, recently used.) In addition, you can filter on Report Suites to show only metrics created in a specific report suite.  To access this Metric Selector, click the Metrics icon  to the left of a report. |
|API for Calculated Metrics|Part of the Adobe Analytics 2.0 API set.|

-->