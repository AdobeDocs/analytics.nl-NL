---
title: Berekende totalen van metriek
description: Leer hoe berekende metriettotalen verschillen in Analysesoftware
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Berekende totalen van metriek

Hoe berekende metrische totalen worden getoond verschilt tussen [!DNL Reports & Analytics] en [!DNL Analysis Workspace]. In deze sectie worden de verschillen beschreven.

## Berekende metrische totalen in [!DNL Reports & Analytics]

Wanneer u rapporten in bekijkt [!DNL Reports & Analytics], tonen de berekende metriek altijd `n/a` onder het totaal. Aangezien alle berekende metriek user-defined zijn, zijn er vele omstandigheden waar dit totaal geen steek houdt. Bekijk het volgende voorbeeld:

Uw organisatie heeft de berekende metrisch `orders` / `visits` gecreeerd om het percentage bezoeken te bepalen dat iets op uw plaats kocht. Als u deze metrisch in een productrapport bracht, worden verscheidene producten toegeschreven aan één enkele orde. Verschillende producten worden aan één enkel bezoek toegeschreven. Indien in dit verslag een berekend metrisch totaal is opgenomen, rijzen de volgende vragen:

| Vraag | Antwoord |
|---|---|
| Is het zinvol om de lijstitems samen te vatten? | Dat gebeurt niet, omdat meerdere producten in één bestelling kunnen worden opgenomen en meerdere producten in één bezoek kunnen worden opgenomen. Indien de posten werden samengevoegd, zouden de totale bestellingen en de totale bezoeken niet overeenkomen met de werkelijke totale bestellingen en het totale aantal bezoeken. |
| Is het zinvol om totale bestellingen en totale bezoeken te nemen? | Dat gebeurt niet omdat het totaal niet overeenkomt met de som van de afzonderlijke regelitems. Daarnaast worden het totaal van de orders en het totaal van de bezoeken afzonderlijk berekend. |

Aangezien er geen logische en concrete methode is om te bepalen of een berekende metrische waarde in rapportering zinvol is, wordt het metrische totaal weggelaten. Als u een totaal wilt verkrijgen, kunt u een van de volgende handelingen uitvoeren:

* Creeer berekende metrisch die de Totale versies van de metriek omvat die u wilt omvatten.
* Creeer een rapport van het Uittreksel van Gegevens, dat kan worden gepland.
* Maak een gegevensaanvraag binnen [!DNL ReportBuilder].
* Gebruik [!DNL Analysis Workspace] (zie hieronder).

## Berekende metrische totalen in [!DNL Analysis Workspace]

Wanneer u gegevens in de Werkruimte van de Analyse bekijkt, worden de berekende metrische totalen getoond in de meeste gevallen. In sommige gevallen is het niet mogelijk een totaal op te geven, bijvoorbeeld wanneer de rijen van het rapport een gemengd formaat hebben (bijvoorbeeld decimaal en valuta).

Wanneer totalen worden weergegeven, worden ze vaak berekend aan de serverzijde, wat betekent dat het totaal gegevens zoals bezoeken of bezoekers dedupliceert. Onder bepaalde omstandigheden worden berekende metriek aan de clientzijde gegenereerd door de rijen van de tabel bij elkaar op te tellen. Dit betekent dat het totaal metriek zoals bezoekers of bezoekers niet dedupliceert. Dit gebeurt:

* Wanneer [statische rijen](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) worden gebruikt in Freeform-tabellen en de **[!UICONTROL Show as sum of current rows]** optie (standaard) is geselecteerd.
* In de [Donut-visualisatie](/help/analyze/analysis-workspace/visualizations/donut.md), zodat de aantallen tot 100% in elkaar optellen.
