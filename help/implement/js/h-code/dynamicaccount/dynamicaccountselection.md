---
title: dynamicAccountSelection
description: Met de variabele dynamicAccountSelection kunt u dynamische accountselectie in- of uitschakelen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# dynamicAccountSelection

> [!IMPORTANT] Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Launch.

De `dynamicAccountSelection` variabele is een Booleaanse waarde die bepaalt of een dynamische accountselectie wordt gebruikt.

Als dit is ingesteld op `true`, zoekt het JavaScript-bestand naar `dynamicAccountMatch` en `dynamicAccountList`.

Indien ingesteld op `false`, of indien deze variabele niet is gedefinieerd, worden de `dynamicAccountMatch` en `dynamicAccountList` variabelen genegeerd.

Als deze variabele niet is gedefinieerd, is de standaardwaarde `false`.

## Syntaxis

```js
s.dynamicAccountSelection = [boolean];
```

## Voorbeeld

```js
s.dynamicAccountSelection = true;
```
