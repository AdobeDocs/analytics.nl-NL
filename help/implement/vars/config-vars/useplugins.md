---
title: usePlugins
description: Schakel de functie doPlugins() in of uit.
feature: Variables
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---

# usePlugins

Indien `usePlugins` is ingeschakeld, wordt de [`doPlugins()`](../functions/doplugins.md) De functie wordt uitgevoerd vlak voordat AppMeasurement wordt gecompileerd en een hit naar Adobe verzendt. Deze variabele inschakelen als u de optie `doPlugins()` functie.

## Plug-ins gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.usePlugins in AppMeasurement en een aangepaste code-editor

De `s.usePlugins` De variabele is een Booleaanse waarde die bepaalt of AppMeasurement de eigenschap `doPlugins()` functie. De standaardwaarde is `false`. Deze variabele instellen op `true` als u de `doPlugins()` in uw implementatie.

```js
s.usePlugins = true;
```
