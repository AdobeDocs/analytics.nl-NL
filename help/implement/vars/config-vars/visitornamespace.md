---
title: bezoekerNameSpace
description: Variabele in ruste die het cookie domein heeft bepaald.
feature: Variables
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# bezoekerNamespace

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruiken [`trackingServer`](trackingserver.md) in plaats daarvan.

In eerdere versies van Adobe Analytics gebruikte AppMeturement de `visitorNameSpace` variabele om het subdomein van te helpen bepalen `2o7.net` waar bezoekerscookies worden opgeslagen. De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Met de invoering van de `trackingServer` en [`trackingServerSecure`](trackingserversecure.md) variabelen, `visitorNameSpace` is niet meer nodig.

>[!TIP]
>
>Adobe raadt u aan cookies van de eerste fabrikant op uw site te gebruiken. First-party cookies gebruiken deze variabele niet.

## Naamruimte van bezoekers met de Adobe Analytics-extensie

[!UICONTROL Visitor Namespace] is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Visitor Namespace] veld.

Adobe raadt u af dit veld te gebruiken. Gebruiken `trackingServer` en `trackingServerSecure` in plaats daarvan.

## s.bezoekorNamespace in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.visitorNamespace` variabele is een tekenreeks die een unieke waarde per organisatie bevat. Oude AppMeturement-bibliotheken hebben deze unieke waarde automatisch opgenomen wanneer ze zijn gedownload van eerdere versies van Adobe Analytics. De huidige bibliotheken AppMeasurement gebruiken deze variabele niet tenzij `trackingServer` en `trackingServerSecure` niet ingesteld.

Als deze variabele nog steeds door uw organisatie wordt vereist, kiest u een waarde die uw organisatie vertegenwoordigt. U kunt deze waarde opslaan in een [document ontwerp oplossing](../../prepare/solution-design.md).

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
