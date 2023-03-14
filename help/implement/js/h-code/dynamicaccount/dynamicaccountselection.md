---
title: dynamicAccountSelection
description: Met de variabele dynamicAccountSelection kunt u dynamische accountselectie in- of uitschakelen.
feature: Implementation Basics
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Data Collection.

De `dynamicAccountSelection` variabele is een Booleaanse waarde die bepaalt of de dynamische accountselectie wordt gebruikt.

Indien ingesteld op `true`, kijkt het JavaScript-bestand naar `dynamicAccountMatch` en `dynamicAccountList`.

Indien ingesteld op `false`of als deze variabele niet is gedefinieerd, wordt de `dynamicAccountMatch` en `dynamicAccountList` variabelen worden genegeerd.

Als deze variabele niet is gedefinieerd, is de standaardwaarde `false`.

## Syntaxis

```js
s.dynamicAccountSelection = [boolean];
```

## Voorbeeld

```js
s.dynamicAccountSelection = true;
```
