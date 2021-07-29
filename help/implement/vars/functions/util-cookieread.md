---
title: Util.cookieRead
description: Hiermee wordt de waarde voor een cookie opgehaald.
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---

# Util.cookieRead

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Met de methode `Util.cookieRead()` kunt u een waarde uit een cookie ophalen.

## Cookies lezen met tags in Adobe Experience Platform

U kunt cookies lezen door waarden in gegevenselementen in te stellen.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het tabblad [!UICONTROL Data Elements] en klik op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op [!UICONTROL Core] en [!UICONTROL Data Element Type] op [!UICONTROL Cookie].
5. Voer de naam van het cookie in het tekstveld in.

De cookiewaarde wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de variabelen van de Analyse toe te wijzen.

## s.Util.cookieRead() in AppMeasurement en aangepaste code-editor

Roep de methode `s.Util.cookieRead()` aan om een gewenste koekjeswaarde te lezen. Zijn enige argument is een koord, dat wordt vereist. Deze methode retourneert een tekenreeks die de cookiewaarde bevat. Als de cookies niet bestaan, wordt een lege tekenreeks geretourneerd.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
