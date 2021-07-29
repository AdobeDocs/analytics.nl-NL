---
title: bezoekerNameSpace
description: Variabele in ruste die het cookie domein heeft bepaald.
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# bezoekerNamespace

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik in plaats hiervan [`trackingServer`](trackingserver.md).

In vorige versies van Adobe Analytics, gebruikte AppMeasurement `visitorNameSpace` variabele om het subdomein van `2o7.net` te bepalen waar de bezoekerskoekjes worden opgeslagen. De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Met de introductie van de variabelen `trackingServer` en [`trackingServerSecure`](trackingserversecure.md) is `visitorNameSpace` niet meer nodig.

>[!TIP]
>
>Adobe raadt u aan cookies van de eerste fabrikant op uw site te gebruiken. First-party cookies gebruiken deze variabele niet.

## Naamruimte van bezoekers met tags in Adobe Experience Platform

[!UICONTROL Visitor Namespace] is een veld onder de  [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Visitor Namespace] zichtbaar wordt.

Adobe raadt u af dit veld te gebruiken. Gebruik in plaats hiervan `trackingServer` en `trackingServerSecure`.

## s.bezoekorNamespace in AppMeasurement en de aangepaste code-editor

De variabele `s.visitorNamespace` is een tekenreeks die een unieke waarde per organisatie bevat. Oude AppMeturement-bibliotheken hebben deze unieke waarde automatisch opgenomen wanneer ze zijn gedownload van eerdere versies van Adobe Analytics. De huidige bibliotheken AppMeasurement gebruiken deze variabele niet tenzij `trackingServer` en `trackingServerSecure` niet worden geplaatst.

Als deze variabele nog steeds door uw organisatie wordt vereist, kiest u een waarde die uw organisatie vertegenwoordigt. U kunt deze waarde opslaan in een [document van het oplossingsontwerp](../../prepare/solution-design.md).

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
