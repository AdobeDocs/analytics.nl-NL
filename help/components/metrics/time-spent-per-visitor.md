---
title: Tijd doorgebracht per bezoeker (seconden)
description: null
translation-type: tm+mt
source-git-commit: 5282ad3f6fdd2853979cbfb2707cc07a698f63a7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Tijd doorgebracht per bezoeker (seconden)

De metrische waarde &#39;Tijd besteed per bezoeker (seconden)&#39; toont de gemiddelde hoeveelheid tijd die bezoekers gedurende het gehele leven van een bezoeker met een bepaalde afmetingswaarde in wisselwerking staan.

Deze metrisch is niet beschikbaar in het Warehouse van Gegevens toe te schrijven aan zijn verschillende verwerkingsarchitectuur.

## Hoe deze metrische waarde wordt berekend

Deze metrische methode gebruikt de formule [`Total seconds spent`](total-seconds-spent.md) `divided by`[`Unique visitors`](unique-visitors.md).

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de volledige tijd van de afmeting die per bezoeker wordt doorgebracht, en de teller is de tijd van de afmetingswaarde die per bezoeker wordt doorgebracht. Als de tijd die de hele dimensie per bezoeker doorbrengt minder is dan de tijd die een bepaalde dimensie heeft doorgebracht per bezoeker, ziet u percentages boven 100%. Het sorteren van gerangschikte rapporten door dit metrisch toont anomalietijd die per bezoekerswaarden wordt doorgebracht, die typisch niet waardevol is. Adobe raadt u aan om in gerangschikte rapporten een andere waarde in te voeren, zoals [Visits](visits.md).

Zie [Tijd besteed overzicht](time-spent.md) voor meer algemene informatie over bestede tijd.
