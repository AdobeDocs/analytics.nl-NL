---
description: Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd.
title: Sorteren op metrisch
uuid: 07da2607-b3fd-463b-90d4-6884a93c7e25
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 15%

---


# Sorteren op metrisch

Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd.

Sorteren op metrisch maakt de rapporten van de Data Warehouse voor u gemakkelijker te interpreteren, en maakt deze rapporten gemakkelijker om met andere Analytics te vergelijken de mening van de het verdelingsrapporten van de Analyse.

Het volgende toont hoe het toelaten van de optie van de Soort van Metriek de rijen in een rapport van de Data Warehouse zal herschikken.

Er zijn vier mogelijke manieren dat de rapporten van de Data Warehouse met de &quot;Soort van Metriek&quot;kunnen worden georganiseerd, die op hoe de granulariteit van de datum, rapporteringsdimensies, of metriek worden gevormd, en of &quot;Max rijen&quot;wordt geplaatst:

* **Layout 1**: Regelitems worden gesorteerd in de woordenboekvolgorde (standaard). Als &quot;Max rijen&quot;wordt geplaatst, slechts worden de eerste N rijen verstrekt in het rapport.
* **Layout 2**: De Data Warehouse past een metrische soort over alle rijen in het rapport toe. De banden in de eerste metrische waarde worden gebroken door tweede metrisch, en dan de derde, etc. Wanneer alle metriek gebonden zijn, wordt de standaardwoordenboekvolgorde van items voor de afbraaklijn toegepast.
* **Layout 3**: Als Lay-out 2, met slechts de hoogste rijen van N (d.w.z., het aantal dat in &quot;maximum rijen&quot;wordt geplaatst) wordt uitgevoerd in het rapport.
* **Layout 4**: Als Lay-out 2, met uitzondering dat de lijnpunten voor elke periode van de datumgranulariteit worden gegroepeerd en binnen dat respectieve tijdwaaier gesorteerd.

Verwijs naar de kolom &quot;Lay-out Rapport&quot; in deze tabel om te bepalen hoe &quot;Metrics Sort&quot; interageert met andere Data Warehouse rapportageopties.

| Sorteren op metrisch? | Heeft Metrisch? | Heeft uitsplitsingen? | Datum granulariteit? | Max. aantal rijen ingesteld? | Rapportindeling |
|---|---|---|---|---|---|
| Nee | Ja of Nee | Ja of Nee | Ja of Nee | Ja of Nee | 3 |
| Ja | Nee | Ja of Nee | Ja of Nee | Ja of Nee | 3 |
| Ja | Ja | Nee | Nee | N.v.t. | 3 |
| Ja | Ja | Nee | Ja of Nee | Nee | 3 |
| Ja | Ja | Ja | Nee | Nee | 2 |
| Ja | Ja | Nee | Ja | Ja | 3 |
| Ja | Ja | Ja | Ja of Nee | Ja | 1 |
| Ja | Ja | Ja | Ja | Nee | 4 |

