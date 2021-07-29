---
title: dynamicAccountSelection
description: Met de variabele dynamicAccountSelection kunt u dynamische accountselectie in- of uitschakelen.
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of de gebruikersinterface voor gegevensverzameling.

De variabele `dynamicAccountSelection` is een Booleaanse waarde die bepaalt of een dynamische accountselectie wordt gebruikt.

Als dit is ingesteld op `true`, zoekt het JavaScript-bestand naar `dynamicAccountMatch` en `dynamicAccountList`.

Indien ingesteld op `false`, of als deze variabele niet is gedefinieerd, worden de variabelen `dynamicAccountMatch` en `dynamicAccountList` genegeerd.

Als deze variabele niet is gedefinieerd, is de standaardwaarde `false`.

## Syntaxis

```js
s.dynamicAccountSelection = [boolean];
```

## Voorbeeld

```js
s.dynamicAccountSelection = true;
```
