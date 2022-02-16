---
title: Componentondersteuning in Data Warehouse
description: Leer welke extra afmetingen en metriek in Data Warehouse beschikbaar zijn en wat niet wordt gesteund.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 4%

---

# Componentondersteuning in Data Warehouse

De unieke verwerkingsarchitectuur van Data Warehouse staat sommige componenten toe die typisch niet beschikbaar in andere mogelijkheden van Adobe Analytics zijn. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor Data Warehouse

Sommige dimensies en maatstaven kunnen in de Data Warehouse worden gebruikt, maar zijn niet beschikbaar met behulp van andere mogelijkheden in Adobe Analytics.

### uitsluitend ondersteunde Dimension

* Experience Cloud-id: Voor implementaties die de Dienst van identiteitskaart van de Experience Cloud (ECID) gebruiken, een aantal met 128 bits dat uit twee samengevoegde aantallen bestaat met 64 bits die aan 19 cijfers worden toegevoegd.
* Pagina-URL: De pagina-URL waarop de treffer heeft plaatsgevonden.
* Aankoop-id&#39;s: Unieke id voor een aankoop, ingesteld met de variabele purchaseID.
* Bezoeker-id: Verschaft de unieke id voor de bezoeker. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [Referentie gegevenskolom](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder Gegevensfeeds voor meer informatie.

### Uitsluitend ondersteunde cijfers

* Bezoeken: Deze meetmethode in het kader van Data Warehouse sluit niet-permanente cookiebezoeken uit.
* Bezoeken - Alle bezoekers: Deze metrische waarde in de context van Data Warehouse heeft een grotere pariteit met de bezoeken metrisch in andere hulpmiddelen binnen Adobe Analytics.

## Componenten niet ondersteund in Data Warehouse

Sommige dimensies en metriek worden niet ondersteund in Data Warehouse.

>[!NOTE]
>
>Als een afmeting of metrisch niet in Data Warehouse wordt gesteund, worden de segmenten die deze componenten gebruiken ook niet gesteund. Controleer altijd de productcompatibiliteit wanneer u een segment maakt of bewerkt.

### Dimension niet ondersteund

* Sommige op tijd gebaseerde afmetingen, zoals:
   * AM/PM
   * Dag van Maand
   * Weekdag
   * Dag van het Jaar
   * Uur van dag
   * Minuut
   * Maand van jaar
   * Kwartaal van jaar
   * Weekdag/Weekend
   * Jaar
* Sommige op paden gebaseerde afmetingen, waaronder:
   * Alle invoerafmetingen, met uitzondering van invoerpagina
   * Alle afmetingen bij afsluiten, behalve Pagina afsluiten en Koppeling afsluiten
   * Hit Depth
   * Retourfrequentie
   * Tijd voorafgaand aan gebeurtenis
   * Tijd besteed op pagina - Emmerd
   * Tijd besteed per bezoek - Emmerd
   * Diepte bezoeken
* Alle zoekpaginanummers
* Hiërarchievariabelen
* Type hit
* Pagina&#39;s niet gevonden (beschikbaar als een dimensie); niet ondersteund voor segmentatie)
* Betaalde zoekopdracht
* Bezoeken van één pagina
* Reden voor reeksspatiëring
* VS

### Metriek niet ondersteund

* Sommige op plakken gebaseerde metriek, die omvatten:
   * Bounces
   * Geopend
   * Gesloten
   * Opnieuw geladen
   * Eenmalige toegang
   * Metrische waarden voor &#39;tijd besteed&#39;
