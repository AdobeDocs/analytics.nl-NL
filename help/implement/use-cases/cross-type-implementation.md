---
title: Houd verschillende implementatietypen bij
description: Gebruik verschillende implementatietypen en volg bezoekers naadloos tussen hen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---

# Houd verschillende implementatietypen bij

De kernarchitectuur van een Adobe Analytics-implementatie is consistent voor alle implementatietypen. Het proces omvat het definiëren van variabelen en het compileren ervan in een afbeeldingsaanvraag die naar de gegevensverzamelingsservers van de Adobe wordt verzonden. Dit concept betekent dat u naadloos tussen AppMeasurement, het Web SDK, en hun respectieve uitbreidingen in de Inzameling van Gegevens van Adobe Experience Platform over verschillende pagina&#39;s van de zelfde plaats kunt schakelen.

Adobe raadt u aan consistentie te behouden in de implementatie van een site door hetzelfde implementatietype op alle pagina&#39;s te gebruiken. Als onderdelen van uw site echter aan andere vereisten voldoen, kunt u deze pagina gebruiken om ervoor te zorgen dat bezoekers consistent tussen pagina&#39;s worden bijgehouden.

Als u meerdere typen implementaties gebruikt (zoals aanvragen voor AppMeasurementen en afbeeldingen met hardcodering), moet u ervoor zorgen dat de volgende variabelen correct zijn ingesteld en met elkaar overeenkomen:

| Variabele | AppMeasurement | Extensie Analytics | Web SDK | Web SDK-extensie | Hardcoded image request |
| --- | --- | --- | --- | --- | --- |
| Reeks-id rapporteren | String-argument binnen [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report suites] onder de [!UICONTROL Library management] delen wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=nl-NL) | Adobe Analytics toevoegen als service wanneer [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL) | Adobe Analytics toevoegen als service wanneer [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL) | Deel van de URL `pathname` (na `/b/ss/`) |
| Trackingserver | De [`trackingServer`](../vars/config-vars/trackingserver.md) en [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) variabelen | [!UICONTROL Tracking Server] en [!UICONTROL SSL Tracking Server] onder de [!UICONTROL General] delen wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=nl-NL) | De `edgeDomain` eigenschap Wanneer [De SDK van het Web configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL) | De [!UICONTROL Edge Domain] wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=nl-NL) | De `hostname` van de URL voor de afbeeldingsaanvraag |
| Experience Cloud ID-service | Implementeren [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=nl-NL) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=nl-NL) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=nl-NL) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=nl-NL) | Maak een [afzonderlijke vraag aan de servers van de Dienst van identiteitskaart](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html?lang=nl-NL) om de gewenste id te verkrijgen |

{style="table-layout:auto"}

Als een van deze variabelen niet consistent is voor elk implementatietype, beschouwt de Adobe ze als aparte bezoekers. Als bezoekers niet naadloos over implementatietypen op uw plaats worden gevolgd, is de gemeenschappelijkste reden dat de Dienst van identiteitskaart verkeerd wordt gevormd. Zie [Implementatiemethoden](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html?lang=nl-NL) in de gebruikershandleiding voor de id-service voor meer informatie.
