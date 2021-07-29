---
title: doPlugins
description: Vorm logica vlak voordat een slag wordt gecompileerd en verzonden naar Adobe.
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# doPlugins

De variabele `doPlugins` doet dienst als &quot;laatste vraag&quot;om waarden in uw implementatie te plaatsen. Als [`usePlugins`](../config-vars/useplugins.md) wordt toegelaten, loopt het automatisch vlak alvorens om het even welk type beeldverzoek wordt gecompileerd en verzonden naar Adobe, die omvatten:

* Alle aanroepen van de paginaweergave ([`t()`](t-method.md))
* Alle verbindingen het volgen ([`tl()`](tl-method.md)) vraag, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de `doPlugins` variabele om insteekcode te roepen en definitieve veranderlijke waarden te plaatsen enkel alvorens een beeldverzoek wordt gecompileerd en naar Adobe verzonden.

## Plug-ins die tags gebruiken in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.doPlugins in AppMeasurement en aangepaste code

Stel de variabele `s.doPlugins` in op een functie die de gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!NOTE]
>
>Stel een functie slechts eenmaal in de implementatie in op de variabele `doPlugins`. Wanneer u de variabele `doPlugins` meerdere keren instelt, wordt alleen de meest recente code gebruikt.

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
>Eerdere versies van AppMeasurement hadden lichtjes verschillende `doPlugins()` code. Adobe raadt u aan de bovenstaande notatie te gebruiken als aanbevolen werkwijze.
