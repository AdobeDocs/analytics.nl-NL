---
title: Gemiddelde tijd op de site
description: De gemiddelde hoeveelheid tijd bestond een bepaald afmetingspunt tussen treffers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Gemiddelde tijd op de site

De metrische waarde &#39;Gemiddelde tijd op site&#39; geeft de hoeveelheid tijd aan die tussen hits voor een bepaald afmetingsitem is verstreken. Dit metrisch is nuttig wanneer u gemiddelde tijd wilt zien die voor specifieke afmetingspunten wordt doorgebracht. U kunt metrisch in tijd ook trenderen om te zien hoe de algemene tijd bestede veranderingen. Deze metrische weergave wordt weergegeven in `HH:MM:SS` indeling.

Deze metrische waarde heeft betrekking op de [tijd die per bezoek](../dimensions/time-spent-per-visit.md) wordt doorgebracht afmeting.

## Hoe deze metrische waarde wordt berekend

Neem voor een bepaald dimensie-item het tijdstempel van elke hit waar dat dimensie-item zich bevindt. Vergelijk dit met de tijdstempel van de volgende hit in het bezoek. Als de hit geen volgende hit heeft, neemt u deze niet op in deze metrische waarde. Uit alle tijd die voor het afmetingspunt wordt doorgebracht, verdeel hen allen door het aantal &quot;opeenvolgingen&quot;voor dat afmetingspunt. Een &quot;opeenvolging&quot;is waar een afmetingspunt het zelfde voor één of meerdere opeenvolgende klappen is. Dit resulterende aantal is metrisch getoond in rapporten.

Neem bijvoorbeeld het volgende bezoek:

| `Timestamp` | `Page` |
| --- | --- |
| `12:03:00` | `Home page` |
| `12:04:20` | `Product page A` |
| `12:05:30` | `Product page A` |
| `12:07:00` | `Product page B` |
| `12:07:40` | `Product page A` |
| `12:08:10` | `Checkout` |
| `12:10:00` | `Purchase` |
| `12:25:00` | `Home page` |
| `12:25:40` | `Product page A` |


Als u gemiddelde tijd op plaats voor het afmetingspunt wilt `Product page A`, neem eerst de hoeveelheid tijd tussen treffers voor die afmeting verstreek:

* **12:04:20 - 12:05:30** - 1 minuut 10 seconden
* **12:05:30 - 12:07:00** - 1 minuut 30 seconden
* **12:07:40 - 12:08:10** - 30 seconden
* **12:25:40 - ?** - Niet inbegrepen

De totale hoeveelheid tijd die voor `Product page A` wordt besteed is `00:03:10`. Dit bezoek heeft twee volgreeksen opgeleverd. de eerste reeks voor de twee opeenvolgende waarden en de tweede voor het uitchecken. Het laatste resultaat van het bezoek is geen opeenvolging, aangezien er geen eindtimestamp is.

De gemiddelde tijd op locatie voor `Product page A` is `00:01:35`.

## Gemiddelde tijd besteed aan plaats (seconden)

De metrische waarde &#39;Gemiddelde tijd die aan plaats (seconden) wordt doorgebracht&#39; toont de zelfde gegevens die als geheel in plaats van in `HH:MM:SS` formaat worden voorgesteld. Deze metrische waarde is het meest waardevol als component binnen berekende metriek.

## De totalen van de uitsplitsing komen niet overeen met het item van de bovenliggende regel

De metrische &#39;Gemiddelde tijd op locatie&#39; gebruikt ononderbroken reeksen van een bepaalde dimensie. De afbraakdimensie is niet afhankelijk van de bovenliggende dimensie bij het berekenen van deze reeksen. Neem bijvoorbeeld het volgende bezoek:

| `Timestamp` | `Page name` | `Site section` |
| --- | --- | --- |
| `12:00:00` | `Home` | `Foxes` |
| `12:00:30` | `Product` | `Foxes` |
| `12:02:10` | `Home` | `Foxes` |
| `12:02:20` | `(None; exit link click)` | `(None; exit link click)` |

Voor de berekening van de gemiddelde tijd ter plaatse voor de dimensie-item `Home` wordt de volgende berekening gebruikt:

```text
(30 + 10) / 2 = 20 seconds average time on site
```

Als u een verdeling gebruikend de dimensie van de secties [van de](../dimensions/site-section.md) Plaats toepaste, zou het de volgende berekening gebruiken:

```text
(30 + 10) / 1 = 40 seconds average time on site
```

Aangezien er één sequentie in de afsplitsingsdimensie was, gebruikt deze een andere noemer dan de bovenliggende dimensie. Deze meetgegevens leveren doorgaans vergelijkbare resultaten op bezoekniveau op, maar kunnen verschillen op raakniveau.

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de gemiddelde tijd van de volledige afmeting ter plaatse, en de teller is de gemiddelde tijd van het afmetingspunt op plaats. Als de gemiddelde tijd van de volledige afmeting op plaats lager is dan de gemiddelde tijd van een bepaald afmetingspunt op plaats, zult u percentages boven 100% zien. Door gerangschikte rapporten te sorteren op deze metrische waarde wordt een afwijkende gemiddelde tijd op plaatswaarden getoond, die typisch niet waardevol is. Adobe raadt u aan om in gerangschikte rapporten een andere waarde in te voeren, zoals [Visits](visits.md).

Zie [Tijd besteed overzicht](time-spent.md) voor meer algemene informatie over bestede tijd.
