---
title: usePlugins
description: Schakel de functie doPlugins() in of uit.
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---

# usePlugins

Als `usePlugins` wordt toegelaten, loopt de [`doPlugins()`](../functions/doplugins.md) functie net alvorens AppMeasurement compileert en een klap naar Adobe verzendt. Schakel deze variabele in als u de functie `doPlugins()` gebruikt.

## Plug-ins gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.usePlugins in AppMeasurement en een aangepaste code-editor

De `s.usePlugins` variabele is een booleaanse waarde die bepaalt of AppMeturement de `doPlugins()` functie roept. De standaardwaarde is `false`. Stel deze variabele in op `true` als u de functie `doPlugins()` in uw implementatie gebruikt.

```js
s.usePlugins = true;
```
