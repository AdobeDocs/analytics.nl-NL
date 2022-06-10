---
title: forceOnline
description: Handmatig de onlinestatus van AppMeasurement instellen.
feature: Variables
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# forceOnline

De `forceOnline()` Met deze methode kunt u de automatisch opgespoorde status van AppMeasurement overschrijven.

>[!WARNING]
>
>Gebruik deze methode alleen als [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOnline()` Methode om AppMeasurement te dwingen hits te behandelen alsof het apparaat online was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Online forceren met de Web SDK

De SDK van het Web ondersteunt offline bijhouden niet.

## Online forceren met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOnline() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

U kunt de `s.forceOnline()` methode overal in uw implementatie nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOnline();
```
