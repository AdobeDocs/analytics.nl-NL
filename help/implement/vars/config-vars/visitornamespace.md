---
title: bezoekerNameSpace
description: Variabele in ruste die het cookie domein heeft bepaald.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# bezoekerNamespace

>[!IMPORTANT] Deze variabele wordt uitgeschakeld. Gebruik [`trackingServer`](trackingserver.md) in plaats hiervan.

In eerdere versies van Adobe Analytics gebruikte AppMeasurement de `visitorNameSpace` variabele om het subdomein te bepalen van `2o7.net` waar bezoekerscookies worden opgeslagen. De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Met de invoering van de `trackingServer` en de [`trackingServerSecure`](trackingserversecure.md) variabelen is `visitorNameSpace` het niet langer nodig.

>[!TIP] Adobe raadt u aan cookies van de eerste fabrikant op uw site te gebruiken. First-party cookies gebruiken deze variabele niet.

## Naamruimte voor bezoekers in Adobe Experience Platform Starten

[!UICONTROL Visitor Namespace] is een veld onder de [!UICONTROL Cookies] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Cookies] [!UICONTROL Visitor Namespace] veld onthult.

Adobe raadt u af dit veld niet te gebruiken. Gebruik `trackingServer` en `trackingServerSecure` in plaats daarvan.

## s.bezoekorNamespace in AppMeasurement en Launch, aangepaste code-editor

De `s.visitorNamespace` variabele is een tekenreeks die een unieke waarde per organisatie bevat. Deze unieke waarde is automatisch opgenomen in oude AppMeturement-bibliotheken wanneer deze vanuit eerdere versies van Adobe Analytics zijn gedownload. De huidige bibliotheken AppMeasurement gebruiken deze variabele niet tenzij `trackingServer` en `trackingServerSecure` niet geplaatst.

Als deze variabele nog steeds door uw organisatie wordt vereist, kiest u een waarde die uw organisatie vertegenwoordigt. U kunt deze waarde opslaan in een [oplossingsontwerpdocument](../../prepare/solution-design.md).

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
