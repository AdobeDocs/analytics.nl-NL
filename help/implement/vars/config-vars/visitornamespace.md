---
title: bezoekerNameSpace
description: (In ruste) Hiermee kunt u het cookie-domein van derden bepalen.
feature: Appmeasurement Implementation
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# bezoekerNamespace

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Gebruik in plaats hiervan [`trackingServer`](trackingserver.md) .

In eerdere versies van Adobe Analytics gebruikte AppMeasurement de variabele `visitorNameSpace` om het subdomein van `2o7.net` te bepalen waar bezoekerscookies worden opgeslagen. De toenemende privacy praktijken in moderne browsers maken derdekoekjes minder betrouwbaar. Met de introductie van de variabelen `trackingServer` en [`trackingServerSecure`](trackingserversecure.md) is `visitorNameSpace` niet langer nodig.

>[!TIP]
>
>Adobe raadt u aan cookies van andere leveranciers op uw site te gebruiken. First-party cookies gebruiken deze variabele niet.

## Naamruimte van bezoekers met de Adobe Analytics-extensie

[!UICONTROL Visitor Namespace] is een veld onder de accordeon van [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Visitor Namespace] zichtbaar wordt.

Adobe raadt u af dit veld niet te gebruiken. Gebruik in plaats hiervan `trackingServer` en `trackingServerSecure` .

## s.bezoekorNamespace in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.visitorNamespace` is een tekenreeks die een unieke waarde per organisatie bevat. Deze unieke waarde wordt automatisch opgenomen in oude AppMeasurement-bibliotheken wanneer deze worden gedownload van eerdere versies van Adobe Analytics. Huidige AppMeasurement-bibliotheken gebruiken deze variabele alleen als `trackingServer` en `trackingServerSecure` niet zijn ingesteld.

Als deze variabele nog steeds door uw organisatie wordt vereist, kiest u een waarde die uw organisatie vertegenwoordigt. U kunt deze waarde in het document van het a [ oplossingsontwerp ](../../prepare/solution-design.md) opslaan.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
