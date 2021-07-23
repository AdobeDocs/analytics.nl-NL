---
title: dynamicAccountMatch
description: De variabele dynamicAccountMatch bepaalt naar welke waarde in dynamische accounts moet worden gekeken.
exl-id: 3b68f2e6-1bd9-4b16-9d03-a87c9217e1b7
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of -tags in Adobe Experience Platform.

De variabele `dynamicAccountMatch` is de waarde die `dynamicAccountList` bekijkt en zijn waarden vergelijkt. Wanneer `dynamicAccountSelection` niet is ingesteld op `true`, wordt deze variabele genegeerd.

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

* Op pagina&#39;s die op een vaste schijf worden opgeslagen, zijn niet meerdere `location`-variabelen gedefinieerd (`location.host` is bijvoorbeeld leeg). Zorg ervoor `s_account` een standaardrapportreeks bevat.
* Wanneer een pagina wordt vertaald via een vertaalengine op het web, zoals Google, werkt het selecteren van dynamische accounts niet naar behoren. Vul de variabele `s_account` aan de serverzijde voor nauwkeuriger tracering.
