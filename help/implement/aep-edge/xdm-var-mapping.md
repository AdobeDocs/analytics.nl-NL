---
title: XML-objectvariabele toewijzen aan Adobe Analytics
description: Geef aan welke XDM-velden door Edge automatisch worden toegewezen aan analytische variabelen.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 5e97c9a4a3c7368cefb3cc6a7bc89a450e6e3f4a
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---

# XML-objectvariabele toewijzen aan Adobe Analytics

In de volgende tabel staan de XDM-variabelen die de Adobe Experience Platform-Edge Network automatisch toewijst aan Adobe Analytics. Als u deze XDM-veldpaden gebruikt, is er geen extra configuratie nodig om gegevens naar Adobe Analytics te verzenden. Deze velden worden opgenomen in de veldgroep **[!UICONTROL Adobe Analytics ExperienceEvent Template]** . U wordt aangeraden deze velden te gebruiken als u gegevens wilt verzenden naar Adobe Analytics en Adobe Experience Platform.

Als uw organisatie van plan is naar Customer Journey Analytics te gaan, raadt Adobe u aan in plaats daarvan het `data` -object te gebruiken om gegevens rechtstreeks naar Adobe Analytics te verzenden zonder zich aan een schema te houden. Op deze manier kan uw organisatie uw eigen schema gebruiken in plaats van [!UICONTROL Adobe Analytics ExperienceEvent Template] (dat minder van toepassing is op Customer Journey Analytics). Zie [ objecten van Gegevens veranderlijke afbeelding aan Adobe Analytics ](data-var-mapping.md) voor een gelijkaardige toewijzingstabel.

## Waardeprioriteiten

De meeste XDM objecten gebieden in deze lijst vallen met a [ gebied van gegevensobjecten ](data-var-mapping.md) samen. Als u zowel een bepaald XDM-objectveld als het bijbehorende gegevensobjectveld instelt, krijgt het gegevensobjectveld prioriteit. Als u zowel het XDM-objectveld als het gegevensobjectveld gebruikt, raadt de Adobe aan aangepaste gebeurtenissen in te stellen met behulp van het gegevensobjectveld. Als het veld `data.__adobe.analytics.events` aanwezig is, worden alle XDM-objectvelden met betrekking tot handel en aangepaste gebeurtenissen overschreven.

## XML-objectveldtoewijzing

De vorige updates aan deze lijst kunnen op [ worden gevonden van deze pagina begaat geschiedenis op GitHub ](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/xdm-var-mapping.md).

| XDM-veldpad | Variabele en beschrijving voor analyse |
| --- | --- |
| `xdm.application.isClose` | De hulp bepaalt de mobiele metrische levenscyclus [ crasht ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | De hulp bepaalt wanneer om de mobiele metrische levenscyclus van de levenscyclus te verhogen [ Eerste Lanceringen ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.closeType` | Hiermee wordt bepaald of een close-gebeurtenis vastloopt of niet. Geldige waarden zijn `close` (een levenscyclussessie eindigt en er is een pauze-gebeurtenis ontvangen voor de vorige sessie) en `unknown` (een levenscyclussessie eindigt zonder een pauze-gebeurtenis). De hulp plaatst de mobiele metrische levenscyclus [ loopt ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) metrisch vast. |
| `xdm.application.isInstall` | De mobiele metrische levenscyclus [ installeert ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isLaunch` | De mobiele metrische levenscyclus [ Lanceringen ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.name` | Helpt de mobiele dimensie van de levenscyclus [ identiteitskaart van de Toepassing ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) plaatsen. |
| `xdm.application.isUpgrade` | De mobiele metrische levenscyclus [ Verbeteringen ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.version` | Helpt de mobiele dimensie van de levenscyclus [ identiteitskaart van de Toepassing ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) plaatsen. |
| `xdm.application.sessionLength` | De mobiele metrische levenscyclus [ Vorige Lengte van de Zitting ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.commerce.checkouts.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op [ metrische controles ](../../components/metrics/checkouts.md) toe. |
| `xdm.commerce.checkouts.value` | Verhoogt de [ metrische controles ](../../components/metrics/checkouts.md) door de gewenste hoeveelheid. |
| `xdm.commerce.order.currencyCode` | Plaatst de [ currencyCode ](../vars/config-vars/currencycode.md) configuratievariabele. |
| `xdm.commerce.order.purchaseID` | Plaatst de [ purchaseID ](../vars/page-vars/purchaseid.md) paginariabele. |
| `xdm.commerce.order.payments[0].transactionID` | Plaatst de [ transactionID ](../vars/page-vars/transactionid.md) paginariabele. |
| `xdm.commerce.productListAdds.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op [ metrische Toevoegingen van de Kunst ](../../components/metrics/cart-additions.md) toe. |
| `xdm.commerce.productListAdds.value` | Verhoogt metrisch de [ Toevoegingen van het Kunst ](../../components/metrics/cart-additions.md). |
| `xdm.commerce.productListOpens.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op [ metrisch van Karretjes ](../../components/metrics/carts.md) toe. |
| `xdm.commerce.productListOpens.value` | Verhoogt metrisch de [ Havens ](../../components/metrics/carts.md). |
| `xdm.commerce.productListRemovals.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op de [ metrische Verwijderingen van de Kunst ](../../components/metrics/cart-removals.md) toe. |
| `xdm.commerce.productListRemovals.value` | Verhoogt metrisch de [ Verwijderingen van de Kaart ](../../components/metrics/cart-removals.md). |
| `xdm.commerce.productListViews.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op de [ metrische Meningen van de Kaart ](../../components/metrics/cart-views.md) toe. |
| `xdm.commerce.productListViews.value` | Verhoogt de [ metrische Meningen van het Kart ](../../components/metrics/cart-views.md). |
| `xdm.commerce.productViews.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op de [ metrische meningen van het Product ](../../components/metrics/product-views.md) toe. |
| `xdm.commerce.productViews.value` | Verhoogt de [ metrische Meningen van het Product ](../../components/metrics/product-views.md). |
| `xdm.commerce.purchases.value` | Verhoogt metrisch de [ Orden ](../../components/metrics/orders.md). |
| `xdm.device.model` | De mobiele dimensie van de levenscyclus [ Naam van het Apparaat ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.device.colorDepth` | De hulp plaatst de ](../../components/dimensions/color-depth.md) dimensie van de Diepte van de 0} Kleur.[ |
| `xdm.device.screenHeight` | De hulp plaatst de ](../../components/dimensions/monitor-resolution.md) dimensie van de Resolutie van de Monitor 0}.[ |
| `xdm.device.screenWidth` | De hulp plaatst de ](../../components/dimensions/monitor-resolution.md) dimensie van de Resolutie van de Monitor 0}.[ |
| `xdm.device.type` | Het type mobiel apparaat. |
| `xdm.environment.browserDetails.acceptLanguage` | De hulp plaatst de ](../../components/dimensions/language.md) dimensie van de Taal 0} {.[ |
| `xdm.environment.browserDetails.cookiesEnabled` | Plaatst de ](../../components/dimensions/cookie-support.md) dimensie van de Steun van het 0} Koekje. [ Geldige waarden zijn `Y` (de browser accepteert cookies) en `N` (de browser weigert cookies). |
| `xdm.environment.browserDetails.javaEnabled` | Plaatst [ toegelaten Java ](../../components/dimensions/java-enabled.md) dimensie. Geldige waarden zijn `Y` (Java is ingeschakeld) en `N` (Java is uitgeschakeld). |
| `xdm.environment.browserDetails.userAgent` | Gebruikt als een fallback [ unieke bezoeker ](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans ingevuld met de `User-Agent` HTTP-aanvraagheader. U kunt dit veld toewijzen aan een eVar als u het wilt gebruiken in rapporten. |
| `xdm.environment.browserDetails.viewportHeight` | Plaatst de [ Browser Hoogte ](../../components/dimensions/browser-height.md) afmeting. |
| `xdm.environment.browserDetails.viewportWidth` | Plaatst de [ Browser dimensie van de Breedte ](../../components/dimensions/browser-width.md). |
| `xdm.environment.carrier` | De mobiele dimensie van de levenscyclus [ Naam van de Drager ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.connectionType` | Helpt het [ type van Verbinding ](../../components/dimensions/connection-type.md) afmeting te plaatsen. |
| `xdm.environment.ipV4` | Gebruikt als een fallback [ unieke bezoeker ](../../components/metrics/unique-visitors.md) identificatiemethode. Doorgaans gevuld met behulp van de `X-Forwarded-For` HTTP-header. |
| `xdm.environment.language` | De mobiele dimensie Locale. |
| `xdm.environment.operatingSystem` | De mobiele dimensie van de levenscyclus [ Werkend Systeem ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.operatingSystemVersion` | De hulp plaatst de mobiele dimensie van de levenscyclus [ Versie van het Werkende Systeem ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Plaatst de respectieve [ eVar ](../../components/dimensions/evar.md) dimensie. |
| `xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier1`<br/>`[...]`<br/>`xdm._experience.analytics.customDImensions.`<br/>`hierarchies.hier5` | Plaatst de respectieve [ dimensie van de Hiërarchie ](/help/components/dimensions/hierarchy.md). |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Overschrijving van het lijstscheidingsteken. Het gebruiken van dit gebied wordt niet geadviseerd, aangezien het scheidingsteken automatisch van [ veranderlijke admin van het Verkeer ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) onder de montages van de rapportreeks wordt teruggewonnen. Als u dit veld gebruikt, kunnen er verschillen optreden tussen het gebruikte scheidingsteken en het scheidingsteken dat door Analytics wordt verwacht. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.values`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Een koordserie die de respectieve [ Prop van de Lijst ](../vars/page-vars/prop.md#list-props) waarden bevat. |
| `xdm._experience.analytics.customDimensions.`<br/>`lists.list1.list[].value`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Voegt alle `value` koorden in elke respectieve `list[]` serie aan zijn respectieve [ variabele van de Lijst ](../vars/page-vars/list.md) samen. Scheidingsteken wordt automatisch gekozen gebaseerd op de waarde die in [ de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) wordt geplaatst. |
| `xdm._experience.analytics.customDimensions.`<br/>`props.prop1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`props.prop75` | Plaatst de respectieve ](../../components/dimensions/prop.md) dimensie van 0} Prop.[ |
| `xdm._experience.analytics.event1to100.`<br/>`event1.id`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.id` | Past [ gebeurtenisrangschikking ](../vars/page-vars/events/event-serialization.md) op de respectieve [ metrische gebeurtenissen van de Douane ](../../components/metrics/custom-events.md) toe. Elke gebeurtenis-id bevindt zich in de bovenliggende 100 groepen. Als u bijvoorbeeld serienummering wilt toepassen op `event678` , gebruikt u `xdm._experience.analytics.event601to700.event678.id` . |
| `xdm._experience.analytics.event1to100.`<br/>`event1.value`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.value` | Verhoogt de respectieve [ metrische gebeurtenissen van de Douane ](../../components/metrics/custom-events.md) door de gewenste hoeveelheid. Elke gebeurtenis bevindt zich in de bovenliggende 100 groepen. Het veld voor `event567` is bijvoorbeeld `xdm._experience.analytics.event501to600.event567.value` . |
| `xdm.identityMap.ECID[0].id` | De [ identiteitskaart van de Identiteitsdienst van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| `xdm.marketing.trackingCode` | Plaatst de [ het Volgen dimensie van de Code ](../../components/dimensions/tracking-code.md). |
| `xdm.media.mediaTimed.completes.value` | De het stromen media metrische [ Volledige Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-complete). |
| `xdm.media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `xdm.media.mediaTimed.federated.value` | De het stromen media metrische [ Federale Gegevens ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#federated-data). |
| `xdm.media.mediaTimed.firstQuartiles.value` | De het stromen media metrische [ Twintig-5 % Teller van de Voortgang ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#twenty-five-progress-marker). |
| `xdm.media.mediaTimed.mediaSegmentView.value` | De het stromen media metrische [ Kijken van het Segment van de Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment-views). |
| `xdm.media.mediaTimed.midpoints.value` | De het stromen media metrische [ 50 % Teller van de Voortgang ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#fifty-progress-marker). |
| `xdm.media.mediaTimed.pauseTime.value` | De het stromen media metrische [ Totale Duur van de Pauze ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#total-pause-duration). |
| `xdm.media.mediaTimed.pauses.value` | De het stromen media metrische [ Gebeurtenissen van de Pauze ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#pause-events). |
| `xdm.mediaCollection.sessionDetails.assetID` | De het stromen media afmeting [ identiteitskaart van Activa ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `xdm.mediaCollection.sessionDetails.friendlyName` | De het stromen media afmeting [ Naam van de Video ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `xdm.mediaCollection.sessionDetails.originator` | De het stromen media afmeting [ Afdeler ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `xdm.mediaCollection.sessionDetails.episode` | De het stromen media afmeting [ Aflevering ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `xdm.mediaCollection.sessionDetails.genre` | De het stromen media afmeting [ Genre ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `xdm.mediaCollection.sessionDetails.rating` | De het stromen media afmeting [ Inhoudsclassificatie ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `xdm.mediaCollection.sessionDetails.season` | De het stromen media afmeting [ Seizoen ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `xdm.mediaCollection.sessionDetails.name` | De het stromen media afmeting [ identiteitskaart van de Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `xdm.mediaCollection.sessionDetails.show` | De het stromen media dimensie [ tonen ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `xdm.mediaCollection.sessionDetails.showType` | De het stromen media afmeting [ toont Type ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `xdm.mediaCollection.sessionDetails.length` | De het stromen media dimensie [ Videolengte ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.@id` | De het stromen media afmeting [ identiteitskaart van de Zitting van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `xdm.mediaCollection.sessionDetails.channel` | Het stromen media afmeting [ Kanaal van de Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `xdm.mediaCollection.sessionDetails.contentType` | Het stromen media afmeting [ Type van Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `xdm.mediaCollection.sessionDetails.network` | Het stromen media afmeting [ Netwerk ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | Het stromen media afmeting [ Segment van de Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `xdm.mediaCollection.sessionDetails.playerName` | De het stromen media afmeting [ Naam van de Speler van de Inhoud ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `xdm.mediaCollection.sessionDetails.appVersion` | De het stromen media afmeting [ Versie van SDK ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `xdm.mediaCollection.sessionDetails.feed` | De het stromen media afmeting [ het Type van Diervoeders van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `xdm.mediaCollection.sessionDetails.streamFormat` | De het stromen media afmeting [ Formaat van de Stroom ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
| `xdm.media.mediaTimed.progress10.value` | De het stromen media metrische [ tien % Teller van de Voortgang ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ten-progress-marker). |
| `xdm.media.mediaTimed.progress95.value` | De het stromen media metrische [ 95 % Teller van de Voortgang ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ninety-five-progress-marker). |
| `xdm.mediaCollection.sessionDetails.hasResume` | De het stromen media metrische [ Inhoud hervat ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-resumes). |
| `xdm.media.mediaTimed.starts.value` | De het stromen media metrische [ Media begint ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-starts). |
| `xdm.media.mediaTimed.thirdQuartiles.value` | De het stromen media metrische [ 75 % Teller van de Voortgang ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#seventy-five-progress-marker). |
| `xdm.media.mediaTimed.timePlayed.value` | De het stromen media metrische [ Tijd van de Inhoud bestede ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-time-spent). |
| `xdm.media.mediaTimed.totalTimePlayed.value` | De het stromen media metrische [ Tijd van Media bestede ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-time-spent). |
| `xdm.placeContext.geo._schema.latitude` | De breedtegraad van de bezoeker. Helpt ](/help/components/dimensions/lifecycle-dimensions.md) afmetingen van de plaats van de de levenscyclus van 0} Mobiele.[ |
| `xdm.placeContext.geo._schema.longitude` | De lengtegellocatie van de bezoeker. Helpt ](/help/components/dimensions/lifecycle-dimensions.md) afmetingen van de plaats van de de levenscyclus van 0} Mobiele.[ |
| `xdm.placeContext.geo.postalCode` | De [ dimensie van het Postcode ](../../components/dimensions/zip-code.md). |
| `xdm.placeContext.geo.stateProvince` | De ](../../components/dimensions/us-states.md) dimensie van de Staten van 0} VS.[ |
| `xdm.placeContext.localTime` | Verschijnt als `t_time_info` in [ het voer van Gegevens ](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md). |
| `xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Past [ productsyntaxis ](../vars/page-vars/products.md) merchandising op eVars toe. |
| `xdm.productListItems[]._experience.analytics.`<br/>`event1to100.event1.value`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Past [ productsyntaxis ](../vars/page-vars/products.md) merchandising op gebeurtenissen toe. |
| `xdm.productListItems[].productCategories[].categoryID` | De [ dimensie van de Categorie ](../../components/dimensions/category.md). Zie ook de [ producten ](../vars/page-vars/products.md) paginariabele. |
| `xdm.productListItems[].name` | De [ dimensie van het Product ](../../components/dimensions/product.md). Zie ook de [ producten ](../vars/page-vars/products.md) paginariabele. Als `xdm.productListItems[].SKU` en `xdm.productListItems[].name` beide gegevens bevatten, wordt de waarde in `xdm.productListItems[].SKU` gebruikt. |
| `xdm.productListItems[].priceTotal` | De hulp bepaalt de [ metrische Inkomsten ](../../components/metrics/revenue.md). Zie ook de [ producten ](../vars/page-vars/products.md) paginariabele. |
| `xdm.productListItems[].quantity` | De hulp bepaalt de [ metrische eenheden ](../../components/metrics/units.md). Zie ook de [ producten ](../vars/page-vars/products.md) paginariabele. |
| `xdm.productListItems[].SKU` | De [ dimensie van het Product ](../../components/dimensions/product.md). Zie ook de [ producten ](../vars/page-vars/products.md) paginariabele. Als `xdm.productListItems[].SKU` en `xdm.productListItems[].name` beide gegevens bevatten, wordt de waarde in `xdm.productListItems[].SKU` gebruikt. |
| `xdm.web.webInteraction.URL` | De [ linkURL ](../vars/config-vars/linkurl.md) implementatievariabele. |
| `xdm.web.webInteraction.name` | De [ verbinding van de Douane ](../../components/dimensions/custom-link.md), [ Verbinding van de Download ](../../components/dimensions/download-link.md), of [ Verbinding van de Uitgang ](../../components/dimensions/exit-link.md) dimensie, afhankelijk van de waarde in `xdm.web.webInteraction.type` |
| `xdm.web.webInteraction.type` | Bepaalt het type van geklikte verbinding. Geldige waarden zijn `other` (Aangepaste koppelingen), `download` (Koppelingen downloaden) en `exit` (Koppelingen afsluiten). |
| `xdm.web.webPageDetails.URL` | De [ pagina URL ](../../components/dimensions/page-url.md) afmeting. |
| `xdm.web.webPageDetails.isErrorPage` | De vlag die de hulp bepaalt &quot;Pagina&#39;s niet gevonden&quot;[ afmeting ](../../components/dimensions/pages-not-found.md) en [ metrisch ](../../components/metrics/pages-not-found.md). |
| `xdm.web.webPageDetails.name` | De [ dimensie van de Pagina ](../../components/dimensions/page.md). |
| `xdm.web.webPageDetails.server` | De [ dimensie van de Server ](../../components/dimensions/server.md). |
| `xdm.web.webPageDetails.siteSection` | De ](../../components/dimensions/site-section.md) dimensie van de Sectie van 0} Plaats.[ |
| `xdm.web.webReferrer.URL` | De [ dimensie van de Verwijzer ](../../components/dimensions/referrer.md). |

{style="table-layout:auto"}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Andere XDM-velden toewijzen aan analytische variabelen

Als er om het even welke afmetingen of metriek zijn die u aan Adobe Analytics wilt toevoegen, kunt u dit door [ variabelen van de Gegevens van de Context ](../vars/page-vars/contextdata.md) doen.

### Impliciete toewijzing

Om het even welke XDM gebiedselementen die niet automatisch in kaart worden gebracht worden verzonden naar Adobe Analytics als Gegevens van de Context met de prefix `a.x.` u kunt deze variabele van contextgegevens aan de gewenste variabele van de Analyse dan in kaart brengen gebruikend [ Regels van de Verwerking ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

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

De Web SDK verzendt die gegevens naar Adobe Analytics als variabele van contextgegevens `a.x._atag.search.term`. Vervolgens kunt u een verwerkingsregel gebruiken om de waarde van die variabele voor de contextgegevens toe te wijzen aan de gewenste variabele Analytics, zoals een `eVar` :

![ de verwerkingsregel van de term van het Onderzoek ](assets/examplerule.png)

## Expliciete toewijzing

U kunt XDM-veldelementen ook expliciet toewijzen als contextgegevens. Elk XDM-veldelement dat expliciet wordt toegewezen, met behulp van het `contextData` -element, wordt zonder voorvoegsel verzonden naar Adobe Analytics als Context Data. U kunt deze variabele van contextgegevens aan de gewenste variabele van Analytics dan in kaart brengen gebruikend [ Regels van de Verwerking ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html). Als u bijvoorbeeld de volgende gebeurtenis verzendt:

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

De Web SDK verzendt die gegevens naar Adobe Analytics als de variabele van contextgegevens `somevalue` met waarde `1`.  Vervolgens kunt u een verwerkingsregel gebruiken om de waarde van die variabele voor de contextgegevens toe te wijzen aan de gewenste variabele Analytics, zoals een `eVar` :

![ de verwerkingsregel van de term van het Onderzoek ](assets/examplerule-explicit.png)
