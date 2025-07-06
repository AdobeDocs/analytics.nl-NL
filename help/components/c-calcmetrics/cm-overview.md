---
description: Meer informatie over berekende metriek die u kunt maken op basis van bestaande metriek.
keywords: Berekende standaarden
title: Overzicht van berekende statistieken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# Overzicht van berekende metriek

Berekend zijn aangepaste metriek die u kunt maken op basis van bestaande metriek.

Berekende metrisch zijn aangepaste metriek die u op basis van bestaande metriek kunt maken. De berekende metriek bieden een flexibele manier aan om, douanemetriek te bouwen te beheren en te leiden die u toelaten om uw gegevens te analyseren zonder het moeten uw implementatie veranderen.

De berekende metriek zijn beschikbaar in elk [!DNL Analytics] pakket, nochtans is het Pak van Adobe Analytics Foundation voor Experience Cloud beperkt tot basis berekende metriek met inbegrip van [ formaattypes (decimaal, tijd, percenten, munt) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md), [ toewijzingsveranderingen (gebrek, lineair, participatie, enz.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md), [ metrische types (standaard, totaal) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md), en [ basisexploitanten ](c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#operators) (voeg toe, trek af, vermenigvuldig, en verdeel).


Zie de [ Beschrijving van het Product van Adobe Analytics ](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html) voor meer informatie.

<!--
Here is a comparison of calculated metrics and advanced calculated metrics capabilities: 

| [Format types (decimal, time, percent, currency)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Attribution changes (default, linear, participation, etc.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Metric types (standard, total)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
|  Basic operators (add, subtract, multiply, divide)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Apply segments](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md)  | ![StopCircle](/help/assets/icons/StopCircle.svg)  | Yes  |
| [Basic functions (count, abs value, mean, etc)](/help/components/c-calcmetrics/cm-reference/cm-functions.md)  | No  | Yes  |
| [Advanced functions (regression, if/then, t-score, etc)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md)  | No  | Yes  |

-->

## Mogelijkheden {#section_A0A5C275B68A4D628950BBB0B1EE631F}

U kunt

* [ creeer metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-workflow.md) over [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection], en [!UICONTROL Contribution Analysis].
* [ creeer gesegmenteerde metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Bijvoorbeeld, kunt u metrisch voor *Nieuwe bezoekers* tot stand brengen, met een telling van mensen voor wie dit de eerste zitting is.

* [ de metriek van het Aandeel ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md) over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.

* [ neem statistische functies ](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) op om u te helpen beter uw gegevens beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

## Beperkingen

Sommige functies van [!DNL Analytics] staan het gebruik van berekende meetwaarden niet toe:

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

>[!MORELIKETHIS]
>
>[ creeer metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-workflow.md)
>>[Metriek samenstellen ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)
>>[Functies gebruiken ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-using-functions.md)
>
