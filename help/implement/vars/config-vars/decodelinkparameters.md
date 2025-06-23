---
title: decodeLinkParameters
description: Dubbelcoderingsvariabelen voor koppelingen bijhouden in- of uitschakelen.
exl-id: 329c521a-b965-4114-93ce-f45f159d4a20
feature: Appmeasurement Implementation
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# decodeLinkParameters

De `decodeLinkParameters` -variabele is een Booleaanse waarde die bepaalt of variabelen voor het bijhouden van koppelingen één keer (indien ingesteld op `true` ) of twee keer (indien ingesteld op `false` ) worden gecodeerd. Alleen van invloed op `linkName` (onderdeel van de methode [`tl()`](../functions/tl-method.md) ) en [`linkURL`](linkurl.md) . AppMeasurement v2.24.0 of hoger is vereist voor gebruik. De standaardwaarde van deze variabele is `false` .

In versies van AppMeasurement vóór v2.24.0 waren variabelen voor het bijhouden van koppelingen altijd twee keer gecodeerd met URL. Hoewel dit geen probleem is voor implementaties die doorgaans vertrouwen op single-bytetekens, zijn met de dubbele codering onjuist gecodeerde waarden voor multi-bytetekens in rapporten gemaakt. Als u deze variabele instelt op `true` , worden de waarden voor het bijhouden van koppelingen eenmaal gecodeerd. Dit is doorgaans het gewenste gedrag.

* Als in uw implementatie multibyte-tekens worden gebruikt en de variabelen voor het bijhouden van koppelingen URL zijn gedecodeerd om dubbele codering van AppMeasurement te compenseren, stelt u deze variabele in op `false` . Met deze waarde blijft de bestaande AppMeasurement-functionaliteit behouden.
* Als in uw implementatie multibyte-tekens worden gebruikt en u geen URL-waarden opgeeft voor het bijhouden van koppelingen, raadt Adobe aan deze variabele in te stellen op `true` .
* Als in uw implementatie geen multi-bytetekens worden gebruikt, is deze variabele niet vereist. Adobe raadt echter aan deze variabele in te stellen op `true` in gevallen waarin multi-byte tekens kunnen worden verzonden.

## Codeer verbindings parameters gebruikend het Web SDK tweemaal

Deze variabele is specifiek voor AppMeasurement, en is niet nodig in om het even welk type van implementatie van SDK van het Web.

## Koppelingsparameters dubbel coderen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.decodeLinkParameters in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De variabele `s.decodeLinkParameters` is een Booleaanse waarde die bepaalt of waarden voor het bijhouden van koppelingen dubbel worden gecodeerd. Als deze variabele niet is gedefinieerd, is de standaardwaarde `false` om de functionaliteit voor bestaande implementaties te behouden. Adobe raadt u aan deze waarde in te stellen op `true` voor alle nieuwe implementaties, vooral als u URL-gecodeerde waarden ziet in koppelingsrapporten.

```js
s.decodeLinkParameters = true;
```
