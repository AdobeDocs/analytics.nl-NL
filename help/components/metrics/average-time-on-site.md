---
title: Gemiddelde tijd op de site
description: De gemiddelde hoeveelheid tijd bestond een bepaald afmetingspunt tussen treffers.
feature: Metrics
exl-id: bf9056e2-4f6d-4c4f-b641-d3146ce269ff
source-git-commit: 7966c7d9add0011831c97fbe0dfcca2acd8afb58
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# Gemiddelde tijd op de site

De metrische waarde &#39;Gemiddelde tijd op site&#39; geeft de hoeveelheid tijd aan die tussen hits voor een bepaald afmetingsitem is verstreken. Dit metrisch is nuttig wanneer u gemiddelde tijd wilt zien die voor specifieke afmetingspunten wordt doorgebracht. U kunt metrisch in tijd ook trenderen om te zien hoe de algemene tijd bestede veranderingen. Deze metrische weergave wordt weergegeven in `HH:MM:SS` gebruiken.

Deze metrische waarde is gerelateerd aan de [Tijd besteed per bezoek](../dimensions/time-spent-per-visit.md) dimensie.

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


Als u een gemiddelde tijd op plaats voor het afmetingspunt wilt `Product page A`, neemt eerst de hoeveelheid tijd die tussen treffers voor die dimensie verstreek:

* **12:04:20 - 12:05:30** - 1 minuut 10 seconden
* **12:05:30 - 12:07:00** - 1 minuut 30 seconden
* **12:07:40 - 12:08:10** - 30 seconden
* **12:25:40 . ?** - Niet inbegrepen

De totale hoeveelheid tijd die is besteed voor `Product page A` is `00:03:10`. Dit bezoek heeft twee volgreeksen opgeleverd. de eerste reeks voor de twee opeenvolgende waarden en de tweede voor het uitchecken. Het laatste resultaat van het bezoek is geen opeenvolging, aangezien er geen eindtimestamp is.

De gemiddelde tijd op locatie voor `Product page A` is `00:01:35`.

>[!NOTE]
>
>Deze metrisch toont een waarde van `"Invalid"` als het dimensie-item alleen resultaten bevat die het laatst tijdens een bezoek zijn geweest. Deze metrisch vereist een verdere slag om bestede tijd te volgen.

## Gemiddelde tijd besteed aan plaats (seconden)

De metrische waarde &#39;Gemiddelde tijd besteed aan site (seconden)&#39; geeft dezelfde gegevens weer als een geheel getal in plaats van in `HH:MM:SS` gebruiken. Deze metrische waarde is het meest waardevol als component binnen berekende metriek.

## De totalen van de uitsplitsing komen niet overeen met het item van de bovenliggende regel

De metrische &#39;Gemiddelde tijd op locatie&#39; gebruikt ononderbroken reeksen van een bepaalde dimensie. De afbraakdimensie is niet afhankelijk van de bovenliggende dimensie bij het berekenen van deze reeksen. Neem bijvoorbeeld het volgende bezoek:

| `Timestamp` | `Page name` | `Site section` |
| --- | --- | --- |
| `12:00:00` | `Home` | `Foxes` |
| `12:00:30` | `Product` | `Foxes` |
| `12:02:10` | `Home` | `Foxes` |
| `12:02:20` | `(None; exit link click)` | `(None; exit link click)` |

Gemiddelde tijd op locatie berekenen voor het dimensie-item `Home` zou de volgende berekening gebruiken:

```text
(30 + 10) / 2 = 20 seconds average time on site
```

Als u een onderverdeling toepast met behulp van [Site-secties](../dimensions/site-section.md) afmeting, wordt de volgende berekening gebruikt:

```text
(30 + 10) / 1 = 40 seconds average time on site
```

Aangezien er één sequentie in de afsplitsingsdimensie was, gebruikt deze een andere noemer dan de bovenliggende dimensie. Deze meetgegevens leveren doorgaans vergelijkbare resultaten op bezoekniveau op, maar kunnen verschillen op raakniveau.

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de gemiddelde tijd van de volledige afmeting ter plaatse, en de teller is de gemiddelde tijd van het afmetingspunt op plaats. Als de gemiddelde tijd van de volledige afmeting op plaats lager is dan de gemiddelde tijd van een bepaald afmetingspunt op plaats, zult u percentages boven 100% zien. Door gerangschikte rapporten te sorteren op deze metrische waarde wordt een afwijkende gemiddelde tijd op plaatswaarden getoond, die typisch niet waardevol is. Adobe raadt aan om te sorteren met een andere waarde, zoals [Bezoeken](visits.md), in gerangschikte verslagen.

Zie [Overzicht van de tijd](time-spent.md) voor meer algemene informatie over de bestede tijd.
