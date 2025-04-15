---
description: Systeemvereisten en een vergelijking van Analysis Workspace, Report Builder, Data Warehouse en Data Workbench
title: Vergelijking en vereisten van Analytics-producten
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: 9a2d4c582b6a3946b658924851e5b5ada2f5a7ee
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 17%

---

# Vergelijking en vereisten van Analytics-producten

Deze pagina bevat een vergelijking van verschillende Adobe Analytics-producten: Analysis Workspace, Report Builder, Data Warehouse, Data Feeds en Analytics API 2.0.

Voor informatie over welk Adobe Analytics-product ik moet gebruiken, zie [Welke Adobe Analytics-tool moet ik gebruiken?](/help/analyze/get-started/which-analytics-tool.md).

| Productnaam en Help-link | [Werkruimte Analyse](/help/analyze/analysis-workspace/home.md) | [Rapport Builder](/help/analyze/report-builder/rb-overview.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytische API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **Methode voor toegang** | [Browser](/help/analyze/get-started/sys-reqs.md) | [MS Excel voor Windows](/help/analyze/legacy-report-builder/setup/system-requirements.md) | Instellen via de browser. [Meer informatie](/help/analyze/get-started/sys-reqs.md) | Instellen via de browser. [Meer informatie](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API-hulpmiddelen. Meld u aan met Adobe Developer-gegevens. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **granulariteit van Gegevens** | Samengevoegd | Samengevoegd | Samengevoegd | Actief | Samengevoegd |
| **beschikbare identiteitskaart van Experience Cloud (ECID)** | Nee | Nee | Ja | Ja | Nee |
| **Tijdstempel beschikbaar** | Nee | Nee | Nee | Ja | Nee |
| **Niveau van verwerking** | Volledig verwerkt | Volledig verwerkt, met apart [real-time rapport](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) | Volledig verwerkt | Volledig verwerkt | Volledig verwerkt |
| **Admin-botfiltergegevens inbegrepen** <br> [Meer informatie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md) | Nee | Ja - afzonderlijk botrapport | Nee | Nee | Nee |
| **Weinig verkeer (Uniques overschreden) verschijnt** <br> [Meer informatie](/help/technotes/low-traffic.md) | Ja | Ja | Nee | Nee | Ja |
| **Zichtbare rijlimiet (vóór paginering)** | 400 | 50000 | Onbegrensd | Onbegrensd | 50000 |
| **Meerdere rapportsuites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja | Nee | Ja | Nee | Ja |
| **Aantal storingen** | Onbegrensd | Maximaal 2 | Onbegrensd | Onbegrensd | Onbeperkt, voer meerdere query&#39;s uit |
| **Segmentatie** <br> [Meer informatie](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja, met [ beperkingen ](/help/components/segmentation/seg-reference/seg-compatibility.md) | Nee | Ja |
| **Berekende metriek** <br> [Meer informatie](/help/components/c-calcmetrics/cm-overview.md) | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) | Ja, met kenmerk | Ja | Nee | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) |
| **de Kanalen van de Marketing** <br> [Meer informatie](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja - [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **de analyse van de Cohort** | [ ja ](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Ja | Nee | Nee | Nee |
| **Attributie** | Ja, met [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) | Beperkt | Nee | Nee | Ja, met [Attributie](/help/analyze/analysis-workspace/attribution/overview.md) | Nee |
| **Curatie** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja - Project- en virtuele rapportsuite | Nee | Nee | Nee | Ja - Alleen virtuele rapportsuite |
| **Projecten delen** <br> [Meer informatie](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, met projectrollen | Ja | Nee | Nee | Nee |
| **Geplande levering** | Ja | Ja | Ja | Ja | Nee |
| **Bestemmingen voor bezorging** | E-mail | E-mail, FTP, SFTP, [publiceren naar Microsoft PowerBI](/help/analyze/legacy-report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC en e-mail | Amazon S3, Azure RBAC, Azure SAS en Google Cloud Platform | - |
| **Verwerking van rapporttijd** in virtuele rapportsuite <br> [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nee | Nee | Nee | Ja |
