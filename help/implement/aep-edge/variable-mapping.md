---
title: Variabeletoewijzing analyseren in Adobe Experience Edge
description: Geef aan welke XDM-velden door Edge automatisch worden toegewezen aan analytische variabelen.
source-git-commit: 984d62f6ece15ebbd41dbbd1e3cb800faa7f323b
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---


# Variabeletoewijzing analyseren in Adobe Experience Edge

In de volgende tabel staan de variabelen die het Adobe Experience Platform Edge Network automatisch toewijst aan Adobe Analytics. Als u deze XDM-veldpaden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden.

| XDM-veldpad | Dimensie en beschrijving van analyses |
| --- | --- |
| `application.id` | De mobiele dimensie [Toepassings-id](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.isClose` | Helpt de mobiele metrische waarde te definiëren [Crashes](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.closeType` | Hiermee wordt bepaald of een close-gebeurtenis vastloopt of niet. Geldige waarden zijn `close` (Een levenscyclussessie eindigt en er is een pauze-gebeurtenis ontvangen voor de vorige sessie) en `unknown` (Een levenscyclussessie eindigt zonder pauze-gebeurtenis). |
| `application.isInstall` | De mobiele metrisch [Installaties](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | De mobiele metrisch [Starten](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.name` | Hiermee kunt u de mobiele dimensie instellen [Toepassings-id](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.launches.value` | De mobiele metrisch [Starten](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isUpgrade` | De mobiele metrisch [Upgrades](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.version` | Hiermee kunt u de mobiele dimensie instellen [Toepassings-id](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.sessionLength` | De mobiele metrisch [Totale lengte sessie](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `commerce.checkouts.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Afbeeldingen](../../components/metrics/checkouts.md) metrisch. |
| `commerce.checkouts.value` | Verhoogt de [Afbeeldingen](../../components/metrics/checkouts.md) met de gewenste hoeveelheid. |
| `commerce.order.currencyCode` | Hiermee stelt u de [currencyCode](../vars/config-vars/currencycode.md) configuratievariabele. |
| `commerce.order.purchaseID` | Hiermee stelt u de [purchaseID](../vars/page-vars/purchaseid.md) paginavariabele. |
| `commerce.productListAdds.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) metrisch. |
| `commerce.productListAdds.value` | Verhoogt de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) met de gewenste hoeveelheid. |
| `commerce.productListOpens.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Houtskaarten](../../components/metrics/carts.md) metrisch. |
| `commerce.productListOpens.value` | Verhoogt de [Houtskaarten](../../components/metrics/carts.md) met de gewenste hoeveelheid. |
| `commerce.productListRemovals.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Winkelwagentjes](../../components/metrics/cart-removals.md) metrisch. |
| `commerce.productListRemovals.value` | Verhoogt de [Winkelwagentjes](../../components/metrics/cart-removals.md) met de gewenste hoeveelheid. |
| `commerce.productListViews.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Kleuraweergaven](../../components/metrics/cart-views.md) metrisch. |
| `commerce.productListViews.value` | Verhoogt de [Kleuraweergaven](../../components/metrics/cart-views.md) met de gewenste hoeveelheid. |
| `commerce.productViews.id` | Toepassingen [gebeurtenisserienummering](../vars/page-vars/events/event-serialization.md) aan de [Productweergaven](../../components/metrics/product-views.md) metrisch. |
| `commerce.productViews.value` | Verhoogt de [Productweergaven](../../components/metrics/product-views.md) met de gewenste hoeveelheid. |
| `commerce.purchases.value` | Verhoogt de [Orders](../../components/metrics/orders.md) met de gewenste hoeveelheid. |
| `device.manufacturer` | De fabrikant van mobiele apparaten. |
| `device.model` | De mobiele dimensie [Apparaatnaam](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `device.modelNumber` | Het modelnummer van het mobiele apparaat. |
| `device.colorDepth` | Hiermee stelt u de [Kleurdiepte](../../components/dimensions/color-depth.md) dimensie. |
| `device.screenHeight` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. Zorg ervoor dat u ook het XDM-veld instelt `device.screenWidth`. |
| `device.screenWidth` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. Zorg ervoor dat u ook het XDM-veld instelt `device.screenHeight`. |
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
| `environment.operatingSystemVersion` | De mobiele dimensie [Versie besturingssysteem](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.type` | Geeft aan of de gebeurtenis afkomstig is van een [ondraaglijk](https://experienceleague.adobe.com/docs/mobile-services/android/wearables-android/c-android-wearables--additional-notes.html) apparaat. Geldige waarden zijn `Application` (de gebeurtenis kwam uit de app), `Extension` (de gebeurtenis kwam uit de verhandelbare app), of `Widget` (de gebeurtenis is afkomstig van een mobiele widget). |
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
| `media.mediaTimed.primaryAssetReference.@id` | De dimensie Media Analytics [Element-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `media.mediaTimed.primaryAssetReference.dc:title` | De dimensie Media Analytics [Videonaam](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | De dimensie Media Analytics [Maker](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Episode.iptc4xmpExt:Number` | De dimensie Media Analytics [Episode](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Genre` | De dimensie Media Analytics [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | De dimensie Media Analytics [Classificatie van inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Season.iptc4xmpExt:Number` | De dimensie Media Analytics [Seizoen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Series.iptc4xmpExt:Identifier` | De dimensie Media Analytics [Inhoud-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Series.iptc4xmpExt:Name` | De dimensie Media Analytics [Tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `media.mediaTimed.primaryAssetReference.showType` | De dimensie Media Analytics [Tekst tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `media.mediaTimed.primaryAssetReference.xmpDM:duration` | De dimensie Media Analytics [Videolengte](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `media.mediaTimed.primaryAssetViewDetails.@id` | De dimensie Media Analytics [Mediasessie-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastChannel` | De dimensie Media Analytics [Inhoudskanaal](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastContentType` | De dimensie Media Analytics [Inhoudstype](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastNetwork` | De dimensie Media Analytics [Netwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `media.mediaTimed.primaryAssetViewDetails.mediaSegmentView.value` | De dimensie Media Analytics [Segment Inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `media.mediaTimed.primaryAssetViewDetails.playerName` | De dimensie Media Analytics [Naam van inhoudspeler](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `media.mediaTimed.primaryAssetViewDetails.playerSDKVersion.version` | De dimensie Media Analytics [SDK-versie](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `media.mediaTimed.primaryAssetViewDetails.sourceFeed` | De dimensie Media Analytics [Type mediafeed](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `media.mediaTimed.primaryAssetViewDetails.streamFormat` | De dimensie Media Analytics [Stroomindeling](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
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
| `productListItems[N].lineItemId` | De [Categorie](../../components/dimensions/category.md) dimensie. |
| `productlistitems[N].name` | De [Product](../../components/dimensions/product.md) dimensie. |
| `productlistitems[N].priceTotal` | Hiermee bepaalt u de [Ontvangsten](../../components/metrics/revenue.md) metrisch. |
| `productlistitems[N].quantity` | Hiermee bepaalt u de [Eenheden](../../components/metrics/units.md) metrisch. |
| `web.webInteraction.URL` | De [linkURL](../vars/config-vars/linkurl.md) implementatievariabele. |
| `web.webInteraction.name` | De [Aangepaste koppeling](../../components/dimensions/custom-link.md), [Koppeling downloaden](../../components/dimensions/download-link.md), of [Koppeling afsluiten](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `web.webInteraction.type` |
| `web.webInteraction.type` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `lnk_o` (Aangepaste koppelingen), `lnk_d` (Koppelingen downloaden) en `lnk_e` (Koppelingen afsluiten). |
| `web.webPageDetails.URL` | De [Pagina-URL](../../components/dimensions/page-url.md) dimensie. |
| `web.webPageDetails.errorPage` | Markering die helpt de pagina&#39;s te bepalen die niet zijn gevonden [dimensie](../../components/dimensions/pages-not-found.md) en [metrisch](../../components/metrics/pages-not-found.md). |
| `web.webPageDetails.name` | De [Pagina](../../components/dimensions/page.md) dimensie. |
| `web.webPageDetails.server` | De [Server](../../components/dimensions/server.md) dimensie. |
| `web.webPageDetails.siteSection` | De [Sectie Site](../../components/dimensions/site-section.md) dimensie. |
| `web.webReferrer.URL` | De [Referenter](../../components/dimensions/referrer.md) dimensie. |

{style=&quot;table-layout:auto&quot;}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Andere XDM-velden toewijzen aan analytische variabelen

Als er dimensies of metriek zijn die u aan Adobe Analytics wilt toevoegen, kunt u dit door [Contextgegevensvariabelen](../vars/page-vars/contextdata.md). Alle XDM-veldelementen worden naar Adobe Analytics verzonden als contextgegevens met het voorvoegsel `a.x`. U kunt deze variabele van contextgegevens aan de gewenste variabele van Analyse dan in kaart brengen gebruikend [Verwerkingsregels](../../admin/admin/c-processing-rules/processing-rules.md). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

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
