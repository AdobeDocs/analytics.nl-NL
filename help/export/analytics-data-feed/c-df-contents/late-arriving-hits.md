---
title: Te laat arriveren
description: Leer hoe de gegevensvoer laat aankomen klappen behandelt.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 5816868d3899d2938330471d1e59757141b16c69
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Te laat arriveren {#late-arriving-hits}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_late_hits"
>title="Te laat aankomen toestaan"
>abstract="Selecteer deze optie om gegevens op te nemen die zijn ontvangen nadat de gegevensinvoertaak de gegevens heeft verwerkt binnen de ingestelde rapportfrequentie (dagelijks, om het uur of om de 15 minuten). Als deze optie is ingeschakeld, controleert elke keer dat een gegevensfeed gegevens verwerkt, de late resultaten die zijn binnengekomen en worden deze in batches opgeslagen met het volgende gegevensdoorvoerbestand dat wordt verzonden."

<!-- markdownlint-enable MD034 -->

Historische gegevens kunnen worden aangeleverd nadat een gegevenfeed-taak een bepaald uur of een bepaalde dag is verwerkt, bijvoorbeeld door middel van treffers met een tijdstempel of gegevensbronnen. Te laat aankomen klappen is een backend aanpassingsinstelling die door Adobe wordt verstrekt helpen deze gegevens in gegevensvoer omvatten.

## Hoe laat arriveren werkt

Wanneer een gegevensvoer normaal gegevens verwerkt, kijkt het slechts gegevens binnen zijn rapporterend venster (typisch het meest recente uur of de dag). Als gegevens worden ontvangen nadat een feed de verwerking van dat rapportagevenster heeft voltooid, worden die gegevens nooit opgenomen in gegevensinvoer.

Als hits laat aankomen ingeschakeld, verandert de verwerkingsmethode om deze gegevens op te nemen. Telkens wanneer een gegevensuitvoer gegevens verwerkt, wordt gekeken naar eventuele late hits en worden deze in batches opgeslagen in het volgende bestand voor gegevenstoevoer dat naar uw FTP-site wordt verzonden.

## Toelatend laat aankomende hits

Te laat aankomen klappen kunnen door Adobe manueel op individuele gegevensvoer worden toegelaten. Overweeg voordat u dit doet het volgende:

* Gegevens voor verschillende dagen worden vaak in gegevensfeeds weergegeven wanneer aanraakresultaten met late aankomst zijn ingeschakeld. Zorg ervoor dat het platform dat u gebruikt om gegevensfeeds in te voeren, gegevens van verschillende dagen in hetzelfde bestand kan bevatten.
* Als een gegevensdoorvoerbestand opnieuw wordt verwerkt, worden de late arriverende resultaten die in het oorspronkelijke bestand zijn opgenomen, opgenomen in het opnieuw verwerkte bestand wanneer de eerste vijf dagen de gegevens opnieuw worden verwerkt. Na 5 dagen worden treffers die te laat aankomen niet meer opgenomen in het opnieuw verwerkte bestand.

Als u laat aankomen hits voor een bestaande terugkerende gegevensfeed wilt inschakelen, dient u contact op te nemen met de klantenservice en de volgende informatie op te nemen:

* Een opmerking die u laat aankomen wilt inschakelen voor een specifieke gegevensfeed
* Reeks-id rapporteren
* Naam gegevensfeed
