---
title: Veelgestelde vragen over Data Warehouse
description: Veelgestelde vragen over Data Warehouse.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---


# Veelgestelde vragen over Data Warehouse

Veelgestelde vragen over Data Warehouse.

## Wanneer ik het drop-down van de granulariteit terwijl het creëren van een verzoek gebruik, welke formaat kan ik de data verwachten om binnen te zijn?

Wanneer het toepassen van granulariteit in een verzoek van de Data Warehouse, wordt de kolom van de &quot;Datum&quot;toegevoegd aan het rapport. Afhankelijk van de geselecteerde granulariteit verandert de datumnotatie.

| Granulariteit | Indeling | Voorbeeld |
| --- | --- | --- |
| Uurlijks | `mmmm d, yyyy` Uur  `H` | 1 januari, 20XX, Uur 0 |
| Dagelijks | `mmmm d, yyyy` | 1 januari 20XX |
| Wekelijks | Week `w, yyyy` | Week 1, 20XX |
| Maandelijks | `mmmm yyyy` | 20XX januari |
| Driemaandelijks | `q` Kwart  `yyyy` | 1e kwartaal 20XX |
| Jaarlijks | `yyyy` | 20XX |

## Hoe werken segmenten als dimensies in de Data Warehouse?

Wanneer u een segment als afmeting in Data Warehouse gebruikt, keert het rapport een kolom terug die `"0"` of `"1"` bevat:

* **`"0"`**: Het item Dimensie voldeed niet aan de criteria van het segment.
* **`"1"`**: Het item Dimensie voldeed aan de criteria van het segment.
