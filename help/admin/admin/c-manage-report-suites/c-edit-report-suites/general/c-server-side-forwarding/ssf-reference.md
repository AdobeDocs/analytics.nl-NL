---
description: Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.
title: Server-kant die gegevens en codeverwijzing door:sturen
feature: Server-Side Forwarding
exl-id: 6ab7bbb6-0709-427b-b9fa-a179dbe55fc9
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Server-kant die gegevens en codeverwijzing door:sturen

Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.

## Configuratievariabelen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameters vooraf ingesteld met `d_*` identificeer speciale, systeem-vlakke zeer belangrijke paren die door ons worden gebruikt [gegevensverzamelingsservers](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/system-components/components-data-collection.html?lang=nl-NL) (DCS). Zie ook [Ondersteunde kenmerken voor DCS API-aanroepen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=nl-NL).

| Parameter | Beschrijving |
|--- |--- |
| `d_rs` | (Krijgt geplaatst met erfenis/het volgen-server-gebaseerde server-zijdoor:sturen) <br>Stel dit in op de rapportsuites die met de hit worden doorgegeven aan Analytics. |
| `d_dst_filter` | (Krijgt reeks met op rapport-reeks-gebaseerde server-kant het door:sturen)  <br>Stel deze optie in op de id&#39;s van de rapportsuite die met de hit aan Analytics zijn doorgegeven. |
| `d_dst` | Set `d_dst=1`  <br>als het verzoek aan Analytics inhoud over de bestemming verwacht dat terug naar de cliënt wordt verzonden. |
| `d_mid` | De Experience Cloud-id die aan Analytics is doorgegeven. |

## HTTP-headers {#section_0549705E76004F9585224AEF872066C0}

Deze kopballen zijn gebieden bevatten informatie zoals verzoeken om gegevens en reacties in een vraag van HTTP.

| HTTP-header | Beschrijving | h_ key geaccepteerd door Audience Manager |
| --- | --- | --- |
| Host | Dit wordt geplaatst aan de specifieke de gastheernaam van de gegevensinzameling van de cliënt die in het de gastheer configuratiedossier van Analytics wordt gespecificeerd. Het verschijnt zoals `host name .demdex.net`. Zie [Inzicht krijgen in oproepen van het demdex-domein](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=nl-NL). | `h_host` |
| Gebruikersagent | Reeks aan de gebruiker-Agent kopbal die binnen tot Analytics wordt overgegaan. | `h_user-agent` |
| Accepteren in taal | Instellen op de  `Accept-Language`  doorgegeven aan Analytics. | `h_accept-language` |
| Verwijzing | Instellen op de pagina-URL die wordt doorgegeven aan Analytics of die wordt verzameld via de `Referer` doorgegeven aan Analytics. | `h_referer` |
| Referenter | Instellen op de pagina-URL die wordt doorgegeven aan Analytics of die wordt verzameld via de `Referrer` doorgegeven aan Analytics. | `h_referrer` |
| Datum | Instellen op de `Date` doorgegeven aan Analytics. | `h_date` |

Bovendien `h_ip` Het signaal wordt geproduceerd van IP van de gastheer die het verzoek naar DCS verzendt.

## Door de klant gedefinieerde signalen {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameters vooraf ingesteld met `c_` door de klant gedefinieerde variabelen identificeren. Zie ook [Ondersteunde kenmerken voor DCS API-aanroepen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=nl-NL).

| Signaal | Beschrijving |
| --- |--- |
| `c_browserWidth`  en `c_browserHeight` | Breedte en hoogte van browservenster. |
| `c_campaign` | Instellen op `s.campaign`. |
| `c_channel` | Instellen op `s.channel`. |
| `c_clientDateTime` | Tijdstempel opgemaakt als `dd/mm/yyy hh:mm:ss  W TZ` . `TZ` is in minuten en komt overeen met de geretourneerde waarde van `Date.getTimezoneOffset` methode. |
| `c_colorDepth` | Opgegeven als 16- of 32-bits kleur. |
| `c_connectionType` | Hiermee wordt het verbindingstype opgegeven. U kunt onder andere de volgende opties kiezen:<ul><li>modem</li><li>lan</li></ul> |
| `c_contextData.*` | Voorbeelden:<ul><li>AppMeasurement: `s.contextData`</li><li>[&quot;categorie&quot;] = &quot;nieuws&quot;;</li><li>Signaal: `c_contextData.category=news`</li></ul> |
| `c_cookiesEnabled` | Hiermee bepaalt u of cookies kunnen worden ingeschakeld. Opties zijn: ja, nee, onbekend |
| `c_currencyCode` | Type valuta dat voor de transactie wordt gebruikt. |
| `c_evar#` | Aangepaste gebeurtenissen |
| `c_events` | Instellen op `s.events`. |
| `c_hier#` | Aangepaste hiërarchievariabelen. |
| `c_javaEnabled` | Hiermee geeft u aan of Java kan worden ingeschakeld. Opties zijn: ja, nee, onbekend |
| `c_javaScriptVersion` | Versie van JavaScript ondersteund door een browser. |
| `c_latitude` | Numerieke breedtegraad |
| `c_linkClick` | Opties: aangepast, download afsluiten |
| `c_linkCustomName` | De aangepaste naam (indien van toepassing) die voor de koppeling is opgegeven. |
| `c_linkDownloadURL` | De URL van downloadkoppelingen. |
| `c_linkExitURL` | De afsluitings-URL. |
| `c_list#` | Aangepaste lijstvariabelen. |
| `c_longitude` | Numerieke lengte. |
| `c_mediaPlayerType` | Voor aanvragen voor het bijhouden van mediastromen. Opties zijn onder meer: andere, primetime |
| `c_pageName` | De paginanaam (indien ingesteld). |
| `c_pageURL` | Het adres van de pagina in de adresbalk van de browser. |
| `c_products` | De producttekenreeks (ingesteld door `s.products`). |
| `c_prop` | Aangepaste props. |
| `c_purchaseID` | Een unieke id voor de aankoop. |
| `c_referrer` | De pagina vóór de huidige pagina. |
| `c_screenResolution` | Schermbreedte en -hoogte (in pixels). |
| `c_server` | Webservernaam (ingesteld door `s.server`). |
| `c_state` | Geografisch gebied (ingesteld door `s.state`). |
| `c_timezone` | Tijdverschuiving (in uren). |
| `c_transactionID` | Een unieke id voor een transactie. |
| `c_zip` | Postcode (ingesteld door `s.zip`). |
