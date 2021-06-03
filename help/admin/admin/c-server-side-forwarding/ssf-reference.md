---
description: Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.
title: Data- en codereferentie server-side doorsturen
uuid: 3eb3ea0f-a530-448d-bba5-6408b2490dc8
exl-id: 6ab7bbb6-0709-427b-b9fa-a179dbe55fc9
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 2%

---

# Data- en codereferentie server-side doorsturen

Een uitvoerige lijst en beschrijvingen van de configuratievariabelen, de kopballen van HTTP, en gegevenssignalen in server-kant door:sturen vraag.

## Configuratievariabelen {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameters die vooraf zijn ingesteld met `d_*` identificeren speciale sleutelwaardeparen op systeemniveau die worden gebruikt door onze [gegevensverzamelingsservers](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/system-components/components-data-collection.html) (DCS). Zie ook [Ondersteunde kenmerken voor DCS API-aanroepen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html).

| Parameter | Beschrijving |
|--- |--- |
| d_rs | (Krijgt geplaatst met erfenis/het volgen-server-gebaseerde server-zijdoor:sturen) <br>Reeks aan de rapportsuites die binnen met de slag aan Analytics worden overgegaan. |
| d_dst_filter | (Haalt reeks met op rapport-reeks-gebaseerde server-kant door:sturen) <br>Reeks aan de de reeks IDs van het rapport die binnen met de slag aan Analytics worden overgegaan. |
| d_dst | Stel d_dst=1 <br>in als het verzoek aan Analytics inhoud over het doel verwacht dat wordt teruggestuurd naar de client. |
| d_mid | De Experience Cloud-id die aan Analytics is doorgegeven. |

## HTTP-headers {#section_0549705E76004F9585224AEF872066C0}

Deze kopballen zijn gebieden bevatten informatie zoals verzoeken om gegevens en reacties in een vraag van HTTP.

<!-- Meike, missing link in table below: "See Understanding Calls to the Demdex Domain" -->

| HTTP-header | Beschrijving |
|--- |--- |
| Host | Dit wordt geplaatst aan de specifieke de gastheernaam van de gegevensinzameling van de cliënt die in het de gastheer configuratiedossier van Analytics wordt gespecificeerd. Het verschijnt zoals   `host name .demdex.net` .  Zie het Begrijpen van Vraag aan het Domein van de Index. |
| Gebruikersagent | Reeks aan de gebruiker-Agent kopbal die binnen tot Analytics wordt overgegaan. |
| X-Original-User-Agent | Slechts plaats als een afwisselende gebruikersagent door één van deze kopballen werd gespecificeerd: </br>`X-Device-User-Agent\ ` </br>`X-Original-User-Agent\`   </br>`X-OperaMini-Phone-UA\`   </br>`X-Skyfire-Phone\`    </br>`X-Bolt-Phone-UA\` |
| X-Forwarded-For | Stel dit in op het IP-adres van de client die het verzoek indient. Analytics heeft de inkomende `X-Forwarded-For`-header al geparseerd en het juiste IP-adres bepaald dat moet worden gebruikt. |
| Accept-Language | Stel de koptekst `Accept-Language` in die wordt doorgegeven aan Analytics. |
| Verwijzing | Stel de URL van de pagina in die wordt doorgegeven aan Analytics of wordt opgehaald via de verwijzingkop die wordt doorgegeven aan Analytics. |

## Door de klant gedefinieerde signalen {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameters die vooraf met `c_` zijn gedefinieerd, identificeren door de klant gedefinieerde variabelen. Zie ook [Ondersteunde Attributen voor Vraag DCS API](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html).

| Signaal | Beschrijving |
|--- |--- |
| c_browserWidth en c_browserHeight | Breedte en hoogte van browservenster. |
| c_campagne | Instellen op s.campagne. |
| c_channel | Instellen op s.channel. |
| c_clientDateTime | Tijdstempel opgemaakt als   dd/mm/jjjj uu:mm:ss W TZ.    TZ is in minuten en komt overeen met de geretourneerde waarde van de methode Date.getTimezoneOffset. |
| c_colorDepth | Opgegeven als 16- of 32-bits kleur. |
| c_connectionType | Hiermee wordt het verbindingstype opgegeven. De volgende opties zijn beschikbaar:<ul><li>modem</li><li>lan</li></ul> |
| c_contextData.* | Voorbeelden:<ul><li>AppMeasurement: s.contextData</li><li>[&quot;category&quot;] = &quot;news&quot;;</li><li>Signaal:  c_contextData.category=news</li></ul> |
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
