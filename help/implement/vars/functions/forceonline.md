---
title: forceOnline
description: Handmatig de onlinestatus van AppMeasurement instellen.
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# forceOnline

Met de methode `forceOnline()` kunt u de automatisch gedetecteerde status van AppMeasurement overschrijven.

>[!IMPORTANT]
>
>Gebruik deze methode alleen wanneer [`trackOffline`](../config-vars/trackoffline.md) is ingeschakeld. Het gebruik van deze functie buiten het offline bijhouden van gegevens kan gegevensverlies veroorzaken.

AppMeasurement detecteert automatisch de onlinestatus van het apparaat. U kunt de methode `forceOnline()` gebruiken om AppMeasurement te dwingen hits te behandelen alsof het apparaat online was. Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel is het overschrijven van de onlinestatus in AppMeasurement.

## Online forceren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.forceOnline() in AppMeasurement en aangepaste code-editor

U kunt de methode `s.forceOnline()` overal in uw implementatie roepen nadat u het voorwerp van Analytics concretiseert.

```js
s.forceOnline();
```
