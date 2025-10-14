---
title: Util.cookieRead
description: Hiermee wordt de waarde voor een cookie opgehaald.
feature: Appmeasurement Implementation
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Util.cookieRead

Met cookies kunt u informatie opslaan en ophalen op meerdere pagina&#39;s in hetzelfde domein. Gebruik de methode `Util.cookieRead()` om een waarde uit een cookie op te halen.

## Cookies lezen met de extensie Adobe Analytics en de extensie Web SDK

U kunt cookies lezen door waarden in gegevenselementen in te stellen.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Data Elements] en klik vervolgens op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Core]** en de vervolgkeuzelijst op [!UICONTROL Data Element Type] op **[!UICONTROL Cookie]** .
5. Voer de cookienaam in het tekstveld in.

De cookiewaarde wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de gewenste variabelen toe te wijzen.

## s.Util.cookieRead() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `s.Util.cookieRead()` aan om een gewenste cookiewaarde te lezen. Zijn enige argument is een koord, dat wordt vereist. Deze methode retourneert een tekenreeks die de waarde van het cookie bevat. Als de cookies niet bestaan, wordt een lege tekenreeks geretourneerd.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
