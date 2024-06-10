---
title: XML-objectvariabele toewijzen aan Adobe Analytics
description: Geef aan welke XDM-velden door Edge automatisch worden toegewezen aan analytische variabelen.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 4bd46fd5a9b98bcca67a66c87c9bca67fa00061a
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---

# XML-objectvariabele toewijzen aan Adobe Analytics

In de volgende tabel staan de XDM-variabelen die de Adobe Experience Platform-Edge Network automatisch toewijst aan Adobe Analytics. Als u deze XDM-veldpaden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden. Deze velden zijn opgenomen in de **[!UICONTROL Adobe Analytics ExperienceEvent Template]** veldgroep. U wordt aangeraden deze velden te gebruiken als u gegevens wilt verzenden naar Adobe Analytics en Adobe Experience Platform.

Als uw organisatie van plan is naar Customer Journey Analytics te gaan, raadt de Adobe u aan in plaats daarvan de `data` -object om gegevens rechtstreeks naar Adobe Analytics te verzenden zonder zich aan een schema te houden. Deze strategie staat uw organisatie toe om uw eigen schema te gebruiken, in plaats van het gebruiken van [!UICONTROL Adobe Analytics ExperienceEvent Template] (minder toepasbaar op Customer Journey Analytics). Zie [Gegevensobjectvariabele toewijzen aan Adobe Analytics](data-var-mapping.md) voor een vergelijkbare toewijzingstabel.

## Waardeprioriteiten

De meeste XDM-objectvelden in deze tabel komen overeen met een [gegevensobjectveld](data-var-mapping.md). Als u zowel een bepaald XDM-objectveld als het bijbehorende gegevensobjectveld instelt, krijgt het gegevensobjectveld prioriteit. Als u zowel het XDM-objectveld als het gegevensobjectveld gebruikt, raadt de Adobe aan aangepaste gebeurtenissen in te stellen met behulp van het gegevensobjectveld. Als het veld `data.__adobe.analytics.events` is aanwezig, overschrijft het alle XDM objecten gebieden met betrekking tot handel en douanegebeurtenissen.

## XML-objectveldtoewijzing

U vindt vorige updates van deze tabel op de pagina [geschiedenis toewijzen op GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/xdm-var-mapping.md).

| XDM-veldpad | Variabele en beschrijving voor analyse |
| --- | --- |
| `xdm.application.isClose` | Helpt de metrische mobiele levenscyclus te bepalen [Crashes](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | Hiermee bepaalt u wanneer de metrische waarde van de mobiele levenscyclus moet worden verhoogd [Eerste keer starten](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.closeType` | Hiermee wordt bepaald of een close-gebeurtenis vastloopt of niet. Geldige waarden zijn `close` (Een levenscyclussessie eindigt en er is een pauze-gebeurtenis ontvangen voor de vorige sessie) en `unknown` (Een levenscyclussessie eindigt zonder pauze-gebeurtenis). Helpt de metrische waarde van de mobiele levenscyclus in te stellen [Crashes](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) metrisch. |
| `xdm.application.isInstall` | De metrische waarde van de mobiele levenscyclus [Installaties](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isLaunch` | De metrische waarde van de mobiele levenscyclus [Starten](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.name` | Helpt de dimensie van de mobiele levenscyclus in te stellen [Toepassings-id](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isUpgrade` | De metrische waarde van de mobiele levenscyclus [Upgrades](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.version` | Helpt de dimensie van de mobiele levenscyclus in te stellen [Toepassings-id](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.sessionLength` | De metrische waarde van de mobiele levenscyclus [Lengte vorige sessie](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.commerce.checkouts.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Afbeeldingen](../../components/metrics/checkouts.md) metrisch. |
| `xdm.commerce.checkouts.value` | Verhoogt de [Afbeeldingen](../../components/metrics/checkouts.md) metrisch met de gewenste hoeveelheid. |
| `xdm.commerce.order.currencyCode` | Hiermee stelt u de [currencyCode](../vars/config-vars/currencycode.md) configuratievariabele. |
| `xdm.commerce.order.purchaseID` | Hiermee stelt u de [purchaseID](../vars/page-vars/purchaseid.md) paginavariabele. |
| `xdm.commerce.order.payments[0].transactionID` | Hiermee stelt u de [transactionID](../vars/page-vars/transactionid.md) paginavariabele. |
| `xdm.commerce.productListAdds.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) metrisch. |
| `xdm.commerce.productListAdds.value` | Verhoogt de [Extra winkelwagentjes](../../components/metrics/cart-additions.md) metrisch. |
| `xdm.commerce.productListOpens.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Houtskaarten](../../components/metrics/carts.md) metrisch. |
| `xdm.commerce.productListOpens.value` | Verhoogt de [Houtskaarten](../../components/metrics/carts.md) metrisch. |
| `xdm.commerce.productListRemovals.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Winkelwagentjes](../../components/metrics/cart-removals.md) metrisch. |
| `xdm.commerce.productListRemovals.value` | Verhoogt de [Winkelwagentjes](../../components/metrics/cart-removals.md) metrisch. |
| `xdm.commerce.productListViews.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Kleuraweergaven](../../components/metrics/cart-views.md) metrisch. |
| `xdm.commerce.productListViews.value` | Verhoogt de [Kleuraweergaven](../../components/metrics/cart-views.md) metrisch. |
| `xdm.commerce.productViews.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de [Productweergaven](../../components/metrics/product-views.md) metrisch. |
| `xdm.commerce.productViews.value` | Verhoogt de [Productweergaven](../../components/metrics/product-views.md) metrisch. |
| `xdm.commerce.purchases.value` | Verhoogt de [Orders](../../components/metrics/orders.md) metrisch. |
| `xdm.device.model` | De dimensie van de mobiele levenscyclus [Apparaatnaam](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.device.colorDepth` | Hiermee stelt u de [Kleurdiepte](../../components/dimensions/color-depth.md) dimensie. |
| `xdm.device.screenHeight` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. |
| `xdm.device.screenWidth` | Hiermee stelt u de [Monitorresolutie](../../components/dimensions/monitor-resolution.md) dimensie. |
| `xdm.device.type` | Het type mobiel apparaat. |
| `xdm.environment.browserDetails.acceptLanguage` | Hiermee stelt u de [Taal](../../components/dimensions/language.md) dimensie. |
| `xdm.environment.browserDetails.cookiesEnabled` | Hiermee stelt u de [Cookie-ondersteuning](../../components/dimensions/cookie-support.md) dimensie. Geldige waarden zijn `Y` (de browser accepteert cookies) en `N` (de browser wijst cookies af). |
| `xdm.environment.browserDetails.javaEnabled` | Hiermee stelt u de [Java ingeschakeld](../../components/dimensions/java-enabled.md) dimensie. Geldige waarden zijn `Y` (Java is ingeschakeld) en `N` (Java is uitgeschakeld). |
| `xdm.environment.browserDetails.userAgent` | Wordt gebruikt als fallback [unieke bezoeker](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans gevuld met de `User-Agent` HTTP request header. U kunt dit veld toewijzen aan een eVar als u het wilt gebruiken in rapporten. |
| `xdm.environment.browserDetails.viewportHeight` | Hiermee stelt u de [Browserhoogte](../../components/dimensions/browser-height.md) dimensie. |
| `xdm.environment.browserDetails.viewportWidth` | Hiermee stelt u de [Browserbreedte](../../components/dimensions/browser-width.md) dimensie. |
| `xdm.environment.carrier` | De dimensie van de mobiele levenscyclus [Naam vervoerder](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.connectionType` | Hiermee stelt u de [Verbindingstype](../../components/dimensions/connection-type.md) dimensie. |
| `xdm.environment.ipV4` | Wordt gebruikt als fallback [unieke bezoeker](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans gevuld met de `X-Forwarded-For` HTTP-header. |
| `xdm.environment.language` | De mobiele dimensie Locale. |
| `xdm.environment.operatingSystem` | De dimensie van de mobiele levenscyclus [Besturingssysteem](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.operatingSystemVersion` | Helpt de dimensie van de mobiele levenscyclus in te stellen [Versie besturingssysteem](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Hiermee worden de respectievelijke instellingen ingesteld [eVar](../../components/dimensions/evar.md) dimensie. |
| `xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier1`<br/>`[...]`<br/>`xdm._experience.analytics.customDImensions.`<br/>`hierarchies.hier5` | Hiermee worden de respectievelijke instellingen ingesteld [Hiërarchie](/help/components/dimensions/hierarchy.md) dimensie. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Overschrijving van het lijstscheidingsteken. Het gebruik van dit veld wordt afgeraden, omdat het scheidingsteken automatisch wordt opgehaald uit [Beheerder verkeersvariabele](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) onder rapportsuite-instellingen. Als u dit veld gebruikt, kunnen er verschillen optreden tussen het gebruikte scheidingsteken en het scheidingsteken dat door Analytics wordt verwacht. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.values`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Een tekenreeks die de respectievelijke [List Prop](../vars/page-vars/prop.md#list-props) waarden. |
| `xdm._experience.analytics.customDimensions.`<br/>`lists.list1.list[].value`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Hiermee worden alle bestanden samengevoegd `value` tekenreeksen in elke respectievelijke `list[]` array met de respectievelijke [Variabele List](../vars/page-vars/list.md). Het scheidingsteken wordt automatisch gekozen op basis van de waarde die is ingesteld in [Instellingen van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). |
| `xdm._experience.analytics.customDimensions.`<br/>`props.prop1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`props.prop75` | Hiermee worden de respectievelijke instellingen ingesteld [Prop](../../components/dimensions/prop.md) dimensie. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.id`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.id` | Toepassingen [gebeurtenisserialisatie](../vars/page-vars/events/event-serialization.md) aan de respectieve [Aangepaste gebeurtenissen](../../components/metrics/custom-events.md) metrisch. Elke gebeurtenis-id bevindt zich in de bovenliggende 100 groepen. Bijvoorbeeld om rangschikking op toe te passen `event678`, gebruik `xdm._experience.analytics.event601to700.event678.id`. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.value`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.value` | Verhoogt de respectieve [Aangepaste gebeurtenissen](../../components/metrics/custom-events.md) metrisch met de gewenste hoeveelheid. Elke gebeurtenis bevindt zich in de bovenliggende 100 groepen. Het veld voor `event567` is `xdm._experience.analytics.event501to600.event567.value`. |
| `xdm.identityMap.ECID[0].id` | De [Adobe Experience Cloud Identity Service ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| `xdm.marketing.trackingCode` | Hiermee stelt u de [Trackingcode](../../components/dimensions/tracking-code.md) dimensie. |
| `xdm.media.mediaTimed.completes.value` | Metrisch voor Media Analytics [Inhoud voltooid](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-complete). |
| `xdm.media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `xdm.media.mediaTimed.federated.value` | Metrisch voor Media Analytics [Federale gegevens](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#federated-data). |
| `xdm.media.mediaTimed.firstQuartiles.value` | Metrisch voor Media Analytics [25 % voortgangsmarkering](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#twenty-five-progress-marker). |
| `xdm.media.mediaTimed.mediaSegmentView.value` | Metrisch voor Media Analytics [Weergaven van inhoudssegmenten](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment-views). |
| `xdm.media.mediaTimed.midpoints.value` | Metrisch voor Media Analytics [Voortgangsmarkering van 50 %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#fifty-progress-marker). |
| `xdm.media.mediaTimed.pauseTime.value` | Metrisch voor Media Analytics [Totale pauzeduur](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#total-pause-duration). |
| `xdm.media.mediaTimed.pauses.value` | Metrisch voor Media Analytics [Gebeurtenissen pauzeren](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#pause-events). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`@id` | De dimensie Media Analytics [Element-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`dc:title` | De dimensie Media Analytics [Videonaam](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | De dimensie Media Analytics [Maker](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Episode.iptc4xmpExt:Number` | De dimensie Media Analytics [Episode](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Genre` | De dimensie Media Analytics [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | De dimensie Media Analytics [Classificatie van inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Season.iptc4xmpExt:Number` | De dimensie Media Analytics [Seizoen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Identifier` | De dimensie Media Analytics [Inhoud-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Name` | De dimensie Media Analytics [Tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`showType` | De dimensie Media Analytics [Tekst tonen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`xmpDM:duration` | De dimensie Media Analytics [Videolengte](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`@id` | De dimensie Media Analytics [Mediasessie-id](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastChannel` | De dimensie Media Analytics [Content Channel](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastContentType` | De dimensie Media Analytics [Inhoudstype](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastNetwork` | De dimensie Media Analytics [Netwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | De dimensie Media Analytics [Segment Inhoud](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`playerName` | De dimensie Media Analytics [Naam van inhoudspeler](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`playerSDKVersion.version` | De dimensie Media Analytics [SDK-versie](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`sourceFeed` | De dimensie Media Analytics [Type mediafeed](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`streamFormat` | De dimensie Media Analytics [Stroomindeling](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
| `xdm.media.mediaTimed.progress10.value` | Metrisch voor Media Analytics [Voortgangsmarkering van tien %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ten-progress-marker). |
| `xdm.media.mediaTimed.progress95.value` | Metrisch voor Media Analytics [95 % voortgangsmarkering](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ninety-five-progress-marker). |
| `xdm.media.mediaTimed.resumes.value` | Metrisch voor Media Analytics [Inhoudshervattingen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-resumes). |
| `xdm.media.mediaTimed.starts.value` | Metrisch voor Media Analytics [Start media](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-starts). |
| `xdm.media.mediaTimed.thirdQuartiles.value` | Metrisch voor Media Analytics [Voortgangsmarkering van 75 %](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#seventy-five-progress-marker). |
| `xdm.media.mediaTimed.timePlayed.value` | Metrisch voor Media Analytics [Tijd van inhoud besteed](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-time-spent). |
| `xdm.media.mediaTimed.totalTimePlayed.value` | Metrisch voor Media Analytics [Tijd besteed aan media](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-time-spent). |
| `xdm.placeContext.geo._schema.latitude` | De breedtegraad van de bezoeker. Helpset [Locatie van mobiele levenscyclus](/help/components/dimensions/lifecycle-dimensions.md) afmetingen. |
| `xdm.placeContext.geo._schema.longitude` | De lengtegellocatie van de bezoeker. Helpset [Locatie van mobiele levenscyclus](/help/components/dimensions/lifecycle-dimensions.md) afmetingen. |
| `xdm.placeContext.geo.postalCode` | De [Postcode](../../components/dimensions/zip-code.md) dimensie. |
| `xdm.placeContext.geo.stateProvince` | De [VS](../../components/dimensions/us-states.md) dimensie. |
| `xdm.placeContext.localTime` | Verschijnt als `t_time_info` in [Gegevensfeeds](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md). |
| `xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Toepassingen [productsyntaxis](../vars/page-vars/products.md) verhandelen naar Vars. |
| `xdm.productListItems[]._experience.analytics.`<br/>`event1to100.event1.value`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Toepassingen [productsyntaxis](../vars/page-vars/products.md) verhandelen naar gebeurtenissen. |
| `xdm.productListItems[].productCategories[].categoryID` | De [Categorie](../../components/dimensions/category.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `xdm.productListItems[].name` | De [Product](../../components/dimensions/product.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. Indien `xdm.productListItems[].SKU` en `xdm.productListItems[].name` beide bevatten gegevens, de waarde in `xdm.productListItems[].SKU` wordt gebruikt. |
| `xdm.productListItems[].priceTotal` | Hiermee bepaalt u de [Ontvangsten](../../components/metrics/revenue.md) metrisch. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `xdm.productListItems[].quantity` | Hiermee bepaalt u de [Eenheden](../../components/metrics/units.md) metrisch. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. |
| `xdm.productListItems[].SKU` | De [Product](../../components/dimensions/product.md) dimensie. Zie ook de [producten](../vars/page-vars/products.md) paginavariabele. Indien `xdm.productListItems[].SKU` en `xdm.productListItems[].name` beide bevatten gegevens, de waarde in `xdm.productListItems[].SKU` wordt gebruikt. |
| `xdm.web.webInteraction.URL` | De [linkURL](../vars/config-vars/linkurl.md) uitvoeringsvariabele. |
| `xdm.web.webInteraction.name` | De [Aangepaste koppeling](../../components/dimensions/custom-link.md), [Koppeling downloaden](../../components/dimensions/download-link.md), of [Koppeling afsluiten](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `xdm.web.webInteraction.type` |
| `xdm.web.webInteraction.type` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `other` (Aangepaste koppelingen), `download` (Koppelingen downloaden) en `exit` (Koppelingen afsluiten). |
| `xdm.web.webPageDetails.URL` | De [Pagina-URL](../../components/dimensions/page-url.md) dimensie. |
| `xdm.web.webPageDetails.isErrorPage` | Markering die helpt de pagina&#39;s te bepalen die niet zijn gevonden [dimensie](../../components/dimensions/pages-not-found.md) en [metrisch](../../components/metrics/pages-not-found.md). |
| `xdm.web.webPageDetails.name` | De [Pagina](../../components/dimensions/page.md) dimensie. |
| `xdm.web.webPageDetails.server` | De [Server](../../components/dimensions/server.md) dimensie. |
| `xdm.web.webPageDetails.siteSection` | De [Sectie Site](../../components/dimensions/site-section.md) dimensie. |
| `xdm.web.webReferrer.URL` | De [Referenter](../../components/dimensions/referrer.md) dimensie. |

{style="table-layout:auto"}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Andere XDM-velden toewijzen aan analytische variabelen

Als er dimensies of metriek zijn die u aan Adobe Analytics wilt toevoegen, kunt u dit door [Contextgegevensvariabelen](../vars/page-vars/contextdata.md).

### Impliciete toewijzing

Alle XDM-veldelementen die niet automatisch worden toegewezen, worden naar Adobe Analytics verzonden als contextgegevens met het voorvoegsel `a.x.` U kunt deze variabele van contextgegevens aan de gewenste variabele van Analyse dan in kaart brengen gebruikend [Verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

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

De Web SDK verzendt die gegevens naar Adobe Analytics als variabele van contextgegevens `a.x._atag.search.term`. U kunt dan een verwerkingsregel gebruiken om die variabele van contextgegevens waarde aan de gewenste variabele van de Analyse toe te wijzen, zoals `eVar`:

![Verwerkingsregel voor zoektermen](assets/examplerule.png)

## Expliciete toewijzing

U kunt XDM-veldelementen ook expliciet toewijzen als contextgegevens. Om het even welk XDM gebiedselement dat uitdrukkelijk in kaart wordt gebracht, gebruikend `contextData` -element, wordt als Context Data zonder voorvoegsel naar Adobe Analytics verzonden. U kunt deze variabele van contextgegevens aan de gewenste variabele van Analyse dan in kaart brengen gebruikend [Verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "analytics": {
                "contextData" : {
                    "someValue" : "1"
                }
            }
        }
    }
})
```

De Web SDK verzendt die gegevens naar Adobe Analytics als variabele van contextgegevens `somevalue` met waarde `1`.  U kunt dan een verwerkingsregel gebruiken om die variabele van contextgegevens waarde aan de gewenste variabele van de Analyse toe te wijzen, zoals `eVar`:

![Verwerkingsregel voor zoektermen](assets/examplerule-explicit.png)
