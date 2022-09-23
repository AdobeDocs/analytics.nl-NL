---
title: collectHighEntropyUserAgentHints
description: Gebruik de variabele collectHighEntropyUserAgentHints om te bepalen of Adobe hoge entropiewenken bij Chromium browsers (bijvoorbeeld Google Chrome en Microsoft Edge) zal vragen.
source-git-commit: 03d12625a0089672fa0a27f8f720065c5ca16a62
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# collectHighEntropyUserAgentHints

Hoog-entropy cliëntwenken worden gebruikt door Adobe Analytics om apparaat en browser identificatie te verbeteren. Meer informatie over clienttips vindt u in [dit overzicht en de veelgestelde vragen](/help/technotes/client-hints.md) alsmede [Google-blog](https://web.dev/user-agent-client-hints/).

## Hoog entropiewenken verzamelen met de SDK van het Web

Hoog entropy cliëntwenken maken deel uit van de contextcategorieën in Web SDK. Zie [Vorm de SDK van het Web van het Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en) voor meer informatie .

## Hoog entropiehints verzamelen met Adobe Analytics Extension

&quot;Verzamel hoge entropie user-agent wenken&quot;is een controledoos onder de Algemene accordeon wanneer het vormen van de uitbreiding van Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/#/@adobepm/data-collection) met uw Adobe-id-referenties.

1. Klik op de gewenste knop [!UICONTROL tag property].

1. Ga naar de [!UICONTROL Extensions] tab, en klik vervolgens op [!UICONTROL Configure] onder Adobe Analytics.

1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Collect high entropy user-agent hints] selectievakje. Deze optie is standaard uitgeschakeld.

## collectHighEntropyUserAgentHints in AppMeasurement

De `s.collectHighEntropyUserAgentHints` Met de variabele wordt bepaald of AppMeasurement hints met hoge entropie vraagt bij Chromium-browsers (bijvoorbeeld Google Chrome en Microsoft Edge). Deze tips worden door Adobe Analytics gebruikt om de apparaat- en browseridentificatie te verbeteren.

Als deze optie is ingesteld op TRUE, worden alle hoge entropiehints aangevraagd vanuit de browser.

`s.collectHighEntropyUserAgentHints = TRUE`

`s.collectHighEntropyUserAgentHints = FALSE`