---
title: Berekende totalen van metriek
description: Meer informatie over berekende totalen in Analysis Workspace
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Berekende totalen van metriek in Analysis Workspace

Wanneer u gegevens in Analysis Workspace bekijkt, worden de berekende metrische totalen in de meeste gevallen getoond. In sommige gevallen is het niet mogelijk een totaal op te geven, bijvoorbeeld wanneer de rijen van het rapport een gemengd formaat hebben (bijvoorbeeld decimaal en valuta).

Wanneer totalen worden weergegeven, worden ze vaak berekend aan de serverzijde, wat betekent dat het totaal gegevens zoals bezoeken of bezoekers dedupliceert. Onder bepaalde omstandigheden worden berekende metriek aan de clientzijde gegenereerd door de rijen van de tabel bij elkaar op te tellen. Dit betekent dat het totaal metriek zoals bezoekers of bezoekers niet dedupliceert. Dit gebeurt:

* Wanneer [statische rijen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) worden gebruikt in Freeform-tabellen en de **[!UICONTROL Show as sum of current rows]** (standaard) is geselecteerd.
* In de [Donut visualisatie](/help/analyze/analysis-workspace/visualizations/donut.md), zodat getallen oplopen tot 100%.

Ga voor meer informatie over totalen in Analysis Workspace naar [Totalen werkruimte](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html?lang=nl-NL#static-row-total).
