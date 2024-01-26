---
title: forceOnline
description: De onlinestatus van het AppMeasurement handmatig instellen.
feature: Variables
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# forceOnline

De `forceOnline()` Met deze methode kunt u de automatisch gedetecteerde status van het AppMeasurement overschrijven.

>[!WARNING]
>
>Gebruik deze methode alleen als [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOnline()` methode om AppMeasurement te dwingen hits te behandelen alsof het apparaat online was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is de status online in AppMeasurement te overschrijven.

## Online forceren met de Web SDK

De SDK van het Web ondersteunt offline bijhouden niet.

## Online forceren met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.forceOnline() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

U kunt de `s.forceOnline()` methode overal in uw implementatie nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOnline();
```
