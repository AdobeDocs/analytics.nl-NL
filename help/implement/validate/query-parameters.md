---
title: Query-parameters voor gegevensverzameling
description: Vermeldt alle parameters van het vraagkoord die in beeldverzoeken worden gebruikt.
feature: Implementation Basics
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
role: Admin, Developer, Leader, User
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 3%

---

# Query-parameters voor gegevensverzameling

De volgende tabel bevat een lijst met alle parameters voor queryreeksen die Adobe gebruikt bij afbeeldingsaanvragen. Deze informatie kan worden gebruikt wanneer het zuiveren gebruikend [ analysatoren van het Pakket ](packet-monitor.md), wanneer [ het hardcoderen beeldverzoeken ](../other/hardcoded.md), of wanneer het gebruiken van [ Dynamische Variabelen ](../vars/page-vars/dynamic-variables.md).

| Parameter | Variabele voor analytische implementatie | Beschrijving |
| --- | --- | --- |
| `aamlh` | Geen | Tip voor Audience Manager-locatie. Wordt gebruikt bij de integratie van Experience Cloud Shared Profile. |
| `aamb` | Geen | Audience Manager blob. Wordt gebruikt bij de integratie van Experience Cloud Shared Profile. |
| `aid` | Geen | Analytische bezoeker-id. |
| `AQB` | Geen | Geeft het begin van een queryreeks voor een afbeeldingsaanvraag aan. |
| `AQE` | Geen | Geeft het einde van een afbeeldingsaanvraag aan, wat betekent dat de aanvraag niet is afgekapt. |
| `bh` | Geen | Browserhoogte (in pixels). Gebruikt in de [ Browser hoogte ](/help/components/dimensions/browser-height.md) afmeting. |
| `bw` | Geen | Browserbreedte (in pixels). Gebruikt in de [ Browser breedte ](/help/components/dimensions/browser-width.md) afmeting. |
| `c` | Geen | Kleurkwaliteit (in bits). Gebruikt in de [ diepte van de Kleur ](/help/components/dimensions/color-depth.md) afmeting. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het begin van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Geeft het einde van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [ Props ](/help/components/dimensions/prop.md), of variabelen van het douaneverkeer. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Het type valuta dat in de hit wordt gebruikt. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Het aantal punten in een domein. Wordt gebruikt om cookies op de juiste wijze op te slaan. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | De tekencodering van de afbeeldingsaanvraag. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | De levensduur van het bezoekerscookie. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Gebruikt in de [ sectie van de Plaats ](/help/components/dimensions/site-section.md) dimensie. |
| `cp` | Geen | Gebruikt in de [ dimensie van het Type van het Actief ](/help/components/dimensions/hit-type.md). |
| `ct` | Geen | Gebruikt in de [ dimensie van het Type van Verbinding ](/help/components/dimensions/connection-type.md). |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Geeft aan wat er moet worden gebruikt voor dynamische variabelen. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Kort voor de queryreeks `events` . |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Door komma&#39;s gescheiden lijst met gebeurtenissen op de pagina. Gebruikt door de meeste [ metriek ](/help/components/metrics/overview.md). |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | De huidige URL van de pagina, maximaal 255 bytes. Gebruikt in de [ pagina URL ](/help/components/dimensions/page-url.md) afmeting. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URL&#39;s die langer zijn dan 255 bytes, worden gesplitst. De eerste 255 bytes worden weergegeven in de parameter `g` en alle resterende bytes worden weergegeven in de parameter `-g` . |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Kort voor de queryreeks `pageName` . |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Kort voor de queryreeks `pageType` . |
| `h.` | [`collectHighEntropyUserAgentHints`](../vars/config-vars/collecthighentropyuseragenthints.md) | Prefix voor verscheidene variabelen die [ wenken van de Cliënt ](/help/technotes/client-hints.md) vertegenwoordigen. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/hier.md) | Hiërarchieafmetingen. |
| `hp` | Geen | Niet meer gebruikt. In vorige versies van Adobe Analytics, bepaalde als huidige URL de homepage van browser was. |
| `j` | Geen | De JavaScript-versie die in de browser is geïnstalleerd. |
| `k` | Geen | Gebruikt in de [ steun van het Koekje ](/help/components/dimensions/cookie-support.md) dimensie. |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | Variabelen weergeven. |
| `lrt` | Geen | De &quot;laatste verzoektiming,&quot;die de roundtrip tijd voor het laatste verzoek, in milliseconden is. Het wordt verzonden slechts wanneer meer dan één verzoek uit een pagina gaat of wanneer de pagina een enig-paginatoepassing (SPA) is. |
| `mid` | Geen | Experience Cloud-bezoeker-id. |
| `ndh` | Geen | Markering die aangeeft of de afbeeldingsaanvraag afkomstig is uit AppMeasurement. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hiermee kunt u bepalen waar cookies worden ingesteld. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Object-id voor de laatste pagina. Wordt gebruikt in Activity Map. |
| `ot` | Geen | Objectnaam voor de laatste pagina. Wordt gebruikt in eerdere versies van Activity Map. |
| `p` | Geen | Niet meer gebruikt. Lijst met plug-ins die in de browser worden gebruikt. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Gebruikt in de [ dimensie van de Pagina ](/help/components/dimensions/page.md). |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Gebruikt in de [ Pagina&#39;s niet gevonden ](/help/components/dimensions/pages-not-found.md) dimensie. |
| `pccr` | Geen | Alleen ingesteld voor nieuwe bezoekers en altijd ingesteld op `true` . Hiermee voorkomt u een oneindige omleiding als een bezoeker cookies weigert. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | Bepaalt het type aangepaste koppeling. Vereist voor [ de verbindingen van de Douane ](/help/components/dimensions/custom-link.md), [ de verbindingen van de Download ](/help/components/dimensions/download-link.md), en [ de verbindingen van de Uitgang ](/help/components/dimensions/exit-link.md). |
| `pev1` | [`linkURL`](../vars/config-vars/linkurl.md) | De URL waarop de aangepaste koppeling is opgetreden. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | Aangepaste naam voor koppelingsvriendelijk. |
| `pev3` | Geen | Niet meer gebruikt. Bijgehouden mijlpalen in vorige versies van videorapportage. |
| `pf` | Geen | Perronmarkering; alleen voor gebruik door Adobe. Niet wijzigen. |
| `pid` | Geen | Pagina-id voor laatste pagina. Wordt gebruikt in eerdere versies van Activity Map. |
| `pidt` | Geen | Type pagina-id voor laatste pagina. Wordt gebruikt in eerdere versies van Activity Map. |
| `pl` | [`products`](../vars/page-vars/products.md) | Kort voor de queryreeks `products` . |
| `products` | [`products`](../vars/page-vars/products.md) | Variabele voor producten. Gebruikt in het [ Product ](/help/components/dimensions/product.md) en [ Categorie ](/help/components/dimensions/category.md) dimensies. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Wordt gebruikt om aankopen te dedupliceren. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Verwijzend URL van de slag. Gebruikt in verkeersbronnen afmetingen, zoals [ Referrer ](/help/components/dimensions/referrer.md) en [ Verwijzend domein ](/help/components/dimensions/referring-domain.md) |
| `s` | Geen | Schermresolutie, in `width x height` . Gebruikt in de [ resoluties van de Monitor ](/help/components/dimensions/monitor-resolution.md) afmeting. |
| `server` | [`server`](../vars/page-vars/server.md) | ](/help/components/dimensions/server.md) dimensie van de Server van 0} {.[ |
| `sv` | [`server`](../vars/page-vars/server.md) | Kort voor de queryreeks `server` . |
| `state` | [`state`](../vars/page-vars/state.md) | Framedimensie. |
| `t` | Geen | Gegenereerde datum/tijd van de hit. Gebruikt de indeling `dd/mm/yyyy hh:mm:ss w o` .<br> - `dd/mm/yyyy hh:mm:ss` is datum/tijd in JavaScript. Maand `0` is januari, maand `11` is december.<br> - `w` is de dag van de week. `0` is zondag, terwijl `6` zaterdag is.<br> - `o` is de negatieve GMT-verschuiving in minuten. `420` is bijvoorbeeld GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | De aangepaste tijdstempel die met de hit is ingesteld. Wordt meestal gebruikt voor offline tracering. |
| `v` | Geen | Gebruikt in [ toegelaten Java ](/help/components/dimensions/java-enabled.md) dimensie. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [ het Volgen de dimensie van de Code ](/help/components/dimensions/tracking-code.md). |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [ eVars ](/help/components/dimensions/evar.md), of de afmetingen van de douaneconversie. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Variabele voor bezoekersidentiteitskaart |
| `vidn` | Geen | Door AppMeasurement ingesteld voor nieuwe bezoekers. Bevat de id-waarde die is opgeslagen in het bezoekerscookie. |
| `vmk` | `vmk` | Niet meer gebruikt. De migratiesleutel van de bezoeker, die implementaties van derde aan eerste-partijkoekjes hielp migreren. |
| `vvp` | `variableProvider` | Wordt gebruikt in Data Connectors. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Gebruikt met Gegevensbronnen om online en off-line gegevens samen te binden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Gebruikt in de [ dimensie van het Postcode ](/help/components/dimensions/zip-code.md). |
