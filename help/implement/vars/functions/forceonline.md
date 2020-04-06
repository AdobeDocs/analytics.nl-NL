---
title: forceOnline
description: Handmatig de onlinestatus van AppMeasurement instellen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# forceOnline

Met de `forceOnline()` methode kunt u de automatisch gedetecteerde status van AppMeasurement overschrijven.

>[!IMPORTANT] Gebruik deze methode alleen als deze [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de `forceOnline()` methode gebruiken om AppMeasurement te dwingen hits te behandelen alsof het apparaat online was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Online forceren in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOnline() in de aangepaste code-editor van AppMeasurement en Launch

U kunt de `s.forceOnline()` methode overal in uw implementatie aanroepen nadat u het object Analytics hebt geïnstantieerd.

```js
s.forceOnline();
```
