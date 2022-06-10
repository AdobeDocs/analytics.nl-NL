---
title: forceOffline
description: Handmatig de onlinestatus van AppMeasurement instellen.
feature: Variables
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# forceOffline

De `forceOffline()` Met deze methode kunt u de automatisch opgespoorde status van AppMeasurement overschrijven.

>[!WARNING]
>
>Gebruik deze functie alleen als [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOffline()` Methode om AppMeasurement te dwingen om hits te behandelen alsof het apparaat offline was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Offline forceren met de Web SDK

De SDK van het Web ondersteunt offline bijhouden niet.

## Offline afdwingen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOffline() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

U kunt de `s.forceOffline()` methode overal in uw implementatie nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOffline();
```
