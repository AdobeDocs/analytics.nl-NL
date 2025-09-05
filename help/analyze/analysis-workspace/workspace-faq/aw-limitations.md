---
description: Meer informatie over bekende beperkingen in Adobe Analysis Workspace en de bijbehorende componenten
title: Bekende beperkingen
feature: Workspace Basics
role: User, Admin
exl-id: 520e970b-1387-4f70-985b-bfe397f4a21b
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# Bekende beperkingen

Hier volgt een lijst met bekende beperkingen in Analysis Workspace en de bijbehorende componenten:

## Tabellen

* Datumvergelijkingskolommen kunnen niet worden toegevoegd wanneer datumbereiken of metriek worden gebruikt als rijen van een tabel.
* Metrisch maken van selectie is uitgeschakeld wanneer segmenten worden gebruikt als rijen van een tabel. Bovendien moet Metrisch maken van selectie niet worden toegepast op kolommen met datumuitlijning.
* Voorwaardelijke opmaak voor splitsingsrijen kan geen aangepaste bereiken gebruiken.
* De totale rijen van de lijst kunnen niet worden getrand wanneer Berekende totalen door de rijwaarden op te tellen wordt toegepast die (typisch wordt gebruikt met Statische rijpunten) plaatsen.

## Visualisaties

* Visualisaties waarbij segmenten zoals [!UICONTROL Fallout] , [!UICONTROL Flow] , [!UICONTROL Cohort] en [!UICONTROL Histogram] worden gebruikt, kunnen berekende metriek niet als invoer accepteren.
* [!UICONTROL Flow]: de afmetingen voor in- en uitstappen, bijvoorbeeld [!UICONTROL Entry page] , kunnen niet worden gebruikt in de stroom.
* [!UICONTROL Cohort]: niet-gehele getallen kunnen niet worden gebruikt als Cohortcriteria.

## Segmenten

* Bepaalde metriek en afmetingen kunnen niet worden gesegmenteerd, zoals [!UICONTROL Events] , [!UICONTROL Persons] , enzovoort.
* Ad hoc segmenten die in [ worden gecreeerd paneeldropzone ](/help/analyze/analysis-workspace/c-panels/panels.md) zijn een type van snel segment. Ze worden alleen weergegeven in het linkerdeelvenster van Workspace of in Segmentbeheer als ze openbaar zijn gemaakt. Voor meer informatie, zie [ Snelle segmenten ](/help/components/segmentation/segmentation-workflow/seg-quick.md).

## Berekende standaarden

* Berekende meetgegevens kunnen niet worden gebruikt in bepaalde visualisaties. Zie [ Visualisaties ](#visualizations).
* Berekende metriek kunnen niet worden gebruikt in het deelvenster [!UICONTROL Attribution] , omdat berekende metriek zelf afzonderlijke attributiemodellen kunnen bevatten.
* Bepaalde componenten en operatoren zijn niet beschikbaar als een berekende metrische waarde wordt gemaakt vanuit Workspace (in tegenstelling tot de waarde die wordt gemaakt op basis van [!UICONTROL Components > segments]). Bijvoorbeeld [!UICONTROL IP Address] .

## Datumbereik

* Aangepaste datumbereiken bieden geen ondersteuning voor [!UICONTROL This day last year] , [!UICONTROL This day last month] , enzovoort.


## Rapportinstellingen

* Sommige instellingen op de pagina [!UICONTROL Report Settings] zijn niet van toepassing. Analysis Workspace gebruikt alleen de [!UICONTROL Language/Currency/Encoding] -instellingen onderaan: [!UICONTROL Thousands separator] , [!UICONTROL Scheduled Report Encoding] en [!UICONTROL CSV Separator Character] .



<!--
# Known limitations in Analysis Workspace 

Here is a list of known limitations in Analysis Workspace and its related components:

## Tables

* Date comparison columns cannot be added when either date ranges or metrics are used as rows of a table.
* Create metric from selection is disabled when segments are used as rows of a table. Additionally, Create metric from selection should not be applied to date-aligned columns.
* Conditional formatting for breakdown rows cannot use custom ranges.
* Table total rows cannot be trended when Calculate totals by summing the row values setting is applied (typically used with Static row items).
* [!UICONTROL Contribution Analysis] can be run at the [!UICONTROL daily] granularity _only_. It cannot be run against [!UICONTROL hourly], [!UICONTROL weekly], etc., data.

## Visualizations

* Visualizations that leverage segmentation, such as [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], and [!UICONTROL Histogram], cannot accept calculated metrics as inputs.
* [!UICONTROL Flow]: Entry/Exit dimensions, e.g. [!UICONTROL Entry page], cannot be used in Flow.
* [!UICONTROL Cohort]: Non-integers cannot be used as Cohort criteria.

## Panels

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## Components > Segments

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Adhoc segments created in the [panel dropzone](/help/analyze/analysis-workspace/c-panels/panels.md) are a type of quick filter. They do not appear in the left rail of Workspace or the Segment component manager unless they are made public. For more information, see [Quick segments](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

## Components > Calculated Metrics

* Calculated metrics cannot be used in certain visualizations. See 'Visualizations' above.
* Calculated metrics cannot be used in the [!UICONTROL Attribution] panel, since calculated metrics themselves can include separate attribution models.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). For example, [!UICONTROL IP Address].

## Components > Date Ranges

* Custom date ranges do not support [!UICONTROL This day last year], [!UICONTROL This day last month], etc.

## Components > Virtual Reports Suites

* When report time processing is enabled, certain components are not supported. For a full list, see [Report Time Processing](/help/components/vrs/vrs-report-time-processing.md).

## Components > All components > Report settings

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. Analysis Workspace uses only the [!UICONTROL Language/Currency/Encoding] settings at the bottom: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], and [!UICONTROL CSV Separator Character].

## Attribution

* A subset of metrics is not supported in [!UICONTROL Attribution]. For a full list, see the [Attribution FAQ](/help/analyze/analysis-workspace/attribution/faq.md).
-->
