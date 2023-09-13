---
description: Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd.
title: Sorteren op metrisch
feature: Data Warehouse
exl-id: 6bd82951-c3b4-4ba2-8e4d-b7c9b351911b
source-git-commit: 42c95198a4d4389308c78c312b5bb37572350cc1
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 14%

---

# Sorteren op metrisch

Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd.

Sorteren op metrisch maakt de rapporten van de Data Warehouse voor u gemakkelijker te interpreteren, en maakt deze rapporten gemakkelijker om met andere Analytics te vergelijken de mening van de het verdelingsrapporten van de Analyse.

Het volgende toont hoe het toelaten van de optie van de Soort van Metriek de rijen in een rapport van de Data Warehouse zal herschikken.

Er zijn vier mogelijke manieren dat de rapporten van de Data Warehouse met de &quot;Soort van Metriek&quot;kunnen worden georganiseerd, die op hoe de granulariteit van de datum, rapporteringsdimensies, of metriek worden gevormd, en of &quot;Max rijen&quot;wordt geplaatst:

* **Layout 1**: Regelitems worden gesorteerd in de woordenboekvolgorde (standaardwaarde). Als &quot;Max rijen&quot;wordt geplaatst, slechts worden de eerste N rijen verstrekt in het rapport.
* **Layout 2**: Data Warehouse past een metrische sortering toe op alle rijen in het rapport. De banden in de eerste metrische waarde worden gebroken door tweede metrisch, en dan de derde, etc. Wanneer alle metriek gebonden zijn, wordt de standaardwoordenboekvolgorde van items voor de afbraaklijn toegepast.
* **Layout 3**: Als Lay-out 2, met slechts de hoogste N rijen (d.w.z., het aantal dat in &quot;maximum rijen&quot;wordt geplaatst) die output in het rapport wordt geplaatst.
* **Layout 4**: Als lay-out 2, met uitzondering dat de lijnpunten voor elke periode van de datumgranulariteit samen worden gegroepeerd en binnen dat respectieve tijdwaaier worden gesorteerd.

Verwijs naar de kolom &quot;Lay-out Rapport&quot; in deze tabel om te bepalen hoe &quot;Metrics Sort&quot; interageert met andere Data Warehouse rapportageopties.

| Sorteren op metrisch? | Heeft Metrisch? | Heeft uitsplitsingen? | Datum granulariteit? | Max. aantal rijen ingesteld? | Rapportindeling |
|---|---|---|---|---|---|
| Nee | Ja of Nee | Ja of Nee | Ja of Nee | Ja of Nee | 1 |
| Ja | Nee | Ja of Nee | Ja of Nee | Ja of Nee | 1 |
| Ja | Ja | Nee | Nee | N.v.t. | 1 |
| Ja | Ja | Nee | Ja of Nee | Nee | 1 |
| Ja | Ja | Ja | Nee | Nee | 2 |
| Ja | Ja | Nee | Ja | Ja | 3 |
| Ja | Ja | Ja | Ja of Nee | Ja | 3 |
| Ja | Ja | Ja | Ja | Nee | 4 |
