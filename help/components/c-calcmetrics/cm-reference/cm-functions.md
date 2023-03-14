---
description: Met de Calculated Metrics Builder kunt u statistische en wiskundige functies toepassen om geavanceerde berekende metriek te bouwen.
title: Referentie van basisfuncties
feature: Calculated Metrics
exl-id: 1a49435c-96d1-4617-bd1a-a5d3b74e3ebd
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 1%

---

# Referentie: basisfuncties

Met de Calculated Metrics Builder kunt u statistische en wiskundige functies toepassen om geavanceerde berekende metriek te bouwen.

Hier volgt een alfabetische lijst van de functies en hun definities.

>[!NOTE]
>
>Wanneer [!DNL metric] wordt geïdentificeerd als een argument in een functie, worden andere expressies van metriek ook toegestaan. Bijvoorbeeld: [!DNL MAXV(metrics)] staat ook [!DNL MAXV(PageViews + Visits)].

## Tabelfuncties versus rijfuncties {#section_8977BE40A47E4ED79EB543A9703A4905}

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is.

## Absolute waarde (rij) {#concept_4CC47884F7CA49D5B84AC898EA596673}

Retourneert de absolute waarde van een getal. De absolute waarde van een getal is het getal met een positieve waarde.

```
ABS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de absolute waarde wilt. |

## Maximum kolom {#concept_B25518D717D24F82B65CDE49A153D3A3}

Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. MAXV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen.

```
MAXV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Minimaal kolom {#concept_5B1033F8ACE9485F9AD3CDC0D146391B}

Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. MINV evalueert verticaal binnen één enkele kolom (metrisch) over afmetingselementen.

```
MINV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Aantal kolommen {#concept_391F04FBC3CC43368CA0C5AACE74D4B1}

Voegt alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toe.

```
SUM(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de totale waarde of som wilt. |

## Aantal (tabel) {#concept_2C6ED2B88AB74481BD130969FB071A41}

Retourneert het aantal of het aantal niet-nulwaarden voor een metrische waarde binnen een kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd).

```
COUNT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde die u wilt tellen. |

## Exponent (rij) {#concept_17554F9D234449FB8DDEE895816B3FF1}

Retourneert *e* verhoogd tot de macht van een bepaald getal. De constante *e* is gelijk aan 2,71828182845904, de basis van de natuurlijke logaritme. EXP is het omgekeerde van LN, de natuurlijke logaritme van een aantal.

```
EXP(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De exponent die op de basis wordt toegepast *e*. |

## Uitstel {#concept_941578534F1E4583B1BEB067C8113A21}

Power Operator

```
pow(x,y) = x<sup>y</sup> = x*x*x*… (y times)
```

## Gemiddeld (tabel) {#concept_F4FF950580304D0B99DA7FBB5DB8730A}

Retourneert het rekenkundig gemiddelde (of gemiddelde) voor een metrische waarde in een kolom.

```
MEAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u het gemiddelde wilt. |

## Mediaan (tabel) {#concept_183EC31208524EDB8463D986DE2E895F}

Retourneert de mediaan voor een metrische waarde in een kolom. De mediaan is het getal in het midden van een reeks getallen, dat wil zeggen dat de helft van de getallen waarden heeft die groter zijn dan of gelijk zijn aan de mediaan, en de helft kleiner dan of gelijk is aan de mediaan.

```
MEDIAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de mediaan wilt. |

## Modulo {#concept_DE0825D7A51643219CB01F59667EA352}

The rest of col1 / col2, using Euclidean Division.

Retourneert de rest na het delen van x door y.

```
x = floor(x/y) + modulo(x,y)
```

De geretourneerde waarde heeft hetzelfde teken als de invoer (of is nul).

```
modulo(4,3) = 1 
modulo(-4,3) = -1 
modulo(-3,3) = 0
```

Als u altijd een positief getal wilt ophalen, gebruikt u

```
modulo(modulo(x,y)+y,y)
```

## Percentage (tabel) {#concept_51DF57B606D14F898E5010DBA61CA979}

Retourneert het k-th-percentiel van waarden voor een metrische waarde. U kunt deze functie gebruiken om een acceptatiedrempel vast te stellen. U kunt bijvoorbeeld afmetingselementen bekijken die boven het 90-percentiel liggen.

```
PERCENTILE(metric,k)
```

| Argument | Beschrijving |
| --- | --- |
| *metrisch* | De metrische kolom die relatieve status definieert. |
| *k* | De percentielwaarde in het bereik 0 tot en met 100. |

## Kwartaal (tabel) {#concept_BFD37F0F23A24AD181407142233FA151}

Retourneert de kwartiel van waarden voor een metrische waarde. Bijvoorbeeld, kunnen de kwartielen worden gebruikt om de hoogste 25% van producten te vinden die de meeste opbrengst drijven. MINV, MEDIAN en MAXV retourneren dezelfde waarde als QUARTILE wanneer quart gelijk is aan respectievelijk 0 (nul), 2 en 4.

```
QUARTILE(metric,quart)
```

| Argument | Beschrijving |
| --- | --- |
| *metrisch* | De metrische waarde waarvoor u de kwartielwaarde wilt. |
| *kwart* | Geeft aan welke *value moet worden geretourneerd. |

&#42;Indien *kwart* = 0, QUARTILE keert de minimumwaarde terug. Indien *kwart* = 1, QUARTILE retourneert het eerste kwartiel (25 percentiel). Indien *kwart* = 2, retourneert QUARTILE het eerste kwartiel (50 percentiel). Indien *kwart* = 3, QUARTILE retourneert het eerste kwartiel (75 percentiel). Indien *kwart* = 4, QUARTILE keert de maximumwaarde terug.

## Rond {#concept_2F12F2A6ACD445A0A8FF648AE4D4CB9E}

Geeft als resultaat het dichtstbijzijnde gehele getal voor een bepaalde waarde. Als u bijvoorbeeld wilt voorkomen dat decimalen van valuta worden gerapporteerd voor de omzet en een product $569,34 heeft, gebruikt u de formule Round( *Ontvangsten*) om de omzet naar de dichtstbijzijnde dollar te afronden, ofwel $569. Een product dat $569,51 rapporteert, wordt afgerond naar de dichtstbijzijnde dollar, ofwel $570.

```
ROUND(metric)
```

| Argument | Beschrijving |
|---|---|
| *getal* | De metrische waarde die u wilt afronden. |

Afgerond zonder een cijfers parameter is het zelfde als rond met een cijfers parameter van 0, namelijk rond aan het dichtstbijzijnde geheel. Met een cijferparameter keert het dat vele cijfers rechts van decimaal terug. Als cijfers negatief zijn, keert het 0&#39;s links van decimaal terug.

```
round( 314.15, 0) = 314
round( 314.15, 1) = 314.1
round( 314.15, -1) = 310
round( 314.15, -2) = 300
```

## Aantal rijen {#concept_0DBF5995881C47CF95F793125F3A0E2B}

Geeft als resultaat het aantal rijen voor een bepaalde kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd). &quot;Onkruisen&quot; wordt geteld als 1.

## Max. rij {#concept_984D045D7EDD4A1ABED454CDF2EC23C5}

Het maximum van de kolommen in elke rij.

## Min. rij {#concept_A6FB9E72C70A43D0B31565E70B8122BD}

Het minimum van de kolommen in elke rij.

## Rijsom {#concept_E9EAB0FC5233498F907E7A078698A98E}

De som van de kolommen van elke rij.

## Vierkante hoofdmap (rij) {#concept_6460DFA51EC24527A2317970FB76D404}

Retourneert de positieve vierkantswortel van een getal. De vierkantswortel van een getal is de waarde van dat getal dat tot de macht 1/2 wordt verheven.

```
SQRT(metric)
```

| Argument | Beschrijving |
| --- | --- |
| *getal* | De metrische waarde waarvoor u de vierkantswortel wilt. |

## Standaardafwijking (tabel) {#concept_A383A8BCC6FA42D7B73F7C83997D782A}

Retourneert de standaardafwijking of vierkantswortel van de variantie, gebaseerd op een samplepopulatie van gegevens.

De vergelijking voor STDEV is:

![](assets/std_dev.png)

Wanneer *x* de waarde van elk monster (*metrisch*), *x̄* is de gemiddelde bevolking en *n* is de bevolkingsgrootte.

```
STDEV(metric)
```

| Argument | Beschrijving |
| --- | --- |
| *metrisch* | De metrische waarde waarvoor u standaardafwijking wilt. |

## Variantie (tabel) {#concept_269751EDC5A34E689112AE16E04A11B0}

Geeft de variantie gebaseerd op een samplepopulatie van gegevens.

De vergelijking voor VARIANCE is:

![](assets/variance_eq.png)

Wanneer *x* de waarde van elk monster (*metrisch*), *x̄* is de gemiddelde bevolking en *n* is de bevolkingsgrootte.

```
VARIANCE(metric)
```

| Argument | Beschrijving |
| --- | --- |
| *metrisch* | De metrische waarde waarvoor u de variantie wilt. |

Als u een variantie wilt berekenen, bekijkt u een hele kolom met getallen. Van die lijst van aantallen berekent u eerst het gemiddelde. Zodra u het gemiddelde hebt gaat u door elke ingang en doet het volgende:

1. Trek het gemiddelde van het getal af.
1. Maak het resultaat vierkant.
1. Voeg dat toe aan het totaal.

Als u de hele kolom hebt doorlopen, hebt u één totaal. Vervolgens deelt u dat totaal door het aantal items in de kolom. Dat getal is de variantie voor de kolom. Het is een enkel getal. Deze wordt echter weergegeven als een kolom met getallen.

Als voorbeeld, laten wij zeggen u een drie-puntenkolom hebt:

1

2

3

Het gemiddelde van deze kolom is 2. De variantie voor de kolom is ((1 - 2)² + (2 - 2)² + (3 - 2)²/3 = 2/3.
