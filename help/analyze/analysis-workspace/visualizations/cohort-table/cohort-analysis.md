---
title: Overzicht van cohortabellen
description: Leer hoe u dieper in de gegevens rondom uw publiek kunt graven en die gegevens kunt onderverdelen in verwante groepen met behulp van cohortanalyse. Gebruik cohortanalyse in Analysis Workspace.
feature: Visualizations
role: User, Admin
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Overzicht van de cohortingtabel {#cohort-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_button"
>title="Cohortingtabel"
>abstract="Maak een cohortvisualisatie om gebruikers te groeperen op basis van de voltooiing van een gebeurtenis en de doorlopende betrokkenheid te analyseren en in de loop van de tijd te verdraaien."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_panel"
>title="Cohortingtabel"
>abstract="Groepeer gebruikers op basis van voltooiing van een gebeurtenis en analyseer vervolgens hun doorlopende betrokkenheid en loop de tijd door.<br/><br/>**Parameters &#x200B;**<br/>**criteria van de Opname**: De componenten die worden gebruikt om uw aanvankelijke bezoekerscohorts te bepalen.<br/>**criteria van de Terugkeer**: De componenten die worden gebruikt om te bepalen als een bezoeker is teruggekeerd."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de lijst van de Cohort in_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [&#x200B; de lijst van het Cohort &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/cohort-table/cohort-analysis) voor_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]



A *cohort* is een groep mensen die gemeenschappelijke kenmerken over een gespecificeerde periode delen. A ![&#x200B; TextNumbered &#x200B;](/help/assets/icons/TextNumbered.svg) **[!UICONTROL Cohort table]** visualisatie is nuttig, bijvoorbeeld, wanneer u wilt leren hoe een cohort met een merk in dienst neemt. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (De Verklaringen van [!UICONTROL Cohort Analysis] zijn beschikbaar op het Web, zoals bij [&#x200B; Analyse 101 van de Cohort &#x200B;](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke afmetingen, metriek, en filters) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [&#x200B; Kromme en Aandeel &#x200B;](/help/analyze/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met een [!UICONTROL Cohort table] :

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Bespreek wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.

[!UICONTROL Cohort table] is beschikbaar voor alle Adobe Analytics-klanten met toegangsrechten tot [!UICONTROL Analysis Workspace] .


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; analyse van de Cohort in Analysis Workspace &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] biedt geen ondersteuning voor niet-filterbare metriek (inclusief berekende meetwaarden), niet-gehele getallen (zoals Opbrengst) of Voorvallen. Alleen metriek die in filters kan worden gebruikt, kan in [!UICONTROL Cohort Analysis] worden gebruikt en kan slechts één voor één worden verhoogd.

Cohort-tabellen in Adobe Analytics ondersteunen op twee gebaseerd metrisch (of numeriek). Purchase.Value (een dubbele waarde) kan bijvoorbeeld worden gebruikt als een insluitings-/retourmetrisch object. Bovendien zijn alle meetgegevens die via de Analytics Source Connector naar Adobe Experience Platform worden doorgegeven, verdubbelbaar.

## Mogelijkheden voor kleurentabellen

De volgende secties beschrijven de eigenschappen van de Analyse van de Cohort die voor nauwkeurige controle over de cohorts toestaan u bouwt.

Voor meer gedetailleerde informatie over het creëren van een cohort en het runnen van a [!UICONTROL Cohort Analysis] rapport, zie [&#x200B; een lijst van de Cohort &#x200B;](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md) vormen.

### Bewaartabel

Een [!UICONTROL Retention] -cohortentabel retourneert personen: elke gegevenscel geeft het onbewerkte aantal en percentage weer van de personen in de cohort die de actie tijdens die periode hebben uitgevoerd. U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![&#x200B; het cohort van de Vermindering van A die de eenheden en het percentage van personen in de cohort toont.](assets/retention-report.png)

### Churn-tabel

Een [!UICONTROL Churn] -cohortabel is het omgekeerde van een retentietabel en toont de personen die in de loop der tijd niet of niet aan de retourcriteria voor uw cohort hebben voldaan. U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![&#x200B; de lijst van het Koord van A die eenheden en percentage van mensen tonen die niet aan de terugkeercriteria voor een cohort beantwoordden.](assets/churn-report.png)

### Rolberekening

U kunt de retentie of het churn berekenen op basis van de vorige kolom, niet de opgenomen kolom, die wordt aangeduid als rolberekening.

![&#x200B; het bewaarrapport van de Cohort dat berekeningen toont die op een vorige kolom van gegevens worden gebaseerd.](assets/retention-report-rolling.png)

### Latentietabel

Een latentietabel meet de tijd die is verstreken voor en na de opnemingsgebeurtenis. De latentie meten is een uitstekend hulpmiddel voor pre- en postanalyse. De kolom **[!UICONTROL Included]** bevindt zich in het midden van de tabel en de tijdsperioden vóór en na de gebeurtenis include worden aan beide zijden weergegeven.

![&#x200B; het rapport van de Cohort van A die de verstreken tijd vóór en na een gebeurtenis tonen.](assets/retention-report-latency.png)

### Cohort aangepaste dimensie

U kunt cohorten maken op basis van een geselecteerde afmeting en niet op basis van een tijd (de standaardinstelling). Gebruik afmetingen zoals [!UICONTROL City geo] , [!UICONTROL Marketing channel] , [!UICONTROL campaign] , [!UICONTROL product] , [!UICONTROL page] , [!UICONTROL region] of een andere dimensie om aan te geven hoe de retentie verandert. Gebaseerd op de verschillende waarden van deze afmetingen.

![&#x200B; het rapport van de Cohort van A die aangepast rapport met geselecteerde dimensies tonen niet de standaardop tijd-gebaseerde cohort.](assets/retention-dimensions.png)

>[!MORELIKETHIS]
>
>[&#x200B; vorm een lijst van de Cohort &#x200B;](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).
>



<!--
A *`cohort`* is a group of people sharing common characteristics over a specified period. [!UICONTROL Cohort Analysis] is useful, for example, when you want to learn how a cohort engages with a brand. You can easily spot changes in trends, then respond accordingly. (Explanations of [!UICONTROL Cohort Analysis] are available on the web, such as at [Cohort Analysis 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

After creating a cohort report, you can curate its components (specific dimensions, metrics, and segments), then share the cohort report with anyone. See [Curate and Share](/help/analyze/analysis-workspace/curate-share/curate.md).

Examples of what you can do with [!UICONTROL Cohort Analysis]:

* Launch campaigns designed to spur a desired action.
* Shift marketing budget at exactly the right time in the customer lifecycle.
* Recognize when to end a trial or an offer, in order to maximize value.
* Gain ideas for A/B testing in areas such as pricing, upgrade path, and so on.

[!UICONTROL Cohort Analysis] is available for all Adobe Analytics customers with access rights to [!UICONTROL Analysis Workspace].


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Cohort analysis in Analysis Workspace](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/overview-of-cohort-tables-in-analysis-workspace){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] does not support non-segmentable metrics (including calculated metrics), non-integer metrics (such as Revenue), or Occurrences. 
>
>Only metrics that can be used in segments can be used in [!UICONTROL Cohort Analysis], and they can only be incremented by >1 at a time. 

## Cohort Analysis capabilities

The following sections describe Cohort Analysis features that allow for fine-tuned control over the cohorts you are building.

For more detailed information about creating a cohort and running a [!UICONTROL Cohort Analysis] report, see [Configure a Cohort Analysis report](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

### [!UICONTROL Retention] Table

A [!UICONTROL Retention] cohort report returns visitors: each data cell shows the raw number and percentage of visitors in the cohort who did the action during that time period. You can include up to 3 metrics and up to 10 segments.

![](assets/retention-report.png)


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Calculate rolling retention](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/calculate-rolling-retention-in-cohort-tables){target="_blank"} for a demo video.

>[!ENDSHADEBOX]



### [!UICONTROL Churn] Table

A [!UICONTROL Churn] cohort is the inverse of a retention table and shows the visitors who fell out or never met the return criteria for your cohort over time. You can include up to 3 metrics and up to 10 segments.

![](assets/churn-report.png)

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Churn analysis](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/churn-analysis-with-cohort-tables){target="_blank"} for a demo video.

>[!ENDSHADEBOX]


### [!UICONTROL Rolling Calculation]

Lets you calculate retention or churn based on the previous column, not the included column.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Table

Measures the time that has elapsed before and after the inclusion event occurred. This is an excellent tool for pre/post analysis. The **[!UICONTROL Included]** column is in the center of the table and time periods before and after the inclusion event are shown on both sides.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Create cohorts based on a selected dimension, and not time-based cohorts, which are the default. Use dimensions such as [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region], or any other dimension in Adobe Analytics to show how retention changes based on the different values of these dimensions.

![](assets/cohort-customizable-cohort-row.png)

-->
