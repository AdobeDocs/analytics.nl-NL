---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Reports & Analytics, Report Builder, Data Warehouse en Data Workbench
title: Analytics-productvergelijking en -vereisten
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: 0017a6657e4de6206cf97dc6cf6f2b132b50b50f
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 36%

---

# Analytics-productvergelijking en -vereisten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Reports &amp; Analytics, Report Builder, Data Warehouse, Data Workbench, Data Feeds en Analytics API 2.0.

Voor informatie over welk Adobe Analytics-product u moet gebruiken, raadpleegt u [Welk Adobe Analytics-gereedschap moet ik gebruiken?](/help/admin/get-started/which-analytics-tool.md).

| Productnaam en Help-koppeling | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Rapporten en analyses](/help/analyze/reports-analytics/getting-started.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/home.html) | [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analyse API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **Toegangsmethode** | [Browser](/help/admin/get-started/sys-reqs.md) | [Browser](/help/admin/get-started/sys-reqs.md) | [MS Excel voor Windows](/help/analyze/report-builder/setup/system-requirements.md) | Opstelling door browser. [Meer informatie](/help/admin/get-started/sys-reqs.md) | [Windows 64-bits](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html) | Opstelling door browser. [Meer informatie](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API-gereedschappen. Aanmelden met Adobe Developer-referenties. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **Korreligheid gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Actief | Samengevoegd |
| **Experience Cloud-id (ECID) beschikbaar** | Nee | Nee | Nee | Ja | Ja | Ja | Nee |
| **Tijdstempel beschikbaar** | Nee | Nee | Nee | Nee | Ja | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig verwerkt, met aparte [real-time rapport](/help/components/c-real-time-reporting/realtime.md) | Volledig verwerkt, met aparte [real-time rapport](/help/components/c-real-time-reporting/realtime.md) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Gegevens van het filter Admin bot inbegrepen** <br> [Meer informatie](/help/admin/admin/bot-removal/bot-removal.md) | Nee | Ja, afzonderlijke beide rapporten | Ja, afzonderlijke beide rapporten | Nee | Nee | Nee | Nee |
| **Laag verkeer (Uniques overschreden) verschijnt** <br> [Meer informatie](/help/technotes/low-traffic.md) | Ja | Ja | Ja | Nee | Nee | Nee | Ja |
| **Zichtbare rijlimiet (vóór paginering)** | 400 | 200 | 50000 | Onbeperkt | Onbeperkt | Onbeperkt | 50000 |
| **Meerdere rapportsuites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja, met beperkingen | Ja | Nee | Ja | Nee | Ja |
| **Aantal uitsplitsingen** | Onbeperkt | Maximaal 2 | Maximaal 2 | Onbeperkt | Onbeperkt | Onbeperkt | Onbeperkt, uitvoeren op meerdere query&#39;s |
| **Segmentatie** <br> [Meer informatie](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja | Ja, met [beperkingen](/help/components/segmentation/seg-reference/seg-compatibility.md) | Ja | Nee | Ja |
| **Berekende standaarden** <br> [Meer informatie](/help/components/c-calcmetrics/cm-overview.md) | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Ja | Ja | Nee | Ja | Nee | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketingkanalen** <br> [Meer informatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja | Ja | Ja - [va_finder, va_near](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Cohortanalyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Nee | Nee | Nee | Ja | Nee | Nee |
| **Attributie** | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Beperkt | Beperkt | Nee | Ja | Nee | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Functies van Virtual Analyst** <br> [Meer informatie](/help/analyze/analysis-workspace/virtual-analyst/overview.md) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
| **Kromming** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Project en vrijwillige VUT | Nee | Nee | Nee | Nee | Nee | Ja - alleen VRS |
| **Projectdeling** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, met projectrollen | Ja | Ja | Nee | Ja | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee | Ja | Nee |
| **Leveringsbestemmingen** | E-mail | E-mail | E-mail, FTP, SFTP [publiceren naar Microsoft PowerBI](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | E-mail, FTP. Neem contact op met de klantenservice voor extra bestemmingsondersteuning, zoals SFTP, Azure Blob, Amazon S3 | - | FTP, SFTP, Azure Blob, Amazon S3 | - |
| **Tijdverwerking van VRS-rapport** <br> [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
