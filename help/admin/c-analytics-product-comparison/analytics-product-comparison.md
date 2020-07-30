---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Reports & Analytics, Ad hoc analysis, Report Builder, Data warehouse en Data Workbench
title: Analytics-productvergelijking en -vereisten
translation-type: tm+mt
source-git-commit: 54d6b4c2993c5b0391b9243c76661db1da4087b8
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 35%

---


# Analytics-productvergelijking en -vereisten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Reports &amp; Analytics, Report Builder, Data warehouse, Data Workbench, Data Feeds en Analytics API 2.0.

Ga [hier](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)voor meer informatie over welk Adobe Analytics-product u wilt gebruiken.

| Productnaam en Help-koppeling | [Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) | [Rapporten en Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/getting-started.html) | [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html) | [Gegevensfeeds](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **Toegangsmethode** | [Browser](https://docs.adobe.com/content/help/nl-NL/analytics/admin/sys-reqs.html) | [Browser](https://docs.adobe.com/content/help/nl-NL/analytics/admin/sys-reqs.html) | [MS Excel voor Windows](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | Opstelling door browser. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/admin/sys-reqs.html) | [Windows 64-bits](https://docs.adobe.com/content/help/en/data-workbench/using/install/c-data-workbench-client-install.html) | Opstelling door browser. [Meer informatie](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html) | RESTful API-gereedschappen. Aanmelden met Adobe I/O-referenties. [Meer informatie](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| **Korreligheid gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Actief | Samengevoegd |
| **Extension Cloud ID (ECID) beschikbaar** | Nee | Nee | Nee | Ja | Ja | Ja | Nee |
| **Tijdstempel beschikbaar** | Nee | Nee | Nee | Nee | Ja | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig verwerkt, met apart [real-time rapport](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | Volledig verwerkt, met apart [real-time rapport](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Gegevens van het filter Admin bot zijn opgenomen** Meer <br>[informatie](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/bot-removal/bot-removal.html) | Nee | Ja, afzonderlijke beide rapporten | Ja, afzonderlijke beide rapporten | Nee | Nee | Nee | Nee |
| **Laag verkeer (Uniques overschreden) verschijnt** Meer <br>[informatie](https://docs.adobe.com/content/help/en/analytics/technotes/low-traffic.html) | Ja | Ja | Ja | Nee | Nee | Nee | Ja |
| **Zichtbare rijlimiet (vóór paginering)** | 400 | 200 | 50000 | Onbeperkt | Onbeperkt | Onbeperkt | 50000 |
| **Meerdere rapportsuites** | [Ja](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html) | Ja, met beperkingen | Ja | Nee | Ja | Nee | Ja |
| **Aantal uitsplitsingen** | Onbeperkt | Maximaal 2 | Maximaal 2 | Onbeperkt | Onbeperkt | Onbeperkt | Onbeperkt, uitvoeren op meerdere query&#39;s |
| **Segmentatie** <br>[Meer informatie](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-workflow.html) | Ja | Ja | Ja | Ja, met [beperkingen](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segment-reference/seg-compatibility.html) | Ja | Nee | Ja |
| **Berekende cijfers** <br>[Meer weten](https://docs.adobe.com/content/help/nl-NL/analytics/components/calculated-metrics/cm-overview.html) | Ja, met [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | Ja | Ja | Nee | Ja | Nee | Ja, met [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **Marketingkanalen** <br>[Meer informatie](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-getting-started-mchannel.html) | Ja | Ja | Ja | Ja | Ja | Ja - [va_finder, va_near](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html) | Ja |
| **Cohortanalyse** | [Ja](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | Nee | Nee | Nee | Ja | Nee | Nee |
| **Attributie** | Ja, met [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | Beperkt | Beperkt | Nee | Ja | Nee | Ja, met [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **Functies** van Virtual Analyst <br>[Meer informatie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/overview.html) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
| **Cursus** <br>[Meer informatie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html) | Ja - Project en vrijwillige VUT | Nee | Nee | Nee | Nee | Nee | Ja - alleen VRS |
| **Projectdeling** <br>[Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/curate-share/share-projects.html) | Ja, met projectrollen | Ja | Ja | Nee | Ja | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee | Ja | Nee |
| **Leveringsbestemmingen** | E-mail | E-mail | E-mail, FTP, SFTP, [publiceren naar Microsoft PowerBI](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/publish-powerbi/power-bi.html) | E-mail, FTP. Neem contact op met de klantenservice voor extra bestemmingsondersteuning, zoals SFTP, Azure Blob, Amazon S3 | - | FTP, SFTP, Azure Blob, Amazon S3 | - |
| **Tijdverwerking** van VRS-rapport <br>[Meer informatie](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-report-time-processing.html) | Ja | Nee | Nee | Nee | Nee | Nee | Ja |
