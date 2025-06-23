---
title: collectHighEntropyUserAgentHints
description: Gebruik de variabele collectHighEntropyUserAgentHints om te bepalen of Adobe hoge entropiewenken bij Chromium browsers (bijvoorbeeld Google Chrome en Microsoft Edge) zal vragen.
exl-id: 97cfa0f9-b35d-4c73-822f-adf30d0b7efc
feature: Appmeasurement Implementation
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# collectHighEntropyUserAgentHints

Hoog-entropy cliëntwenken worden gebruikt door Adobe Analytics om apparaat en browser identificatie te verbeteren. Deze optie is beschikbaar vanaf versie 2.23.0 van AppMeasurement.js. Lees meer over cliëntwenken in [ dit overzicht en FAQ ](/help/technotes/client-hints.md) evenals [ Google blog ](https://web.dev/user-agent-client-hints/).

## Tips voor hoge entropie verzamelen met de Web SDK

Hoog-entropy cliëntwenken maken deel uit van de contextcategorieën in Web SDK. Zie [ SDK van het Web van het Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) voor meer details vormen.

## Hoog-entropiewenken verzamelen met de Uitbreiding van Adobe Analytics

**[!UICONTROL Collect high-entropy user-agent hints]** is een selectievakje onder de algemene accordeon bij het configureren van de Adobe Analytics-extensie.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/#/@adobepm/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op het gewenste [!UICONTROL tag property] .
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL General] uit, zodat het selectievakje [!UICONTROL Collect high entropy user-agent hints] zichtbaar wordt. Deze optie is standaard uitgeschakeld.

## collectHighEntropyUserAgentHints in AppMeasurement

De `s.collectHighEntropyUserAgentHints` -variabele bepaalt of AppMeasurement bij Chromium-browsers (bijvoorbeeld Google Chrome of Microsoft Edge) hoge entropiehints aanvraagt. Deze tips worden door Adobe Analytics gebruikt om de apparaat- en browseridentificatie te verbeteren.

Als deze optie is ingesteld op `true` , worden alle hoge entropiehints aangevraagd vanuit de browser.

```js
s.collectHighEntropyUserAgentHints = true;
```
