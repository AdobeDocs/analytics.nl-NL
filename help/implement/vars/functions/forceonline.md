---
title: forceOnline
description: Stel de onlinestatus van AppMeasurement handmatig in.
feature: Appmeasurement Implementation
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# forceOnline

Met de methode `forceOnline()` kunt u de automatisch gedetecteerde status van AppMeasurement overschrijven.

>[!WARNING]
>
>Gebruik deze methode alleen als [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de methode `forceOnline()` gebruiken om AppMeasurement te dwingen hits te behandelen alsof het apparaat online was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Online forceren met de Web SDK

De Web SDK ondersteunt offline bijhouden niet.

## Online forceren met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.forceOnline() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

U kunt de methode `s.forceOnline()` overal in uw implementatie aanroepen nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOnline();
```
