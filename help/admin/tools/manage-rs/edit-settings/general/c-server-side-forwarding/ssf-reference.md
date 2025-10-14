---
description: Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.
title: Server-kant die gegevens en codeverwijzing door:sturen
feature: Report Suite Settings
exl-id: 6ab7bbb6-0709-427b-b9fa-a179dbe55fc9
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Server-kant die gegevens en codeverwijzing door:sturen

Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.

## Configuratievariabelen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

De parameters prefixen met `d_*` identificeren speciale, systeem-vlakke zeer belangrijke paren die door onze [&#x200B; servers van de gegevensinzameling &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/system-components/components-data-collection.html?lang=nl-NL) worden gebruikt (DCS). Zie ook [&#x200B; Gesteunde Attributen voor vraag DCS API &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=nl-NL).

| Parameter | Beschrijving |
|--- |--- |
| `d_rs` | (Krijgt reeks met erfenis/het volgen-server-gebaseerde server-kant door:sturen) <br> reeks aan de rapportsuites die binnen met de klap aan Analytics worden overgegaan. |
| `d_dst_filter` | (Haalt reeks met op rapport-reeks-gebaseerde server-kant door:sturen) <br> die aan de reeks IDs van het rapport wordt geplaatst binnen met de slag aan Analytics wordt overgegaan. |
| `d_dst` | Plaats `d_dst=1` <br> als het verzoek aan Analytics inhoud over de bestemming verwacht die terug naar de cliënt moet worden verzonden. |
| `d_mid` | De Experience Cloud-id die aan Analytics is doorgegeven. |

## HTTP-headers {#section_0549705E76004F9585224AEF872066C0}

Deze kopballen zijn gebieden bevatten informatie zoals verzoeken om gegevens en reacties in een vraag van HTTP.

| HTTP-header | Beschrijving | h_ key geaccepteerd door Audience Manager |
| --- | --- | --- |
| Host | Dit wordt geplaatst aan de specifieke de gastheernaam van de gegevensinzameling van de cliënt die in het de gastheer configuratiedossier van Analytics wordt gespecificeerd. De naam wordt weergegeven als `host name .demdex.net` . Zie [&#x200B; Begrip Vraag aan het Domein van de Index &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=nl-NL). | `h_host` |
| Gebruikersagent | Reeks aan de gebruiker-Agent kopbal die binnen tot Analytics wordt overgegaan. | `h_user-agent` |
| Accepteren in taal | Instellen op de header `Accept-Language` die wordt doorgegeven aan Analytics. | `h_accept-language` |
| Verwijzing | Stel de URL van de pagina in die wordt doorgegeven aan Analytics of die wordt opgehaald via de header `Referer` die wordt doorgegeven aan Analytics. | `h_referer` |
| Referenter | Stel de URL van de pagina in die wordt doorgegeven aan Analytics of die wordt opgehaald via de header `Referrer` die wordt doorgegeven aan Analytics. | `h_referrer` |
| Datum | Instellen op de header `Date` die wordt doorgegeven aan Analytics. | `h_date` |

Bovendien wordt een `h_ip` signaal geproduceerd van IP van de gastheer die het verzoek naar DCS verzendt.

## Door de klant gedefinieerde signalen {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameters die voorafgaan aan `c_` identificeren door de klant gedefinieerde variabelen. Zie ook [&#x200B; Gesteunde Attributen voor Vraag DCS API &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=nl-NL).

| Signaal | Beschrijving |
| --- |--- |
| `c_browserWidth` en `c_browserHeight` | Breedte en hoogte van browservenster. |
| `c_campaign` | Wordt ingesteld door `s.campaign` . |
| `c_channel` | Wordt ingesteld door `s.channel` . |
| `c_clientDateTime` | Tijdstempel opgemaakt als `dd/mm/yyy hh:mm:ss  W TZ` . `TZ` is in minuten en komt overeen met de geretourneerde waarde van de methode `Date.getTimezoneOffset` . |
| `c_colorDepth` | Opgegeven als 16- of 32-bits kleur. |
| `c_connectionType` | Hiermee wordt het verbindingstype opgegeven. U kunt onder andere de volgende opties kiezen:<ul><li>modem</li><li>lan</li></ul> |
| `c_contextData.*` | Voorbeelden:<ul><li>AppMeasurement: `s.contextData`</li><li>[ &quot;categorie&quot;] = &quot;nieuws&quot;;</li><li>Signal: `c_contextData.category=news`</li></ul> |
| `c_cookiesEnabled` | Hiermee bepaalt u of cookies kunnen worden ingeschakeld. Opties zijn: ja, nee, onbekend |
| `c_currencyCode` | Type valuta dat voor de transactie wordt gebruikt. |
| `c_evar#` | Aangepaste gebeurtenissen |
| `c_events` | Wordt ingesteld door `s.events` . |
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
| `c_products` | De productreeks (ingesteld door `s.products`). |
| `c_prop` | Aangepaste props. |
| `c_purchaseID` | Een unieke id voor de aankoop. |
| `c_referrer` | De pagina vóór de huidige pagina. |
| `c_screenResolution` | Schermbreedte en -hoogte (in pixels). |
| `c_server` | Naam webserver (ingesteld door `s.server`). |
| `c_state` | Geografisch gebied (ingesteld door `s.state`). |
| `c_timezone` | Tijdverschuiving (in uren). |
| `c_transactionID` | Een unieke id voor een transactie. |
| `c_zip` | Postcode (ingesteld door `s.zip`). |
