---
title: Implementatiemethoden vergelijken
description: Zie de voordelen van elke methode die gegevens naar Adobe Analytics verzendt.
exl-id: 19353255-6356-4426-a2ef-5a2672a00eca
feature: Implementation Basics
source-git-commit: 61264d9f4ff2f1e961a613b81461efa826bc3d23
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 3%

---

# Implementatiemethoden vergelijken

Zie hoe elke methode om Adobe Analytics uit te voeren met elkaar vergelijkt. U kunt deze lijsten gebruiken om uw organisatie te helpen de meest ideale manier bepalen om gegevens naar Adobe te verzenden. Klik op elke kolom voor meer specifieke informatie.

## Web

| | [AppMeasurement](/help/implement/js/overview.md) | [Adobe Analytics-extensie](/help/implement/launch/overview.md) | [Web SDK](/help/implement/aep-edge/web-sdk/overview.md#web-sdk) | [Web SDK-extensie](/help/implement/aep-edge/web-sdk/overview.md#web-sdk-extension) |
| --- | --- | --- | --- | --- |
| Implementatievereisten | Referentie `AppMeasurement.js` op elke pagina variabelen definiëren, gegevens verzenden met `s.t()` naar Adobe Analytics | De markeringslader van de verwijzing op elke pagina, gebruik de UI van de Inzameling van Gegevens om variabelen te bepalen en gegevens naar Adobe Analytics te verzenden | Referentie `Alloy.js` op elke pagina, gebruik `alloy("sendEvent",{})` XDM-objecten samenstellen en de gewenste gegevens verzenden met Edge Network naar Adobe Analytics | De markeringslader van de verwijzing op elke pagina, gebruik de UI van de Inzameling van Gegevens om voorwerpen XDM samen te stellen en de gewenste gegevens te verzenden gebruikend het Netwerk van de Rand naar Adobe Analytics |
| Gegevensbestemming | Direct verzonden naar Adobe Analytics | Direct verzonden naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics |
| Probleem bij het aanbrengen van aanpassingen in de implementatie | Vereist toegang tot websitecode voor elke implementatiewijziging | Wijzig de websitecode eenmaal om de loader-tag te installeren. Alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling | Vereist toegang tot websitecode voor elke implementatiewijziging | Wijzig de websitecode eenmaal om de loader-tag te installeren. Alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling |
| Hoe A4T wordt behandeld | A4T-aanroepen worden opgenomen in resultaten die naar Adobe worden verzonden | A4T-aanroepen worden opgenomen in resultaten die naar Adobe worden verzonden | A4T-aanroepen worden verzonden als afzonderlijke treffers | A4T-aanroepen worden verzonden als afzonderlijke treffers |
| Contextdata | Gebruiken `s.contextData`. | Gebruiken `s.contextData` in aangepaste codeblokken | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. |

{style="table-layout:auto"}

## Mobiel en andere

>[!CAUTION]
>
>Ondersteuning voor versie 4 Mobile SDK&#39;s is beëindigd op 31 augustus 2021. Zie [Veelgestelde vragen over beëindiging van de ondersteuning van Mobiele SDK’s versie 4](https://developer.adobe.com/client-sdks/documentation/v4-end-of-life-faq/) voor meer informatie.


| | [Mobiele SDK](/help/implement/aep-edge/mobile-sdk/overview.md) | [Server-API](/help/implement/aep-edge/server-api/overview.md) |
| --- | --- | --- |
| Implementatievereisten | De markeringslader van de verwijzing in app, dan gebruik directe API vraag of regels in de UI van de Inzameling van Gegevens om voorwerpen XDM samen te stellen en de gewenste gegevens te verzenden gebruikend het Netwerk van de Rand naar Adobe Analytics | Edge Network Server-API&#39;s gebruiken om XDM-objecten samen te stellen en de gewenste gegevens via Edge Network naar Adobe Analytics te verzenden |
| Gegevensbestemming | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics |
| Probleem bij het aanbrengen van aanpassingen in de implementatie | Wijzig de toepassingscode waar directe API-aanroepen worden uitgevoerd of wijzig de gebruikersinterface van de gegevensverzameling | Vereist toegang tot toepassingscode voor elke implementatieverandering |
| Hoe A4T wordt behandeld | A4T-aanroepen worden verzonden als afzonderlijke treffers | A4T-aanroepen worden verzonden als afzonderlijke treffers |
| Contextdata | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen |

{style="table-layout:auto"}
