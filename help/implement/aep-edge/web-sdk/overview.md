---
title: Adobe Analytics implementeren met de Adobe Experience Platform Web SDK
description: Gebruik de uitbreiding van SDK van het Web in de Inzameling van Gegevens van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden.
source-git-commit: 6979736e1849d25af2141e0ab76a143605a90620
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 4%

---


# Adobe Analytics implementeren met de Adobe Experience Platform Web SDK

U kunt de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html) om gegevens naar Adobe Analytics te verzenden. Deze implementatiemethode werkt door de [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) in een indeling die wordt gebruikt door Analytics.

## Instellen

Analytics instellen voor het ontvangen van XDM-gegevens:

1. Installeren en [vormen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html).

1. Zorg ervoor dat de toepasselijke rapportsuites aan de gegevens worden in kaart gebracht u wilt. XDM-gegevens worden automatisch vanuit Adobe Experience Edge naar de rapportsuite verzonden.
