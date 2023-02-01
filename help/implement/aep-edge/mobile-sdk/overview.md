---
title: Adobe Analytics implementeren met de Adobe Experience Platform Mobile SDK
description: Gebruik de extensie Mobile SDK in Adobe Experience Platform Data Collection om gegevens naar Adobe Analytics te verzenden.
source-git-commit: 5adc3fe1eab0a358573ebdc12e51c6753e85b14c
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 1%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Mobile SDK

De Adobe Experience Platform Mobile SDK helpt Adobe Experience Cloud-oplossingen en -services aan te schaffen in uw mobiele apps. Deze functie is beschikbaar voor Android™, iOS en verschillende platformonafhankelijke ontwikkelframeworks. De configuratie wordt behandeld door de Inzameling van Gegevens van Adobe Experience Platform.
>[!IMPORTANT]
>
>Een Adobe Analytics-extensie is ook beschikbaar in Adobe Experience Platform Data Collection. Als u deze extensie installeert, profiteert u niet van XDM of Edge Network.

## Adobe Experience Platform SDK

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics die de uitbreidingsworkflow voor Analytics gebruikt](../../assets/mobilesdk-annotated.png)

| | Taak | Meer informatie | |-| —|| | 1 | Zorg ervoor dat u beschikt over **een rapportsuite gedefinieerd**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Schema&#39;s en gegevenssets instellen**. Om gegevensinzameling voor gebruik over toepassingen te standaardiseren die hefboomwerking Adobe Experience Platform, heeft Adobe de open en openbaar gedocumenteerde norm, het Model van de Gegevens van de Ervaring (XDM) gecreeerd. | [Schema&#39;s en gegevenssets instellen](https://developer.adobe.com/client-sdks/documentation/getting-started/set-up-schemas-and-datasets/) | | 3 | **Een gegevensstroom configureren**. Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web SDK van Adobe Experience Platform. | [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 4 | **Een Adobe Analytics-service toevoegen** naar uw gegevensstroom. Deze service bepaalt of en hoe gegevens naar Adobe Analytics worden verzonden. | [Adobe Analytics-service toevoegen aan een gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 5 | **Een mobiele eigenschap maken**. Een eigenschap is een container die u vult met extensies, regels, gegevenselementen en bibliotheken. | [Een mobiele eigenschap instellen](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 6 | **De extensie Adobe Experience Platform Edge Network installeren** in de eigenschap mobile tag en configureer de datastream in de extensie. | [Adobe Experience Platform Edge Network](https://developer.adobe.com/client-sdks/documentation/edge-network/) | | 7 | **Code in uw app gebruiken** om de benodigde extensies te registreren en de tagconfiguratie te laden. | [Configuratie instellen](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 8 | **Functies implementeren en testen** met een combinatie van de gegevenselementen, regels, extra extensies en API-aanroepen van de tag in uw app. Inspect, validate, en foutopsporing gegevensverzameling en ervaringen voor uw mobiele toepassing. | [De voorbeeldtoepassing gebruiken](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 9 | **De implementatie van uw mobiele app uitbreiden en valideren** voordat het naar de productie wordt verplaatst. | |


## Adobe Analytics-extensie.

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics die de uitbreidingsworkflow voor Analytics gebruikt](../../assets/mobilesdk-analytics-annotated.png)

| | Taak | Meer informatie | |-| —|| | 1 | Zorg ervoor dat u beschikt over **een rapportsuite gedefinieerd**. | [Report Suite Manager](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Een mobiele eigenschap maken**. Een eigenschap is een container die u vult met extensies, regels, gegevenselementen en bibliotheken. | [Een mobiele eigenschap instellen](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 3 | **De Adobe Analytics-extensie installeren** in de eigenschap mobile tag en configureer de extensie zodanig dat deze naar uw rapportsuite verwijst. | [Adobe Analytics-extensie voor mobiele eigenschap](https://developer.adobe.com/client-sdks/documentation/adobe-analytics/) | | 4 | **Code in uw app gebruiken** om de benodigde extensies te registreren en de tagconfiguratie te laden. | [Configuratie instellen](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 5 | **Functies implementeren en testen** met een combinatie van de gegevenselementen, regels, extra extensies en API-aanroepen van de tag in uw app. Inspect, validate, en foutopsporing gegevensverzameling en ervaringen voor uw mobiele toepassing. | [De voorbeeldtoepassing gebruiken](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 6 | **De implementatie van uw mobiele app uitbreiden en valideren** voordat het naar de productie wordt verplaatst. | |

## Aanvullende bronnen

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#)

- [Mobiele SDK-documentatie](https://developer.adobe.com/client-sdks/documentation/)



