---
title: Adobe Analytics implementeren met de Adobe Experience Platform Web SDK
description: Gebruik SDK van het Web om gegevens naar Adobe Analytics te verzenden.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: d6c16d8841110e3382248f4c9ce3c2f2e32fe454
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Web SDK

U kunt de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/web-sdk/home.html?lang=nl-NL) om gegevens naar Adobe Analytics te verzenden. Er zijn twee belangrijkste methodes om het Web SDK uit te voeren, en elke methode heeft twee implementatietypen:

| | **Migreren vanuit AppMeasurement** | **Clean Web SDK-implementatie** |
| --- | --- | --- |
| **Tags gebruiken** | [Migreren van de uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md) | [Gegevens naar Adobe Analytics verzenden met de Web SDK-extensie](web-sdk-tag-extension.md) |
| **JavaScript gebruiken** | [Migreren van AppMeasurement naar de Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md) | [Gegevens naar Adobe Analytics verzenden met de Web SDK JavaScript-bibliotheek](web-sdk-javascript-library.md) |

Als uw organisatie een nieuwe implementatie van SDK van het Web vereist en van plan is om Customer Journey Analytics in de toekomst te gebruiken, adviseert de Adobe een schone implementatie van SDK van het Web gebruikend uw eigen schema. Zie [Gegevens invoeren via de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) in de gebruikershandleiding van de Customer Journey Analytics.

## Aanvullende bronnen

Tags kunnen zeer aangepast worden. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=nl-NL#): Leer hoe de interface werkt en welke extensies beschikbaar zijn.

- [Adobe Experience Platform Web SDK-documentatie](https://experienceleague.adobe.com/docs/web-sdk.html?lang=nl-NL)
