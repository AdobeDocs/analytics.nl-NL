---
title: collectHighEntropyUserAgentHints
description: Gebruik de variabele collectHighEntropyUserAgentHints om te bepalen of Adobe hoge entropiewenken bij Chromium browsers (bijvoorbeeld Google Chrome en Microsoft Edge) zal vragen.
source-git-commit: 885a8f229fa814053e4766f3b38b6e7fb209fc00
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# collectHighEntropyUserAgentHints

Hoog-entropy cliëntwenken worden gebruikt door Adobe Analytics om apparaat en browser identificatie te verbeteren. Deze optie is beschikbaar vanaf versie 2.23.0 van AppMeasurment.js. Meer informatie over clienttips vindt u in [dit overzicht en de veelgestelde vragen](/help/technotes/client-hints.md) alsmede [Google-blog](https://web.dev/user-agent-client-hints/).

## Hoog-entropiewenken verzamelen gebruikend het Web SDK

Hoog-entropy cliëntwenken maken deel uit van de contextcategorieën in Web SDK. Zie [Vorm de SDK van het Web van het Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en) voor meer informatie .

## Hoog-entropiewenken verzamelen met de Uitbreiding van Adobe Analytics

**[!UICONTROL Collect high-entropy user-agent hints]** is een selectievakje onder de algemene accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/#/@adobepm/data-collection) met uw Adobe-id-referenties.

1. Klik op de gewenste knop [!UICONTROL tag property].

1. Ga naar de [!UICONTROL Extensions] tab, en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.

1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Collect high entropy user-agent hints] selectievakje. Deze optie is standaard uitgeschakeld.

## collectHighEntropyUserAgentHints in AppMeasurement

De `s.collectHighEntropyUserAgentHints` Met de variabele wordt bepaald of AppMeasurement hints met hoge entropie vraagt bij Chromium-browsers (bijvoorbeeld Google Chrome en Microsoft Edge). Deze tips worden door Adobe Analytics gebruikt om de apparaat- en browseridentificatie te verbeteren.

Als deze optie is ingesteld op TRUE, worden alle hoge entropiehints aangevraagd vanuit de browser.

`s.collectHighEntropyUserAgentHints = TRUE`

`s.collectHighEntropyUserAgentHints = FALSE`
