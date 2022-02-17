---
title: offlineThrottleDelay
description: Hiermee bepaalt u de frequentie van treffers wanneer een apparaat weer online komt.
feature: Variables
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# offlineThrottleDelay

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Wanneer een apparaat weer online komt, worden alle treffers die op het apparaat worden opgeslagen verzonden naar de servers van de Adobe gegevensinzameling. Een groot aantal resultaten in de wachtrij kan mogelijk van invloed zijn op de prestaties van oudere apparaten. Gebruik de `offlineThrottleDelay` variabele om te bepalen hoe vaak reeksen in de wachtrij naar Adobe worden verzonden.

## Offline Throttle Delay met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineThrottleDelay in AppMeasurement en aangepaste code-editor

De `s.offlineThrottleDelay` variabele is een geheel getal dat het aantal milliseconden vertegenwoordigt dat AppMeasurement wacht tussen het verzenden van in de wachtrij staande hits. De standaardwaarde is `0`, wat betekent dat alle in de wachtrij staande hits tegelijk worden verzonden. Indien `trackOffline` is `false`Deze variabele doet niets.

```js
s.offlineThrottleDelay = 500;
```
