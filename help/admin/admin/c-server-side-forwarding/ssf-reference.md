---
description: Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.
title: Server-kant die gegevens en codeverwijzing door:sturen
uuid: 3eb3ea0f-a530-448d-bba5-6408b2490dc8
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Server-kant die gegevens en codeverwijzing door:sturen

Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.

## Configuratievariabelen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameters die vooraf zijn ingesteld met `d_*` identificatie van speciale sleutelwaardeparen op systeemniveau die worden gebruikt door onze [gegevensverzamelingsservers](https://marketing.adobe.com/resources/help/en_US/aam/c_compcollect.html) (DCS). Zie ook [Ondersteunde kenmerken voor DCS API-aanroepen](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html).

| Parameter | Beschrijving |
|--- |--- |
| d_rs | (Haalt reeks met erfenis/het volgen-server-gebaseerde server-kant door:sturen) <br>die aan de rapportreeksen worden geplaatst die binnen met de slag aan Analytics worden overgegaan. |
| d_dst_filter | (Haalt reeks met op rapport-reeks-gebaseerde server-kant het door:sturen) <br>Reeks aan het rapport reeks IDs binnen die met de slag aan Analytics wordt overgegaan. |
| d_dst | Stel d_dst=1 in <br>als het verzoek aan Analytics inhoud over het doel verwacht dat wordt teruggestuurd naar de client. |
| d_mid | De Experience Cloud-id die aan Analytics is doorgegeven. |

## HTTP-headers {#section_0549705E76004F9585224AEF872066C0}

Deze kopballen zijn gebieden bevatten informatie zoals verzoeken om gegevens en reacties in een vraag van HTTP.

<!-- Meike, missing link in table below: "See Understanding Calls to the Demdex Domain" -->

| HTTP-header | Beschrijving |
|--- |--- |
| Host | Dit wordt geplaatst aan de specifieke de gastheernaam van de gegevensinzameling van de cliënt die in het de gastheer configuratiedossier van Analytics wordt gespecificeerd. Het wordt weergegeven als `host name .demdex.net` .  Zie het Begrijpen van Vraag aan het Domein van de Index. |
| Gebruikersagent | Reeks aan de gebruiker-Agent kopbal die binnen tot Analytics wordt overgegaan. |
| X-Original-User-Agent | Slechts plaats als een afwisselende gebruikersagent door één van deze kopballen werd gespecificeerd: </br>`X-Device-User-Agent\ `  </br>`X-Original-User-Agent\`   </br>`X-OperaMini-Phone-UA\`   </br>`X-Skyfire-Phone\`    </br>`X-Bolt-Phone-UA\` |
| X-Forwarded-For | Stel dit in op het IP-adres van de client die het verzoek indient. Analytics heeft de binnenkomende `X-Forwarded-For` header al geparseerd en het juiste IP-adres bepaald. |
| Accept-Language | Instellen op de `Accept-Language` header die wordt doorgegeven aan Analytics. |
| Verwijzing | Stel de URL van de pagina in die wordt doorgegeven aan Analytics of wordt opgehaald via de verwijzingkop die wordt doorgegeven aan Analytics. |

## Door de klant gedefinieerde signalen {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

De parameters prefixed met `c_` identificeren klant-bepaalde variabelen. Zie ook [Gesteunde Attributen voor Vraag](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html)DCS API.

| Signaal | Beschrijving |
|--- |--- |
| c_browserWidth en c_browserHeight | Breedte en hoogte van browservenster. |
| c_campagne | Instellen op s.campagne. |
| c_channel | Instellen op s.channel. |
| c_clientDateTime | Tijdstempel opgemaakt als dd/mm/jjjj uu:mm:ss W TZ.    TZ is in minuten en komt overeen met de geretourneerde waarde van de methode Date.getTimezoneOffset. |
| c_colorDepth | Opgegeven als 16- of 32-bits kleur. |
| c_connectionType | Hiermee wordt het verbindingstype opgegeven. De volgende opties zijn beschikbaar:<ul><li>modem</li><li>lan</li></ul> |
| c_contextData.* | Voorbeelden:<ul><li>AppMeasurement: s.contextData</li><li>[&quot;categorie&quot;] = &quot;nieuws&quot;;</li><li>Signaal:  c_contextData.category=news</li></ul> |
| c_cookiesEnabled | Hiermee bepaalt u of cookies kunnen worden ingeschakeld. De volgende opties zijn beschikbaar: ja, nee, onbekend |
| c_currencyCode | Type valuta dat voor de transactie wordt gebruikt. |
| c_evar# | Aangepaste gebeurtenissen |
| c_events | Ingesteld op s.events. |
| c_hier# | Aangepaste hiërarchievariabelen. |
| c_javaEnabled | Hiermee geeft u aan of Java kan worden ingeschakeld. De volgende opties zijn beschikbaar: ja, nee, onbekend |
| c_javaScriptVersion | Versie van JavaScript ondersteund door een browser. |
| c_latitude | Numerieke breedtegraad |
| c_linkClick | De volgende opties zijn beschikbaar: aangepast, download exit |
| c_linkCustomName | De aangepaste naam (indien van toepassing) die voor de koppeling is opgegeven. |
| c_linkDownloadURL | De URL van downloadkoppelingen. |
| c_linkExitURL | De afsluitings-URL. |
| c_list# | Aangepaste lijstvariabelen. |
| c_longitude | Numerieke lengtegraad. |
| c_mediaPlayerType | Voor aanvragen voor het bijhouden van mediastromen. De volgende opties zijn beschikbaar:  andere, primetime |
| c_pageName | De paginanaam (indien ingesteld). |
| c_pageURL | Het adres van de pagina in de adresbalk van de browser. |
| c_products | De producttekenreeks (ingesteld door s.products ). |
| c_prop | Aangepaste props. |
| c_purchaseID | Een unieke id voor de aankoop. |
| c_reference | De pagina vóór de huidige pagina. |
| c_screenResolution | Schermbreedte en -hoogte (in pixels). |
| c_server | Webservernaam (ingesteld door s.server). |
| c_state | Geografisch gebied (ingesteld door s.state). |
| c_timezone | Tijdverschuiving (in uren). |
| c_transactionID | Een unieke id voor een transactie. |
| c_zip | Postcode (ingesteld door s.zip). |
