---
title: Componentondersteuning in Data Warehouse
description: Leer welke extra afmetingen en metriek in Data Warehouse beschikbaar zijn en wat niet wordt gesteund.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: ecd02a087e7ab344ccfbad1d5e1c30260577002c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 3%

---

# Componentondersteuning in Data Warehouse

De unieke verwerking in de architectuur van de Data Warehouse staat sommige componenten toe die typisch niet beschikbaar in andere mogelijkheden van Adobe Analytics zijn. Door zijn unieke architectuur, zijn sommige componenten niet beschikbaar voor gebruik in of rapporten of segmenten. Gebruik deze pagina om te begrijpen wat u kunt gebruiken en wat niet.

## Componenten die uniek zijn voor de Data Warehouse

Sommige dimensies en metriek die in Data Warehouse kunnen worden gebruikt zijn niet beschikbaar wanneer het gebruiken van andere mogelijkheden in Adobe Analytics.

### Uitsluitend ondersteunde Dimensionen

* **Experience Cloud-id**: Voor implementaties die de Dienst van identiteitskaart van het Experience Cloud (ECID) gebruiken, een aantal met 128 bits dat uit twee samengevoegde aantallen bestaat met 64 bits die aan 19 cijfers worden toegevoegd.
* **Pagina-URL**: De pagina-URL waarop de treffer is opgetreden.
* **Aankoop-id&#39;s**: Unieke id voor een aankoop, ingesteld met de variabele purchaseID.
* **Bezoeker-id**: Hiermee wordt de unieke id voor de bezoeker opgegeven. Deze waarde is gelijk aan de samengevoegde waarde van `visid_high` en `visid_low` kolommen in gegevensfeeds. Zie [Referentie gegevenskolom](../analytics-data-feed/c-df-contents/datafeeds-reference.md) onder Gegevensfeeds voor meer informatie.

### Uitsluitend ondersteunde cijfers

* **Bezoeken**: In deze meetmethode in het kader van de Data Warehouse worden niet-permanente cookiebezoeken uitgesloten.
* **Bezoeken - Alle bezoekers**: Deze metrische waarde in het kader van Data Warehouse heeft een grotere pariteit met de bezoeken metrisch in andere hulpmiddelen binnen Adobe Analytics.

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
   * Retourfrequentie
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
   * Geopend
   * Gesloten
   * Opnieuw geladen
   * Eenmalige toegang
   * Metrische waarden voor &#39;tijd besteed&#39;
* Deelnemings-metriek (zoals beschreven in [Een &quot;Deelname&quot;-metrisch maken](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md))

### Dimensionen die op een andere manier worden ondersteund

De volgende op tijd gebaseerde afmetingen worden ondersteund. De uitvoer van datums is echter niet standaard wanneer deze afmetingen worden gebruikt. Het jaar wordt met name gecompenseerd door 1900 en de maanden zijn op nul gebaseerd.

* Jaar
* Kwart
* Maand
* Week
* Dag
* Uur
* Minute
