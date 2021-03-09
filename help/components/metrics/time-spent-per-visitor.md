---
title: Tijd doorgebracht per bezoeker (seconden)
description: De metrische waarde 'Tijd besteed per bezoeker (seconden)' toont de gemiddelde hoeveelheid tijd die bezoekers met een bepaald afmetingspunt tijdens het volledige leven van een bezoeker in wisselwerking staan.
translation-type: tm+mt
source-git-commit: 4d0d5ca99049e48fcf1f248f78ecef94534b6815
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Tijd doorgebracht per bezoeker (seconden)

De metrische waarde [!UICONTROL Time spent per visitor (seconds)] toont de gemiddelde hoeveelheid tijd die bezoekers met een bepaald afmetingspunt tijdens het volledige leven van een bezoeker in wisselwerking staan.

Dit metrisch is niet beschikbaar in Data Warehouse wegens zijn verschillende verwerkingsarchitectuur.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde gebruikt de formule [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md).

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de volledige tijd van de afmeting die per bezoeker wordt doorgebracht, en de teller is de tijd van de afmetingspunt die per bezoeker wordt doorgebracht. Als de tijd die de hele dimensie per bezoeker doorbrengt minder is dan de tijd die een bepaald dimensie-item per bezoeker doorbrengt, ziet u percentages boven 100%. Het sorteren van gerangschikte rapporten door dit metrisch toont anomalietijd die per bezoekerswaarden wordt doorgebracht, die typisch niet waardevol is. Adobe raadt aan om in gerangschikte rapporten te sorteren met een andere metrische waarde, zoals [Visits](visits.md).

Zie [Overzicht van de bestede tijd](time-spent.md) voor meer algemene informatie over de doorgebrachte tijd.
