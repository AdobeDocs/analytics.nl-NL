---
title: Basisfuncties
description: Meer informatie over berekende standaardmeetkundige functies.
feature: Calculated Metrics
exl-id: 63775753-337b-4dec-a3a2-a3a0ee9aac2e
role: User
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 1%

---

# Basisfuncties


De [ Berekende metrieke bouwer ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) laat u statistische en wiskundige functies toepassen. Dit artikel documenteert alfabetische lijst van de functies en hun definities.

>[!NOTE]
>
>Waar [!DNL metric] wordt geïdentificeerd als een argument in een functie, zijn andere expressies van metriek ook toegestaan. Bijvoorbeeld, [ MAXIMUM VAN DE KOLOM (metriek) ](#column-maximum) staat ook voor [ MAXIMUM VAN DE KOLOM (PageViews + Visits) ](#column-maximum) toe.



## Tabelfuncties versus rijfuncties

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is.

Waar toepasselijk en relevant, is een functie geannoteerd met het type van functie: [!BADGE  Lijst ]{type="Neutral"} of [!BADGE  Rij ]{type="Neutral"}

## Wat betekent de parameter include-zeros?

Het vertelt of nullen in de berekening moeten worden opgenomen. Soms betekent nul *niets*, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en dan metrische vertoningen van de Pagina aan het rapport toevoegt, zijn er plotseling meer rijen voor uw opbrengst, die allen nul zijn. U wilt waarschijnlijk niet dat extra metrisch om het even welke **[MEAN](cm-functions.md#mean)**, **[MINIMUM VAN DE RIJ](cm-functions.md#row-min)**, **[KWALITEIT](cm-functions.md#quartile)**, en meer berekeningen te beïnvloeden die u in de opbrengstkolom hebt. In dit geval controleert u de parameter `include-zeros` .

Een alternatief scenario is dat u twee metriek van rente hebt en één een hoger gemiddelde of een minimum heeft omdat sommige rijen nul zijn.  In dat geval kunt u ervoor kiezen om de parameter niet te controleren en nullen op te nemen



## Absolute waarde {#absolute-value}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-abs"
>title="Absolute waarde"
>abstract="Retourneert de absolute waarde van een getal. De absolute waarde van een getal is het getal met een positieve waarde."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ABSOLUTE VALUE(metric)]**

[!BADGE  Rij ]{type="Neutral"} keert de absolute waarde van een aantal terug. De absolute waarde van een getal is het getal met een positieve waarde.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de absolute waarde wilt berekenen. |


## Maximum kolom {#column-maximum}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-col-max"
>title="Maximum kolom"
>abstract="Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. MAXV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL COLUMN MAXIMUM(metric, include_zeros)]**

Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. MAXV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Minimaal kolom {#column-minimum}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-col-min"
>title="Minimaal kolom"
>abstract="Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. MINV evalueert verticaal binnen één enkele kolom (metrisch) over afmetingselementen."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL COLUMN MINIMUM(metric, include_zeros)]**

Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. MINV evalueert verticaal binnen één enkele kolom (metrisch) over afmetingselementen.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Aantal kolommen {#column-sum}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-col-sum"
>title="Aantal kolommen"
>abstract="Voegt alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toe."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL COLUMN SUM(metric)]**

Voegt alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toe.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |


## Aantal {#count}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-count"
>title="Aantal"
>abstract="Retourneert het aantal of het aantal niet-nulwaarden voor een metrische waarde binnen een kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd)."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL COUNT(metric)]**

[!BADGE  Lijst ]{type="Neutral"} keert het aantal, of de telling, van niet-nul waarden voor metrisch binnen een kolom (het aantal unieke die elementen terug binnen een dimensie worden gemeld).

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde die u wilt tellen. |


## Exponent {#exponent}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-exp"
>title="Exponent"
>abstract="Retourneert e verhoogd tot de macht van een bepaald getal. De constante e is gelijk aan 2,71828182845904, de basis van de natuurlijke logaritme. EXPONENT is het omgekeerde van LN, de natuurlijke logaritme van een getal."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EXPONENT(metric)]**

[!BADGE  Keert de Rij ]{type="Neutral"} terug wordt opgeheven aan de macht van een bepaald aantal. De constante e is gelijk aan 2,71828182845904, de basis van de natuurlijke logaritme. EXPONENT is het omgekeerde van LN, de natuurlijke logaritme van een getal.

| Argument | Beschrijving |
|---|---|
| metrisch | De exponent die op de basis e wordt toegepast. |


## Gemiddeld {#mean}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-mean"
>title="Gemiddeld"
>abstract="Retourneert het rekenkundig gemiddelde (of gemiddelde) voor een metrische waarde in een kolom."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL MEAN(metric, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert het rekenkundig gemiddelde, of het gemiddelde, voor metrisch in een kolom terug.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u het gemiddelde wilt berekenen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Mediaan {#median}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-median"
>title="Mediaan"
>abstract="Retourneert de mediaan voor een metrische waarde in een kolom. De mediaan is het getal in het midden van een reeks getallen. De helft van de getallen heeft waarden die groter zijn dan of gelijk zijn aan de mediaan, en de helft is kleiner dan of gelijk aan de mediaan."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL MEDIAN(metric, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert mediaan voor metrisch in een kolom terug. De mediaan is het getal in het midden van een reeks getallen. De helft van de getallen heeft waarden die groter zijn dan of gelijk zijn aan de mediaan, en de helft is kleiner dan of gelijk aan de mediaan.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de mediaan wilt berekenen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Modulo {#modulo}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-modulo"
>title="Modulo"
>abstract="Retourneert de rest na het delen van x door y met behulp van Euclidean-divisie. "

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL MODULO(metric_X, metric_Y)]**

Retourneert de rest na het delen van x door y met behulp van Euclidean-divisie.

| Argument | Beschrijving |
|---|---|
| metrisch_X | De eerste metrische waarde die u wilt delen. |
| metrisch_Y | De tweede metrische waarde die u wilt verdelen. |

### Voorbeelden

De geretourneerde waarde heeft hetzelfde teken als de invoer (of is nul).

```
MODULO(4,3) = 1
MODULO(-4,3) = -1
MODULO(-3,3) = 0
```

Om ervoor te zorgen dat u altijd een positief getal krijgt, gebruikt u

```
MODULO(MODULO(x,y)+y,y)
```

## Percentage {#percentile}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-percentile"
>title="Percentage"
>abstract="Retourneert het nde percentiel. Dit is een waarde tussen 0 en 100. Wanneer n &lt; 0, gebruikt de functie nul. Wanneer n > 100, keert de functie 100 terug."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL PERCENTILE(metric, k, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert het nde percentiel terug, dat een waarde tussen 0 en 100 is. Wanneer n &lt; 0, gebruikt de functie nul. Wanneer n > 100, keert de functie 100 terug.

| Argument | Beschrijving |
|---|---|
| metrisch | De percentielwaarde in het bereik 0 tot en met 100. |
| k | De metrische kolom die relatieve status definieert. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |



## Power Operator {#power-operator}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-pow"
>title="Power Operator"
>abstract="Retourneert x opgevoerd naar de y-macht."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL POWER OPERATOR(metric_X, metrix_Y)]**

Retourneert x opgevoerd naar de y-macht.

| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u aan de macht wilt verhogen measured_Y. |
| metrisch_Y | De macht u zou willen verhogen metrisch_X aan. |


## Kwart {#quartile}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-quartile"
>title="Kwart"
>abstract="Retourneert de kwartiel van waarden voor een metrische waarde. Bijvoorbeeld, kunnen de kwartielen worden gebruikt om de hoogste 25% van producten te vinden die de meeste opbrengst drijven."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL QUARTILE(metric, quartile, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert de kwartiel van waarden voor metrisch terug. Bijvoorbeeld, kunnen de kwartielen worden gebruikt om de hoogste 25% van producten te vinden die de meeste opbrengst drijven. [ MINIMUM VAN DE KOLOM ](#column-minimum), [ GEMIDDELD ](#median), en [ MAXIMUM VAN DE KOLOM ](#column-maximum) keren de zelfde waarde terug zoals [ KWALITEIT ](#quartile) wanneer kwartiel aan `0` (nul) gelijk is, `2`, en `4`, respectievelijk.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de kwartielwaarde wilt berekenen. |
| kwartiel | Geeft aan welke kwartielwaarde moet worden geretourneerd. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Rond {#round}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-round"
>title="Rond"
>abstract="Rond zonder a *aantal* parameter is het zelfde als rond met a *aantal* parameter van 0, namelijk rond aan het dichtstbijzijnde geheel.  Met a *aantal* parameter, ROUND keert de *aantal* cijfers rechts van decimaal terug.  Als *aantal* negatief is, keert het 0&#39;s links van decimaal terug."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ROUND(metric, number)]**

Rond zonder a *aantal* parameter is het zelfde als rond met a *aantal* parameter van 0, namelijk rond aan het dichtstbijzijnde geheel.  Met a *aantal* parameter, ROUND keert de *aantal* cijfers rechts van decimaal terug.  Als *aantal* negatief is, keert het 0&#39;s links van decimaal terug.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde die u wilt afronden. |
| getal | Hoeveel cijfers rechts van decimaal om terug te keren. (Als negatief nul links van decimaal terugkeert). |

### Voorbeelden

```
ROUND( 314.15, 0) = 314
ROUND( 314.15, 1) = 314.1
ROUND( 314.15, -1) = 310
ROUND( 314.15, -2) = 300
```

## Aantal rijen {#row-count}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-count-rows"
>title="Aantal rijen"
>abstract="Geeft als resultaat het aantal rijen voor een bepaalde kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd). *meer uniques* wordt geteld als 1."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ROW COUNT()]**

Geeft als resultaat het aantal rijen voor een bepaalde kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd). *meer uniques* wordt geteld als 1.


## Max. rij {#row-max}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-row-max"
>title="Max. rij"
>abstract="Maximaal aantal kolommen per rij."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ROW MAX(metric, include_zeros)]**

Maximaal aantal kolommen per rij.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Min. rij {#row-min}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-row-min"
>title="Min. rij"
>abstract="Minimaal van de kolommen van elke rij."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ROW MIN(metric, include_zeros)]**

Minimaal van de kolommen van elke rij.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |



## Rijsom {#row-sum}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-row-sum"
>title="Rijsom"
>abstract="Som van de kolommen van elke rij."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ROW SUM(metric, include_zeros)]**

Som van de kolommen van elke rij.

| Argument | Beschrijving |
|---|---|
| metrisch | Vereist minstens één metrisch maar kan om het even welk aantal metriek als parameters nemen. |


## Vierkante hoofdmap {#square-root}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-sqrt"
>title="Vierkante hoofdmap"
>abstract="Retourneert de positieve vierkantswortel van een getal. De vierkantswortel van een getal is de waarde van dat getal dat tot de macht 1/2 wordt verheven."

<!-- markdownlint-enable MD034 -->


![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL SQUARE ROOT(metric, include_zeros)]**

[!BADGE  Rij ]{type="Neutral"} keert de positieve vierkantswortel van een aantal terug. De vierkantswortel van een getal is de waarde van dat getal dat tot de macht 1/2 wordt verheven.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de vierkantswortel wilt berekenen. |


## Standaardafwijking {#standard-deviation}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-stdev"
>title="Standaardafwijking"
>abstract="Retourneert de standaardafwijking, of vierkantswortel van de variantie, gebaseerd op een samplepopulatie van gegevens."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL STANDARD DEVIATION(metric, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert de standaardafwijking, of de vierkantswortel van de variantie terug, die op een steekproefpopulatie van gegevens wordt gebaseerd.

| Argument | Beschrijving |
|---|---|
| | De metrische waarde waarvoor u de standaardafwijking wilt berekenen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


## Variantie {#variance}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="functions-variance"
>title="Variantie"
>abstract="Geeft de variantie gebaseerd op een samplepopulatie van gegevens."

<!-- markdownlint-enable MD034 -->

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL VARIANCE(metric, include_zeros)]**

[!BADGE  Lijst ]{type="Neutral"} keert de variantie terug die op een steekproefpopulatie van gegevens wordt gebaseerd.

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de variantie wilt berekenen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen. |


De vergelijking voor VARIANCE is:

![](assets/variance_eq.png){width="100"}

Waar *x* het steekproefmiddel is, [ MEAN (*metrisch*) ](#mean), en *n* is de steekproefgrootte.


Als u een variantie wilt berekenen, bekijkt u een hele kolom met getallen. Van die lijst van aantallen berekent u eerst het gemiddelde. Zodra u het gemiddelde hebt, gaat u door elke ingang en doet het volgende:

1. Trek het gemiddelde van het getal af.

1. Maak het resultaat vierkant.

1. Voeg dat toe aan het totaal.

Nadat u de hele kolom hebt doorlopen, hebt u één totaal. Vervolgens deelt u dat totaal door het aantal items in de kolom. Dat getal is de variantie voor de kolom. Het is een enkel getal. Deze wordt echter weergegeven als een kolom met getallen.

In het voorbeeld van de volgende kolom met drie items:

| kolom |
|:---:|
| 1 |
| 2 |
| 3 |

Het gemiddelde van deze kolom is 2. De variantie voor de kolom is ((1 - 2) <sup> 2 </sup> + (2 - 2) <sup> </sup> + (3 - 2) <sup> 2 </sup>/3) = 2/3.

<!--

## Absolute Value (Row)

Returns the absolute value of a number. The absolute value of a number is the number with a positive value.

```
ABS(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric for which you want the absolute value.  |

## Column Maximum

Returns the largest value in a set of dimension elements for a metric column. MAXV evaluates vertically within a single column (metric) across dimension elements.

```
MAXV(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | A metric that you would like to have evaluated.  |

## Column Minimum 

Returns the smallest value in a set of dimension elements for a metric column. MINV evaluates vertically within a single column (metric) across dimension elements.

```
MINV(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | A metric that you would like to have evaluated.  |

## Column Sum 

Adds all of the numeric values for a metric within a column (across the elements of a dimension).

```
SUM(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric for which you want the total value or sum.  |

## Count (Table) 

Returns the number, or count, of non-zero values for a metric within a column (the number of unique elements reported within a dimension).

```
COUNT(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric that you want to count.  |

## Exponent (Row) 

Returns *e* raised to the power of a given number. The constant *e* equals 2.71828182845904, the base of the natural logarithm. EXP is the inverse of LN, the natural logarithm of a number.

```
EXP(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The exponent applied to the base *e*.  |

## Exponentiation 

Power Operator


pow(x,y) = x<sup>y</sup> = x*x*x*… (y times)


## Mean (Table) 

Returns the arithmetic mean, or average, for a metric in a column.

```
MEAN(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric for which you want the average.  |

## Median (Table) 

Returns the median for a metric in a column. The median is the number in the middle of a set of numbers—that is, half the numbers have values that are greater than or equal to the median, and half are less than or equal to the median.

```
MEDIAN(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric for which you want the median.  |

## Modulo 

The remainder of col1 / col2, using Euclidean division.

Returns the remainder after dividing x by y.

```
x = floor(x/y) + modulo(x,y)
```

The return value has the same sign as the input (or is zero).

```
modulo(4,3) = 1 
modulo(-4,3) = -1 
modulo(-3,3) = 0
```

To always get a positive number, use 

```
modulo(modulo(x,y)+y,y)
```

## Percentile (Table) 

Returns the k-th percentile of values for a metric. You can use this function to establish a threshold of acceptance. For example, you can decide to examine dimension elements who score above the 90  percentile.

```
PERCENTILE(metric,k)
```

<table id="table_35CD840ACFB44CD9979881DB8823CC53"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argument </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>metric</i> </td> 
   <td colname="col2"> The metric column that defines relative standing. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> The percentile value in the range 0 to 100, inclusive. </td> 
  </tr> 
 </tbody> 
</table>

## Quartile (Table) 

Returns the quartile of values for a metric. For example, quartiles can be used to find the top 25% of products driving the most revenue. MINV, MEDIAN, and MAXV return the same value as QUARTILE when quart is equal to 0 (zero), 2, and 4, respectively.

```
QUARTILE(metric,quart)
```

<table id="table_64EA3DAAE77541439D59FAF0353F83A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argument </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>metric</i> </td> 
   <td colname="col2"> The metric for which you want the quartile value. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>quart </p> </td> 
   <td colname="col2"> Indicates which *value to return. </td> 
  </tr> 
 </tbody> 
</table>

&#42;If *quart* = 0, QUARTILE returns the minimum value. If *quart* = 1, QUARTILE returns the first quartile (25 percentile). If *quart* = 2, QUARTILE returns the first quartile (50 percentile). If *quart* = 3, QUARTILE returns the first quartile (75 percentile). If *quart* = 4, QUARTILE returns the maximum value.

## Round 

Returns the nearest integer for a given value. For example, if you want to avoid reporting currency decimals for revenue and a product has $569.34, use the formula Round( *Revenue*) to round revenue to the nearest dollar, or $569. A product reporting $569.51 will be round to the nearest dollar, or $570.

```
ROUND(metric)
```

|  Argument  | Description  |
|---|---|
|  *number* | The metric you want to round.  |

Round without a digits parameter is the same as round with a digits parameter of 0, namely round to the nearest integer. With a digits parameter it returns that many digits to the right of the decimal. If digits is negative, it returns 0's to the left of the decimal.

```
round( 314.15, 0) = 314 
round( 314.15, 1) = 314.1 
round( 314.15, -1) = 310 
round( 314.15, -2) = 300
```

## Row Count 

Returns the count of rows for a given column (the number of unique elements reported within a dimension). "Uniques exceeded" is counted as 1.

## Row Max 

The maximum of the columns in each row.

## Row Min 

The minimum of the columns in each row.

## Row Sum

The sum of the columns of each row.

## Square Root (Row) 

Returns the positive square root of a number. The square root of a number is the value of that number raised to the power of 1/2.

```
SQRT(metric)
```

|  Argument  | Description  |
|---|---|
|  *number* | The metric for which you want the square root.  |

## Standard Deviation (Table) 

Returns the standard deviation, or square root of the variance, based on a sample population of data.

The equation for STDEV is:

![](assets/std_dev.png)

where x is the sample mean (*metric*) and *n* is the sample size.

```
STDEV(metric)
```

<table id="table_8BCF2E4B02434AABAAD026FB3C4E8B2F"> 
 <tbody> 
  <tr> 
   <td> <b> Argument</b> </td> 
   <td> <b> Description</b> </td> 
  </tr> 
  <tr> 
   <td> <b> <i> metric</i> </b> </td> 
   <td> <p> The metric for which you want for standard deviation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variance (Table) 

Returns the variance based on a sample population of data.

The equation for VARIANCE is:

![](assets/variance_eq.png)

where x is the sample mean, MEAN(*metric*), and *n* is the sample size.

```
VARIANCE(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric for which you want the variance.  |

In order to calculate a variance you look at an entire column of numbers. From that list of numbers you first calculate the average. Once you have the average you go through each entry and do the following:

1. Subtract the average from the number.

2. Square the result.

3. Add that to the total.

Once you have iterated over the entire column you have a single total. You then divide that total by the number of items in the column. That number is the variance for the column. It is a single number. It is, however, displayed as a column of numbers.

In case of a three-item column:

1

2

3

The average of this column is 2. The variance for the column will be ((1 - 2)<sup>2</sup> + (2 - 2)<sup>2</sup> + (3 - 2)<sup>2</sup>/3 = 2/3.

-->