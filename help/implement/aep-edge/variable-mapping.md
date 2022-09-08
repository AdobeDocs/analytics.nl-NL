---
title: Variabeletoewijzing analyseren in Adobe Experience Edge
description: Geef aan welke XDM-velden door Edge automatisch worden toegewezen aan analytische variabelen.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
source-git-commit: e42c125da0c48ff01267e3a18aaec8374652809e
workflow-type: tm+mt
source-wordcount: '1386'
ht-degree: 0%

---

# Variabeletoewijzing analyseren in Adobe Experience Edge

In de volgende tabel staan de variabelen die het Adobe Experience Platform Edge Network automatisch toewijst aan Adobe Analytics. Als u deze XDM-veldpaden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden.

| XDM-veldpad | Dimensie en beschrijving van analyses |
| --- | --- |
| `application.isClose` | Helpt de mobiele metrische waarde te definiëren [Crashes](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isInstall` | Helpt u te bepalen wanneer u de mobiele meting wilt verhogen [Eerste keer starten](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | Helpt u te bepalen wanneer u de mobiele meting wilt verhogen [Eerste keer starten](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.closeType` | Hiermee wordt bepaald of een close-gebeurtenis vastloopt of niet. Geldige waarden zijn `close` (Een levenscyclussessie eindigt en er is een pauze-gebeurtenis ontvangen voor de vorige sessie) en `unknown` (Een levenscyclussessie eindigt zonder pauze-gebeurtenis). Hiermee stelt u de [Crashes](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics) metrisch. |
| `application.isInstall` | De mobiele metrisch [Installaties](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | De mobiele metrisch [Starten](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.name` | Hiermee kunt u de mobiele dimensie instellen [Toepassings-id](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.isUpgrade` | De mobiele metrisch [Upgrades](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.version` | Hiermee kunt u de mobiele dimensie instellen [Toepassings-id](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.sessionLength` | De mobiele metrisch [Lengte vorige sessie](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `commerce.checkouts.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Afbeeldingen](../../components/metrics/checkouts.md) metrisch. |
| `commerce.checkouts.value` | Verhoogt de [Afbeeldingen](../../components/metrics/checkouts.md) met de gewenste hoeveelheid. |
| `commerce.order.currencyCode` | Hiermee stelt u de [currencyCode](../vars/config-vars/currencycode.md) configuratievariabele. |
| `commerce.order.purchaseID` | Hiermee stelt u de [purchaseID](../vars/page-vars/purchaseid.md) paginavariabele. |
| `commerce.order.transactionID` | Hiermee stelt u de [transactionID](../vars/page-vars/transactionid.md) paginavariabele. |
| `commerce.productListAdds.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) metrisch. |
| `commerce.productListAdds.value` | Verhoogt de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) metrisch. |
| `commerce.productListOpens.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Houtskaarten](../../components/metrics/carts.md) metrisch. |
| `commerce.productListOpens.value` | Verhoogt de [Houtskaarten](../../components/metrics/carts.md) metrisch. |
| `commerce.productListRemovals.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Winkelwagentjes](../../components/metrics/cart-removals.md) metrisch. |
| `commerce.productListRemovals.value` | Verhoogt de [Winkelwagentjes](../../components/metrics/cart-removals.md) metrisch. |
| `commerce.productListViews.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Kleuraweergaven](../../components/metrics/cart-views.md) metrisch. |
| `commerce.productListViews.value` | Verhoogt de [Kleuraweergaven](../../components/metrics/cart-views.md) metrisch. |
| `commerce.productViews.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Productweergaven](../../components/metrics/product-views.md) metrisch. |
| `commerce.productViews.value` | Verhoogt de [Productweergaven](../../components/metrics/product-views.md) metrisch. |
| `commerce.purchases.value` | Verhoogt de [Orders](../../components/metrics/orders.md) metrisch. |
| `device.model` | De mobiele dimensie [Apparaatnaam](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `device.colorDepth` | Hiermee stelt u de [Kleurdiepte](../../components/dimensions/color-depth.md) dimensie. |
| `device.screenHeight` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. |
| `device.screenWidth` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. |
| `device.type` | Het type mobiel apparaat. |
| `environment.browserDetails.acceptLanguage` | Hiermee stelt u de [Taal](../../components/dimensions/language.md) dimensie. |
| `environment.browserDetails.cookiesEnabled` | Hiermee stelt u de [Cookie-ondersteuning](../../components/dimensions/cookie-support.md) dimensie. Geldige waarden zijn `Y` (de browser accepteert cookies) en `N` (de browser wijst cookies af). |
| `environment.browserDetails.javaEnabled` | Hiermee stelt u de [Java ingeschakeld](../../components/dimensions/java-enabled.md) dimensie. Geldige waarden zijn `Y` (Java is ingeschakeld) en `N` (Java is uitgeschakeld). |
| `environment.browserDetails.userAgent` | Wordt gebruikt als fallback [unieke bezoeker](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans gevuld met de `User-Agent` HTTP request header. U kunt dit veld toewijzen aan een eVar als u het wilt gebruiken in rapporten. |
| `environment.browserDetails.viewportHeight` | Hiermee stelt u de [Browserhoogte](../../components/dimensions/browser-height.md) dimensie. |
| `environment.browserDetails.viewportWidth` | Hiermee stelt u de [Browserbreedte](../../components/dimensions/browser-width.md) dimensie. |
| `environment.carrier` | De mobiele dimensie [Naam vervoerder](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.connectionType` | Hiermee stelt u de [Verbindingstype](../../components/dimensions/connection-type.md) dimensie. |
| `environment.ipV4` | Wordt gebruikt als fallback [unieke bezoeker](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans gevuld met de `X-Forwarded-For` HTTP-header. |
| `environment.language` | De mobiele dimensie Locale. |
| `environment.operatingSystem` | De mobiele dimensie [Besturingssysteem](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.operatingSystemVersion` | Hiermee stelt u de [Versie besturingssysteem](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions) dimensie. |
| `_experience.analytics.customDimensions.`<br/>`eVars.eVar1` -<br/>`_experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Hiermee worden de respectievelijke instellingen ingesteld [eVar](../../components/dimensions/evar.md) dimensie. |
| `_experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter` -<br/>`_experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Het scheidingsteken dat voor een gegeven wordt gebruikt [List Prop](../vars/page-vars/prop.md#list-props). |
| `_experience.analytics.customDimensions.`<br/>`listProps.prop1.values` -<br/>`_experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Een tekenreeks die de respectievelijke [List Prop](../vars/page-vars/prop.md#list-props) waarden. |
| `_experience.analytics.customDimensions.`<br/>`lists.list1.list[].value` -<br/>`_experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Hiermee worden alle bestanden samengevoegd `value` tekenreeksen in elke respectievelijke `list[]` array aan zijn respectieve [Variabele List](../vars/page-vars/list.md) met behulp van komma-scheidingstekens. |
| `_experience.analytics.customDimensions.`<br/>`props.prop1` -<br/>`_experience.analytics.customDimensions.`<br/>`props.prop75` | Hiermee worden de respectievelijke instellingen ingesteld [Prop](../../components/dimensions/prop.md) dimensie. |
| `_experience.analytics.event1to100.`<br/>`event1.id` -<br/>`_experience.analytics.event901to1000.`<br/>`event1000.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de respectieve [Aangepaste gebeurtenissen](../../components/metrics/custom-events.md) metrisch. |
| `_experience.analytics.event1to100.`<br/>`event1.value` -<br/>`_experience.analytics.event901to1000.`<br/>`event1000.value` | Verhoogt de respectieve [Aangepaste gebeurtenissen](../../components/metrics/custom-events.md) met de gewenste hoeveelheid. |
| `identityMap.ECID[0].id` | De [Adobe Experience Cloud Identity Service ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| `marketing.trackingCode` | Hiermee stelt u de [Trackingcode](../../components/dimensions/tracking-code.md) dimensie. |
| `media.mediaTimed.completes.value` | Metrisch voor Media Analytics [Inhoud voltooid](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-complete). |
| `media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `media.mediaTimed.federated.value` | Metrisch voor Media Analytics [Federale gegevens](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#federated-data). |
| `media.mediaTimed.firstQuartiles.value` | Metrisch voor Media Analytics [25 % voortgangsmarkering](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#twenty-five-progress-marker). |
| `media.mediaTimed.mediaSegmentView.value` | Metrisch voor Media Analytics [Weergaven van inhoudssegmenten](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment-views). |
| `media.mediaTimed.midpoints.value` | Metrisch voor Media Analytics [Voortgangsmarkering van 50 %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#fifty-progress-marker). |
| `media.mediaTimed.pauseTime.value` | Metrisch voor Media Analytics [Totale pauzeduur](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#total-pause-duration). |
| `media.mediaTimed.pauses.value` | Metrisch voor Media Analytics [Gebeurtenissen pauzeren](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#pause-events). |
| `media.mediaTimed.primaryAssetReference.`<br/>`@id` | De dimensie Media Analytics [Element-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`dc:title` | De dimensie Media Analytics [Videonaam](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | De dimensie Media Analytics [Maker](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Episode.iptc4xmpExt:Number` | De dimensie Media Analytics [Episode](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Genre` | De dimensie Media Analytics [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | De dimensie Media Analytics [Classificatie van inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Season.iptc4xmpExt:Number` | De dimensie Media Analytics [Seizoen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Identifier` | De dimensie Media Analytics [Inhoud-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Name` | De dimensie Media Analytics [Tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `media.mediaTimed.primaryAssetReference.`<br/>`showType` | De dimensie Media Analytics [Tekst tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `media.mediaTimed.primaryAssetReference.`<br/>`xmpDM:duration` | De dimensie Media Analytics [Videolengte](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`@id` | De dimensie Media Analytics [Mediasessie-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastChannel` | De dimensie Media Analytics [Inhoudskanaal](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastContentType` | De dimensie Media Analytics [Inhoudstype](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastNetwork` | De dimensie Media Analytics [Netwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | De dimensie Media Analytics [Segment Inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerName` | De dimensie Media Analytics [Naam van inhoudspeler](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerSDKVersion.version` | De dimensie Media Analytics [SDK-versie](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`sourceFeed` | De dimensie Media Analytics [Type mediafeed](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`streamFormat` | De dimensie Media Analytics [Stroomindeling](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
| `media.mediaTimed.progress10.value` | Metrisch voor Media Analytics [Voortgangsmarkering van tien %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ten-progress-marker). |
| `media.mediaTimed.progress95.value` | Metrisch voor Media Analytics [95 % voortgangsmarkering](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ninety-five-progress-marker). |
| `media.mediaTimed.resumes.value` | Metrisch voor Media Analytics [Inhoudsresultaten](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-resumes). |
| `media.mediaTimed.starts.value` | Metrisch voor Media Analytics [Start media](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-starts). |
| `media.mediaTimed.thirdQuartiles.value` | Metrisch voor Media Analytics [Voortgangsmarkering van 75 %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#seventy-five-progress-marker). |
| `media.mediaTimed.timePlayed.value` | Metrisch voor Media Analytics [Tijd van inhoud besteed](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-time-spent). |
| `media.mediaTimed.totalTimePlayed.value` | Metrisch voor Media Analytics [Tijd besteed aan media](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-time-spent). |
| `placeContext.geo.latitude` | De mobiele afmeting Latitude. |
| `placeContext.geo.longitude` | De mobiele afmetingslengte. |
| `placeContext.geo.postalCode` | De [Postcode](../../components/dimensions/zip-code.md) dimensie. |
| `placeContext.geo.stateProvince` | De [VS](../../components/dimensions/us-states.md) dimensie. |
| `productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1` -<br/>`productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Toepassingen [productsyntaxis](../vars/page-vars/products.md) verhandelen naar eVars. |
| `productListItems[]._experience.analytics.`<br/>`event1to100.event1.value` -<br/>`productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Toepassingen [productsyntaxis](../vars/page-vars/products.md) verhandelen naar gebeurtenissen. |
| `productListItems[].lineItemId` | De [Categorie](../../components/dimensions/category.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `productListItems[].name` | De [Product](../../components/dimensions/product.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. Indien `productListItems[].SKU` en `productListItems[].name` beide bevatten gegevens, de waarde in `productListItems[].SKU` wordt gebruikt. |
| `productListItems[].priceTotal` | Hiermee bepaalt u de [Ontvangsten](../../components/metrics/revenue.md) metrisch. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `productListItems[].quantity` | Hiermee bepaalt u de [Eenheden](../../components/metrics/units.md) metrisch. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `productListItems[].SKU` | De [Product](../../components/dimensions/product.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. Indien `productListItems[].SKU` en `productListItems[].name` beide bevatten gegevens, de waarde in `productListItems[].SKU` wordt gebruikt. |
| `web.webInteraction.URL` | De [linkURL](../vars/config-vars/linkurl.md) implementatievariabele. |
| `web.webInteraction.name` | De [Aangepaste koppeling](../../components/dimensions/custom-link.md), [Koppeling downloaden](../../components/dimensions/download-link.md), of [Koppeling afsluiten](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `web.webInteraction.type` |
| `web.webInteraction.type` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `other` (Aangepaste koppelingen), `download` (Koppelingen downloaden) en `exit` (Koppelingen afsluiten). |
| `web.webPageDetails.URL` | De [Pagina-URL](../../components/dimensions/page-url.md) dimensie. |
| `web.webPageDetails.errorPage` | Markering die helpt de pagina&#39;s te bepalen die niet zijn gevonden [dimensie](../../components/dimensions/pages-not-found.md) en [metrisch](../../components/metrics/pages-not-found.md). |
| `web.webPageDetails.name` | De [Pagina](../../components/dimensions/page.md) dimensie. |
| `web.webPageDetails.server` | De [Server](../../components/dimensions/server.md) dimensie. |
| `web.webPageDetails.siteSection` | De [Sectie Site](../../components/dimensions/site-section.md) dimensie. |
| `web.webReferrer.URL` | De [Referenter](../../components/dimensions/referrer.md) dimensie. |

{style=&quot;table-layout:auto&quot;}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Andere XDM-velden toewijzen aan analytische variabelen

Als er dimensies of metriek zijn die u aan Adobe Analytics wilt toevoegen, kunt u dit door [Contextgegevensvariabelen](../vars/page-vars/contextdata.md). Alle XDM-veldelementen die niet automatisch worden toegewezen, worden naar Adobe Analytics verzonden als contextgegevens met het voorvoegsel a.x. U kunt deze variabele van contextgegevens aan de gewenste variabele van Analyse dan in kaart brengen gebruikend [Verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=en). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "search":{
                "term":"Example search term"
            }
        }
    }
})
```

De Web SDK verzendt die gegevens naar Adobe Analytics als variabele van contextgegevens `a.x._atag.search.term`. U kunt een verwerkingsregel dan gebruiken om die veranderlijke waarde van contextgegevens aan de gewenste variabele van Analytics, zoals een eVar toe te wijzen:

![Verwerkingsregel voor zoektermen](assets/examplerule.png)
