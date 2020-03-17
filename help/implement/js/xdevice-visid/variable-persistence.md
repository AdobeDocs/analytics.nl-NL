---
description: Wanneer bezoekersprofielen worden samengevoegd nadat ze zijn gekoppeld aan dezelfde variabele voor de bezoekersidentiteitskaart, wordt de toewijzing niet gewijzigd in de historische gegevensset.
keywords: Analytics Implementation
title: Toewijzing en persistentie
topic: Developer and implementation
uuid: 5dd706be-83f6-498a-a856-e3c5af995348
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Toewijzing en persistentie

> [!IMPORTANT] Deze methode voor het identificeren van bezoekers op verschillende apparaten wordt niet langer aanbevolen. Zie [Apparaatanalyse](/help/components/cda/cda-home.md) in de gebruikershandleiding voor componenten.

Wanneer bezoekersprofielen worden samengevoegd nadat ze zijn gekoppeld aan dezelfde variabele voor de bezoekersidentiteitskaart, wordt de toewijzing niet gewijzigd in de historische gegevensset.

* Wanneer de variabele `s.visitorID` is ingesteld en op een hit wordt verzonden, controleert Adobe op andere bezoekersprofielen met een overeenkomende bezoeker-id.
* Als er een profiel bestaat, wordt het bezoekersprofiel dat al in het systeem is, vanaf dat punt gebruikt en wordt het vorige bezoekersprofiel niet meer gebruikt.
* Als er geen overeenkomende bezoeker-id wordt gevonden, wordt een nieuw profiel gemaakt.

Wanneer een niet-geverifieerde klant voor het eerst op uw site arriveert, wordt aan die klant een bezoekersprofiel toegewezen door Adobe Analytics. Wanneer het nieuwe profiel is gemaakt, wordt het ene bezoek beëindigd en het andere bezoek gestart.

## Voorbeeld 1

In het onderstaande voorbeeld ziet u hoe gegevens naar Adobe Analytics worden verzonden wanneer een klant voor het eerst op het eerste apparaat verifieert:

* `eVar16` heeft een vervaldatum van 1 dag en `evar17` verloopt bij een bezoek.
* De `post_visitor_id` kolom staat voor het profiel dat wordt bijgehouden door Adobe Analytics. Post-kolommen worden doorgaans weergegeven in gegevensfeeds. Zie [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md) in de gebruikershandleiding bij Exporteren.
* De `post_evar16` kolommen en de `post_evar17` kolommen tonen aan dat eVars blijvend zijn.
* `cust_visid` vertegenwoordigt een waarde die is ingesteld in `s.visitorID`.
* Elke rij is één &#39;hit&#39;, één aanvraag die naar Adobe Analytics-gegevensverzamelingsservers wordt verzonden.

![Voorbeeld 1 van een ander apparaat](assets/xdevice_first.jpg)

Bij de eerste gegevensverbinding met een eerder niet-herkende `s.visitorID` waarde (`u999` hierboven) wordt een nieuw profiel gemaakt. Persistente waarden uit het vorige profiel worden overgebracht naar het nieuwe profiel.

* Vars die tijdens het bezoek verlopen, worden niet naar het geverifieerde profiel gekopieerd. De bovenstaande waarde `car` is niet blijvend.
* Waarden die door andere maatregelen vervallen, worden naar het geverifieerde profiel gekopieerd. De waarde `apple` blijft bestaan.
* Voor de eVars die worden voortgeduurd, wordt geen metrische instantie geregistreerd. Dit betekent wanneer het gebruiken van de identificatie van de dwars-apparatenbezoeker, het mogelijk is om rapporten te zien waar de Unieke metrische Bezoek voor een waarde eVar groter is dan metrisch van de Instantie.

> [!NOTE] Als een gebruiker nieuw is voor uw site (nog niet eerder op dit apparaat is bezocht) en binnen ongeveer 3 minuten na aankomst wordt geverifieerd, blijven er geen waarden over voor het geverifieerde profiel.

## Voorbeeld 2

In het onderstaande voorbeeld ziet u hoe gegevens naar Adobe Analytics worden verzonden wanneer een klant op een nieuw apparaat verifieert nadat het apparaat eerder is geverifieerd op een ander apparaat.

![Voorbeeld 2 van verschillende apparaten](assets/xdevice-subsequent.jpg)

Wanneer de klant verifieert, worden zij aangepast aan het vorige &quot;voor authentiek verklaarde&quot;profiel - `2947539300`. Het profiel dat aan het begin van dit bezoek ( `5477766334477`) wordt gebruikt, wordt niet meer gebruikt en er blijven geen gegevens uit het bestand aanwezig.

* Geo-segmentatiegegevens worden geregistreerd op basis van de eerste hit van het bezoek en worden niet gewijzigd voor één bezoek, ongeacht het gebruikte apparaat. Dit betekent dat bij een volgende gegevensverbinding op een nieuw apparaat de geo-segmentatiegegevens over het algemeen niet worden opgenomen.
* De kolommen van de technologie zoals browser, werkend systeem, en kleurendiepte worden geregistreerd bij de eerste klap van een bezoek. Net als bij Geo-Segmenteringswaarden worden ze niet naar het profiel waaraan u een koppeling hebt toegevoegd, gekopieerd.
* Marketingkanalen overschrijven andere kanalen op een volgende gegevensverbinding die een eerste verificatie voor dat apparaat bevat.
