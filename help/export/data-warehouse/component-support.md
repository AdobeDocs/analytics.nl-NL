---
title: Componentondersteuning in Data Warehouse
description: Leer welke extra afmetingen en metriek beschikbaar in het Warehouse van Gegevens zijn en wat niet wordt gesteund.
translation-type: tm+mt
source-git-commit: 00d4d59cb4c922b54a97ef7000e294ef3bf61f20

---


# Componentondersteuning in Data Warehouse

De unieke verwerkingsarchitectuur van het Data Warehouse maakt het mogelijk dat bepaalde componenten die gewoonlijk niet beschikbaar zijn in andere mogelijkheden van Adobe Analytics, beschikbaar zijn. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor Data Warehouse

Sommige dimensies en metriek kunnen worden gebruikt in Data Warehouse, maar zijn niet beschikbaar met behulp van andere mogelijkheden in Adobe Analytics.

### Exclusief ondersteunde afmetingen

* Experience Cloud ID: Voor implementaties die de dienst van identiteitskaart van de Wolk van de Ervaring gebruiken (ECID), een aantal met 128 bits dat uit twee samengevoegde aantallen bestaat 64 bits die aan 19 cijfers worden toegevoegd.
* Pagina-URL: De pagina-URL waarop de treffer heeft plaatsgevonden.
* Aankoop-id&#39;s: Unieke id voor een aankoop, ingesteld met de variabele purchaseID.
* Bezoeker-id: Verschaft de unieke id voor de bezoeker. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [Gegevens kolomverwijzing](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder Gegevensfeeds voor meer informatie.

### Uitsluitend ondersteunde cijfers

* Bezoeken: Deze metrische waarde in de context van Data Warehouse sluit niet-permanente cookie bezoeken uit.
* Bezoeken - Alle bezoekers: Deze metrische waarde in de context van het Pakhuis van Gegevens heeft dichter pariteit met de bezoeken metrisch in andere hulpmiddelen binnen de Analytics van Adobe.

## Componenten die niet worden ondersteund in Data Warehouse

Sommige dimensies en metriek worden niet ondersteund in Data Warehouse.

> [!NOTE] Als een afmeting of metrisch niet in het Pakhuis van Gegevens wordt gesteund, worden de segmenten die deze componenten gebruiken ook niet gesteund. Controleer altijd de productcompatibiliteit wanneer u een segment maakt of bewerkt.

### Afmetingen niet ondersteund

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
   * Geretourneerde frequentie
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
   * Berichten
   * Afsluiten
   * Opnieuw laden
   * Enkelvoudige toegang
   * Metrische waarden voor &#39;tijd besteed&#39;
