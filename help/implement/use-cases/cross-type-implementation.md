---
title: Verschillende implementatietypen bijhouden
description: Gebruik verschillende implementatietypen en volg bezoekers naadloos tussen hen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: 90914569256cf891cb3cf693843e7cf9ede2f4ce
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 3%

---

# Verschillende implementatietypen bijhouden

De kernarchitectuur van een Adobe Analytics-implementatie is consistent voor alle implementatietypen. Het proces impliceert het bepalen van en het compileren van hen in een beeldverzoek dat naar de servers van de Adobe gegevensinzameling wordt verzonden. Dit concept betekent dat u naadloos tussen AppMeasurement, het Web SDK, en hun respectieve uitbreidingen in de Inzameling van Gegevens van Adobe Experience Platform over verschillende pagina&#39;s van de zelfde plaats kunt schakelen.

Adobe raadt u aan consistentie te behouden in de implementatie van een site door hetzelfde implementatietype op alle pagina&#39;s te gebruiken. Als onderdelen van uw site echter aan andere vereisten voldoen, kunt u deze pagina gebruiken om ervoor te zorgen dat bezoekers consistent tussen pagina&#39;s worden bijgehouden.

Als u meer dan één type implementatie gebruikt (zoals AppMeasurement en hardcoded afbeeldingsverzoeken), moet u ervoor zorgen dat de volgende variabelen correct zijn ingesteld en met elkaar overeenkomen:

| Variabele | AppMeasurement | Extensie Analytics | Web SDK | Web SDK-extensie | Hardcoded image request |
| --- | --- | --- | --- | --- | --- |
| Set-id rapporteren | String-argument binnen [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report suites] onder de [!UICONTROL Library management] delen wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | Adobe Analytics toevoegen als service wanneer [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | Adobe Analytics toevoegen als service wanneer [Een gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | Deel van de URL `pathname` (na `/b/ss/`) |
| Trackingserver | De [`trackingServer`](../vars/config-vars/trackingserver.md) en [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) variabelen | [!UICONTROL Tracking Server] en [!UICONTROL SSL Tracking Server] onder de [!UICONTROL General] delen wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | De `edgeDomain` eigenschap Wanneer [De SDK van het Web configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) | De [!UICONTROL Edge Domain] wanneer [De extensie configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) | De `hostname` van de URL voor de afbeeldingsaanvraag |
| Experience Cloud ID-service | Implementeren [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Gebruik de [Adobe Experience Cloud ID Service-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Een [afzonderlijke vraag aan de servers van de Dienst van identiteitskaart](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html) om de gewenste id te verkrijgen |

{style="table-layout:auto"}

Als een van deze variabelen niet consistent is voor elk implementatietype, beschouwt Adobe ze als aparte bezoekers. Als bezoekers niet naadloos over implementatietypen op uw plaats worden gevolgd, is de gemeenschappelijkste reden dat de Dienst van identiteitskaart verkeerd wordt gevormd. Zie [Implementatiemethoden](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html) in de gebruikershandleiding voor de id-service voor meer informatie.
