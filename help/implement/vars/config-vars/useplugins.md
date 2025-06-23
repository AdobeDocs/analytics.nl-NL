---
title: usePlugins
description: Schakel de functie doPlugins() in of uit.
feature: Appmeasurement Implementation
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# usePlugins

Als `usePlugins` is ingeschakeld, wordt de functie [`doPlugins()`](../functions/doplugins.md) uitgevoerd net voordat AppMeasurement een hit compileert en naar Adobe verzendt. Schakel deze variabele in als u de functie `doPlugins()` gebruikt.

## De callback van `onBeforeEventSend` gebruiken met de Web SDK

Hoewel de SDK van het Web geen booleaanse waarde heeft om de uitvoering van extra logica te behandelen alvorens de gegevens naar Adobe worden verzonden, kunt u `onBeforeEventSend` callback registreren om gegevens te wijzigen. Zie [ Veranderend gebeurtenissen globaal ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

## Plug-ins gebruiken met de Adobe Analytics-extensie

Adobe verstrekt een uitbreiding geëtiketteerd &quot;Gemeenschappelijke Insteekmodules van Analytics&quot;die u toestaat om meeste [ stop-ins ](../plugins/impl-plugins.md) te roepen. Installeer de extensie en roep de gewenste plug-in binnen een regel.

Als de gewenste insteekmodule niet is opgenomen in de Adobe-extensie, gebruikt u de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.usePlugins in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.usePlugins` is een Booleaanse waarde die bepaalt of AppMeasurement de functie `doPlugins()` aanroept. De standaardwaarde is `false` . Stel deze variabele in op `true` als u de functie `doPlugins()` in uw implementatie gebruikt.

```js
s.usePlugins = true;
```
