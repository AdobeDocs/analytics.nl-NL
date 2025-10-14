---
title: Implementatiemethoden vergelijken
description: Zie de voordelen van elke methode die gegevens naar Adobe Analytics verzendt.
exl-id: 19353255-6356-4426-a2ef-5a2672a00eca
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 8e701a3da6f04ccf2d7ac3abd10c6df86feb00a7
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Implementatiemethoden vergelijken

Zie hoe elke methode om Adobe Analytics uit te voeren met elkaar vergelijkt. U kunt deze tabellen gebruiken om uw organisatie te helpen de ideale manier te bepalen om gegevens naar Adobe te verzenden. Klik op elke kolom voor meer specifieke informatie.

## Web

| | [AppMeasurement](/help/implement/js/overview.md) | [&#x200B; de uitbreiding van Adobe Analytics &#x200B;](/help/implement/launch/overview.md) | [&#x200B; SDK van het Web &#x200B;](/help/implement/aep-edge/web-sdk/overview.md#web-sdk) | [&#x200B; de uitbreiding van SDK van het Web &#x200B;](/help/implement/aep-edge/web-sdk/overview.md#web-sdk-extension) |
| --- | --- | --- | --- | --- |
| Implementatievereisten | Verwijzing `AppMeasurement.js` op elke pagina, definieer variabelen, verzend gegevens met `s.t()` naar Adobe Analytics | De markeringslader van de verwijzing op elke pagina, gebruik de UI van de Inzameling van Gegevens om variabelen te bepalen en gegevens naar Adobe Analytics te verzenden | Referentie `Alloy.js` op elke pagina gebruikt u `alloy("sendEvent",{})` om XDM-objecten samen te stellen en de gewenste gegevens te verzenden met Edge Network naar Adobe Analytics | De markeringslader van de verwijzing op elke pagina, gebruik de UI van de Inzameling van Gegevens om voorwerpen XDM samen te stellen en de gewenste gegevens te verzenden gebruikend Edge Network naar Adobe Analytics |
| Gegevensbestemming | Direct verzonden naar Adobe Analytics | Direct verzonden naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics |
| Probleem bij het aanbrengen van aanpassingen in de implementatie | Vereist toegang tot websitecode voor elke implementatiewijziging | Wijzig de websitecode eenmaal om de loader-tag te installeren. Alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling | Vereist toegang tot websitecode voor elke implementatiewijziging | Wijzig de websitecode eenmaal om de loader-tag te installeren. Alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling |
| Hoe A4T wordt behandeld | A4T-aanroepen worden opgenomen in resultaten die naar Adobe worden verzonden | A4T-aanroepen worden opgenomen in resultaten die naar Adobe worden verzonden | A4T-aanroepen worden verzonden als afzonderlijke treffers | A4T-aanroepen worden verzonden als afzonderlijke treffers |
| Contextgegevens | Gebruik `s.contextData` . | `s.contextData` gebruiken in aangepaste codeblokken | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. |

{style="table-layout:auto"}

## Mobiel en andere

>[!CAUTION]
>
>Ondersteuning voor versie 4 Mobile SDK&#39;s is beëindigd op 31 augustus 2021. Zie [&#x200B; Adobe Mobiele Veelgestelde Veelgestelde vragen van de Diensten van het Eind van de Eind-van-leven &#x200B;](https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.html?lang=nl-NL) voor meer informatie.


| | [&#x200B; Mobiele SDK &#x200B;](/help/implement/aep-edge/mobile-sdk/overview.md) | [&#x200B; Edge Network API &#x200B;](/help/implement/aep-edge/api/overview.md) |
| --- | --- | --- |
| Implementatievereisten | De markeringslader van de verwijzing in app, dan gebruik directe API vraag of regels in de UI van de Inzameling van Gegevens om XDM voorwerpen samen te stellen en de gewenste gegevens te verzenden gebruikend Edge Network aan Adobe Analytics | De Edge Network API gebruiken om XDM-objecten samen te stellen en de gewenste gegevens met Edge Network naar Adobe Analytics te verzenden |
| Gegevensbestemming | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics |
| Probleem bij het aanbrengen van aanpassingen in de implementatie | Wijzig de toepassingscode waar directe API-aanroepen worden uitgevoerd of wijzig de gebruikersinterface van de gegevensverzameling | Vereist toegang tot toepassingscode voor elke implementatieverandering |
| Hoe A4T wordt behandeld | A4T-aanroepen worden verzonden als afzonderlijke treffers | A4T-aanroepen worden verzonden als afzonderlijke treffers |
| Contextgegevens | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen. | Alle niet-toegewezen velden worden automatisch verzonden als `a.x.*` contextgegevensvariabelen |

{style="table-layout:auto"}
