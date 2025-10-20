---
title: Houd verschillende implementatietypen bij
description: Gebruik verschillende implementatietypen en volg bezoekers naadloos tussen hen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Houd verschillende implementatietypen bij

De kernarchitectuur van een Adobe Analytics-implementatie is consistent voor alle implementatietypen. Het proces omvat het definiëren van variabelen en het compileren ervan in een afbeeldingsaanvraag die naar Adobe-servers voor gegevensverzameling wordt verzonden. Dit concept houdt in dat u naadloos kunt schakelen tussen AppMeasurement, de Web SDK en hun respectievelijke extensies in Adobe Experience Platform Data Collection op verschillende pagina&#39;s van dezelfde site.

Adobe raadt u aan consistentie te behouden in de implementatie van een site door hetzelfde implementatietype op alle pagina&#39;s te gebruiken. Als onderdelen van uw site echter aan andere vereisten voldoen, kunt u deze pagina gebruiken om ervoor te zorgen dat bezoekers consistent tussen pagina&#39;s worden bijgehouden.

Als u meer dan één type implementatie gebruikt (zoals AppMeasurement en verzoeken om een gecodeerde afbeelding), moet u ervoor zorgen dat de volgende variabelen correct zijn ingesteld en met elkaar overeenkomen.

>[!NOTE]
>
>Voor alle implementatietypen moet hetzelfde type bezoekersidentificatie worden gebruikt (verouderde analyse-id of Bezoekersidentiteitsservice). Adobe raadt u aan om de Bezoeker-id-service waar mogelijk in alle implementaties te gebruiken.

| Variabele | AppMeasurement | Extensie Analytics | Web SDK (Alloy) | Web SDK-tagextensie | Hardcoded image request |
| --- | --- | --- | --- | --- | --- |
| Reeks-id rapporteren | Tekenreeksargument in [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report suites] onder de [!UICONTROL Library management] sectie wanneer [&#x200B; het Vormen van de uitbreiding &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | Voeg Adobe Analytics als dienst toe wanneer [&#x200B; het Vormen van een datastream &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | Voeg Adobe Analytics als dienst toe wanneer [&#x200B; het Vormen van een datastream &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | Deel van de URL `pathname` (na `/b/ss/`) |
| Experience Cloud ID-service | Implementeren [`VisitorAPI.js`](appmeasurement.md) | Gebruik de [&#x200B; uitbreiding van de Dienst van identiteitskaart van Experience Cloud &#x200B;](analytics-extension.md) | [&#x200B; Inheems inbegrepen &#x200B;](alloy.md) | [&#x200B; Inheems inbegrepen &#x200B;](web-sdk-extension.md) | Maak a [&#x200B; afzonderlijke vraag aan de Dienst van identiteitskaart &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html) om gewenste identiteitskaart te verkrijgen en `mid` in het vraagkoord te omvatten |
| Edge-domein | De variabele [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) | [!UICONTROL SSL Tracking Server] onder de [!UICONTROL General] sectie wanneer [&#x200B; het Vormen van de uitbreiding &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | Het `edgeDomain` bezit wanneer [&#x200B; Vormend het Web SDK &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) | Het [!UICONTROL Edge Domain] gebied wanneer [&#x200B; het Vormen van de uitbreiding &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) | De `hostname` van de URL van de afbeeldingsaanvraag |

Als een van deze variabelen niet consistent is voor elk implementatietype, kan Adobe ze als aparte bezoekers beschouwen. Als bezoekers niet naadloos over implementatietypen op uw plaats worden gevolgd, is de gemeenschappelijkste reden dat de Dienst van identiteitskaart verkeerd wordt gevormd. Zorg ervoor dat elk implementatietype op de juiste wijze dezelfde Experience Cloud-id (`mid`) op uw site verkrijgt.
