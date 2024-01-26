---
title: dynamicAccountSelection
description: Met de variabele dynamicAccountSelection kunt u dynamische accountselectie in- of uitschakelen.
feature: Implementation Basics
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige bibliotheken van AppMeasurementen of Adobe Experience Platform-gegevensverzameling.

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
