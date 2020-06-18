---
title: Queryparameters voor dataverzameling
description: Vermeldt alle parameters van het vraagkoord die in beeldverzoeken worden gebruikt.
translation-type: tm+mt
source-git-commit: edf3ac3ebc99444b86bcd9239cef9ed84d797565
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 5%

---


# Queryparameters voor dataverzameling

De volgende tabel bevat een lijst met alle parameters voor queryreeksen die Adobe gebruikt bij afbeeldingsaanvragen. Deze informatie kan worden gebruikt wanneer het zuiveren gebruikend de analysatoren [van het](packet-monitor.md)Pakket, wanneer het [hardcoderen van beeld verzoeken](../other/hardcoded.md), of wanneer het gebruiken van [Dynamische Variabelen](../vars/page-vars/dynamic-variables.md).

| Parameter | Analytics-implementatievariabele | Beschrijving |
| --- | --- | --- |
| `aamlh` | Geen | Tip voor locatie van Audience Manager. Wordt gebruikt bij de integratie van Experience Cloud Shared Profile. |
| `aamb` | Geen | Audience Manager blob. Wordt gebruikt bij de integratie van Experience Cloud Shared Profile. |
| `aid` | Geen | Analytics-bezoeker-id. |
| `AQB` | Geen | Geeft het begin van een queryreeks voor een afbeeldingsaanvraag aan. |
| `AQE` | Geen | Geeft het einde van een afbeeldingsaanvraag aan, wat betekent dat de aanvraag niet is afgekapt. |
| `bh` | Geen | Browserhoogte (in pixels). Wordt gebruikt in de hoogte [van de](/help/components/dimensions/browser-height.md) browser. |
| `bw` | Geen | Browserbreedte (in pixels). Wordt gebruikt in de breedte [van de](/help/components/dimensions/browser-width.md) browser. |
| `c` | Geen | Kleurkwaliteit (in bits). Wordt gebruikt in de dimensie [Kleurdiepte](/help/components/dimensions/color-depth.md) . |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het begin van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het einde van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [Props](/help/components/dimensions/prop.md), of variabelen van het douaneverkeer. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Het type valuta dat in de hit wordt gebruikt. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Het aantal punten in een domein. Wordt gebruikt om cookies op de juiste wijze op te slaan. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | De tekencodering van de afbeeldingsaanvraag. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | De levensduur van het bezoekerscookie. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Wordt gebruikt in de dimensie [Site-secties](/help/components/dimensions/site-section.md) . |
| `cp` | Geen | Wordt gebruikt in de afmetingen Type [](/help/components/dimensions/hit-type.md) Actief. |
| `ct` | Geen | Wordt gebruikt in de dimensie [Verbindingstype](/help/components/dimensions/connection-type.md) . |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Geeft aan wat er moet worden gebruikt voor dynamische variabelen. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Shorthand voor de `events` queryreeks. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Door komma&#39;s gescheiden lijst met gebeurtenissen op de pagina. Wordt gebruikt door de meeste [meetwaarden](/help/components/metrics/overview.md). |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | De huidige URL van de pagina, maximaal 255 bytes. Wordt gebruikt in de [pagina-URL](/help/components/dimensions/page-url.md) -dimensie. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URL&#39;s die langer zijn dan 255 bytes, worden gesplitst. De eerste 255 bytes verschijnen in de `g` parameter, en alle resterende bytes verschijnen in de `-g` parameter. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Shorthand voor de `pageName` queryreeks. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Shorthand voor de `pageType` queryreeks. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/hier.md) | Hiërarchieafmetingen. |
| `hp` | Geen | Niet meer gebruikt. In vorige versies van Adobe Analytics, bepaalde als huidige URL de homepage van browser was. |
| `j` | Geen | De JavaScript-versie die in de browser is geïnstalleerd. |
| `k` | Geen | Wordt gebruikt in de dimensie [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) . |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | Lijstvariabelen. |
| `mid` | Geen | Experience Cloud-bezoeker-id. |
| `ndh` | Geen | Markering die aangeeft of de afbeeldingsaanvraag afkomstig is van AppMeasurement. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hiermee kunt u bepalen waar cookies worden ingesteld. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Object-id voor de laatste pagina. Wordt gebruikt in de Activity Map. |
| `ot` | Geen | Objectnaam voor de laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `p` | Geen | Niet meer gebruikt. Lijst met plug-ins die in de browser worden gebruikt. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Wordt gebruikt in de afmetingen [Pagina](/help/components/dimensions/page.md) . |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Wordt gebruikt in de [pagina&#39;s. Geen dimensie gevonden](/help/components/dimensions/pages-not-found.md) . |
| `pccr` | Geen | Alleen ingesteld voor nieuwe bezoekers en altijd ingesteld op `true`. Hiermee voorkomt u een oneindige omleiding. |
| `pe` | [`linkType`](../vars/config-vars/linktype.md) | Bepaalt het type aangepaste koppeling. Vereist voor [Aangepaste koppelingen](/help/components/dimensions/custom-link.md), [Download-koppelingen](/help/components/dimensions/download-link.md)en [Afsluiten](/help/components/dimensions/exit-link.md). |
| `pev1` | Geen | De URL waarop de aangepaste koppeling is opgetreden. |
| `pev2` | [`linkName`](../vars/config-vars/linkname.md) | Aangepaste naam voor koppelingsvriendelijk. |
| `pev3` | Geen | Niet meer gebruikt. Bijgehouden mijlpalen in vorige versies van videoverslag. |
| `pf` | Geen | markering van het Platform; alleen voor gebruik door Adobe. Niet wijzigen. |
| `pid` | Geen | Pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pidt` | Geen | Type pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activity Map. |
| `pl` | [`products`](../vars/page-vars/products.md) | Shorthand voor de `products` queryreeks. |
| `products` | [`products`](../vars/page-vars/products.md) | Variabele voor producten. Gebruikt in de afmetingen van het [product](/help/components/dimensions/product.md) en de [categorie](/help/components/dimensions/category.md) . |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Wordt gebruikt om aankopen te dedupliceren. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Verwijzend URL van de slag. Gebruikt in verkeersbronnen dimensies, zoals [Referrer](/help/components/dimensions/referrer.md) en [Verwijzend domein](/help/components/dimensions/referring-domain.md) |
| `s` | Geen | Schermresolutie, in `width x height`. Wordt gebruikt in de dimensie resoluties [van](/help/components/dimensions/monitor-resolution.md) Monitor. |
| `server` | [`server`](../vars/page-vars/server.md) | [Serverdimensie](/help/components/dimensions/server.md) . |
| `sv` | [`server`](../vars/page-vars/server.md) | Shorthand voor de `server` queryreeks. |
| `state` | [`state`](../vars/page-vars/state.md) | Framedimensie. |
| `t` | Geen | Gegenereerde datum/tijd van de hit. Gebruikt de indeling `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` is datum/tijd in JavaScript. Maand `0` is Januari, terwijl maand December `11` is.<br>- `w` is de dag van de week. `0` is zondag, terwijl `6` het zaterdag is.<br>- `o` is de negatieve GMT-verschuiving in minuten. Bijvoorbeeld: `420` is GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | De aangepaste tijdstempel die met de hit is ingesteld. Wordt meestal gebruikt voor offline tracering. |
| `v` | Geen | Wordt gebruikt in de dimensie [Java ingeschakeld](/help/components/dimensions/java-enabled.md) . |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [Dimensie code](/help/components/dimensions/tracking-code.md) bijhouden. |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [Vars](/help/components/dimensions/evar.md)of aangepaste conversieafmetingen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Variabele voor bezoekersidentiteitskaart |
| `vmk` | `vmk` | Niet meer gebruikt. De migratiesleutel van de bezoeker, die implementaties van derde aan eerste-partijkoekjes hielp migreren. |
| `vvp` | `variableProvider` | Wordt gebruikt in gegevensconnectors. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Gebruikt met Gegevensbronnen om online en off-line gegevens samen te binden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Wordt gebruikt in de dimensie [Postcode](/help/components/dimensions/zip-code.md) . |
