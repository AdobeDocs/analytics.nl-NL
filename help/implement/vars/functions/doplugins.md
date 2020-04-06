---
title: doPlugins
description: Configureer logica vlak voordat een hit wordt gecompileerd en naar Adobe verzonden.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# doPlugins

De `doPlugins` variabele fungeert als een &#39;laatste aanroep&#39; om waarden in te stellen in uw implementatie. Als [`usePlugins`](../config-vars/useplugins.md) deze optie is ingeschakeld, wordt deze automatisch uitgevoerd vlak voordat een type afbeeldingsaanvraag wordt gecompileerd en naar Adobe verzonden, zoals:

* Alle aanroepen in de paginaweergave ([`t()`](t-method.md))
* Alle verbindingen het volgen ([`tl()`](tl-method.md)) vraag, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de `doPlugins` variabele om insteekcode aan te roepen en de uiteindelijke waarden van de variabelen in te stellen vlak voordat een afbeeldingsaanvraag wordt gecompileerd en naar Adobe verzonden.

## Plug-ins in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.doPlugins in AppMeasurement en Launch, aangepaste code

Stel de `s.doPlugins` variabele in op een functie die de gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!NOTE] Stel een functie slechts eenmaal in de implementatie in op de `doPlugins` variabele. Als u de `doPlugins` variabele meerdere keren instelt, wordt alleen de meest recente code gebruikt.

## Voorbeelden

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

>[!NOTE] Eerdere versies van AppMeasurement hadden iets verschillende `doPlugins()` code. Adobe raadt u aan bovenstaande indeling als beste praktijk te gebruiken.
