---
title: usePlugins
description: Schakel de functie doPlugins() in of uit.
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# usePlugins

Als `usePlugins` deze optie is ingeschakeld, wordt de `doPlugins()` functie uitgevoerd vlak voordat AppMeasurement wordt gecompileerd en wordt een hit naar Adobe verzonden. Schakel deze variabele in als u de `doPlugins()` functie gebruikt.

## Plug-ins gebruiken in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.usePlugins in AppMeasurement en Launch, aangepaste code-editor

De `s.usePlugins` variabele is een Booleaanse waarde die bepaalt of AppMeturement de `doPlugins()` functie aanroept. De standaardwaarde is `false`. Stel deze variabele in op `true` als u de `doPlugins()` functie in uw implementatie gebruikt.

```js
s.usePlugins = true;
```
