---
description: Tabelgegevens die de kolommen in de gegevensinvoer beschrijven.
keywords: Gegevensfeed;kolommen
subtopic: data feeds
title: Referentie gegevenskolom
feature: Data Feeds
exl-id: e1492147-6e7f-4921-b509-898e7efda596
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '3676'
ht-degree: 0%

---

# Referentie gegevenskolom

Gebruik deze pagina om te leren welke gegevens in elke kolom zijn. De meeste implementaties gebruiken niet elke kolom, zodat kan deze pagina worden van verwijzingen voorzien wanneer het bepalen van welke kolommen in de uitvoer van een gegevensvoer te omvatten.

>[!IMPORTANT]
>
>Voor elke bepaalde kolom (bijvoorbeeld een kolom die is gedefinieerd als 255 tekens) kan een gegevensfeed extra tekens verzenden als gevolg van de toevoeging van tekens die aan waarden ontsnappen in een tekenreeks. Houd rekening met deze mogelijke extra tekens als uw implementatie regelmatig waarden verzendt die de tekenlimiet overschrijden.

## Kolommen, beschrijvingen en gegevenstypen

>[!NOTE]
>
>De meeste kolommen bevatten een vergelijkbare kolom met een voorvoegsel `post_` . Post kolommen bevatten waarden na server-zijlogica, verwerkingsregels, en regels VISTA. Adobe raadt aan in de meeste gevallen postkolommen te gebruiken. Zie [ Veelgestelde Veelgestelde vragen van het voer van Gegevens ](../df-faq.md) voor meer informatie.

De vorige updates aan deze lijst kunnen op [ worden gevonden van deze pagina begaat geschiedenis op GitHub ](https://github.com/AdobeDocs/analytics.en/commits/main/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).

| Kolomnaam | Kolombeschrijving | Gegevenstype |
| --- | --- | --- |
| **`accept_language`** | Hiermee worden alle geaccepteerde talen weergegeven, zoals wordt aangegeven in de HTTP-header Accept-Language in een afbeeldingsaanvraag. | teken(20) |
| **`adload`** | Media en laden | varchar(255) |
| **`aemassetid`** | Een variabele van meerdere waarden die aan Activa IDs (GUIDs) van een reeks Adobe Experience Manager Assets beantwoordt. Incrementele indrukgebeurtenissen. | text |
| **`aemassetsource`** | Identificeert de bron van de gebeurtenis asset. Wordt gebruikt in Adobe Experience Manager. | varchar(255) |
| **`aemclickedassetid`** | Element-id van een Adobe Experience Manager-element. De verhogingen klikken Gebeurtenissen. | varchar(255) |
| **`browser`** | Een numerieke id die de browser vertegenwoordigt. Verwijst naar de opzoektabel van `browser.tsv` . | int zonder teken |
| **`browser_height`** | De [ Browser Hoogte ](/help/components/dimensions/browser-height.md) afmeting. | small int zonder teken |
| **`browser_width`** | De [ Browser Breedte ](/help/components/dimensions/browser-width.md) | small int zonder teken |
| **`c_color`** | Bitdiepte van het kleurenpalet. Gebruikt als deel van het berekenen van de [ diepte van de Kleur ](/help/components/dimensions/color-depth.md) afmeting. AppMeasurement gebruikt de JavaScript-functie `screen.colorDepth()` . | teken(20) |
| **`campaign`** | De [ het Volgen dimensie van de Code ](/help/components/dimensions/tracking-code.md). | varchar(255) |
| **`carrier`** | Adobe Advertising-integratievariabele. Geeft de mobiele drager aan. De zeer belangrijke waarde voor `carrier.tsv` [ Dynamische raadpleging ](dynamic-lookups.md). | varchar(100) |
| **`ch_hdr`** | Clienttips die via de HTTP-aanvraagheader worden verzameld. | text |
| **`ch_js`** | Clienttips die zijn verzameld via de JavaScript API voor clienttips van de gebruikersagent. | text |
| **`channel`** | De [ sectie van de Plaats ](/help/components/dimensions/site-section.md) dimensie. | varchar(100) |
| **`clickmaplink`** | Activity Map-koppeling | varchar(255) |
| **`clickmaplinkbyregion`** | Koppeling Activity Map naar regio | varchar(255) |
| **`clickmappage`** | Activity Map-pagina | varchar(255) |
| **`clickmapregion`** | Activity Map | varchar(255) |
| **`code_ver`** | API of SDK-versie van client die wordt gebruikt om de afbeeldingsaanvraag te compileren en te verzenden. | teken(16) |
| **`color`** | Id van kleurdiepte gebaseerd op de waarde van de kolom `c_color` . Verwijst naar de opzoektabel van `color_depth.tsv` . | small int zonder teken |
| **`connection_type`** | Een numerieke id die het verbindingstype vertegenwoordigt. Het [ type van Verbinding ](/help/components/dimensions/connection-type.md) afmeting. Verwijst naar de opzoektabel van `connection_type.tsv` . | tinyint zonder teken |
| **`cookies`** | De [ steun van het Koekje ](/help/components/dimensions/cookie-support.md) dimensie.<br> Y: Toegelaten <br> N: Gehandicapte <br> U: Onbekend | teken(1) |
| **`country`** | Een numerieke id die het land van de bezoeker vertegenwoordigt. Verwijst naar de opzoektabel van `country.tsv` . | small int zonder teken |
| **`ct_connect_type`** | Verwant aan de `connection_type` kolom. De meest voorkomende waarden zijn LAN/Wifi, Mobile Carrier en Modem. | teken(20) |
| **`curr_factor`** | Bepaalt de decimale valutapositie en wordt gebruikt voor valutaomrekening. In USD worden bijvoorbeeld twee decimalen gebruikt, zodat deze kolomwaarde `2` is. | tinyint |
| **`curr_rate`** | De wisselkoers op het tijdstip van de transactie. Adobe werkt samen met XE om de wisselkoers van de huidige dag te bepalen. | decimaal (24,12) |
| **`currency`** | De valutacode die tijdens de transactie werd gebruikt. Instellen met [`currencyCode`](/help/implement/vars/config-vars/currencycode.md). | teken(8) |
| **`cust_hit_time_gmt`** | Alleen voor tijdstempels geschikte rapportsuites. De tijdstempel die met de hit wordt verzonden, gebaseerd in UNIX®-tijd. | int |
| **`cust_visid`** | De aangepaste bezoeker-id, indien ingesteld met [`visitorID`](/help/implement/vars/config-vars/visitorid.md) . | varchar(255) |
| **`customer_perspective`** | Hiermee wordt bepaald of de hit een mobiele achtergrondhit is. Zie [ context-bewuste zittingen ](/help/components/vrs/vrs-mobile-visit-processing.md) voor meer informatie. | tinyint zonder teken |
| **`daily_visitor`** | Een vlag die bepaalt als de slag een nieuwe dagelijkse bezoeker is. | tinyint zonder teken |
| **`dataprivacyconsentoptin`** | De [ dimensie van het beheer van 0} het beheer opt-in. ](/help/components/dimensions/cm-opt-in.md) Er kunnen meerdere waarden aanwezig zijn per hit, gescheiden door een pipe (`\|`). Geldige waarden zijn `DMP` en `SELL` . | varchar(100) |
| **`dataprivacyconsentoptout`** | De [ dimensie van het 0} beheer van de Toestemming. ](/help/components/dimensions/cm-opt-out.md) Er kunnen meerdere waarden aanwezig zijn per hit, gescheiden door een pipe (`\|`). Geldige waarden zijn `SSF` , `DMP` en `SELL` . | varchar(100) |
| **`dataprivacydmaconsent`** | Een waarde die aangeeft of er toestemming is verkregen voor het verzenden van gegevens van Adobe Analytics via Adobe Advertising naar derde reclamebureaus (zoals Google). Zie [ Toestemming toevoegen ](/help/components/dimensions/ad-consent.md) voor meer informatie. | varchar(100) |
| **`date_time`** | De tijd van de treffer in leesbare formaat, die op de tijdzone van de rapportreeks wordt gebaseerd. | datetime |
| **`domain`** | De [ dimensie van het Domein ](/help/components/dimensions/domain.md). Gebaseerd op het toegangspunt van Internet van de bezoeker. | varchar(100) |
| **`duplicate_events`** | Vermeldt elke gebeurtenis die als een duplicaat is geteld. | varchar(255) |
| **`duplicate_purchase`** | Een markering die bepaalt of de aankoopgebeurtenis voor deze hit wordt genegeerd omdat het een duplicaat is. | tinyint zonder teken |
| **`duplicated_from`** | Wordt alleen gebruikt in rapportsuites die de VISTA-regels voor raakkopieën bevatten. Geeft aan uit welke rapportsuite de treffer is gekopieerd. | varchar(40) |
| **`ef_id`** | De `ef_id` die wordt gebruikt in Adobe Advertising-integratie. | varchar(255) |
| **`evar1 - evar250`** | Aangepaste variabelen 1-250. Gebruikt in [ eVar ](/help/components/dimensions/evar.md) afmetingen. Elke organisatie gebruikt eVars anders. De beste plaats voor meer informatie over hoe uw organisatie respectieve eVars bevolkt a [ document van het oplossingsontwerp ](/help/implement/prepare/solution-design.md) specifiek voor uw organisatie zou zijn. | varchar(255) |
| **`event_list`** | Lijst met door komma&#39;s gescheiden numerieke id&#39;s die gebeurtenissen vertegenwoordigen die tijdens de hit worden geactiveerd. Omvat zowel standaardgebeurtenissen als [ douanegebeurtenissen 1-1000 ](/help/components/metrics/custom-events.md). Gebruikt `event.tsv` lookup. | text |
| **`exclude_hit`** | Een vlag die bepaalt of de treffer van rapportering wordt uitgesloten. De kolom `visit_num` wordt niet verhoogd voor uitgesloten treffers.<br> 1: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br> 2: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br> 3: niet meer gebruikt. De agentenuitsluiting van de gebruiker <br> 4: Uitsluiting die op IP adres <br> wordt gebaseerd 5: De virtuele klapinfo die, zoals `page_url`, `pagename`, `page_event`, of `event_list`<br> 6 ontbreekt: JavaScript verwerkte niet correct hit <br> 7: De rekening-specifieke uitsluiting, zoals in een VISTA regels <br> 8: Niet gebruikt. Alternatieve accountspecifieke uitsluiting.<br> 9: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br> 10: Ongeldige muntcode <br> 11: Hit die een timestamp op een timestamp-enige rapportreeks mist, of een klap bevatte een timestamp op een niet-timestamp rapportreeks <br> 12: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br> 13: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br> 14: Bezet van het doel die niet met een Beïnvloed Analytics <br> 15 aanpaste: Momenteel niet gebruikt.<br> 16: De klap van de Wolk van de Reclame die niet aan een Besloten Analytics aanpaste | tinyint zonder teken |
| **`first_hit_page_url`** | De allereerste URL van de bezoeker. | varchar(255) |
| **`first_hit_pagename`** | De [ originele 1} afmeting van de ingangspagina van de Ingang. ](/help/components/dimensions/entry-dimensions.md) De oorspronkelijke naam van de ingangspagina van de bezoeker. | varchar(100) |
| **`first_hit_ref_domain`** | De [ Originele verwijzende domein ](/help/components/dimensions/original-referring-domain.md) dimensie. Gebaseerd op `first_hit_referrer` . Het allereerste verwijzende domein van de bezoeker. | varchar(100) |
| **`first_hit_ref_type`** | Een numerieke id die het referentietype van de allereerste referentie van de bezoeker vertegenwoordigt. Verwijst naar de opzoektabel van `referrer_type.tsv` . | tinyint zonder teken |
| **`first_hit_referrer`** | De allereerste verwijzende URL van de bezoeker. | varchar(255) |
| **`first_hit_time_gmt`** | Tijdstempel van de allereerste hit van de bezoeker in UNIX®-tijd. | int |
| **`geo_city`** | De naam van de stad waar de hit vandaan kwam, op basis van IP. Gebruikt in de [ Steden ](/help/components/dimensions/cities.md) dimensie. | teken(32) |
| **`geo_country`** | De afkorting van het land waar de treffer vandaan kwam, gebaseerd op IP. Gebruikt in de [ dimensie van Landen ](/help/components/dimensions/countries.md). | teken(4) |
| **`geo_dma`** | Een numerieke id van het demografische gebied waar de hit vandaan kwam, gebaseerd op IP. Gebruikt in de [ dimensie DMA ](/help/components/dimensions/us-dma.md) van de VS. | int zonder teken |
| **`geo_region`** | De naam van de staat of regio waar de treffer vandaan kwam, gebaseerd op IP. Gebruikt in de [ Gebieden ](/help/components/dimensions/regions.md) dimensie. | teken(32) |
| **`geo_zip`** | De postcode waaruit de hit afkomstig was, gebaseerd op IP. Helpt de [ dimensie van het Postcode ](/help/components/dimensions/zip-code.md) bevolken. Zie ook `zip` . | varchar(16) |
| **`hit_source`** | De bron waar de hit vandaan kwam. De bronnen 1, 2 en 6 van de it worden gefactureerd. <br> 1: Standaard beeldverzoek zonder timestamp <br> 2: Standaard beeldverzoek met timestamp <br> 3: Levende gegevensbron uploadt met timestamps <br> 4: Niet gebruikt <br> 5: Generic gegevensbron uploadt <br> 6: Volledige het uploaden van de bron van verwerkingsgegevens <br> 7: TransactieID gegevensbron uploadt <br> 8: Niet meer gebruikt; Vorige versies van Adobe Adverting Cloud geen gegevensbronnen <br> 9}: langer gebruikt; Adobe Sociale summiere metriek <br> 10: Audience Manager server-side het door:sturen gebruikt | tinyint zonder teken |
| **`hit_time_gmt`** | Het tijdstempel van de hit Adobe data collection servers heeft de hit ontvangen, gebaseerd op UNIX® time. | int |
| **`hitid_high`** | Wordt gebruikt met `hitid_low` om een hit te identificeren. | bigint zonder teken |
| **`hitid_low`** | Wordt gebruikt met `hitid_high` om een hit te identificeren. | bigint zonder teken |
| **`hourly_visitor`** | Een vlag die bepaalt als de slag een nieuwe uurbezoeker is. | tinyint zonder teken |
| **`ip`** | Het IPv4-adres, gebaseerd op de HTTP-header van de afbeeldingsaanvraag. Enkel en wederzijds aan `ipv6`; als deze kolom een niet-verduisterd IP adres bevat, is `ipv6` leeg. | teken(20) |
| **`ipv6`** | Het gecomprimeerde IPv6-adres, indien beschikbaar. Enkel en wederzijds aan `ip`; als deze kolom een niet-verduisterd IP adres bevat, is `ip` leeg. | varchar(40) |
| **`j_jscript`** | Versie van JavaScript wordt ondersteund door de browser. | teken(5) |
| **`java_enabled`** | De [[!UICONTROL Java enabled]](/help/components/dimensions/java-enabled.md) . <br> Y: Toegelaten <br> N: Gehandicapte <br> U: Onbekend | teken(1) |
| **`javascript`** | Een opzoekings-id van de JavaScript-versie, gebaseerd op `j_jscript` . Verwijst naar de opzoektabel van `javascript_version` . | tinyint zonder teken |
| **`language`** | Een numerieke id die de taal van de bezoeker vertegenwoordigt. Verwijst naar de opzoektabel van `languages.tsv` . | small int zonder teken |
| **`last_hit_time_gmt`** | Tijdstempel (in UNIX®-tijd) van de voorgaande hit. Hiermee wordt de [[!UICONTROL Days since last visit]](/help/components/dimensions/days-since-last-visit.md) -dimensie berekend. | int |
| **`last_purchase_num`** | De [ dimensie van de loyaliteit van 0} Klant. ](/help/components/dimensions/customer-loyalty.md) Het aantal eerdere aankopen dat de bezoeker heeft gedaan. <br> 0: Geen vroegere aankopen (niet een klant) <br> 1: 1 voorafgaande aankoop (nieuwe klant) <br> 2: 2 vroegere aankopen (terugkeerklant) <br> 3: 3 of meer vroegere aankopen (loyale klant) | int zonder teken |
| **`last_purchase_time_gmt`** | Wordt gebruikt in de [[!UICONTROL Days since last purchase]](/help/components/dimensions/days-since-last-purchase.md) -dimensie. Tijdstempel (in UNIX®-tijd) van de laatste aanschaf. Voor eerste aankopen en bezoekers die nog niet eerder een aankoop hebben gedaan, is deze waarde `0` . | int |
| **`latlon1`** | Locatie (tot 10 km) | varchar(255) |
| **`latlon23`** | Locatie (tot 100 m) | varchar(255) |
| **`latlon45`** | Locatie (tot 1 m) | varchar(255) |
| **`mc_audiences`** | Lijst met Audience Manager-segment-id&#39;s waartoe de bezoeker behoort. In de kolom `post_mc_audiences` wordt het scheidingsteken gewijzigd in `--**--` . | text |
| **`mcvisid`** | Experience Cloud-bezoeker-id. 128-bits getal dat bestaat uit twee samengevoegde 64-bits getallen opgevuld tot 19 cijfers. | varchar(255) |
| **`mobile_id`** | Als de gebruiker een mobiel apparaat gebruikt, is dit de numerieke id van het apparaat. De zeer belangrijke waarde voor `mobile_attributes.tsv` [ Dynamische raadpleging ](dynamic-lookups.md). | int |
| **`mobileaction`** | Mobiele handeling. Automatisch verzamelen wanneer `trackAction` wordt aangeroepen in mobiele implementaties. Hiermee kunt u in de app automatisch tekenen met handelingen. | varchar(100) |
| **`mobileappid`** | Mobiele toepassings-id. Slaat de toepassingsnaam en -versie op in de volgende indeling: `[AppName] [BundleVersion]` | varchar(255) |
| **`mobileappperformanceappid`** | Wordt gebruikt in de Apteligent-gegevensconnector. De toepassings-id die in Apteligent wordt gebruikt. | varchar(255) |
| **`mobileappperformancecrashid`** | Wordt gebruikt in de Apteligent-gegevensconnector. De crash-id die in Apteligent wordt gebruikt. | varchar(255) |
| **`mobileappstoreobjectid`** | Wordt gebruikt in de gegevensconnector [!DNL Appfigures] . Object-id van App store. | varchar(255) |
| **`mobilebeaconmajor`** | Belangrijkste baken voor mobiele services | varchar(100) |
| **`mobilebeaconminor`** | Kleine beperking van het baken voor mobiele services | varchar(100) |
| **`mobilebeaconproximity`** | Bandennabijheid mobiele services | varchar(255) |
| **`mobilebeaconuuid`** | Mobile Services-baken UUID | varchar(100) |
| **`mobilecampaigncontent`** | De naam of id van de inhoud die de koppeling heeft weergegeven. Bevolkt door Mobile App Acquisition. | varchar(255) |
| **`mobilecampaignmedium`** | Marketingmedium, zoals banner of e-mail. Bevolkt door Mobile App Acquisition. | varchar(255) |
| **`mobilecampaignname`** | De naam van de campagne, die ook in de campagnevariabele wordt opgeslagen. Bevolkt door Mobile App Acquisition. | varchar(255) |
| **`mobilecampaignsource`** | Originele referentie, zoals nieuwsbrief of sociaal medianetwerk. Bevolkt door Mobile App Acquisition. | varchar(255) |
| **`mobilecampaignterm`** | Betaalde trefwoorden of andere termen die u met deze overname wilt bijhouden. Bevolkt door Mobile App Acquisition. | varchar(255) |
| **`mobiledayofweek`** | Het nummer van de weekdag waarop de app is gestart. | varchar(255) |
| **`mobiledayssincefirstuse`** | Aantal dagen sinds de app voor de eerste keer is uitgevoerd. | varchar(255) |
| **`mobiledayssincelastuse`** | Aantal dagen sinds de app voor de laatste keer is uitgevoerd. | varchar(255) |
| **`mobiledeeplinkid`** | Verzameld op basis van de variabele met contextgegevens `a.deeplink.id` . Wordt gebruikt in overnamerapporten als een identifier voor een koppeling naar een mobiele overname. | varchar(255) |
| **`mobiledevice`** | Naam van mobiel apparaat. In iOS wordt de notatie opgeslagen als een door komma&#39;s gescheiden tekenreeks van 2 cijfers. Het eerste getal vertegenwoordigt de apparaatgeneratie en het tweede getal vertegenwoordigt de apparaatfamilie. | varchar(255) |
| **`mobilehourofday`** | Definieert het uur van de dag waarop de app is gestart. Volg de numerieke notatie van 24 uur. | varchar(255) |
| **`mobileinstalldate`** | Datum mobiele installatie. Vermeldt de datum van de eerste keer dat een gebruiker de mobiele app opent. | varchar(255) |
| **`mobilelaunchnumber`** | Elke keer dat de mobiele app wordt gestart, neemt deze met één toe. | varchar(255) |
| **`mobilemessagebuttonname`** | Verzameld op basis van de variabele met contextgegevens `a.message.button.id` . Wordt gebruikt voor in-app berichten om de knop te identificeren waarmee het bericht is gesloten. | varchar(100) |
| **`mobilemessageid`** | Berichtings-id in de app | varchar(255) |
| **`mobilemessageonline`** | Bericht online in de app | varchar(255) |
| **`mobilemessagepushoptin`** | Verzameld op basis van de variabele met contextgegevens `a.push.optin` . Stel dit in op &quot;true&quot; wanneer de gebruiker op Push Messaging klikt; anders is de waarde &quot;false&quot;. | varchar(255) |
| **`mobilemessagepushpayloadid`** | Verzameld op basis van de variabele met contextgegevens `a.push.payloadid` . Gebruikt in duw overseinen als nuttige ladings herkenningsteken. | varchar(255) |
| **`mobileosversion`** | Versie van besturingssysteem voor mobiele services | varchar(255) |
| **`mobileplaceaccuracy`** | Verzameld op basis van de variabele met contextgegevens `a.loc.acc` . Geeft de nauwkeurigheid van de GPS in meters aan op het moment van verzameling. | varchar(255) |
| **`mobileplacecategory`** | Verzameld op basis van de variabele met contextgegevens `a.loc.category` . Beschrijft de categorie van een specifieke plaats. | varchar(255) |
| **`mobileplaceid`** | Verzameld op basis van de variabele met contextgegevens `a.loc.id` . Identificatiecode voor een bepaald aandachtspunt. | varchar(255) |
| **`mobilepushoptin`** | Push-optie voor mobiele services | varchar(255) |
| **`mobilepushpayloadid`** | Mobiele services - Push-lading-id | varchar(255) |
| **`mobilerelaunchcampaigncontent`** | Inhoud voor mobiele services starten | varchar(255) |
| **`mobilerelaunchcampaignmedium`** | Mobiele services, startmedium | varchar(255) |
| **`mobilerelaunchcampaignsource`** | Bron voor mobiele services | varchar(255) |
| **`mobilerelaunchcampaignterm`** | Starten van mobiele services | varchar(255) |
| **`mobilerelaunchcampaigntrackingcode`** | Verzameld op basis van de variabele met contextgegevens `a.launch.campaign.trackingcode` . Wordt gebruikt in aankopen als de code voor het bijhouden van de opstartiecampagne. | varchar(255) |
| **`mobileresolution`** | Resolutie van het mobiele apparaat. `[Width] x [Height]` in pixels. | varchar(255) |
| **`monthly_visitor`** | Een markering die bepaalt of de bezoeker uniek is voor de huidige maand. | tinyint zonder teken |
| **`mvvar1`** - `mvvar3` | [ de veranderlijke ](/help/implement/vars/page-vars/list.md) waarden van de Lijst. Bevat een lijst met gescheiden waarden, afhankelijk van de implementatie. De kolommen `post_mvvar1` - `post_mvvar3` vervangen het oorspronkelijke scheidingsteken door `--**--` . | text |
| **`mvvar1_instances`** - `mvvar3_instances` | De waarden van de lijstvariabele die op de huidige treffer werden geplaatst. Hiermee vervangt u het oorspronkelijke scheidingsteken door `--**--` . De kolommen `post` bevatten doorgaans geen gegevens. | text |
| **`new_visit`** | Een vlag die bepaalt als de huidige slag een nieuw bezoek is. Door Adobe ingesteld na 30 minuten inactiviteit van het bezoek. | tinyint zonder teken |
| **`os`** | Een numerieke id die het besturingssysteem van de bezoeker vertegenwoordigt. Gebaseerd op de kolom `user_agent` . De zeer belangrijke waarde voor `operating_system.tsv` standaardraadpleging en `operating_system_type.tsv` [ Dynamische raadpleging ](dynamic-lookups.md). | int zonder teken |
| **`page_event`** | Het type hit dat wordt verzonden in de aanvraag voor de afbeelding (standaardhit, downloadkoppeling, aangepaste koppeling, afsluitkoppeling). Zie [ de gebeurtenisraadpleging van de Pagina ](datafeeds-page-event.md). | tinyint zonder teken |
| **`page_event_var1`** | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De URL van de downloadkoppeling, exit-koppeling of aangepaste koppeling waarop is geklikt. | text |
| **`page_event_var2`** | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De aangepaste naam (indien opgegeven) van de koppeling. Plaatst de [ verbinding van de Douane ](/help/components/dimensions/custom-link.md), [ verbinding van de Download ](/help/components/dimensions/download-link.md), of [ Verbinding van de Uitgang ](/help/components/dimensions/exit-link.md) afhankelijk van de waarde in `page_event`. | varchar(100) |
| **`page_type`** | De [ Pagina&#39;s niet gevonden ](/help/components/dimensions/pages-not-found.md) dimensie, die typisch voor 404 pagina&#39;s wordt gebruikt. | teken(20) |
| **`page_url`** | De URL van de hit. `post_page_url` wordt gestript voor aanvragen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md) ) en gebruikt een gegevenstype varchar(255). | text |
| **`pagename`** | De [ dimensie van de Pagina ](/help/components/dimensions/page.md). Als de variabele [`pagename`](/help/implement/vars/page-vars/pagename.md) leeg is, gebruikt Analytics in plaats daarvan `page_url` . | varchar(100) |
| **`pagename_no_url`** | Vergelijkbaar met `pagename` , maar dit komt niet overeen met `page_url` . Alleen de kolom `post` is beschikbaar. | varchar(100) |
| **`paid_search`** | Een vlag die bepaalt als de treffer betaalde onderzoeksopsporing aanpast. | tinyint zonder teken |
| **`persistent_cookie`** | Gebruikt in de [ Persistent koekjessteun ](/help/components/dimensions/persistent-cookie-support.md) dimensie. Geeft aan of de bezoeker cookies ondersteunt die na elke hit niet worden verwijderd. | teken(1) |
| **`pointofinterest`** | Naam van interesepunt voor mobiele services | varchar(255) |
| **`pointofinterestdistance`** | Afstand van mobiele services tot belangencentrum | varchar(255) |
| **`post_`** kolommen | Bevat de waarde die uiteindelijk in rapporten wordt gebruikt. Elke postkolom wordt bevolkt na server-zijlogica, verwerkingsregels, en regels VISTA. Adobe raadt aan in de meeste gevallen postkolommen te gebruiken. | Zie de desbetreffende niet-postkolom |
| **`product_list`** | De paginariabele [`products`](/help/implement/vars/page-vars/products.md) . De hulp bevolkt verscheidene dimensies en metriek, met inbegrip van [ Categorie ](/help/components/dimensions/category.md), [ Product ](/help/components/dimensions/product.md), [ Eenheden ](/help/components/metrics/units.md), en [ Inkomsten ](/help/components/metrics/revenue.md). | text |
| **`prop1`** - `prop75` | Aangepaste verkeersvariabelen 1-75. Gebruikt in [ Prop ](/help/components/dimensions/prop.md) afmetingen. | varchar(100) |
| **`purchaseid`** | De unieke id voor een aankoop, zoals ingesteld met de variabele [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) . Wordt gebruikt door de kolom `duplicate_purchase` . | teken(20) |
| **`quarterly_visitor`** | Een vlag die bepaalt als de treffer een nieuwe driemaandelijkse bezoeker is. | tinyint zonder teken |
| **`ref_domain`** | De [ Verwijzende domein ](/help/components/dimensions/referring-domain.md) dimensie. Gebaseerd op de kolom `referrer` . | varchar(100) |
| **`ref_type`** | Een numerieke id die het verwijzingstype voor de treffer vertegenwoordigt. Gebruikt in het [ type van Referateur ](/help/components/dimensions/referrer-type.md) afmeting. <br> 1: Binnen uw plaats <br> 2: Andere websites <br> 3: De motoren van het onderzoek <br> 4: Harde aandrijving <br> 5: USENET <br> 6: Typed/Bladwijzerplaat (geen referentie) <br> 7: E-mail <br> 8: Geen JavaScript <br> 9: Sociale Netwerken | tinyint zonder teken |
| **`referrer`** | De [ dimensie van de Verwijzer ](/help/components/dimensions/referrer.md). Hoewel `referrer` een gegevenstype varchar(255) gebruikt, gebruikt `post_referrer` een gegevenstype varchar(244). | varchar(255) |
| **`resolution`** | Een numerieke id die de resolutie van het beeldscherm aangeeft. Gebruikt in de [ resolutie ](/help/components/dimensions/monitor-resolution.md) dimensie van de Monitor. Gebruikt `resolution.tsv` opzoektabel. | small int zonder teken |
| **`s_kwcid`** | Trefwoord-id gebruikt in Adobe Advertising-integratie. | varchar(255) |
| **`s_resolution`** | Waarde van resolutie voor onbewerkt scherm. Wordt verzameld met de JavaScript-functie `screen.width x screen.height` . | teken(20) |
| **`search_engine`** | Een numerieke id die staat voor het zoekprogramma waarmee de bezoeker naar uw site is doorverwezen. Gebruikt in [ afmetingen van de Motor van het 0} Onderzoek. ](/help/components/dimensions/search-engine.md) Verwijst naar de opzoektabel van `search_engines.tsv` . | small int zonder teken |
| **`search_page_num`** | Gebruikt door [ Al Rank van de Pagina van het Onderzoek ](/help/components/dimensions/all-search-page-rank.md) afmeting. Hiermee geeft u aan op welke pagina met zoekresultaten uw site is weergegeven voordat de gebruiker op uw site heeft geklikt. | small int zonder teken |
| **`secondary_hit`** | Een vlag die bepaalt als de slag een secundaire slag is. Deze markering is doorgaans afkomstig van taggen met meerdere suite- en VISTA-regels die treffers kopiëren. | tinyint zonder teken |
| **`sourceid`** | Source-id | int zonder teken |
| **`state`** | Staatvariabele. | varchar(50) |
| **`stats_server`** | Niet gebruiken. Interne Adobe-server die de hit heeft verwerkt. | teken(30) |
| **`t_time_info`** | Lokale tijd voor de bezoeker. Indeling is: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| **`tnt`** | Wordt gebruikt in Adobe Target-integratie. Vertegenwoordigt alle tests momenteel gekwalificeerd voor. Indeling is: `TargetCampaignID:TargetRecipeID:TargetType\|Event/Action` . | text |
| **`tnt_action`** | Wordt gebruikt in Adobe Target-integratie. Geeft alle tests aan waarvoor de hit geschikt is. | text |
| **`tnt_instances`** | Wordt gebruikt in Adobe Target-integratie. Variabele voor doelinstanties. | text |
| **`transactionid`** | Een unieke id waarbij verschillende gegevenspunten later via gegevensbronnen kunnen worden geüpload. Verzameld met de variabele [`transactionID`](/help/implement/vars/page-vars/transactionid.md) . | text |
| **`truncated_hit`** | Een vlag die erop wijst dat het beeldverzoek werd beknot. Geeft aan dat een gedeeltelijke hit is ontvangen. <br> Y: Hit werd afgebroken; gedeeltelijke hit ontving <br> N: Hit werd niet afgebroken; volledige ontvangen hit | teken(1) |
| **`user_agent`** | De userAgent-tekenreeks die wordt verzonden in de HTTP-header van de afbeeldingsaanvraag. | text |
| **`user_hash`** | Niet gebruiken. Hash op de rapportsuite-id. Gebruik in plaats hiervan `username` . | int zonder teken |
| **`user_server`** | Gebruikt in de [ dimensie van de Server ](/help/components/dimensions/server.md). | varchar(100) |
| **`userid`** | Niet gebruiken. De numerieke id voor de rapportsuite-id. Gebruik in plaats hiervan `username` . | int zonder teken |
| **`username`** | De rapportsuite-id voor de hit. | teken(40) |
| **`va_closer_detail`** | De [ Laatste dimensie van aanrakingsdetail ](/help/components/dimensions/last-touch-detail.md). | varchar(255) |
| **`va_closer_id`** | Een numerieke identiteitskaart die de [ Laatste dimensie van het aanrakingskanaal ](/help/components/dimensions/last-touch-channel.md) identificeert. De zoekopdracht voor deze id vindt u in de Manager voor marketingkanalen. | tinyint zonder teken |
| **`va_finder_detail`** | De [ Eerste aanrakingsdetail ](/help/components/dimensions/first-touch-detail.md) dimensie. | varchar(255) |
| **`va_finder_id`** | Een numerieke identiteitskaart die de [ Eerste dimensie van het aanrakingskanaal ](/help/components/dimensions/first-touch-channel.md) identificeert. De zoekopdracht voor deze id vindt u in de Manager voor marketingkanalen. | tinyint zonder teken |
| **`va_instance_event`** | Een vlag die de Instanties van het Kanaal van de Marketing [ ](/help/components/metrics/instances.md) identificeert. | tinyint zonder teken |
| **`va_new_engagement`** | Een vlag die het Kanaal van de Marketing [ Nieuwe overeenkomsten ](/help/components/metrics/new-engagements.md) identificeert. | tinyint zonder teken |
| **`video`** | De [ Inhoud ](/help/components/dimensions/sm-core.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoad`** | De [ Advertentie ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadinpod`** | De [ Advertentie in podpositie ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadlength`** | De [ lengte van de Advertentie (veranderlijk) ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | integer |
| **`videoadload`** | De [ Advertentie laadt ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadname`** | De [ naam van de Advertentie (veranderlijk) ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadplayername`** | De [ naam van de speler van de Advertentie ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadpod`** | De [ peul van de Advertentie ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoadvertiser`** | De [ Advertiser ](/help/components/dimensions/sm-ads.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoaudioalbum`** | Het [ album ](/help/components/dimensions/sm-audio-metadata.md) stromen media de dienstendimensie van de Album. | varchar(255) |
| **`videoaudioartist`** | De [ Kunstenaars ](/help/components/dimensions/sm-audio-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoaudioauthor`** | De [ het stromen van de auteur ](/help/components/dimensions/sm-audio-metadata.md) media de dienstendimensie. | varchar(255) |
| **`videoaudiolabel`** | Het [ Etiket ](/help/components/dimensions/sm-audio-metadata.md) stromen media de dienstendimensie. | varchar(255) |
| **`videoaudiopublisher`** | De [ Uitgever ](/help/components/dimensions/sm-audio-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoaudiostation`** | De [ het stromen van de Post ](/help/components/dimensions/sm-audio-metadata.md) media de dienstendimensie. | varchar(255) |
| **`videocampaign`** | De [ het stromen media de dienstendimensie van identiteitskaart van de Campagne ](/help/components/dimensions/sm-ads.md). | varchar(255) |
| **`videochannel`** | Het [ kanaal van de Inhoud ](/help/components/dimensions/sm-core.md) stromen media de dienstendimensie. | varchar(255) |
| **`videochapter`** | De [ dimensie van de Hoofdstuk ](/help/components/dimensions/sm-chapters.md) het stromen media diensten. | varchar(255) |
| **`videocontenttype`** | Het [ type van Inhoud ](/help/components/dimensions/sm-core.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videodaypart`** | Het [ stromen van het deel van de Dag deel ](/help/components/dimensions/sm-video-metadata.md) media de dienstendimensie. | varchar(255) |
| **`videoepisode`** | De [ Episode ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videofeedtype`** | Het [ de voedertype van Media ](/help/components/dimensions/sm-video-metadata.md) stromen media de dienstendimensie. | varchar(255) |
| **`videogenre`** | De [ Genre ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie. Deze dimensie maakt het mogelijk meerdere waarden in dezelfde hit te gebruiken, gescheiden door een komma. | text |
| **`videolength`** | De [ lengte van de Inhoud (veranderlijk) ](/help/components/dimensions/sm-core.md) het stromen media de dienstendimensie. | integer |
| **`videomvpd`** | De [ MVPD ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoname`** | De [ naam van de Inhoud (veranderlijke) ](/help/components/dimensions/sm-core.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videonetwork`** | De [ het stromen media van het 0} Netwerk {dimensie.](/help/components/dimensions/sm-video-metadata.md) | varchar(255) |
| **`videopath`** | De [ weg van Media ](/help/components/dimensions/sm-core.md) het stromen media de dienstendimensie. | varchar(100) |
| **`videoplayername`** | De [ het stromen media de dienstendimensie van de speler van 0} Inhoud {.](/help/components/dimensions/sm-core.md) | varchar(255) |
| **`videotime`** | De [ tijd van de Inhoud besteedde ](/help/components/metrics/sm-core.md) het stromen media diensten metrisch. | integer |
| **`videoqoebitrateaverageevar`** | De [ Gemiddelde bitrate ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoqoebitratechangecountevar`** | De [ Bitrate verandert ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoqoebuffercountevar`** | De [ gebeurtenissen van de Buffer ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoqoebuffertimeevar`** | De [ Totale bufferduur ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoqoedroppedframecountevar`** | De [ Gedropte kaders ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoqoeerrorcountevar`** | De [ het stromen media van de fouten ](/help/components/dimensions/sm-quality.md) dimensie van de Fouten {. | varchar(255) |
| **`videoqoeextneralerrors`** | De [ Externe fout IDs ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. Deze dimensie staat veelvoudige waarden in de zelfde klap toe. | text |
| **`videoqoeplayersdkerrors`** | De [ de foutenIDs van SDK van de Speler ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie. Deze dimensie staat veelvoudige waarden in de zelfde klap toe. | text |
| **`videoqoetimetostartevar`** | De [ Tijd om ](/help/components/dimensions/sm-quality.md) het stromen media de dienstendimensie te beginnen. | varchar(255) |
| **`videoseason`** | De [ Seizoen ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videosegment`** | Het [ segment van de Inhoud ](/help/components/dimensions/sm-core.md) stromen media de dienstendimensie. | varchar(255) |
| **`videoshow`** | [ toon ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie. | varchar(255) |
| **`videoshowtype`** | [ toon type ](/help/components/dimensions/sm-video-metadata.md) het stromen media de dienstendimensie van de media. | varchar(255) |
| **`videostreamtype`** | Het [ type van Stroom ](/help/components/dimensions/sm-core.md) stromen media de dienstendimensie. | varchar(255) |
| **`visid_high`** | Wordt gebruikt met `visid_low` om een bezoeker op unieke wijze te identificeren. | bigint zonder teken |
| **`visid_low`** | Wordt gebruikt met `visid_high` om een bezoeker op unieke wijze te identificeren. | bigint zonder teken |
| **`visid_new`** | Een markering die bepaalt of de treffer een pas gegenereerde bezoeker-id bevat. | teken(1) |
| **`visid_timestamp`** | Als een bezoekersidentiteitskaart nieuw wordt geproduceerd, verstrekt timestamp in de tijd van UNIX® van toen bezoekersidentiteitskaart werd geproduceerd. | int |
| **`visid_type`** | Niet voor extern gebruik; intern gebruikt door Adobe voor het verwerken van optimalisaties. Een numerieke id die staat voor de methode waarmee de bezoeker wordt geïdentificeerd.<br>`0`: Aangepaste bezoeker-id of Onbekend/niet van toepassing <br>`1`: IP en fallback van gebruikersagent <br>`2`: Koptekst van HTTP Mobile Subscriber <br>`3`: oude cookie-waarde (`s_vi`) <br>`4`: Fallback-cookie-waarde (`s_fid`) <br>`5`: Identiteitsservice | tinyint zonder teken |
| **`visit_keywords`** | De [ dimensie van het sleutelwoord van het Onderzoek ](/help/components/dimensions/search-keyword.md). Deze kolom gebruikt een niet-standaard karaktergrens van varchar (244) om achterste die logica aan te passen door Adobe wordt gebruikt. | varchar(244) |
| **`visit_num`** | De [ dimensie van het aantal van het Bezoek ](/help/components/dimensions/visit-number.md). Begint bij 1, en verhoogt telkens als een nieuw bezoek per bezoeker begint. | int zonder teken |
| **`visit_page_num`** | De [ diepte van de Actief ](/help/components/dimensions/hit-depth.md) dimensie. Verhoogt met 1 voor elke hit die de bezoeker genereert. Hiermee herstelt u elk bezoek. | int zonder teken |
| **`visit_ref_domain`** | Gebaseerd op de kolom `visit_referrer` . Het eerste verwijzende domein van het bezoek. | varchar(100) |
| **`visit_ref_type`** | Een numerieke id die het referentietype van de eerste referentie van het bezoek vertegenwoordigt. Verwijst naar de opzoektabel van `referrer_type.tsv` . | tinyint zonder teken |
| **`visit_referrer`** | De eerste referentie van het bezoek. | varchar(255) |
| **`visit_search_engine`** | Een numerieke id die de eerste zoekfunctie van het bezoek vertegenwoordigt. Verwijst naar de opzoektabel van `search_engines.tsv` . | small int zonder teken |
| **`visit_start_page_url`** | De eerste URL van het bezoek. | varchar(255) |
| **`visit_start_pagename`** | De waarde Paginanaam in de eerste hit van het bezoek. | varchar(100) |
| **`visit_start_time_gmt`** | Tijdstempel (in UNIX®-tijd) van de eerste hit van het bezoek. | int |
| **`weekly_visitor`** | Een vlag die bepaalt als de slag een nieuwe wekelijkse bezoeker is. | tinyint zonder teken |
| **`yearly_visitor`** | Een vlag die bepaalt als de klap een nieuwe jaarlijkse bezoeker is. | tinyint zonder teken |
| **`zip`** | Helpt de [ dimensie van het Postcode ](/help/components/dimensions/zip-code.md) bevolken. Zie ook `geo_zip` . | varchar(50) |

{style="table-layout:auto"}

## Ongebruikte of gepensioneerde kolommen

De volgende lijst met kolommen wordt niet gebruikt, verwijderd of bevat op een andere manier geen waarde voor de rapportage. Sommige van deze kolommen zijn gekoppeld aan functies die zijn ingesteld op zonsondergang, terwijl andere kolommen niet langer nodig zijn vanwege nieuwe en robuustere functies. De meeste van deze kolommen bevatten geen gegevens; kolommen die nog gegevens kunnen bevatten, worden niet ondersteund door de huidige bibliotheken voor gegevensverzameling en zijn niet beschikbaar in Analysis Workspace.

* `adclassificationcreative`
* `click_action`
* `click_action_type`
* `click_context`
* `click_context_type`
* `click_sourceid`
* `click_tag`
* `hier1` - `hier5`
* `homepage`
* `ip2`
* `mobileacquisitionclicks`
* `mobileactioninapptime`
* `mobileactiontotaltime`
* `mobileappperformanceaffectedusers`
* `mobileappperformanceappid.app-perf-app-name`
* `mobileappperformanceappid.app-perf-platform`
* `mobileappperformancecrashes`
* `mobileappperformancecrashid.app-perf-crash-name`
* `mobileappperformanceloads`
* `mobileappstoreavgrating`
* `mobileappstoredownloads`
* `mobileappstoreinapprevenue`
* `mobileappstoreinapproyalties`
* `mobileappstoreobjectid.app-store-user`
* `mobileappstoreobjectid.application-name`
* `mobileappstoreobjectid.application-version`
* `mobileappstoreobjectid.appstore-name`
* `mobileappstoreobjectid.category-name`
* `mobileappstoreobjectid.country-name`
* `mobileappstoreobjectid.device-manufacturer`
* `mobileappstoreobjectid.device-name`
* `mobileappstoreobjectid.in-app-name`
* `mobileappstoreobjectid.platform-name-version`
* `mobileappstoreobjectid.rank-category-type`
* `mobileappstoreobjectid.region-name`
* `mobileappstoreobjectid.review-comment`
* `mobileappstoreobjectid.review-title`
* `mobileappstoreoneoffrevenue`
* `mobileappstoreoneoffroyalties`
* `mobileappstorepurchases`
* `mobileappstorerank`
* `mobileappstorerankdivisor`
* `mobileappstorerating`
* `mobileappstoreratingdivisor`
* `mobileavgprevsessionlength`
* `mobilecrashes`
* `mobilecrashrate`
* `mobiledailyengagedusers`
* `mobiledayssincelastupgrade`
* `mobiledeeplinkid.name`
* `mobileinstalls`
* `mobilelaunches`
* `mobilelaunchessincelastupgrade`
* `mobileltv`
* `mobileltvtotal`
* `mobilemessageclicks`
* `mobilemessageid.dest`
* `mobilemessageid.name`
* `mobilemessageid.type`
* `mobilemessageimpressions`
* `mobilemessagepushpayloadid.name`
* `mobilemessageviews`
* `mobilemonthlyengagedusers`
* `mobileosenvironment`
* `mobileplacedwelltime`
* `mobileplaceentry`
* `mobileplaceexit`
* `mobileprevsessionlength`
* `mobilerelaunchcampaigntrackingcode.name`
* `mobileupgrades`
* `namespace`
* `p_plugins`
* `page_event_var3`
* `partner_plugins`
* `plugins`
* `prev_page`
* `product_merchandising`
* `sampled_hit`
* `service`
* `socialaccountandappids`
* `socialassettrackingcode`
* `socialauthor`
* `socialaveragesentiment`
* `socialaveragesentiment (deprecated)`
* `socialcontentprovider`
* `socialfbstories`
* `socialfbstorytellers`
* `socialinteractioncount`
* `socialinteractiontype`
* `sociallanguage`
* `sociallatlong`
* `sociallikeadds`
* `sociallink`
* `sociallink (deprecated)`
* `socialmentions`
* `socialowneddefinitioninsighttype`
* `socialowneddefinitioninsightvalue`
* `socialowneddefinitionmetric`
* `socialowneddefinitionpropertyvspost`
* `socialownedpostids`
* `socialownedpropertyid`
* `socialownedpropertyname`
* `socialownedpropertypropertyvsapp`
* `socialpageviews`
* `socialpostviews`
* `socialproperty`
* `socialproperty (deprecated)`
* `socialpubcomments`
* `socialpubposts`
* `socialpubrecommends`
* `socialpubsubscribers`
* `socialterm`
* `socialtermslist`
* `socialtermslist (deprecated)`
* `socialtotalsentiment`
* `survey`
* `survey_instances`
* `tnt_post_vista`
* `ua_color`
* `ua_os`
* `ua_pixels`
* `videoauthorized`
* `videoaverageminuteaudience`
* `videochaptercomplete`
* `videochapterstart`
* `videochaptertime`
* `videopause`
* `videopausecount`
* `videopausetime`
* `videoplay`
* `videoprogress10`
* `videoprogress25`
* `videoprogress50`
* `videoprogress75`
* `videoprogress96`
* `videoqoebitrateaverage`
* `videoqoebitratechange`
* `videoqoebuffer`
* `videoqoedropbeforestart`
* `videoqoedroppedframes`
* `videoqoeerror`
* `videoresume`
* `videototaltime`
* `videouniquetimeplayed`

>[!MORELIKETHIS]
>
>[ XDM objecten veranderlijke afbeelding ](/help/implement/aep-edge/xdm-var-mapping.md)
>>[Gegevensobjectvariabele toewijzen ](/help/implement/aep-edge/data-var-mapping.md)
