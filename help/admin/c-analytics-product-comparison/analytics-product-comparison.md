---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Reports & Analytics, Ad hoc analysis, Report Builder, Data warehouse en Data Workbench
title: Analytics-productvergelijking en -vereisten
translation-type: tm+mt
source-git-commit: f3fa1cfd718339e58764bf4b39b07ccf2eae12c3
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 39%

---


# Analytics-productvergelijking en -vereisten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Reports &amp; Analytics, Report Builder, Data warehouse, Data Workbench, Data Feeds en Analytics API 2.0.

Ga [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)voor meer informatie over welk Adobe Analytics-product u wilt gebruiken.

| Productnaam en Help-koppeling | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Rapporten en Analytics](/help/analyze/reports-analytics/getting-started.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html) | [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **Toegangsmethode** | [Browser](/help/admin/sys-reqs.md) | [Browser](/help/admin/sys-reqs.md) | [MS Excel voor Windows](/help/analyze/report-builder/setup/system-requirements.md) | Opstelling door browser. [Meer informatie](/help/admin/sys-reqs.md) | [Windows 64-bits](https://docs.adobe.com/content/help/en/data-workbench/using/install/c-data-workbench-client-install.html) | Opstelling door browser. [Meer informatie](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API-gereedschappen. Aanmelden met Adobe I/O-referenties. [Meer informatie](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| **Korreligheid gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Actief | Samengevoegd |
| **Extension Cloud ID (ECID) beschikbaar** | Nee | Nee | Nee | Ja | Ja | Ja | Nee |
| **Tijdstempel beschikbaar** | Nee | Nee | Nee | Nee | Ja | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig verwerkt, met apart [real-time rapport](/help/components/c-real-time-reporting/realtime.md) | Volledig verwerkt, met apart [real-time rapport](/help/components/c-real-time-reporting/realtime.md) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Gegevens van het filter Admin bot inbegrepen** <br> [Meer informatie](/help/admin/admin/bot-removal/bot-removal.md) | Nee | Ja, afzonderlijke beide rapporten | Ja, afzonderlijke beide rapporten | Nee | Nee | Nee | Nee |
| **Laag verkeer (Uniques overschreden) verschijnt** <br> [Meer informatie](/help/technotes/low-traffic.md) | Ja | Ja | Ja | Nee | Nee | Nee | Ja |
| **Zichtbare rijlimiet (vóór paginering)** | 400 | 200 | 50000 | Onbeperkt | Onbeperkt | Onbeperkt | 50000 |
| **Meerdere rapportsuites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja, met beperkingen | Ja | Nee | Ja | Nee | Ja |
| **Aantal uitsplitsingen** | Onbeperkt | Maximaal 2 | Maximaal 2 | Onbeperkt | Onbeperkt | Onbeperkt | Onbeperkt, uitvoeren op meerdere query&#39;s |
| **Segmentatie** <br> [Meer informatie](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja | Ja, met [beperkingen](/help/components/c-segmentation/seg-reference/seg-compatibility.md) | Ja | Nee | Ja |
| **Berekende standaarden** <br> [Meer informatie](/help/components/c-calcmetrics/cm-overview.md) | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Ja | Ja | Nee | Ja | Nee | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketingkanalen** <br> [Meer informatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja | Ja | Ja - [va_finder, va_near](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Cohortanalyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Nee | Nee | Nee | Ja | Nee | Nee |
| **Attributie** | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) | Beperkt | Beperkt | Nee | Ja | Nee | Ja, met [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Functies van Virtual Analyst** <br> [Meer informatie](/help/analyze/analysis-workspace/virtual-analyst/overview.md) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
| **Kromming** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Project en vrijwillige VUT | Nee | Nee | Nee | Nee | Nee | Ja - alleen VRS |
| **Projectdeling** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, met projectrollen | Ja | Ja | Nee | Ja | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee | Ja | Nee |
| **Leveringsbestemmingen** | E-mail | E-mail | E-mail, FTP, SFTP, [publiceren naar Microsoft PowerBI](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | E-mail, FTP. Neem contact op met de klantenservice voor extra bestemmingsondersteuning, zoals SFTP, Azure Blob, Amazon S3 | - | FTP, SFTP, Azure Blob, Amazon S3 | - |
| **Tijdverwerking van VRS-rapport** <br> [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
