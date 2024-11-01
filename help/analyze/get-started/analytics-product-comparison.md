---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Report Builder, Data Warehouse en Data Workbench
title: Analyse van productvergelijking en vereisten
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: 16046af6b7a78bdc4bfaf7e5ec7d05c55f2ebc01
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 17%

---

# Analyse van productvergelijking en vereisten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Report Builder, Data Warehouse, Data Feeds en Analytics API 2.0.

Voor informatie over welk product van Adobe Analytics te gebruiken, zie [ Welk hulpmiddel van Adobe Analytics zou moeten ik gebruiken?](/help/analyze/get-started/which-analytics-tool.md).

| Productnaam en Help-koppeling | [ Analysis Workspace ](/help/analyze/analysis-workspace/home.md) | [ Report Builder ](/help/analyze/report-builder/report-buider-overview.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) | [ Analytics API 2.0 ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **methode van de Toegang** | [Browser](/help/analyze/get-started/sys-reqs.md) | [ MS Excel voor Vensters ](/help/analyze/legacy-report-builder/setup/system-requirements.md) | Opstelling door browser. [Meer informatie](/help/analyze/get-started/sys-reqs.md) | Opstelling door browser. [Meer informatie](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API-gereedschappen. Aanmelden met Adobe Developer-referenties. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **granulariteit van Gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Samengevoegd |
| **beschikbare identiteitskaart van het Experience Cloud (ECID)** | Nee | Nee | Ja | Ja | Nee |
| **beschikbare Tijdstempel van 0}** | Nee | Nee | Nee | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig-verwerkt, met afzonderlijk [ rapport in real time ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Admin bot filtergegevens inbegrepen** <br> [Meer informatie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md) | Nee | Ja, afzonderlijke beide rapporten | Nee | Nee | Nee |
| **Laag verkeer (Uniques overschreden) verschijnt** <br> [Meer informatie](/help/technotes/low-traffic.md) | Ja | Ja | Nee | Nee | Ja |
| **Zichtbare rijgrens (vóór paginering)** | 400 | 50000 | Onbeperkt | Onbeperkt | 50000 |
| **Veelvoudige rapportsuites** | [ ja ](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja | Nee | Ja | Nee | Ja |
| **Aantal onderbrekingen** | Onbeperkt | Maximaal 2 | Onbeperkt | Onbeperkt | Onbeperkt, uitvoeren op meerdere query&#39;s |
| **Segmentatie** <br> [Meer informatie](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja, met [ beperkingen ](/help/components/segmentation/seg-reference/seg-compatibility.md) | Nee | Ja |
| **Berekende metriek** <br> [Meer informatie](/help/components/c-calcmetrics/cm-overview.md) | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) | Ja, met kenmerk | Ja | Nee | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **de Kanalen van de Marketing** <br> [Meer informatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja - [ va_finder, va_near ](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **de analyse van de Cohort** | [ ja ](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Ja | Nee | Nee | Nee |
| **Attributie** | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) | Beperkt | Nee | Nee | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) | Nee |
| **Kromming** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Project en Virtual Report Suite | Nee | Nee | Nee | Ja - alleen Virtual Report Suite |
| **Project delend** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, met projectrollen | Ja | Nee | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee |
| **de bestemmingen van de Levering** | E-mail | E-mail, FTP, SFTP, [ het publiceren aan Microsoft PowerBI ](/help/analyze/legacy-report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC en Email | Amazon S3, Azure RBAC, Azure SAS en Google Cloud Platform | - |
| **Virtuele het tijdverwerking van het rapport van de rapportreeks van de rapportreeks** <br> [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nee | Nee | Nee | Ja |
