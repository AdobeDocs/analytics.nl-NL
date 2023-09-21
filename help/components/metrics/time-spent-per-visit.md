---
title: Tijd doorgebracht per bezoek (cijfers)
description: De hoeveelheid tijd die per bezoek voor de afmetingspost wordt doorgebracht.
feature: Metrics
exl-id: 0f951196-66a2-4733-bb62-4555a9331efb
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Tijd doorgebracht per bezoek (seconden)

*Deze hulppagina beschrijft hoe de &quot;Tijd besteed per bezoek&quot;als metrisch werkt. Zie de [Tijd besteed per bezoek](../dimensions/time-spent-per-visit.md) dimensie voor meer informatie.*

De &#39;Tijd besteed per bezoek (seconden)&#39; [metrisch](overview.md) geeft de gemiddelde hoeveelheid tijd weer die bezoekers tijdens elk bezoek met een bepaald dimensie-item in wisselwerking staan.

Dit metrisch is niet beschikbaar in Data Warehouse wegens zijn verschillende verwerkingsarchitectuur.

## Hoe deze metrische waarde wordt berekend

Deze methode gebruikt de formule [`[Total seconds spent]`](total-seconds-spent.md) `divided by (`[`[Visits]`](visits.md) `minus` [`[Bounces]`](bounces.md)`)`.

## Vergelijking met gemiddelde tijd op locatie

Deze metrische en [Gemiddelde tijd die op de locatie is doorgebracht](average-time-on-site.md) zijn vergelijkbaar, maar hebben verschillende belangrijke verschillen. Beide meeteenheden gebruiken &#39;Totaal aantal bestede seconden&#39; als teller. Bij &#39;Gemiddelde tijd op locatie&#39; worden echter de reeksen gebruikt die een dimensie-item als noemer bevatten. De tijd die per bezoek wordt doorgebracht gebruikt de telling van het bezoek als noemer.

Als gevolg hiervan leveren deze meetgegevens vergelijkbare resultaten op bij een bezoek, maar ze verschillen per hit.

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de tijd die de hele dimensie per bezoek besteedt, en de teller is de tijd die het dimensie-item per bezoek besteedt. Als de volledige tijd van de afmeting per bezoek lager is dan de tijd die een bepaald afmetingspunt per bezoek besteedt, zult u percentages boven 100% zien. Het sorteren van gerangschikte rapporten door dit metrisch toont anomalietijd die per het bezoek wordt doorgebracht waarden, die typisch niet waardevol is. Adobe beveelt sorteren met een andere metrische waarde aan, zoals [Bezoeken](visits.md), in gerangschikte verslagen.

Zie [Overzicht van de tijd](time-spent.md) voor meer algemene informatie over de bestede tijd.
