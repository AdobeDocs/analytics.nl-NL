---
title: Util.cookieRead
description: Hiermee wordt de waarde voor een cookie opgehaald.
feature: Variables
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Util.cookieRead

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de `Util.cookieRead()` methode om een waarde van een cookie op te halen.

## Cookies lezen met de Adobe Analytics-extensie en de Web SDK-extensie

U kunt cookies lezen door waarden in gegevenselementen in te stellen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Data Elements] klikt u op het gewenste gegevenselement (of maakt u een gegevenselement).
4. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar **[!UICONTROL Core]** en de [!UICONTROL Data Element Type] tot **[!UICONTROL Cookie]**.
5. Voer de cookienaam in het tekstveld in.

De cookiewaarde wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de gewenste variabelen toe te wijzen.

## s.Util.cookieRead() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de `s.Util.cookieRead()` methode om een gewenste cookiewaarde te lezen. Zijn enige argument is een koord, dat wordt vereist. Deze methode retourneert een tekenreeks die de waarde van het cookie bevat. Als de cookies niet bestaan, wordt een lege tekenreeks geretourneerd.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
