---
title: decodeLinkParameters
description: Schakel AppMeasurement dubbele codering van koppelingsvolgvariabelen in of uit.
exl-id: 7a4cea23-5ae6-4a8b-82a6-c68f9a1f9c49
feature: Variables
source-git-commit: 53f4048db02331e807edd4d55311861d2350efe3
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# decodeLinkParameters

De `decodeLinkParameters` variable is a boolean that determines if link tracking variables get encoded once (if set to `true`) of tweemaal (indien ingesteld op `false`). Alleen effecten `linkName` (deel van de [`tl()`](../functions/tl-method.md) methode) en [`linkURL`](linkurl.md). Voor gebruik is AppMeasurement 2.23.1 of hoger vereist. De standaardwaarde van deze variabele is `false`.

In eerdere versies van AppMeasurement waren koppelingsvolgvariabelen altijd twee keer gecodeerd met URL. Hoewel dit geen probleem is voor implementaties die doorgaans vertrouwen op single-bytetekens, zijn met de dubbele codering onjuist gecodeerde waarden voor multi-bytetekens in rapporten gemaakt. Deze variabele instellen op `true` codeert de waarden voor het bijhouden van koppelingen eenmaal. Dit is doorgaans het gewenste gedrag.

* Als in uw implementatie multibyte-tekens worden gebruikt en de variabelen voor het bijhouden van koppelingen URL-gedecodeerd zijn om de dubbele codering van het AppMeasurement te verschuiven, stelt u deze variabele in op `false`. Met deze waarde blijft de bestaande functionaliteit van het AppMeasurement behouden.
* Als in uw implementatie multibyte-tekens worden gebruikt en u geen URL-waarden voor het bijhouden van koppelingen gebruikt, raadt Adobe aan deze variabele in te stellen op `true`.
* Als in uw implementatie geen multi-bytetekens worden gebruikt, is deze variabele niet vereist. Adobe raadt echter aan deze variabele in te stellen op `true` in gevallen waarin multi-byte tekens kunnen worden verzonden.

## Codeer verbindings parameters gebruikend het Web SDK tweemaal

Deze variabele is specifiek voor AppMeasurement, en is niet nodig in om het even welk type van implementatie van SDK van het Web.

## Koppelingsparameters dubbel coderen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.decodeLinkParameters in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.decodeLinkParameters` variable is a boolean that determines if link tracking values get double encoded. Als deze variabele niet is gedefinieerd, is de standaardwaarde `false` om functionaliteit voor bestaande implementaties te behouden. Adobe raadt u aan deze waarde in te stellen op `true` voor alle nieuwe implementaties, vooral als u URL gecodeerde waarden in verbinding het volgen rapporten ziet.

```js
s.decodeLinkParameters = true;
```
