---
title: offlineThrottleDelay
description: Hiermee bepaalt u de frequentie van treffers wanneer een apparaat weer online komt.
feature: Variables
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# offlineThrottleDelay

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Wanneer een apparaat online terugkomt, worden alle treffers die op het apparaat worden opgeslagen verzonden naar de servers van de de gegevensinzameling van de Adobe. Een groot aantal resultaten in de wachtrij kan mogelijk van invloed zijn op de prestaties van oudere apparaten. Gebruik de `offlineThrottleDelay` variabele om te bepalen hoe vaak de een rij gevormde klappen naar Adobe worden verzonden.

## Offline Throttle Delay met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.offlineThrottleDelay in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.offlineThrottleDelay` variabele is een geheel getal dat het aantal milliseconden vertegenwoordigt dat AppMeasurement wacht tussen het verzenden van in de wachtrij geplaatste hits. De standaardwaarde is `0`, wat betekent dat alle in de wachtrij staande hits tegelijk worden verzonden. Indien `trackOffline` is `false`Deze variabele doet niets.

```js
s.offlineThrottleDelay = 500;
```
