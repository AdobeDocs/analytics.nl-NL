---
title: usePlugins
description: Schakel de functie doPlugins() in of uit.
feature: Variables
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# usePlugins

Indien `usePlugins` is ingeschakeld, wordt de [`doPlugins()`](../functions/doplugins.md) De functie wordt uitgevoerd vlak voordat het AppMeasurement wordt gecompileerd en een hit naar de Adobe wordt verzonden. Deze variabele inschakelen als u de optie `doPlugins()` functie.

## Gebruik de `onBeforeEventSend` callback die SDK van het Web gebruikt

Terwijl SDK van het Web geen booleaanse waarde heeft om de uitvoering van extra logica te behandelen alvorens het gegeven wordt verzonden naar Adobe, kunt u registreren `onBeforeEventSend` callback om gegevens te wijzigen. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

## Plug-ins gebruiken met de Adobe Analytics-extensie

Adobe biedt een extensie met de naam &#39;Common Analytics Plugins&#39; waarmee u de meeste [Plug-ins](../plugins/impl-plugins.md). Installeer de extensie en roep de gewenste plug-in binnen een regel.

Als de gewenste insteekmodule niet is opgenomen in de extensie Adobe, gebruikt u de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.usePlugins in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.usePlugins` variable is een boolean die bepaalt of het AppMeasurement de eigenschap `doPlugins()` functie. De standaardwaarde is `false`. Deze variabele instellen op `true` als u de `doPlugins()` in uw implementatie.

```js
s.usePlugins = true;
```
