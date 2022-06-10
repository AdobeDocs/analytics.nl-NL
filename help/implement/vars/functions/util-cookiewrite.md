---
title: Util.cookieWrite
description: Schrijft een waarde voor een cookie.
feature: Variables
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# Util.cookieWrite

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de `Util.cookieWrite()` methode om een waarde in te stellen op een cookie. U kunt de [`Util.cookieRead()`](util-cookieread.md) methode om waarden op te halen die zijn ingesteld met `Util.cookieWrite()`.

## Cookies instellen met de extensie Adobe Analytics en de extensie Web SDK

Met de gegevensverzameling van Adobe Experience Platform kunt u geen cookies instellen in de interface.

## s.Util.cookieWrite() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de `s.Util.cookieWrite()` een methode om een cookie in te stellen op de gewenste waarde.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

Er is een optioneel derde argument beschikbaar dat bepaalt wanneer het cookie verloopt. Cookies ingesteld met `s.Util.cookieWrite()` verlopen standaard aan het einde van de browsersessie.

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
