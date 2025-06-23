---
title: offlineThrottleDelay
description: Hiermee bepaalt u de frequentie van treffers wanneer een apparaat weer online komt.
feature: Appmeasurement Implementation
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# offlineThrottleDelay

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Wanneer een apparaat weer online komt, worden alle treffers die op het apparaat zijn opgeslagen naar de servers van de de gegevensinzameling van Adobe verzonden. Een groot aantal resultaten in de wachtrij kan mogelijk van invloed zijn op de prestaties van oudere apparaten. Gebruik de variabele `offlineThrottleDelay` om te bepalen hoe vaak hits in de wachtrij naar Adobe worden verzonden.

## Offlinevertragingstijd met gebruik van de Web SDK

De Web SDK ondersteunt offline bijhouden niet.

## Offlinevertragingstijd met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.offlineThrottleDelay in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.offlineThrottleDelay` variabele is een geheel getal dat het aantal milliseconden vertegenwoordigt dat AppMeasurement wacht tussen het verzenden van in de wachtrij geplaatste hits. De standaardwaarde is `0` . Dit houdt in dat alle in de wachtrij geplaatste hits tegelijk worden verzonden. Wanneer `trackOffline` is `false` , heeft deze variabele geen effect.

```js
s.offlineThrottleDelay = 500;
```
