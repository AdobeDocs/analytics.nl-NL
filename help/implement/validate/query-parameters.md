---
title: Queryparameters voor dataverzameling
description: Vermeldt alle parameters van het vraagkoord die in beeldverzoeken worden gebruikt.
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
source-git-commit: 7025d132da9d281da6d57973a195a5e86a39bf18
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 5%

---

# Queryparameters voor dataverzameling

De volgende lijst maakt een lijst van alle parameters van het vraagkoord Adobe gebruikt in beeldverzoeken. Deze informatie kan worden gebruikt wanneer het zuiveren gebruikend [Pakketanalysatoren](packet-monitor.md), wanneer [hardcoding beeld verzoeken](../other/hardcoded.md), of wanneer het gebruiken van [Dynamische Variabelen](../vars/page-vars/dynamic-variables.md).

| Parameter | Variabele voor analytische implementatie | Beschrijving |
| --- | --- | --- |
| `aamlh` | Geen | Tip voor locatie van Audience Manager. Wordt gebruikt bij de Experience Cloud-integratie van gedeeld profiel. |
| `aamb` | Geen | Audience Manager blob. Wordt gebruikt bij de Experience Cloud-integratie van gedeeld profiel. |
| `aid` | Geen | Analytische bezoeker-id. |
| `AQB` | Geen | Geeft het begin van een queryreeks voor een afbeeldingsaanvraag aan. |
| `AQE` | Geen | Geeft het einde van een afbeeldingsaanvraag aan, wat betekent dat de aanvraag niet is afgekapt. |
| `bh` | Geen | Browserhoogte (in pixels). Wordt gebruikt in de afmetingen [Browserhoogte](/help/components/dimensions/browser-height.md). |
| `bw` | Geen | Browserbreedte (in pixels). Wordt gebruikt in de afmetingen [Browserbreedte](/help/components/dimensions/browser-width.md). |
| `c` | Geen | Kleurkwaliteit (in bits). Wordt gebruikt in de [Kleurdiepte](/help/components/dimensions/color-depth.md)-dimensie. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het begin van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het einde van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `c1` - `c75` | [`prop1` -  `prop75`](../vars/page-vars/prop.md) | [Props](/help/components/dimensions/prop.md), of variabelen van het douaneverkeer. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Het type valuta dat in de hit wordt gebruikt. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Het aantal punten in een domein. Wordt gebruikt om cookies op de juiste wijze op te slaan. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | De tekencodering van de afbeeldingsaanvraag. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | De levensduur van het bezoekerscookie. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Wordt gebruikt in de [Site-secties](/help/components/dimensions/site-section.md)-dimensie. |
| `cp` | Geen | Wordt gebruikt in de [Hit Type](/help/components/dimensions/hit-type.md)-dimensie. |
| `ct` | Geen | Gebruikt in [het Type van Verbinding](/help/components/dimensions/connection-type.md) afmeting. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Geeft aan wat er moet worden gebruikt voor dynamische variabelen. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Shorthand voor het `events` vraagkoord. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Door komma&#39;s gescheiden lijst met gebeurtenissen op de pagina. Wordt gebruikt door de meeste [metriek](/help/components/metrics/overview.md). |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | De huidige URL van de pagina, maximaal 255 bytes. Wordt gebruikt in de [Pagina-URL](/help/components/dimensions/page-url.md)-dimensie. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URL&#39;s die langer zijn dan 255 bytes, worden gesplitst. De eerste 255 bytes verschijnen in de `g` parameter, en alle resterende bytes verschijnen in `-g` parameter. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Shorthand voor het `pageName` vraagkoord. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Shorthand voor het `pageType` vraagkoord. |
| `h1` -  `h5` | [`hier1` -  `hier5`](../vars/page-vars/hier.md) | Hiërarchieafmetingen. |
| `hp` | Geen | Niet meer gebruikt. In vorige versies van Adobe Analytics, bepaalde als huidige URL de homepage van browser was. |
| `j` | Geen | De JavaScript-versie die in de browser is geïnstalleerd. |
| `k` | Geen | Wordt gebruikt in de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md)-dimensie. |
| `l1` -  `l3` | [`list1` -  `list3`](../vars/page-vars/list.md) | Lijstvariabelen. |
| `lrt` | Geen | De &quot;laatste verzoektiming,&quot;die de roundtrip tijd voor het laatste verzoek, in milliseconden is. Deze wordt alleen verzonden wanneer meerdere aanvragen van een pagina worden verzonden of wanneer de pagina een toepassing van één pagina is (SPA). |
| `mid` | Geen | Experience Cloud bezoeker-id. |
| `ndh` | Geen | Markering die aangeeft of de afbeeldingsaanvraag afkomstig is van AppMeasurement. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hiermee kunt u bepalen waar cookies worden ingesteld. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Object-id voor de laatste pagina. Wordt gebruikt in de Activity Map. |
| `ot` | Geen | Objectnaam voor de laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `p` | Geen | Niet meer gebruikt. Lijst met plug-ins die in de browser worden gebruikt. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Gebruikt in [Pagina](/help/components/dimensions/page.md) afmeting. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Gebruikt in [Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) dimensie. |
| `pccr` | Geen | Alleen ingesteld voor nieuwe bezoekers en altijd ingesteld op `true`. Hiermee voorkomt u een oneindige omleiding. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | Bepaalt het type aangepaste koppeling. Vereist voor [Aangepaste koppelingen](/help/components/dimensions/custom-link.md), [Koppelingen downloaden](/help/components/dimensions/download-link.md) en [Koppelingen afsluiten](/help/components/dimensions/exit-link.md). |
| `pev1` | Geen | De URL waarop de aangepaste koppeling is opgetreden. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | Aangepaste naam voor koppelingsvriendelijk. |
| `pev3` | Geen | Niet meer gebruikt. Bijgehouden mijlpalen in vorige versies van videoverslag. |
| `pf` | Geen | markering van het Platform; uitsluitend voor gebruik door Adobe. Niet wijzigen. |
| `pid` | Geen | Pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pidt` | Geen | Type pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pl` | [`products`](../vars/page-vars/products.md) | Shorthand voor het `products` vraagkoord. |
| `products` | [`products`](../vars/page-vars/products.md) | Variabele voor producten. Gebruikt in [Product](/help/components/dimensions/product.md) en [Categorie](/help/components/dimensions/category.md) afmetingen. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Wordt gebruikt om aankopen te dedupliceren. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Verwijzend URL van de slag. Gebruikt in verkeersbronnen afmetingen zoals [Referrer](/help/components/dimensions/referrer.md) en [Refering domain](/help/components/dimensions/referring-domain.md) |
| `s` | Geen | Schermresolutie, in `width x height`. Wordt gebruikt in de [Monitor-resoluties](/help/components/dimensions/monitor-resolution.md)-dimensie. |
| `server` | [`server`](../vars/page-vars/server.md) | [](/help/components/dimensions/server.md) Serverdimensie. |
| `sv` | [`server`](../vars/page-vars/server.md) | Shorthand voor het `server` vraagkoord. |
| `state` | [`state`](../vars/page-vars/state.md) | Framedimensie. |
| `t` | Geen | Gegenereerde datum/tijd van de hit. Gebruikt de indeling `dd/mm/yyyy hh:mm:ss w o`.<br>-  `dd/mm/yyyy hh:mm:ss` is datum/tijd in JavaScript. Maand `0` is Januari, terwijl maand `11` is December.<br>-  `w` is de dag van de week. `0` is zondag, terwijl  `6` het zaterdag is.<br>-  `o` is de negatieve GMT-verschuiving in minuten. `420` is bijvoorbeeld GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | De aangepaste tijdstempel die met de hit is ingesteld. Wordt meestal gebruikt voor offline tracering. |
| `v` | Geen | Gebruikt in [toegelaten Java](/help/components/dimensions/java-enabled.md) afmeting. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [Codedimensie ](/help/components/dimensions/tracking-code.md) bijhouden. |
| `v1` -  `v250` | [`evar1` -  `eVar250`](../vars/page-vars/evar.md) | [Vars](/help/components/dimensions/evar.md) of aangepaste conversieafmetingen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Variabele voor bezoekersidentiteitskaart |
| `vmk` | `vmk` | Niet meer gebruikt. De migratiesleutel van de bezoeker, die implementaties van derde aan eerste-partijkoekjes hielp migreren. |
| `vvp` | `variableProvider` | Wordt gebruikt in gegevensconnectors. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Gebruikt met Gegevensbronnen om online en off-line gegevens samen te binden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Wordt gebruikt in de [Zip-code](/help/components/dimensions/zip-code.md)-dimensie. |
