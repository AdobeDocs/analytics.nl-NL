---
product: analytics
audience: all
user-guide-title: Analytics-implementatiehandleiding
breadcrumb-title: Implementatiehandleiding
user-guide-description: 'Pas aan welke gegevens worden verzameld om meer uit Adobe Analytics te halen. '
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 69%

---


# Adobe Analytics-implementatiehandleiding {#implementation}

+ [Adobe Analytics implementeren](home.md)
+ [Opmerkingen bij de release Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
+ [Releaseopmerkingen bij AppMeasurement](appmeasurement-updates.md)
+ Variabelen, functies en methoden van Analytics {#vars}
   + [Overzicht](vars/overview.md)
   + Configuratievariabelen {#config-vars}
      + [Overzicht van configuratievariabelen](vars/config-vars/configuration-variables.md)
      + [abort](vars/config-vars/abort.md)
      + [account](vars/config-vars/account.md)
      + [charSet](vars/config-vars/charset.md)
      + [cookieDomain](vars/config-vars/cookiedomain.md)
      + [cookieDomainPeriods](vars/config-vars/cookiedomainperiods.md)
      + [cookieLifetime](vars/config-vars/cookielifetime.md)
      + [currencyCode](vars/config-vars/currencycode.md)
      + [dynamicVariablePrefix](vars/config-vars/dynamicvariableprefix.md)
      + [fpCookieDomainPeriods](vars/config-vars/fpcookiedomainperiods.md)
      + [linkDownloadFileTypes](vars/config-vars/linkdownloadfiletypes.md)
      + [linkExternalFilters](vars/config-vars/linkexternalfilters.md)
      + [linkInternalFilters](vars/config-vars/linkinternalfilters.md)
      + [linkLeaveQueryString](vars/config-vars/linkleavequerystring.md)
      + [linkTrackEvents](vars/config-vars/linktrackevents.md)
      + [linkTrackVars](vars/config-vars/linktrackvars.md)
      + [linkURL](vars/config-vars/linkurl.md)
      + [offlineHitLimit](vars/config-vars/offlinehitlimit.md)
      + [offlineThrottleDelay](vars/config-vars/offlinethrottledelay.md)
      + [trackDownloadLinks](vars/config-vars/trackdownloadlinks.md)
      + [trackExternalLinks](vars/config-vars/trackexternallinks.md)
      + [trackingServer](vars/config-vars/trackingserver.md)
      + [trackingServerSecure](vars/config-vars/trackingserversecure.md)
      + [trackInlineStats](vars/config-vars/trackinlinestats.md)
      + [trackOffline](vars/config-vars/trackoffline.md)
      + [useBeacon](vars/config-vars/usebeacon.md)
      + [useLinkTrackSessionStorage](vars/config-vars/uselinktracksessionstorage.md)
      + [usePlugins](vars/config-vars/useplugins.md)
      + [visitorID](vars/config-vars/visitorid.md)
      + [visitorNamespace](vars/config-vars/visitornamespace.md)
      + [writeSecureCookies](vars/config-vars/writesecurecookies.md)
   + Paginariabelen {#page-vars}
      + [Overzicht van paginavariabelen](vars/page-vars/page-variables.md)
      + [campaign](vars/page-vars/campaign.md)
      + [channel](vars/page-vars/channel.md)
      + [contextData](vars/page-vars/contextdata.md)
      + [Dynamische variabelen](vars/page-vars/dynamic-variables.md)
      + [eVar](vars/page-vars/evar.md)
      + [eVar (Merchandising)](vars/page-vars/evar-merchandising.md)
      + events {#events}
         + [Overzicht van gebeurtenissen](vars/page-vars/events/events-overview.md)
         + [Aankoopgebeurtenis](vars/page-vars/events/event-purchase.md)
         + [Gebeurtenisserialisatie](vars/page-vars/events/event-serialization.md)
      + [hier](vars/page-vars/hier.md)
      + [list](vars/page-vars/list.md)
      + [pageName](vars/page-vars/pagename.md)
      + [pageType](vars/page-vars/pagetype.md)
      + [pageURL](vars/page-vars/pageurl.md)
      + [products](vars/page-vars/products.md)
      + [prop](vars/page-vars/prop.md)
      + [purchaseID](vars/page-vars/purchaseid.md)
      + [referrer](vars/page-vars/referrer.md)
      + [s_objectID](vars/page-vars/s-objectid.md)
      + [server](vars/page-vars/server.md)
      + [state](vars/page-vars/state.md)
      + [timestamp](vars/page-vars/timestamp.md)
      + [transactionID](vars/page-vars/transactionid.md)
      + [zip](vars/page-vars/zip.md)
   + Functies en methoden {#functions}
      + [Overzicht van functies](vars/functions/overview.md)
      + [s_gi](vars/functions/s-gi.md)
      + [t](vars/functions/t-method.md)
      + [tl](vars/functions/tl-method.md)
      + [clearVars](vars/functions/clearvars.md)
      + [doPlugins](vars/functions/doplugins.md)
      + [forceOffline](vars/functions/forceoffline.md)
      + [forceOnline](vars/functions/forceonline.md)
      + [registerPreTrackCallback](vars/functions/registerpretrackcallback.md)
      + [registerPostTrackCallback](vars/functions/registerposttrackcallback.md)
      + [sa](vars/functions/sa-method.md)
      + [Util.cookieRead](vars/functions/util-cookieread.md)
      + [Util.cookieWrite](vars/functions/util-cookiewrite.md)
      + [Util.getQueryParam](vars/functions/util-getqueryparam.md)
   + Plug-ins {#plugins}
      + [Overzicht van plug-ins](vars/plugins/impl-plugins.md)
      + [addProductEvar](vars/plugins/addproductevar.md)
      + [addProductEvent](vars/plugins/addproductevent.md)
      + [apl](vars/plugins/apl.md)
      + [cleanStr](vars/plugins/cleanstr.md)
      + [formatTime](vars/plugins/formattime.md)
      + [getAndPersistValue](vars/plugins/getandpersistvalue.md)
      + [getGeoCoordinates](vars/plugins/getgeocoordinates.md)
      + [getNewRepeat](vars/plugins/getnewrepeat.md)
      + [getPageLoadTime](vars/plugins/getpageloadtime.md)
      + [getPageName](vars/plugins/getpagename.md)
      + [getPercentPageViewed](vars/plugins/getpercentpageviewed.md)
      + [getPreviousValue](vars/plugins/getpreviousvalue.md)
      + [getQueryParam](vars/plugins/getqueryparam.md)
      + [getResponsiveLayout](vars/plugins/getresponsivelayout.md)
      + [getTimeBetweenEvents](vars/plugins/gettimebetweenevents.md)
      + [getTimeParting](vars/plugins/gettimeparting.md)
      + [getTimeSinceLastVisit](vars/plugins/gettimesincelastvisit.md)
      + [getTimeToComplete](vars/plugins/gettimetocomplete.md)
      + [getValOnce](vars/plugins/getvalonce.md)
      + [getVisitDuration](vars/plugins/getvisitduration.md)
      + [getVisitNum](vars/plugins/getvisitnum.md)
      + [inList](vars/plugins/inlist.md)
      + [manageVars](vars/plugins/managevars.md)
      + [Nummersuite](vars/plugins/numberssuite.md)
      + [p_fo](vars/plugins/p-fo.md)
      + [pt](vars/plugins/pt-plugin.md)
      + [removeFromList](vars/plugins/removefromlist.md)
      + [websiteBot](vars/plugins/websitebot.md)
   + [Module integreren](vars/integrate.md)
+ Implementatie van Adobe Analytics voorbereiden {#prepare}
   + [Een datalaag maken](prepare/data-layer.md)
   + [Overwegingen voor algemene rapportsuites](prepare/global-rs.md)
   + [Tags implementeren met meerdere suite](prepare/multi-suite-tagging.md)
   + [Implementatiemodel](prepare/implementation-modal.md)
   + [Een document voor het ontwerp van een oplossing maken](prepare/solution-design.md)
   + [Een bestaande Adobe Analytics-implementatie op zich nemen](prepare/existing-implementation.md)
+ Analyses implementeren met gebruik van Experience Platform Edge {#aep-edge}
   + [Overzicht van Experience Edge](aep-edge/overview.md)
   + [Variabele toewijzen](aep-edge/variable-mapping.md)
   + Web SDK {#web-sdk}
      + [Overzicht van Web SDK](aep-edge/web-sdk/overview.md)
   + Mobile SDK {#mobile-sdk}
      + [Overzicht van Mobile SDK](aep-edge/mobile-sdk/overview.md)
   + Edge-API {#edge-api}
      + [Overzicht van Edge API](aep-edge/edge-api/overview.md)
+ Analyses implementeren met de extensie Adobe Analytics {#launch}
   + [Overzicht van codes](launch/overview.md)
   + [Een Adobe Analytics-tageigenschap maken](launch/create-analytics-property.md)
   + [Distribueren naar een ontwikkelomgeving](launch/deploy-dev.md)
   + [Valideren en publiceren naar productie](launch/validate-publish-prod.md)
   + [Datalaagobjecten toewijzen aan data-elementen](launch/layer-to-elements.md)
   + [Taggegevenselementen toewijzen aan analytische variabelen](launch/elements-to-variable.md)
+ Analytics implementeren met JavaScript {#js}
   + [JavaScript-overzicht](js/overview.md)
   + [Opt-outkoppelingen implementeren](js/opt-out.md)
   + [Overschrijvingen van variabelen](js/overrides.md)
   + [Migreren vanuit H-code](js/migrate-from-hcode.md)
   + H-code {#h-code}
      + [H Code-overzicht](js/h-code/overview.md)
      + Dynamische accounts {#dynamicaccount}
         + [Overzicht van dynamische accounts](js/h-code/dynamicaccount/overview.md)
         + [dynamicAccountList](js/h-code/dynamicaccount/dynamicaccountlist.md)
         + [dynamicAccountMatch](js/h-code/dynamicaccount/dynamicaccountmatch.md)
         + [dynamicAccountSelection](js/h-code/dynamicaccount/dynamicaccountselection.md)
      + [Problemen met H-code oplossen](js/h-code/troubleshooting.md)
   + Verouderde cross-device identificatie {#xdevice-visid}
      + [Overzicht van het verbinden van gebruikers via verschillende apparaten](js/xdevice-visid/xdevice-connecting.md)
      + [Persistentie van variabelen](js/xdevice-visid/variable-persistence.md)
      + [Voorbeeld van bezoek](js/xdevice-visid/visit-example.md)
      + [Veelgestelde vragen over verouderde cross-device](js/xdevice-visid/xdevice-faq.md)
   + [Problemen met AppMeasurement oplossen](js/troubleshooting.md)
+ Analytics implementeren op andere platforms {#other}
   + [Analytics implementeren met behulp van hardwarematige afbeeldingsaanvragen](other/hardcoded.md)
   + [Analytics implementeren met DTM](other/dtm-implementation-overview.md)
   + [Analytics implementeren op Ajax](other/ajax.md)
   + [Analytics implementeren op AMP](other/amp.md)
   + [Analytics implementeren op digitale assistenten](other/digital-assistants.md)
   + [Analytics implementeren op Facebook Instant Articles](other/fb-instant-articles.md)
+ [Analytics implementeren op mobiele apparaten](mobile-device-sdk.md)
+ Gebruiksscenario&#39;s implementeren {#use-cases}
   + [AppMeasurement gebruiken met iFrames](use-cases/iframe.md)
   + [Verschillende implementatietypen bijhouden](use-cases/cross-type-implementation.md)
   + [Externe e-mailtracering](use-cases/email-external.md)
+ Uw implementatie valideren {#validate}
   + [Verouderde Adobe Experience Cloud-foutopsporing](validate/debugger.md)
   + [Queryparameters voor dataverzameling](validate/query-parameters.md)
   + [Pakketbewaking](validate/packet-monitor.md)
   + [Hash-botsingen](validate/hash-collisions.md)
+ [Veelgestelde vragen](faq.md)
+ Uw implementatie controleren {#review}
   + [Gerichte revisie (na elke release van de website)](review/focused-review.md)
   + [Volledige controle (elke 6 maanden)](review/full-review.md)
   + [De bovenste 5 KPI&#39;s defini??ren](review/define-kpis.md)
