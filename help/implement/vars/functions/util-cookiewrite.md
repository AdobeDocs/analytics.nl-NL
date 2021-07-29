---
title: Util.cookieWrite
description: Schrijft een waarde voor een cookie.
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# Util.cookieWrite

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de methode `Util.cookieWrite()` om een waarde in te stellen op een cookie. Met de methode [`Util.cookieRead()`](util-cookieread.md) kunt u waarden ophalen die zijn ingesteld met `Util.cookieWrite()`.

## Cookies instellen met tags in Adobe Experience Platform

De UI van de Inzameling van Gegevens verstrekt niet de capaciteit om koekjes in de interface te plaatsen. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.Util.cookieWrite() in AppMeasurement en aangepaste code-editor

Roep de methode `s.Util.cookieWrite()` aan om een koekje aan een gewenste waarde te plaatsen.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

Er is een optioneel derde argument beschikbaar dat bepaalt wanneer het cookie verloopt. Cookies die zijn ingesteld met `s.Util.cookieWrite()` verlopen standaard aan het einde van de browsersessie.

```js
// Set a cookie with an expiration 6 months from now
var cookieDate = new Date();
cookieDate.setMonth(cookieDate.getMonth() + 6);
s.Util.cookieWrite("example_cookie","Example 6-month cookie",cookieDate);
```

## Voorbeelden

U kunt een variabele instantiëren wanneer het schrijven van een cookie is geslaagd. Deze variabele is een booleaanse waarde.

```js
var success = s.Util.cookieWrite("example_cookie","Example cookie value");
if (success) {
  console.log("Cookie written successfully");
} else {
  console.log("Cookie write failed");
}
```
