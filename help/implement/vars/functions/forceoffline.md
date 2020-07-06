---
title: forceOffline
description: Handmatig de onlinestatus van AppMeasurement instellen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# forceOffline

Met de `forceOffline()` methode kunt u de automatisch gedetecteerde status van AppMeasurement overschrijven.

>[!IMPORTANT]
>
>Gebruik deze functie alleen als deze [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOffline()` methode gebruiken om AppMeasurement te dwingen om hits te behandelen alsof het apparaat offline was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Offline afdwingen bij starten van Adobe Experience Platform

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOffline() in de aangepaste code-editor van AppMeasurement en Launch

U kunt de `s.forceOffline()` methode overal in uw implementatie aanroepen nadat u het Analytics-object hebt geïnstantieerd.

```js
s.forceOffline();
```
