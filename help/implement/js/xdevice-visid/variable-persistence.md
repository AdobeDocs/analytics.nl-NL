---
description: Wanneer bezoekersprofielen worden samengevoegd nadat ze zijn gekoppeld aan dezelfde variabele voor de bezoekersidentiteitskaart, wordt de toewijzing niet gewijzigd in de historische gegevensset.
keywords: Analyseimplementatie
title: Toewijzing en persistentie
feature: Implementation Basics
exl-id: 7a6305f6-c8ec-4f26-8373-45ce586bc69d
role: Developer
source-git-commit: e242276f931e9939081b948a9d9ef8a087e16461
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Toewijzing en persistentie

>[!IMPORTANT]
>
>Deze methode voor het identificeren van bezoekers op verschillende apparaten wordt niet langer aanbevolen. Zie [&#x200B; Analytics van het Apparaat &#x200B;](/help/components/cda/overview.md) in de de gebruikersgids van Componenten.

Wanneer bezoekersprofielen worden samengevoegd nadat ze zijn gekoppeld aan dezelfde variabele voor de bezoekersidentiteitskaart, wordt de toewijzing niet gewijzigd in de historische gegevensset.

* Wanneer de variabele `visitorID` wordt ingesteld en verzonden bij een treffer, controleert Adobe of er andere bezoekersprofielen zijn die een overeenkomende bezoeker-id hebben.
* Als er een profiel bestaat, wordt het bezoekersprofiel dat al in het systeem is, vanaf dat punt gebruikt en wordt het vorige bezoekersprofiel niet meer gebruikt.
* Als er geen overeenkomende bezoeker-id wordt gevonden, wordt een nieuw profiel gemaakt.

Wanneer een niet-geverifieerde klant voor het eerst op uw site arriveert, wordt aan die klant een bezoekersprofiel toegewezen door Adobe Analytics. Wanneer het nieuwe profiel is gemaakt, wordt het ene bezoek beëindigd en het andere bezoek gestart.

## Voorbeeld 1

In het onderstaande voorbeeld ziet u hoe gegevens naar Adobe Analytics worden verzonden wanneer een klant voor het eerst op het eerste apparaat verifieert:

* `eVar16` heeft een vervaldatum van 1 dag en `evar17` verloopt tijdens een bezoek.
* De kolom `post_visitor_id` vertegenwoordigt het profiel dat door Adobe Analytics wordt gehandhaafd. Post-kolommen worden doorgaans weergegeven in gegevensfeeds. Zie [&#x200B; het voer van Gegevens &#x200B;](/help/export/analytics-data-feed/data-feed-overview.md) in de de gebruikersgids van de Uitvoer.
* De kolommen `post_evar16` en `post_evar17` laten de persistentie van eVars zien.
* `cust_visid` vertegenwoordigt een waarde die is ingesteld in `visitorID` .
* Elke rij is één &#39;hit&#39;, één aanvraag die naar Adobe Analytics-servers voor gegevensverzameling wordt verzonden.

![&#x200B; Voorbeeld 1 van dwars-apparaat &#x200B;](assets/xdevice_first.jpg)

Bij de eerste gegevensverbinding met een eerder niet-herkende `visitorID` -waarde (`u999` hierboven) wordt een nieuw profiel gemaakt. Persistente waarden uit het vorige profiel worden overgebracht naar het nieuwe profiel.

* Vars die tijdens het bezoek verlopen, worden niet naar het geverifieerde profiel gekopieerd. De bovenstaande waarde `car` is niet blijvend.
* Waarden die door andere maatregelen vervallen, worden naar het geverifieerde profiel gekopieerd. De waarde `apple` blijft bestaan.
* Voor de eVars die worden voortgeduurd, wordt geen metrische instantie geregistreerd. Dit betekent wanneer het gebruiken van de identificatie van de dwars-apparatenbezoeker, het mogelijk is om rapporten te zien waar de Unieke metrische Bezoek voor een waarde van eVar groter is dan metrisch van de Instantie.

>[!NOTE]
>
>Als een gebruiker nieuw is voor uw site (nog niet eerder op dit apparaat is bezocht) en binnen ongeveer 3 minuten na aankomst wordt geverifieerd, blijven er geen waarden over voor het geverifieerde profiel.

## Voorbeeld 2

In het onderstaande voorbeeld ziet u hoe gegevens naar Adobe Analytics worden verzonden wanneer een klant op een nieuw apparaat verifieert nadat deze eerder op een ander apparaat is geverifieerd.

![&#x200B; dwars-apparatenvoorbeeld 2 &#x200B;](assets/xdevice-subsequent.jpg)

Wanneer de klant verifieert, worden deze overeenkomen met het vorige &#39;geverifieerde&#39; profiel - `2947539300` . Het profiel dat aan het begin van dit bezoek ( `5477766334477` ) wordt gebruikt, wordt niet meer gebruikt en er blijven geen gegevens uit het bestand aanwezig.

* Geo-segmentatiegegevens worden geregistreerd op basis van de eerste hit van het bezoek en worden niet gewijzigd voor één bezoek, ongeacht het gebruikte apparaat. Dit betekent dat bij een volgende gegevensverbinding op een nieuw apparaat de geo-segmentatiegegevens over het algemeen niet worden opgenomen.
* De kolommen van de technologie zoals browser, werkend systeem, en kleurendiepte worden geregistreerd bij de eerste klap van een bezoek. Net als bij Geo-Segmenteringswaarden worden ze niet naar het profiel waaraan u een koppeling hebt toegevoegd, gekopieerd.
* Marketingkanalen overschrijven andere kanalen op een volgende gegevensverbinding die een eerste verificatie voor dat apparaat bevat.
