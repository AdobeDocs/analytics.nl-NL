---
title: Query-parameters voor gegevensverzameling
description: Vermeldt alle parameters van het vraagkoord die in beeldverzoeken worden gebruikt.
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# Query-parameters voor gegevensverzameling

De volgende tabel bevat een lijst met alle parameters voor queryreeksen die Adobe gebruikt bij afbeeldingsaanvragen. Deze informatie kan worden gebruikt wanneer het zuiveren gebruikend de analysatoren [van het](packet-monitor.md)Pakket, wanneer het [hardcoderen van beeld verzoeken](../other/hardcoded.md), of wanneer het gebruiken van [Dynamische Variabelen](../vars/page-vars/dynamic-variables.md).

| Parameter | Variabele voor analytische implementatie | Beschrijving |
| --- | --- | --- |
| `aamlh` | Geen | Locatiehint van Audience Manager. Wordt gebruikt in de integratie van gedeelde profielen in de cloud. |
| `aamb` | Geen | Publiek Manager blob. Wordt gebruikt in de integratie van gedeelde profielen in de cloud. |
| `aid` | Geen | Analytische bezoeker-id. |
| `AQB` | Geen | Geeft het begin van een queryreeks voor een afbeeldingsaanvraag aan. |
| `AQE` | Geen | Geeft het einde van een afbeeldingsaanvraag aan, wat betekent dat de aanvraag niet is afgekapt. |
| `bh` | Geen | Browserhoogte (in pixels). Wordt gebruikt in de afmetingen Browserhoogte. |
| `bw` | Geen | Browserbreedte (in pixels). Wordt gebruikt in de afmetingen Browserbreedte. |
| `c` | Geen | Kleurkwaliteit (in bits). Wordt gebruikt in de dimensie Kleurdiepte. |
| `c.` | `contextData` | Geeft het begin van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `.c` | `contextData` | Geeft het einde van contextgegevensvariabelen aan. Bevat nooit een waarde. |
| `c1` - `c75` | `prop1` - `prop75` | Aangepaste verkeersvariabelen. |
| `cc` | `currencyCode` | Het type valuta dat in de hit wordt gebruikt. |
| `cdp` | `cookieDomainPeriods` | Het aantal punten in een domein. Wordt gebruikt om cookies op de juiste wijze op te slaan. |
| `ce` | `charSet` | De tekencodering van de afbeeldingsaanvraag. |
| `cl` | `cookieLifetime` | De levensduur van het bezoekerscookie. |
| `ch` | `channel` | Wordt gebruikt in de dimensie Sitesecties. |
| `cp` | Geen | Wordt gebruikt in de afmetingen Type hoogte. |
| `ct` | Geen | Gebruikt in de afmeting van het Type van Verbinding. |
| `D` | `dynamicVariablePrefix` | Geeft aan wat er moet worden gebruikt voor dynamische variabelen. |
| `ev` | `events` | Shorthand voor de `events` queryreeks. |
| `events` | `events` | Door komma&#39;s gescheiden lijst met gebeurtenissen op de pagina. |
| `g` | `pageURL` | De huidige URL van de pagina, maximaal 255 bytes. |
| `-g` | `pageURL` | URL&#39;s die langer zijn dan 255 bytes, worden gesplitst. De eerste 255 bytes verschijnen in de `g` parameter, en alle resterende bytes verschijnen in de `-g` parameter. |
| `gn` | `pageName` | Shorthand voor de `pageName` queryreeks. |
| `gt` | `pageType` | Shorthand voor de `pageType` queryreeks. |
| `h1` - `h5` | `hier1` - `hier5` | Hiërarchievariabelen. |
| `hp` | Geen | Niet meer gebruikt. In eerdere versies van Adobe Analytics werd bepaald of de huidige URL de startpagina van de browser was. |
| `j` | Geen | De JavaScript-versie die in de browser is geïnstalleerd. |
| `k` | Geen | Gebruikt in de dimensie van de Steun van het Koekje. |
| `l1` - `l3` | `list1` - `list3` | Variabelen weergeven. |
| `mid` | Geen | Experience Cloud-bezoeker-id. |
| `ndh` | Geen | Markering die aangeeft of de afbeeldingsaanvraag afkomstig is van AppMeasurement. |
| `ns` | `visitorNameSpace` | Hiermee kunt u bepalen waar cookies worden ingesteld. |
| `oid` | `objectID` | Object-id voor de laatste pagina. Wordt gebruikt in Activiteitenkaart. |
| `ot` | Geen | Objectnaam voor de laatste pagina. Wordt gebruikt in vorige versies van Activiteitenkaart. |
| `p` | Geen | Niet meer gebruikt. Lijst met plug-ins die in de browser worden gebruikt. |
| `pageName` | `pageName` | Wordt gebruikt in de afmetingen Pagina. |
| `pageType` | `pageType` | Wordt gebruikt in de afmetingen Pagina&#39;s niet gevonden. |
| `pccr` | Geen | Alleen ingesteld voor nieuwe bezoekers en altijd ingesteld op `true`. Voorkomt oneindige omleidingen. |
| `pe` | `linkType` | Bepaalt het type aangepaste koppeling. |
| `pev1` | Geen | De URL waarop de aangepaste koppeling is opgetreden. |
| `pev2` | Geen | Aangepaste naam voor koppelingsvriendelijk. |
| `pev3` | Geen | Niet meer gebruikt. Bijgehouden mijlpalen in vorige versies van videoverslag. |
| `pf` | Geen | Perronvlag; alleen voor gebruik door Adobe. Niet wijzigen. |
| `pid` | Geen | Pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activiteitenkaart. |
| `pidt` | Geen | Type pagina-id voor laatste pagina. Wordt gebruikt in vorige versies van Activiteitenkaart. |
| `pl` | `products` | Shorthand voor de `products` queryreeks. |
| `products` | `products` | Variabele voor producten. |
| `purchaseID` | `purchaseID` | Wordt gebruikt om aankopen te dedupliceren. |
| `r` | `referrer` | Verwijzend URL van de slag. |
| `s` | Geen | Wordt gebruikt in de dimensie Resoluties van het beeldscherm. Schermresolutie, in `width x height`. |
| `server` | `server` | Serverdimensie. |
| `sv` | `server` | Shorthand voor de `server` queryreeks. |
| `state` | `state` | Framedimensie. |
| `t` | Geen | Gegenereerde datum/tijd van de hit. Gebruikt de indeling `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` is datum/tijd in JavaScript. Maand `0` is Januari, terwijl maand December `11` is.<br>- `w` is de dag van de week. `0` is zondag, terwijl `6` het zaterdag is.<br>- `o` is de negatieve GMT-verschuiving in minuten. Bijvoorbeeld: `420` is GMT-7. |
| `ts` | `timestamp` | De aangepaste tijdstempel die met de hit is ingesteld. Wordt meestal gebruikt voor offline tracering. |
| `v` | Geen | Wordt gebruikt in de dimensie Java Enabled. |
| `v0` | `campaign` | Dimensie code bijhouden. |
| `v1` - `v250` | `evar1` - `eVar250` | Aangepaste conversieafmetingen. |
| `vid` | `visitorID` | Variabele voor bezoekersidentiteitskaart |
| `vmk` | `vmk` | Niet meer gebruikt. Hiermee kunt u overstappen van cookies van derden naar cookies van andere leveranciers. |
| `vvp` | `variableProvider` | Wordt gebruikt in gegevensconnectors. |
| `xact` | `transactionID` | Gebruikt met Gegevensbronnen om gegevens samen te verbinden. |
| `zip` | `zip` | Wordt gebruikt in de dimensie Postcode. |
