---
title: forceOffline
description: Handmatig de onlinestatus van AppMeasurement instellen.
feature: Variables
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# forceOffline

De `forceOffline()` Met deze methode kunt u de automatisch opgespoorde status van AppMeasurement overschrijven.

>[!IMPORTANT]
>
>Gebruik deze functie alleen als [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOffline()` Methode om AppMeasurement te dwingen om hits te behandelen alsof het apparaat offline was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Offline forceren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOffline() in AppMeasurement en aangepaste code-editor

U kunt de `s.forceOffline()` methode overal in uw implementatie nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOffline();
```
