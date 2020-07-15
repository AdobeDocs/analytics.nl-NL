---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Reports & Analytics, Ad hoc analysis, Report Builder, Data warehouse en Data Workbench
title: Analytics-productvergelijking en -vereisten
translation-type: tm+mt
source-git-commit: cb3948f03e65edf18b7f3c54c891b77629b41dc0
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 34%

---


# Analytics-productvergelijking en -vereisten

Systeemvereisten en een vergelijking van Analysis Workspace, Reports &amp; Analytics, Report Builder, Data warehouse, Data Workbench, Analytics API 2.0., Data Feeds en Customer Journey Analytics.

Ga [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)voor meer informatie over het Adobe Analytics-product dat u wilt gebruiken.

| Productnaam en Help-koppeling | [Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) | [Rapporten en Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/getting-started.html) | [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html) | Analytics API 2.0 | Gegevensfeeds | Customer Journey Analytics |
|---|---|---|---|---|---|---|
| **Toegangsmethode** | Browser oplossing voor het bouwen van robuuste, projecten van de douaneanalyse, en het democratiseren van inzichten. | Browseroplossing voor digitale analyse. | Browser oplossing die rapporten in .csv formaat produceert. Kan bestanden in tableau-indeling genereren. | Multikanaalanalyseprogramma voor geavanceerde analyse, zoals het modelleren van de douaneattributie, voorspellende analyse, en 360 klantenanalyse. |  |  |  |
| **Uitsplitsingen rapporteren** | Onbeperkt | Maximaal 2 correlaties | Maximaal 2 correlaties | Voert volledig uitgevouwen, onbeperkte uitsplitsingen uit, onderverdeeld door segment. | Onbeperkt |  |  |  |
| **Segmentvergelijkingen** | Onbeperkt | Tot 2 segmenten | Onbeperkt (gegevensverzoek stapelen) | 1 segment. Ondersteunt meerdere (gestapelde) segmenten. | Onbeperkt |  |  |  |
| **Uitvoerlimiet rij** | 400 | 200 | 50,000 | Onbeperkt | Aanpasbaar |  |  |  |
| **Unieke waardemaxima** (binnen eVar-/prop-rapporten) | 500 K-2 MM | 500 K-2 MM | 500 K-2 MM | Onbeperkt | Aanpasbaar |  |  |  |
| **Trechter/Pacht** | Ja: [Uitvallen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)/[stroom](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/reports.html) | Ja | Nee | Ja |  |  |  |
| **Geavanceerde reisanalyse van klanten** | Yes: [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-landing.html) | Nee | Nee | Nee | Ja |  |  |  |
| **Cohortanalyse** | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | Nee | Nee | Nee | Ja |  |  |  |
| **Geavanceerde kenmerken** | Ja: [Attributie-IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution-iq.html) | Beperkt - eerste/laatste/lineair | Beperkt - eerste/laatste/lineair | Beperkt - eerste/laatste/lineair | Ja |  |  |  |
| **Verbeterde visualisatieopties** | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) | Nee | Ja | Nee | Ja |  |  |  |
| **Aanpasbare indeling** | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) | Ja, [dashboards](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/dashboard.html) | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/layout/configure-the-custom-layout.html) | De resultaten van de soort door onderverdeling of door metriek. | Ja |  |  |  |
| **Projectcuratie** (Vereenvoudig rapporten voor niet-analisten) | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html) | Nee | Ja | Nee | Ja |  |  |  |
| **Project delen** | [Ja: alle/alle gebruikers](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html) | [Ja: alle/alle gebruikers](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/scheduling.html) | Ja: alle/alle gebruikers | Nee | Ja |  |  |  |
| **Geplande levering van rapport** | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/schedule-projects.html) | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/scheduling.html) | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/t-schedule-a-data-request.html) | Ja | Ja |  |  |  |
| **Systeemvereisten** | <br>[BrowserMeer...](https://docs.adobe.com/content/help/nl-NL/analytics/admin/sys-reqs.html) | <br>[BrowserMeer...](https://docs.adobe.com/content/help/nl-NL/analytics/admin/sys-reqs.html) | Windows, MS<br>[ExcelMore...](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | Browser en programma om .csv dossiers zoals MS Excel te openen. Kan bestanden in tableau-indeling genereren. | Windows 64-bits, goede grafische adapter voor OpenGL 3.2 [Meer...](https://docs.adobe.com/content/help/en/data-workbench/using/install/c-data-workbench-client-install.html) |  |  |  |
| **Compatibiliteit met Virtual Report Suite (rapporttijdverwerking)** | Ja | Ja | Ja | Nee | Ja? |  |  |  |
| **Meerdere rapportsets** | Ja | Nee | Nee | Nee | Ja? |  |  |  |
| **Berekende statistieken** | Ja | Ja | Ja | Ja | Ja |  |  |  |
| **Compatibiliteit met marketingkanalen** | Ja | Ja | Ja | ? | ? |  |  |  |
| **Korreligheid** |  |  |  |  |  |  |  |  |
| **Anomaliedetectie** | Ja | Nee |  |  |  |  |  |  |
| **Contributieanalyse** | Ja | Nee | Nee | Nee | Ja |  |  |  |
| **Segmenttypen** |  |  |  |  |  |  |  |  |