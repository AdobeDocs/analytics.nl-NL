---
title: Componentondersteuning in Data Warehouse
description: Leer welke extra afmetingen en metriek beschikbaar zijn in Data Warehouse en wat niet wordt gesteund.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Componentondersteuning in Data Warehouse

De unieke verwerking in de architectuur van Data Warehouse staat sommige componenten toe die typisch niet beschikbaar in andere mogelijkheden van Adobe Analytics zijn. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor Data Warehouse

Sommige dimensies en metriek die in Data Warehouse kunnen worden gebruikt, zijn niet beschikbaar wanneer u andere mogelijkheden in Adobe Analytics gebruikt.

### Exclusief ondersteunde afmetingen

* **identiteitskaart van Experience Cloud**: Voor implementaties die de Dienst van identiteitskaart van Experience Cloud (ECID) gebruiken, een aantal met 128 bits dat uit twee samengevoegde aantallen bestaat met 64 bits die aan 19 cijfers worden toegevoegd.
* **pagina URL**: De pagina URL de slag voorkwam op.
* **Inkoop IDs**: Unieke herkenningsteken voor een aankoop, die gebruikend de purchaseID variabele wordt geplaatst.
* **identiteitskaart van de Bezoeker**: Verstrekt het unieke herkenningsteken voor de bezoeker. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [ de kolomverwijzing van Gegevens ](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder de Diersen van Gegevens voor meer informatie.

### Uitsluitend ondersteunde cijfers

* **bezoeken**: Deze metrisch in context van Data Warehouse sluit niet-blijvende koekjesbezoeken uit.
* **bezoeken - Alle Bezoekers**: Dit metrisch in context van Data Warehouse heeft nauwere pariteit met de bezoeken metrisch in andere hulpmiddelen binnen Adobe Analytics.

## Componenten die niet worden ondersteund in Data Warehouse

Sommige dimensies en metriek worden niet ondersteund in Data Warehouse.

>[!NOTE]
>
>Als een dimensie of metrisch niet in Data Warehouse wordt gesteund, worden de segmenten die deze componenten gebruiken ook niet gesteund. Controleer altijd de productcompatibiliteit wanneer u een segment maakt of bewerkt.

### Afmetingen niet ondersteund

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
* De metriek van de participatie (zoals die in [ wordt beschreven bouwt metrische &quot;Deelname&quot;](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md))

### Dimensies die op een andere manier worden ondersteund (niet-standaarddatumopmaak)

De volgende op tijd gebaseerde afmetingen worden ondersteund:

* Jaar
* Kwart
* Maand
* Week
* Dag
* Uur
* Minute

De uitvoer van datums is echter niet standaard wanneer deze afmetingen worden gebruikt.

Houd rekening met het volgende wanneer u de uitvoer van datums in Data Warehouse berekent:

* De datumafmetingen worden in de volgende notatie weergegeven: `1YYMMDDHHMM`

* Het jaar (JJ) wordt verschoven met 1900. Dit betekent dat u `1900` toevoegt aan de eerste 3 waarden van het datumveld.

  Als de waarde van het veld Datumbereik in Data Warehouse bijvoorbeeld `1250901` is, voegt u 1900 tot en met 125 toe. Dit resulteert in het jaar 2025.

* Alle maanden zijn op nul gebaseerd, waarbij januari wordt vertegenwoordigd door 00, februari door 01 enzovoort, als volgt:

   * 00: januari
   * 01 februari
   * 02: maart
   * 03 april
   * 04 mei
   * 05 juni
   * 06 juli
   * 07: augustus
   * 08 september
   * 09 oktober
   * 10 november
   * 11: december

  Als de waarde van het veld Datumbereik in Data Warehouse bijvoorbeeld `1250901` is, wordt de maand weergegeven als 09, wat oktober aangeeft.




## Segmenten als afmetingen in Data Warehouse

Wanneer u een segment als een dimensie gebruikt in Data Warehouse, retourneert het rapport een kolom die `"0"` of `"1"` bevat:

* **`"0"`**: Het dimensie-item voldoet niet aan de criteria van het segment.
* **`"1"`**: Het dimensie-item voldoet aan de criteria van het segment.
