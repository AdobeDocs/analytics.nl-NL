---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Reports & Analytics, Report Builder, Data Warehouse en Data Workbench
title: Analyse van productvergelijking en vereisten
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 17%

---

# Analyse van productvergelijking en vereisten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Report Builder, Data Warehouse, Data Feeds en Analytics API 2.0.

Voor informatie over welk Adobe Analytics-product u moet gebruiken, raadpleegt u [Welk Adobe Analytics-gereedschap moet ik gebruiken?](/help/analyze/get-started/which-analytics-tool.md).

| Productnaam en Help-koppeling | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analyse API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **Toegangsmethode** | [Browser](/help/analyze/get-started/sys-reqs.md) | [MS Excel voor Windows](/help/analyze/report-builder/setup/system-requirements.md) | Opstelling door browser. [Meer informatie](/help/analyze/get-started/sys-reqs.md) | Opstelling door browser. [Meer informatie](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API-gereedschappen. Aanmelden met Adobe Developer-referenties. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **Korreligheid gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Samengevoegd |
| **Experience Cloud-id (ECID) beschikbaar** | Nee | Nee | Ja | Ja | Nee |
| **Tijdstempel beschikbaar** | Nee | Nee | Nee | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig verwerkt, met aparte [real-time rapport](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Gegevens van het filter Admin bot inbegrepen** <br> [Meer informatie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md) | Nee | Ja, afzonderlijke beide rapporten | Nee | Nee | Nee |
| **Laag verkeer (Uniques overschreden) wordt weergegeven** <br> [Meer informatie](/help/technotes/low-traffic.md) | Ja | Ja | Nee | Nee | Ja |
| **Zichtbare rijlimiet (vóór paginering)** | 400 | 50000 | Onbeperkt | Onbeperkt | 50000 |
| **Meerdere rapportsuites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja | Nee | Ja | Nee | Ja |
| **Aantal uitsplitsingen** | Onbeperkt | Maximaal 2 | Onbeperkt | Onbeperkt | Onbeperkt, uitvoeren op meerdere query&#39;s |
| **Segmentering** <br> [Meer informatie](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja, met [beperkingen](/help/components/segmentation/seg-reference/seg-compatibility.md) | Nee | Ja |
| **Berekende cijfers** <br> [Meer informatie](/help/components/c-calcmetrics/cm-overview.md) | Ja, met [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) | Ja, met kenmerk | Ja | Nee | Ja, met [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketingkanalen** <br> [Meer informatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja - [va_finder, va_near](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Cohortanalyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Ja | Nee | Nee | Nee |
| **Attributie** | Ja, met [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) | Beperkt | Nee | Nee | Ja, met [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) | Nee |
| **Kromming** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Project en Virtual Report Suite | Nee | Nee | Nee | Ja - alleen Virtual Report Suite |
| **Projectdeling** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, met projectrollen | Ja | Nee | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee |
| **Leveringsbestemmingen** | E-mail | E-mail, FTP, SFTP [publiceren naar Microsoft PowerBI](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC en Email | Amazon S3, Azure RBAC, Azure SAS en Google Cloud Platform | - |
| **Rapporttijdverwerking van virtuele rapportsuite** <br> [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nee | Nee | Nee | Ja |
