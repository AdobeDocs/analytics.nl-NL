---
title: Componentondersteuning in Data warehouse
description: Leer welke extra dimensies en metriek beschikbaar zijn in Data warehouse en wat niet wordt gesteund.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 4%

---


# Componentondersteuning in Data warehouse

Bij unieke Data warehouse-verwerkingsarchitectuur zijn bepaalde componenten niet standaard beschikbaar in Adobe Analytics. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor Data warehouse

Sommige dimensies en meetgegevens kunnen worden gebruikt in Data warehouse, maar zijn niet beschikbaar met behulp van andere mogelijkheden in Adobe Analytics.

### Exclusief ondersteunde afmetingen

* Experience Cloud-id: Voor implementaties die de Experience Cloud ID Service (ECID) gebruiken, een 128-bits aantal dat uit twee samengevoegde 64-bits aantallen bestaat die aan 19 cijfers worden toegevoegd.
* Pagina-URL: De pagina-URL waarop de treffer heeft plaatsgevonden.
* Aankoop-id&#39;s: Unieke id voor een aankoop, ingesteld met de variabele purchaseID.
* Bezoeker-id: Verschaft de unieke id voor de bezoeker. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [Gegevens kolomverwijzing](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder Gegevensfeeds voor meer informatie.

### Uitsluitend ondersteunde cijfers

* Bezoeken: Deze meetmethode in het kader van Data warehouse sluit niet-permanente cookiebezoeken uit.
* Bezoeken - Alle bezoekers: Deze maatstaf in de context van Data warehouse is meer gelijk aan de metrische bezoeken in andere gereedschappen in Adobe Analytics.

## Componenten niet ondersteund in Data warehouse

Sommige afmetingen en meetwaarden worden niet ondersteund in Data warehouse.

>[!NOTE]
>
>Als een afmeting of metrisch niet in Data warehouse wordt gesteund, worden de segmenten die deze componenten gebruiken ook niet gesteund. Controleer altijd de productcompatibiliteit wanneer u een segment maakt of bewerkt.

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
