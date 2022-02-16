---
title: Te laat arriveren
description: Leer hoe de gegevensvoer laat aankomen klappen behandelt.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 1%

---

# Te laat arriveren

Historische gegevens kunnen worden aangeleverd nadat een gegevenfeed-taak een bepaald uur of een bepaalde dag is verwerkt, bijvoorbeeld door middel van treffers met een tijdstempel of gegevensbronnen. Te laat aankomen klappen is een backend aanpassingsplaatsen die door Adobe wordt verstrekt helpen deze gegevens in gegevensvoer omvatten.

## Hoe laat arriveren werkt

Wanneer een gegevensvoer normaal gegevens verwerkt, kijkt het slechts gegevens binnen zijn rapporterend venster (typisch het meest recente uur of de dag). Als gegevens worden ontvangen nadat een feed de verwerking van dat rapportagevenster heeft voltooid, worden die gegevens nooit opgenomen in gegevensinvoer.

Als hits laat aankomen ingeschakeld, verandert de verwerkingsmethode om deze gegevens op te nemen. Telkens wanneer een gegevensuitvoer gegevens verwerkt, wordt gekeken naar eventuele late hits en worden deze in batches opgeslagen in het volgende bestand voor gegevenstoevoer dat naar uw FTP-site wordt verzonden.

## Toelatend laat aankomende hits

Te laat aankomen klappen kunnen manueel door Adobe op individuele gegevensvoer worden toegelaten. Overweeg voordat u dit doet het volgende:

* Gegevens voor verschillende dagen worden vaak in gegevensfeeds weergegeven wanneer aanraakresultaten met late aankomst zijn ingeschakeld. Zorg ervoor dat het platform dat u gebruikt om gegevensfeeds in te voeren, gegevens van verschillende dagen in hetzelfde bestand kan bevatten.
* Te laat aankomen verhoogt verwerkingstijd. Deze vertraging is meestal minder dan een uur, maar kan meerdere uren of langer duren als uw rapportsuite een groot aantal late arriverende hits ontvangt. Adobe raadt aan deze instelling niet in te schakelen als tijdige aankomst voor gegevensfeeds noodzakelijk is voor de workflow van uw organisatie.
* Als een bestand met gegevensinvoer opnieuw wordt verwerkt, worden de late bereikresultaten die in het oorspronkelijke bestand zijn opgenomen, niet opgenomen in het opnieuw verwerkte bestand.

Als u laat aankomen hits voor een bestaande terugkerende gegevensfeed wilt inschakelen, dient u contact op te nemen met de klantenservice en de volgende informatie op te nemen:

* Een opmerking die u laat aankomen wilt inschakelen voor een specifieke gegevensfeed
* Set-id rapporteren
* Naam gegevensfeed
