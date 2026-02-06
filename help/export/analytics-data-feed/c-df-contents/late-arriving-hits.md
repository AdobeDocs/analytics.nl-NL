---
title: Te laat aankomende treffers
description: Leer hoe de gegevensvoer laat-aankomende klappen behandelt.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 4d0007d1a23a81f0d5ba60541b4f7b9ac7b00ace
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Te laat arriveren {#late-arriving-hits}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_late_hits"
>title="Te laat aankomen toestaan"
>abstract="Selecteer deze optie om gegevens op te nemen die zijn ontvangen nadat de gegevensinvoertaak de gegevens heeft verwerkt binnen de ingestelde rapportagefrequentie (gewoonlijk dagelijks of per uur). Als deze optie is ingeschakeld, controleert elke keer dat een gegevensfeed gegevens verwerkt, de late resultaten die zijn binnengekomen en worden deze in batches opgeslagen met het volgende gegevensdoorvoerbestand dat wordt verzonden."

<!-- markdownlint-enable MD034 -->

## Begrijp laat aankomende klappen

Historische gegevens kunnen worden aangeleverd nadat een gegevenfeed-taak een bepaald uur of een bepaalde dag is verwerkt, bijvoorbeeld door middel van treffers met een tijdstempel of gegevensbronnen.

Wanneer een gegevensvoer normaal gegevens verwerkt, kijkt het slechts gegevens binnen zijn rapporterend venster (typisch het meest recente uur of de dag). Als gegevens worden ontvangen nadat een feed de verwerking van dat rapportagevenster heeft voltooid, worden die gegevens nooit opgenomen in gegevensinvoer.

Als klapresultaten op het laatste moment zijn ingeschakeld, wordt de verwerkingsmethode gewijzigd en worden deze gegevens opgenomen. Telkens als een gegevensuitvoer gegevens verwerkt, kijkt het naar om het even welke late klappen die zijn gearriveerd en partijen hen in het volgende dossier van de gegevensvoer die wordt verzonden.

## Te laat aankomen hits inschakelen

Overweeg het volgende voordat u de optie inschakelt waarmee aanraakproblemen met late invoer voor een gegevensfeed worden toegestaan:

* Gegevens voor verschillende dagen worden vaak in gegevensfeeds weergegeven wanneer aanraakresultaten met late afgifte zijn ingeschakeld. Zorg ervoor dat het platform dat u gebruikt om gegevensfeeds in te voeren, gegevens van verschillende dagen in hetzelfde bestand kan bevatten.
* Als een bestand met gegevensinvoer opnieuw wordt verwerkt, worden de treffers die pas na aankomst in het oorspronkelijke bestand zijn opgenomen, opgenomen in het opnieuw verwerkte bestand wanneer de eerste vijf dagen na de verwerking opnieuw worden verwerkt. Na 5 dagen worden treffers die te laat aankomen niet meer opgenomen in het opnieuw verwerkte bestand.

U kunt laat-aankomstgeluiden toelaten wanneer het creëren van of het uitgeven van een gegevensvoer door de optie, **[!UICONTROL Allow late-arriving hits]** toe te laten, zoals die in [&#x200B; wordt beschreven creeer een gegevensvoer &#x200B;](/help/export/analytics-data-feed/create-feed.md).
