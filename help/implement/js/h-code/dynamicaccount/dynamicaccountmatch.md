---
title: dynamicAccountMatch
description: De variabele dynamicAccountMatch bepaalt naar welke waarde in dynamische accounts moet worden gekeken.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Launch.

De `dynamicAccountMatch` variabele is de waarde die de waarden `dynamicAccountList` bekijkt en vergelijkt. Wanneer `dynamicAccountSelection` deze variabele niet is ingesteld op `true`, wordt deze genegeerd.

Wanneer deze variabele niet is gedefinieerd, is de standaardwaarde `window.location.host`.

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

* Voor pagina&#39;s die op een vaste schijf worden opgeslagen, zijn geen verschillende `location` variabelen gedefinieerd ( `location.host` is bijvoorbeeld leeg). Zorg ervoor `s_account` bevat een standaardrapportreeks.
* Wanneer een pagina wordt vertaald via een vertaalengine op het web, zoals Google, werkt het selecteren van dynamische accounts niet naar behoren. Vul de `s_account` variabele server-side in voor nauwkeuriger tracering.
