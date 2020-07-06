---
title: dynamicAccountSelection
description: Met de variabele dynamicAccountSelection kunt u dynamische accountselectie in- of uitschakelen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# dynamicAccountSelection

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Launch.

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
