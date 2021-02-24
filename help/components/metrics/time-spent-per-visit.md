---
title: Tijd besteed per bezoek
description: De hoeveelheid tijd die per bezoek voor de afmetingspost wordt doorgebracht.
translation-type: tm+mt
source-git-commit: dc5c51f68ab22bd4f1368aa0656c66ee53d99103
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---


# Tijd doorgebracht per bezoek (seconden)

*Deze hulppagina beschrijft hoe de &quot;Tijd besteed per bezoek&quot;als metrisch werkt. Zie [De tijd die per bezoek wordt doorgebracht](../dimensions/time-spent-per-visit.md) dimensie voor meer informatie.*

De metrische waarde &#39;Tijd besteed per bezoek (seconden)&#39; toont de gemiddelde hoeveelheid tijd die bezoekers tijdens elk bezoek met een bepaald dimensie-item in wisselwerking staan.

Dit metrisch is niet beschikbaar in Data Warehouse wegens zijn verschillende verwerkingsarchitectuur.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde gebruikt de formule [`[Total seconds spent]`](total-seconds-spent.md) `divided by (`[`[Visits]`](visits.md) `minus` [`[Bounces]`](bounces.md)`)`.

## Vergelijking met gemiddelde tijd op locatie

Deze metrische waarde en [Gemiddelde tijd die aan plaats](average-time-on-site.md) wordt doorgebracht zijn gelijkaardig, maar hebben verscheidene zeer belangrijke verschillen. Beide meeteenheden gebruiken &#39;Totaal aantal bestede seconden&#39; als teller. Bij &#39;Gemiddelde tijd op locatie&#39; worden echter de reeksen gebruikt die een dimensie-item als noemer bevatten. De tijd die per bezoek wordt doorgebracht gebruikt de telling van het bezoek als noemer.

Als gevolg hiervan leveren deze meetgegevens vergelijkbare resultaten op bij een bezoek, maar ze verschillen per hit.

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de tijd die de hele dimensie per bezoek besteedt, en de teller is de tijd die het dimensie-item per bezoek besteedt. Als de volledige tijd van de afmeting per bezoek lager is dan de tijd die een bepaald afmetingspunt per bezoek besteedt, zult u percentages boven 100% zien. Het sorteren van gerangschikte rapporten door dit metrisch toont anomalietijd die per het bezoek wordt doorgebracht waarden, die typisch niet waardevol is. Adobe raadt aan om in gerangschikte rapporten te sorteren met een andere metrische waarde, zoals [Visits](visits.md).

Zie [Overzicht van de bestede tijd](time-spent.md) voor meer algemene informatie over de doorgebrachte tijd.
