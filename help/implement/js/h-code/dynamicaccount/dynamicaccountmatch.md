---
title: dynamicAccountMatch
description: De variabele dynamicAccountMatch bepaalt naar welke waarde in dynamische accounts moet worden gekeken.
feature: Implementation Basics
exl-id: 3b68f2e6-1bd9-4b16-9d03-a87c9217e1b7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of -tags in Adobe Experience Platform.

De `dynamicAccountMatch` variabele is de waarde die `dynamicAccountList` bekijkt en vergelijkt zijn waarden. Indien `dynamicAccountSelection` is niet ingesteld op `true`, wordt deze variabele genegeerd.

Als deze variabele niet is gedefinieerd, is de standaardwaarde `window.location.host`.

## Syntaxis

```js
s.dynamicAccountMatch=[DOM object]
```

## Voorbeelden

```js
// Look at the URL path to determine report suite
s.dynamicAccountMatch = location.pathname;

// Use a query string
s.dynamicAccountMatch = location.search;

// Use the full URL
s.dynamicAccountMatch = location.href;

// Use concatenated variables
s.dynamicAccountMatch =  location.hostname + location.pathname + location.search;
```

## Aanvullende opmerkingen

* Pagina&#39;s die zijn opgeslagen op een vaste schijf hebben niet meerdere `location` gedefinieerde variabelen (bijvoorbeeld `location.host` is leeg). Controleer of `s_account` bevat een standaardrapportsuite.
* Wanneer een pagina wordt vertaald via een vertaalengine op het web, zoals Google, werkt het selecteren van dynamische accounts niet naar behoren. Vul de optie `s_account` variabele server-kant.
