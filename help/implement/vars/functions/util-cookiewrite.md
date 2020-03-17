---
title: Util.cookieWrite
description: Schrijft een waarde voor een cookie.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Util.cookieWrite

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de `Util.cookieWrite` methode om een waarde in te stellen op een cookie. U kunt de `Util.cookieRead` methode gebruiken om waarden terug te winnen die gebruikend worden geplaatst `Util.cookieWrite`.

## Cookies instellen in Adobe Experience Platform Launch

Het starten biedt niet de mogelijkheid cookies in de interface in te stellen. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.Util.cookieWrite() in de aangepaste code-editor AppMeasurement en Launch

Roep de `s.Util.cookieWrite()` methode aan om een koekje aan een gewenste waarde te plaatsen.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

Er is een optioneel derde argument beschikbaar dat bepaalt wanneer het cookie verloopt. Cookies die zijn ingesteld met gebruik van `s.Util.cookieWrite()` verlopen standaard aan het einde van de browsersessie.

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
