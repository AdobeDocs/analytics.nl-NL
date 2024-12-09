---
title: Componentondersteuning in Data Warehouse
description: Leer welke extra afmetingen en metriek in Data Warehouse beschikbaar zijn en wat niet wordt gesteund.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Componentondersteuning in Data Warehouse

De unieke verwerking in de architectuur van de Data Warehouse staat sommige componenten toe die typisch niet beschikbaar in andere mogelijkheden van Adobe Analytics zijn. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor de Data Warehouse

Sommige dimensies en metriek die in Data Warehouse kunnen worden gebruikt zijn niet beschikbaar wanneer het gebruiken van andere mogelijkheden in Adobe Analytics.

### Uitsluitend ondersteunde Dimensionen

* **identiteitskaart van het Experience Cloud**: Voor implementaties die de Dienst van identiteitskaart van het Experience Cloud (ECID) gebruiken, een aantal met 128 bits dat uit twee samengevoegde aantallen bestaat met 64 bits die aan 19 cijfers worden toegevoegd.
* **pagina URL**: De pagina URL de slag voorkwam op.
* **Inkoop IDs**: Unieke herkenningsteken voor een aankoop, die gebruikend de purchaseID variabele wordt geplaatst.
* **identiteitskaart van de Bezoeker**: Verstrekt het unieke herkenningsteken voor de bezoeker. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [ de kolomverwijzing van Gegevens ](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder de Diersen van Gegevens voor meer informatie.

### Uitsluitend ondersteunde cijfers

* **bezoeken**: Deze metrisch in de context van Data Warehouse sluit niet-blijvende koekjesbezoeken uit.
* **bezoeken - Alle Bezoekers**: Dit metrisch in context van Data Warehouse heeft nauwere pariteit met de bezoeken metrisch in andere hulpmiddelen binnen Adobe Analytics.

## Componenten niet ondersteund in Data Warehouse

Sommige dimensies en metriek worden niet ondersteund in Data Warehouse.

>[!NOTE]
>
>Als een afmeting of metrisch niet in Data Warehouse wordt gesteund, worden de segmenten die deze componenten gebruiken ook niet gesteund. Controleer altijd de productcompatibiliteit wanneer u een segment maakt of bewerkt.

### Dimensionen worden niet ondersteund

* AM/PM
* Sommige op paden gebaseerde afmetingen, waaronder:
   * Alle invoerafmetingen, met uitzondering van invoerpagina
   * Alle afmetingen bij afsluiten, behalve Pagina afsluiten en Koppeling afsluiten
   * Hoogte
   * Geretourneerde frequentie
   * Tijd voorafgaand aan gebeurtenis
   * Tijd besteed op pagina - Emmerd
   * Tijd besteed per bezoek - Emmerd
* Alle zoekpaginanummers
* Hiërarchievariabelen
* Type hit
* Pagina&#39;s niet gevonden (beschikbaar als een dimensie; niet ondersteund voor segmentatie)
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
* De metriek van de participatie (zoals die in [ wordt beschreven bouwt metrische &quot;Deelname&quot;](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md))

### Dimensionen die op een andere manier worden ondersteund

De volgende op tijd gebaseerde afmetingen worden ondersteund. De uitvoer van datums is echter niet standaard wanneer deze afmetingen worden gebruikt. Het jaar wordt met name gecompenseerd door 1900 en de maanden zijn op nul gebaseerd.

* Jaar
* Kwart
* Maand
* Week
* Dag
* Uur
* Minute

## Segmenten als afmetingen in Data Warehouse

Wanneer u een segment als een afmeting in Data Warehouse gebruikt, keert het rapport een kolom terug die `"0"` of `"1"` bevat:

* **`"0"`**: Het dimensie-item voldoet niet aan de criteria van het segment.
* **`"1"`**: Het dimensie-item voldoet aan de criteria van het segment.
