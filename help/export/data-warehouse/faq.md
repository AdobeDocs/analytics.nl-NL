---
title: Data Warehouse FAQ
description: Veelgestelde vragen over Data Warehouse.
feature: Data Warehouse
exl-id: 51c3ba17-a8b2-4030-9521-355ebbbfcd0d
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---

# Veelgestelde vragen over Data Warehouse

Frequently asked questions for Data Warehouse.

## When I use the granularity dropdown while creating a request, what format can I expect the dates to be in?

Wanneer het toepassen van granulariteit in een verzoek van de Data Warehouse, wordt de kolom van de &quot;Datum&quot;toegevoegd aan het rapport. Afhankelijk van de geselecteerde granulariteit verandert de datumnotatie.

| Granulariteit | Format | Voorbeeld |
| --- | --- | --- |
| Uurlijks | `mmmm d, yyyy` Uur `H` | January 1, 20XX, Hour 0 |
| Dagelijks | `mmmm d, yyyy` | 1 januari 20XX |
| Wekelijks | Week `w, yyyy` | Week 1, 20XX |
| Maandelijks | `mmmm yyyy` | 20XX januari |
| Driemaandelijks | `q` Kwart `yyyy` | 1e kwartaal 20XX |
| Jaarlijks | `yyyy` | 20XX |

## Hoe werken segmenten als dimensies in de Data Warehouse?

Wanneer u een segment als afmeting in Data Warehouse gebruikt, keert het rapport een kolom terug die `"0"` of `"1"`:

* **`"0"`**: The dimension item did not meet the segment&#39;s criteria.
* **`"1"`**: The dimension item met the segment&#39;s criteria.
