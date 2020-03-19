---
title: Util.cookieRead
description: Hiermee wordt de waarde voor een cookie opgehaald.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Util.cookieRead

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de `Util.cookieRead()` methode om een waarde van een cookie op te halen.

## Cookies lezen in Adobe Experience Platform Launch

U kunt cookies lezen door waarden in gegevenselementen in te stellen.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Data Elements] tabblad en klik vervolgens op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op [!UICONTROL Core]en de [!UICONTROL Data Element Type] op [!UICONTROL Cookie].
5. Voer de naam van het cookie in het tekstveld in.

De cookiewaarde wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de variabelen van de Analyse toe te wijzen.

## s.Util.cookieRead() in de aangepaste code-editor AppMeasurement en Launch

Roep de `s.Util.cookieRead()` methode aan om een gewenste koekjeswaarde te lezen. Zijn enige argument is een koord, dat wordt vereist. Deze methode retourneert een tekenreeks die de cookiewaarde bevat. Als de cookies niet bestaan, wordt een lege tekenreeks geretourneerd.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
