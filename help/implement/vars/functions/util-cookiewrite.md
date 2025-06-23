---
title: Util.cookieWrite
description: Schrijft een waarde voor een cookie.
feature: Appmeasurement Implementation
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# Util.cookieWrite

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de methode `Util.cookieWrite()` om een waarde in te stellen op een cookie. U kunt de methode [`Util.cookieRead()`](util-cookieread.md) gebruiken om waarden op te halen die zijn ingesteld met `Util.cookieWrite()` .

## Cookies instellen met de extensie Adobe Analytics en Web SDK

Met Adobe Experience Platform Data Collection kunnen cookies niet worden ingesteld in de interface.

## s.Util.cookieWrite() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `s.Util.cookieWrite()` aan om een cookie in te stellen op een gewenste waarde.

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
