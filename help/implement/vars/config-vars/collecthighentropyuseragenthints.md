---
title: collectHighEntropyUserAgentHints
description: Gebruik de variabele collectHighEntropyUserAgentHints om te bepalen of Adobe hoge entropiewenken bij Chromium browsers (bijvoorbeeld Google Chrome en Microsoft Edge) zal vragen.
exl-id: 97cfa0f9-b35d-4c73-822f-adf30d0b7efc
source-git-commit: 5318079d6ad972e66494cd7b7f3bd64359b11012
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# collectHighEntropyUserAgentHints

Hoog-entropy cliëntwenken worden gebruikt door Adobe Analytics om apparaat en browser identificatie te verbeteren. Deze optie is beschikbaar vanaf versie 2.23.0 van AppMeasurement.js. Meer informatie over clienttips vindt u in [dit overzicht en de veelgestelde vragen](/help/technotes/client-hints.md) alsmede [Google-blog](https://web.dev/user-agent-client-hints/).

## Hoog-entropiewenken verzamelen gebruikend het Web SDK

Hoog-entropy cliëntwenken maken deel uit van de contextcategorieën in Web SDK. Zie [Vorm de SDK van het Web van het Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) voor meer informatie .

## Hoog-entropiewenken verzamelen met de Uitbreiding van Adobe Analytics

**[!UICONTROL Collect high-entropy user-agent hints]** is een selectievakje onder de algemene accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/#/@adobepm/data-collection) met uw Adobe-id-referenties.

1. Klik op de gewenste knop [!UICONTROL tag property].

1. Ga naar de [!UICONTROL Extensions] tab, en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.

1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Collect high entropy user-agent hints] selectievakje. Deze optie is standaard uitgeschakeld.

## collectHighEntropyUserAgentHints in AppMeasurement

De `s.collectHighEntropyUserAgentHints` De variabele bepaalt of AppMeturement hoge entropiewenken van browsers van het Chroom vraagt (bijvoorbeeld, Google Chrome of Microsoft Edge). Deze tips worden door Adobe Analytics gebruikt om de apparaat- en browseridentificatie te verbeteren.

Indien ingesteld op `true`, worden alle hoge entropiehints aangevraagd vanuit de browser.

```js
s.collectHighEntropyUserAgentHints = true;
```
