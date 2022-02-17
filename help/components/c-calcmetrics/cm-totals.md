---
title: Totalen van berekende standaard
description: Leer hoe berekende metriettotalen verschillen in Analysesoftware
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 1%

---

# Totalen van berekende standaard

Hoe berekende metrische totalen worden getoond verschilt tussen [!DNL Reports & Analytics] en [!DNL Analysis Workspace]. In deze sectie worden de verschillen beschreven.

## Berekende metrische totalen in [!DNL Reports & Analytics]

Wanneer u rapporten bekijkt in [!DNL Reports & Analytics], berekende metriek altijd weergeven `n/a` onder het totaal. Aangezien alle berekende metriek user-defined zijn, zijn er vele omstandigheden waar dit totaal geen steek houdt. Bekijk het volgende voorbeeld:

Uw organisatie heeft berekend metrisch gecreeerd `orders` / `visits` om het percentage te bepalen van bezoeken dat iets op uw plaats kocht. Als u deze metrisch in een productrapport bracht, worden verscheidene producten toegeschreven aan één enkele orde. Verschillende producten worden aan één enkel bezoek toegeschreven. Indien in dit verslag een berekend metrisch totaal is opgenomen, rijzen de volgende vragen:

| Vraag | Antwoord |
|---|---|
| Is het zinvol om de lijstitems samen te vatten? | Dat gebeurt niet, omdat meerdere producten in één bestelling kunnen worden opgenomen en meerdere producten in één bezoek kunnen worden opgenomen. Indien de posten werden samengevoegd, zouden de totale bestellingen en de totale bezoeken niet overeenkomen met de werkelijke totale bestellingen en het totale aantal bezoeken. |
| Is het zinvol om totale bestellingen en totale bezoeken te nemen? | Dat gebeurt niet omdat het totaal niet overeenkomt met de som van de afzonderlijke regelitems. Daarnaast worden het totaal van de orders en het totaal van de bezoeken afzonderlijk berekend. |

Aangezien er geen logische en concrete methode is om te bepalen of een berekende metrische waarde in rapportering zinvol is, wordt het metrische totaal weggelaten. Als u een totaal wilt verkrijgen, kunt u een van de volgende handelingen uitvoeren:

* Creeer berekende metrisch die de Totale versies van de metriek omvat die u wilt omvatten.
* Creeer een rapport van het Uittreksel van Gegevens, dat kan worden gepland.
* Een gegevensverzoek maken binnen [!DNL ReportBuilder].
* Gebruiken [!DNL Analysis Workspace] (zie hieronder).

## Berekende metrische totalen in [!DNL Analysis Workspace]

Wanneer u gegevens in Analysis Workspace bekijkt, worden de berekende metrische totalen in de meeste gevallen getoond. In sommige gevallen is het niet mogelijk een totaal op te geven, bijvoorbeeld wanneer de rijen van het rapport een gemengd formaat hebben (bijvoorbeeld decimaal en valuta).

Wanneer totalen worden weergegeven, worden ze vaak berekend aan de serverzijde, wat betekent dat het totaal gegevens zoals bezoeken of bezoekers dedupliceert. Onder bepaalde omstandigheden worden berekende metriek aan de clientzijde gegenereerd door de rijen van de tabel bij elkaar op te tellen. Dit betekent dat het totaal metriek zoals bezoekers of bezoekers niet dedupliceert. Dit gebeurt:

* Wanneer [statische rijen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) worden gebruikt in Freeform-tabellen en de **[!UICONTROL Show as sum of current rows]** (standaard) is geselecteerd.
* In de [Donut visualisatie](/help/analyze/analysis-workspace/visualizations/donut.md), zodat getallen oplopen tot 100%.

Ga voor meer informatie over totalen in Analysis Workspace naar [Totalen werkruimte](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html?lang=en#static-row-total).
