---
title: Adobe Analytics implementeren met de Adobe Experience Platform Web SDK
description: Gebruik de uitbreiding van SDK van het Web in de Inzameling van Gegevens van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden.
source-git-commit: 472faef9c6ef99d4e58f2f5a9a71ca8d058f0ee2
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 1%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Web SDK

U kunt de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html) om gegevens naar Adobe Analytics te verzenden. Deze implementatiemethode werkt door de [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) in een indeling die wordt gebruikt door Analytics.

U kunt gegevens naar de Rand van de Ervaring direct verzenden gebruikend het Web SDK, of door de uitbreiding van SDK van het Web in Markeringen.

## Web SDK

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics implementeren met Web SDK-workflow](../../assets/websdk-annotated.png)

| | Taak | Meer informatie | |-| —|| | 1 | Zorg ervoor dat u beschikt over **een rapportsuite gedefinieerd**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Installatieschema&#39;s en gegevenssets**. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd. | [Overzicht van schema&#39;s](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) en [Overzicht van de gebruikersinterface voor gegevensbestanden](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en) | | 3 | **Een gegevenslaag maken** om het bijhouden van de gegevens op uw website te beheren. | [Een gegevenslaag maken](../../prepare/data-layer.md) | | 4 | **De vooraf gebouwde zelfstandige versie installeren**. U kunt verwijzen naar de bibliotheek (`alloy.js`) rechtstreeks op de CDN op de pagina of download en host deze op uw eigen infrastructuur. U kunt ook het NPM-pakket gebruiken. | [De vooraf gebouwde zelfstandige versie installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version) en [Het NPM-pakket gebruiken](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-3%3A-using-the-npm-package)| | 5 | **Een gegevensstroom configureren**. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform. | [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 6 | **Een Adobe Analytics-service toevoegen** naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden. | [Adobe Analytics-service toevoegen aan een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 7 | **De SDK van het web configureren**. Zorg ervoor dat de bibliotheek die u in stap 4 hebt geïnstalleerd, correct is geconfigureerd met de gegevensstroom-id (voorheen bekend als edge configuration id (`edgeConfigId`), organisatie-id (`orgId`) en andere beschikbare opties. | [De SDK van het web configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en) | | 8 | **Opdrachten uitvoeren** en/of **gebeurtenissen track**. Nadat de basiscode op uw webpagina is geïmplementeerd, kunt u beginnen met het uitvoeren van opdrachten en het volgen van gebeurtenissen met de SDK. | [Opdrachten uitvoeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=en) en [Gebeurtenissen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=en) | | 9 | **Uw implementatie uitbreiden en valideren** voordat het naar de productie wordt verplaatst. | |



## Web SDK-extensie

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics implementeren met de webSDK-uitbreidingsworkflow](../../assets/websdk-extension-annotated.png)

| | Taak | Meer informatie | |-| —|| | 1 | Zorg ervoor dat u beschikt over **een rapportsuite gedefinieerd**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Installatieschema&#39;s en gegevenssets**. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd. | [Overzicht van schema&#39;s](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) en [Overzicht van de gebruikersinterface voor gegevensbestanden](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en) | | 3 | **Een gegevenslaag maken** om het bijhouden van de gegevens op uw website te beheren. | [Een gegevenslaag maken](../../prepare/data-layer.md) | | 4 | **Een gegevensstroom configureren**. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform. | [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 5 | **Een Adobe Analytics-service toevoegen** naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden. | [Adobe Analytics-service toevoegen aan een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 6 | **Een tag-eigenschap maken**. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.| [Een eigenschap voor tags maken of configureren voor het web](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en#for-web) | | 7 | **De Web SDK-extensie installeren en configureren** in uw eigenschap tag. Vorm de uitbreiding van SDK van het Web om gegevens naar de datastream te verzenden die in stap 4 wordt gevormd. | [Overzicht van Adobe Experience Platform Web SDK-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=en) | | 8 | **Interfereren, valideren en publiceren** aan de productie. Voeg de eigenschap tag toe aan uw website. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen. | [Overzicht van publicatie](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=en) |



## Aanvullende bronnen

Tags kunnen in hoge mate worden aangepast. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): Leer hoe de interface werkt en welke extensies beschikbaar zijn.

- [Adobe Experience Platform Web SDK-documentatie](https://experienceleague.adobe.com/docs/web-sdk.html?lang=en)
