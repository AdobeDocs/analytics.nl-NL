---
title: Berekende totalen van metriek
description: Meer informatie over berekende totalen in Analysis Workspace
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Berekende totalen van metriek

Wanneer u gegevens in Analysis Workspace bekijkt, worden de berekende metrische totalen in de meeste gevallen getoond. In sommige gevallen is het niet mogelijk een totaal op te geven, bijvoorbeeld wanneer de rijen van het rapport een gemengd formaat hebben (bijvoorbeeld decimaal en valuta).

Wanneer totalen worden weergegeven, worden ze vaak berekend aan de serverzijde, wat betekent dat het totaal gegevens zoals bezoeken of bezoekers dedupliceert. Onder bepaalde omstandigheden worden berekende metriek aan de clientzijde gegenereerd door de rijen van de tabel bij elkaar op te tellen. Dit betekent dat het totaal metriek zoals bezoekers of bezoekers niet dedupliceert. Dit gebeurt:

* Wanneer [&#x200B; statische rijen &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) in Freeform lijsten worden gebruikt en de **[!UICONTROL Show as sum of current rows]** optie (gebrek) wordt geselecteerd.
* In de [&#x200B; visualisatie van de Donut &#x200B;](/help/analyze/analysis-workspace/visualizations/donut.md), zodat de aantallen tot 100% toevoegen.

Voor meer informatie over totalen in Analysis Workspace, bezoek [&#x200B; totalen van Workspace &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md#static-row-total).
