---
title: Queryparameters voor dataverzameling
description: Vermeldt alle parameters van het vraagkoord die in beeldverzoeken worden gebruikt.
feature: Validation
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
source-git-commit: 799c7d2636dc2ba5db90d2dc400462a412aea9f1
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 5%

---

# Queryparameters voor dataverzameling

De volgende lijst maakt een lijst van alle parameters van het vraagkoord Adobe gebruikt in beeldverzoeken. Deze informatie kan worden gebruikt bij foutopsporing met [Pakketanalysatoren](packet-monitor.md), wanneer [hardwarematige afbeeldingsverzoeken](../other/hardcoded.md)of bij gebruik [Dynamische variabelen](../vars/page-vars/dynamic-variables.md).

| Parameter | Variabele voor analytische implementatie | Beschrijving |
| --- | --- | --- |
| `aamlh` | Geen | Tip voor locatie van Audience Manager. Wordt gebruikt bij de Experience Cloud-integratie van gedeeld profiel. |
| `aamb` | Geen | Audience Manager blob. Wordt gebruikt bij de Experience Cloud-integratie van gedeeld profiel. |
| `aid` | Geen | Analytische bezoeker-id. |
| `AQB` | Geen | Geeft het begin van een queryreeks voor een afbeeldingsaanvraag aan. |
| `AQE` | Geen | Geeft het einde van een afbeeldingsaanvraag aan, wat betekent dat de aanvraag niet is afgekapt. |
| `bh` | Geen | Browserhoogte (in pixels). Gebruikt in de [Hoogte browser](/help/components/dimensions/browser-height.md) dimensie. |
| `bw` | Geen | Browserbreedte (in pixels). Gebruikt in de [Browserbreedte](/help/components/dimensions/browser-width.md) dimensie. |
| `c` | Geen | Kleurkwaliteit (in bits). Gebruikt in de [Kleurdiepte](/help/components/dimensions/color-depth.md) dimensie. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het begin van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het einde van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [Props](/help/components/dimensions/prop.md)of variabelen voor aangepast verkeer. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Het type valuta dat in de hit wordt gebruikt. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Het aantal punten in een domein. Wordt gebruikt om cookies op de juiste wijze op te slaan. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | De tekencodering van de afbeeldingsaanvraag. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | De levensduur van het bezoekerscookie. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Gebruikt in de [Site-secties](/help/components/dimensions/site-section.md) dimensie. |
| `cp` | Geen | Gebruikt in de [Type hit](/help/components/dimensions/hit-type.md) dimensie. |
| `ct` | Geen | Gebruikt in de [Verbindingstype](/help/components/dimensions/connection-type.md) dimensie. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Geeft aan wat er moet worden gebruikt voor dynamische variabelen. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Shorthand voor de `events` queryreeks. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Door komma&#39;s gescheiden lijst met gebeurtenissen op de pagina. Meestal gebruikt [cijfers](/help/components/metrics/overview.md). |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | De huidige URL van de pagina, maximaal 255 bytes. Gebruikt in de [Pagina-URL](/help/components/dimensions/page-url.md) dimensie. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URL&#39;s die langer zijn dan 255 bytes, worden gesplitst. De eerste 255 bytes verschijnen in `g` en alle resterende bytes worden weergegeven in het deelvenster `-g` parameter. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Shorthand voor de `pageName` queryreeks. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Shorthand voor de `pageType` queryreeks. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/hier.md) | Hiërarchieafmetingen. |
| `hp` | Geen | Niet meer gebruikt. In vorige versies van Adobe Analytics, bepaalde als huidige URL de homepage van browser was. |
| `j` | Geen | De JavaScript-versie die in de browser is geïnstalleerd. |
| `k` | Geen | Gebruikt in de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) dimensie. |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | Lijstvariabelen. |
| `lrt` | Geen | De &quot;laatste verzoektiming,&quot;die de roundtrip tijd voor het laatste verzoek, in milliseconden is. Deze wordt alleen verzonden wanneer meerdere aanvragen van een pagina worden verzonden of wanneer de pagina een toepassing van één pagina is (SPA). |
| `mid` | Geen | Experience Cloud bezoeker-id. |
| `ndh` | Geen | Markering die aangeeft of de afbeeldingsaanvraag afkomstig is van AppMeasurement. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hiermee kunt u bepalen waar cookies worden ingesteld. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Object-id voor de laatste pagina. Wordt gebruikt in de Activity Map. |
| `ot` | Geen | Objectnaam voor de laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `p` | Geen | Niet meer gebruikt. Lijst met plug-ins die in de browser worden gebruikt. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Gebruikt in de [Pagina](/help/components/dimensions/page.md) dimensie. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Gebruikt in de [Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) dimensie. |
| `pccr` | Geen | Alleen ingesteld voor nieuwe bezoekers en altijd ingesteld op `true`. Hiermee voorkomt u een oneindige omleiding als een bezoeker cookies weigert. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | Bepaalt het type aangepaste koppeling. Vereist voor [Aangepaste koppelingen](/help/components/dimensions/custom-link.md), [Koppelingen downloaden](/help/components/dimensions/download-link.md), en [Koppelingen afsluiten](/help/components/dimensions/exit-link.md). |
| `pev1` | Geen | De URL waarop de aangepaste koppeling is opgetreden. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | Aangepaste naam voor koppelingsvriendelijk. |
| `pev3` | Geen | Niet meer gebruikt. Bijgehouden mijlpalen in vorige versies van videoverslag. |
| `pf` | Geen | markering van het Platform; uitsluitend voor gebruik door Adobe. Niet wijzigen. |
| `pid` | Geen | Pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pidt` | Geen | Type pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pl` | [`products`](../vars/page-vars/products.md) | Shorthand voor de `products` queryreeks. |
| `products` | [`products`](../vars/page-vars/products.md) | Variabele voor producten. Gebruikt in de [Product](/help/components/dimensions/product.md) en [Categorie](/help/components/dimensions/category.md) afmetingen. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Wordt gebruikt om aankopen te dedupliceren. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Verwijzend URL van de slag. Gebruikt in verkeersbronnen afmetingen, zoals [Referenter](/help/components/dimensions/referrer.md) en [Verwijzen naar domein](/help/components/dimensions/referring-domain.md) |
| `s` | Geen | schermresolutie, in `width x height`. Gebruikt in de [Monitorresoluties](/help/components/dimensions/monitor-resolution.md) dimensie. |
| `server` | [`server`](../vars/page-vars/server.md) | [Server](/help/components/dimensions/server.md) dimensie. |
| `sv` | [`server`](../vars/page-vars/server.md) | Shorthand voor de `server` queryreeks. |
| `state` | [`state`](../vars/page-vars/state.md) | Framedimensie. |
| `t` | Geen | Gegenereerde datum/tijd van de hit. Gebruikt de indeling `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` is datum/tijd in JavaScript. Maand `0` is januari, terwijl maand `11` is december.<br>- `w` is de dag van de week. `0` is zondag, terwijl `6` is zaterdag.<br>- `o` is de negatieve GMT-verschuiving in minuten. Bijvoorbeeld: `420` is GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | De aangepaste tijdstempel die met de hit is ingesteld. Wordt meestal gebruikt voor offline tracering. |
| `v` | Geen | Gebruikt in de [Java ingeschakeld](/help/components/dimensions/java-enabled.md) dimensie. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [Trackingcode](/help/components/dimensions/tracking-code.md) dimensie. |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [eVars](/help/components/dimensions/evar.md)of aangepaste conversieafmetingen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Variabele voor bezoekersidentiteitskaart |
| `vidn` | Geen | Ingesteld op AppMeasurement voor nieuwe bezoekers. Bevat de id-waarde die is opgeslagen in het bezoekerscookie. |
| `vmk` | `vmk` | Niet meer gebruikt. De migratiesleutel van de bezoeker, die implementaties van derde aan eerste-partijkoekjes hielp migreren. |
| `vvp` | `variableProvider` | Wordt gebruikt in gegevensconnectors. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Gebruikt met Gegevensbronnen om online en off-line gegevens samen te binden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Gebruikt in de [Postcode](/help/components/dimensions/zip-code.md) dimensie. |
