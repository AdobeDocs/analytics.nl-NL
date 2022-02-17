---
title: doPlugins
description: Vorm logica vlak voordat een slag wordt gecompileerd en verzonden naar Adobe.
feature: Variables
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# doPlugins

De `doPlugins` De variabele fungeert als een &#39;laatste aanroep&#39; om waarden in te stellen in uw implementatie. Indien [`usePlugins`](../config-vars/useplugins.md) wordt toegelaten, loopt het automatisch net alvorens om het even welk type beeldverzoek wordt gecompileerd en verzonden naar Adobe, die omvat:

* Alle paginaweergaven ([`t()`](t-method.md)) oproepen
* Alle koppelingen bijhouden ([`tl()`](tl-method.md)) oproepen, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de `doPlugins` variabele om insteekcode aan te roepen en definitieve veranderlijke waarden in te stellen vlak alvorens een beeldverzoek wordt gecompileerd en verzonden naar Adobe.

## Plug-ins die tags gebruiken in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.doPlugins in AppMeasurement en aangepaste code

Stel de `s.doPlugins` aan een functie die gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!NOTE]
>
>Een functie instellen op de `doPlugins` variabele slechts eenmaal in uw implementatie. Als u de `doPlugins` meerdere keren variabele, alleen de meest recente code wordt gebruikt.

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

>[!NOTE]
>
>Eerdere versies van AppMeasurement hadden iets verschillende versies `doPlugins()` code. Adobe raadt u aan de bovenstaande notatie te gebruiken als aanbevolen werkwijze.
