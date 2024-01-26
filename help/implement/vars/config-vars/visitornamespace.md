---
title: bezoekerNameSpace
description: Variabele in ruste die het cookie domein heeft bepaald.
feature: Variables
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# bezoekerNamespace

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruiken [`trackingServer`](trackingserver.md) in plaats daarvan.

In eerdere versies van Adobe Analytics gebruikte AppMeasurement de `visitorNameSpace` variabele om het subdomein van te helpen bepalen `2o7.net` waar bezoekerscookies worden opgeslagen. De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Met de invoering van de `trackingServer` en [`trackingServerSecure`](trackingserversecure.md) variabelen, `visitorNameSpace` is niet meer nodig.

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

## s.bezoekorNamespace in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.visitorNamespace` variabele is een tekenreeks die een unieke waarde per organisatie bevat. Deze unieke waarde wordt automatisch opgenomen in oude bibliotheken met AppMeasurementen die u hebt gedownload van eerdere versies van Adobe Analytics. In bibliotheken met huidige AppMeasurementen wordt deze variabele alleen gebruikt `trackingServer` en `trackingServerSecure` niet ingesteld.

Als deze variabele nog steeds door uw organisatie wordt vereist, kiest u een waarde die uw organisatie vertegenwoordigt. U kunt deze waarde opslaan in een [document ontwerp oplossing](../../prepare/solution-design.md).

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
