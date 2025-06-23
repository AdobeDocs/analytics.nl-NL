---
title: forceOffline
description: Stel de onlinestatus van AppMeasurement handmatig in.
feature: Appmeasurement Implementation
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# forceOffline

Met de methode `forceOffline()` kunt u de automatisch gedetecteerde status van AppMeasurement overschrijven.

>[!WARNING]
>
>Gebruik deze functie alleen wanneer [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de methode `forceOffline()` gebruiken om AppMeasurement te dwingen hits te behandelen alsof het apparaat offline was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Offline forceren met de Web SDK

De Web SDK ondersteunt offline bijhouden niet.

## Offline afdwingen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.forceOffline() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

U kunt de methode `s.forceOffline()` overal in uw implementatie aanroepen nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOffline();
```
