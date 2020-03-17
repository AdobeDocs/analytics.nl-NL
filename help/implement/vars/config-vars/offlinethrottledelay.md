---
title: offlineThrottleDelay
description: Hiermee bepaalt u de frequentie van treffers wanneer een apparaat weer online komt.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# offlineThrottleDelay

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Wanneer een apparaat weer online komt, worden alle treffers die op het apparaat zijn opgeslagen naar de servers van de gegevensinzameling van Adobe verzonden. Een groot aantal resultaten in de wachtrij kan mogelijk van invloed zijn op de prestaties van oudere apparaten. Gebruik de `offlineThrottleDelay` variabele om te bepalen hoe vaak hits in de wachtrij naar Adobe worden verzonden.

## Offline Throttle Delay in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineThrottleDelay in AppMeasurement en Launch, aangepaste code-editor

De `s.offlineThrottleDelay` variabele is een geheel getal dat het aantal milliseconden vertegenwoordigt dat AppMeasurement wacht tussen het verzenden van in de wachtrij staande hits. De standaardwaarde is `0`, wat betekent dat alle in de wachtrij geplaatste treffers tegelijk worden verzonden. Wanneer `trackOffline` `false`dit wel het geval is, heeft deze variabele geen effect.

```js
s.offlineThrottleDelay = 500;
```
