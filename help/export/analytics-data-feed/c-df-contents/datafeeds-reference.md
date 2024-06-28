---
description: Tabelgegevens die de kolommen in de gegevensinvoer beschrijven.
keywords: Gegevensfeed;kolommen
subtopic: data feeds
title: Referentie gegevenskolom
feature: Data Feeds
exl-id: e1492147-6e7f-4921-b509-898e7efda596
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '3415'
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
>De meeste kolommen bevatten een vergelijkbare kolom met een voorvoegsel van `post_`. Post-kolommen bevatten waarden na logica aan de serverzijde, verwerkingsregels en VISTA-regels. Adobe raadt in de meeste gevallen aan postkolommen te gebruiken. Zie [Veelgestelde vragen over gegevensfeeds](../df-faq.md) voor meer informatie .

U vindt vorige updates van deze tabel op de pagina [geschiedenis toewijzen op GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).

| Kolomnaam | Kolombeschrijving | Gegevenstype |
| --- | --- | --- |
| **`accept_language`** | Hiermee worden alle geaccepteerde talen weergegeven, zoals wordt aangegeven in de HTTP-header Accept-Language in een afbeeldingsaanvraag. | teken(20) |
| **`adload`** | Media en laden | varchar(255) |
| **`aemassetid`** | Een variabele van meerdere waarden die aan Activa IDs (GUIDs) van een reeks Adobe Experience Manager Assets beantwoordt. Incrementele indrukgebeurtenissen. | Sms |
| **`aemassetsource`** | Identificeert de bron van de gebeurtenis van het middel. Wordt gebruikt in Adobe Experience Manager. | Varchar (255) |
| **`aemclickedassetid`** | Element-id van een Adobe Experience Manager-element. De verhogingen klikken Gebeurtenissen. | varchar(255) |
| **`browser`** | Een numerieke id die de browser vertegenwoordigt. Verwijst naar de `browser.tsv` opzoektabel. | niet ondertekend |
| **`browser_height`** | De [afmeting Browserhoogte](/help/components/dimensions/browser-height.md) . | smallint niet ondertekend |
| **`browser_width`** | De [browserbreedte](/help/components/dimensions/browser-width.md) | small int zonder teken |
| **`c_color`** | Bitdiepte van het kleurenpalet. Wordt gebruikt als onderdeel van de berekening van de [Kleurdiepte](/help/components/dimensions/color-depth.md) dimensie. AppMeasurement gebruikt de JavaScript-functie `screen.colorDepth()`. | teken(20) |
| **`campaign`** | De [Trackingcode](/help/components/dimensions/tracking-code.md) dimensie. | varchar(255) |
| **`carrier`** | Adobe Advertising integratie variabele. Geeft de mobiele drager aan. De sleutelwaarde voor `carrier.tsv` [Dynamische zoekopdracht](dynamic-lookups.md). | varchar(100) |
| **`ch_hdr`** | Clienttips die via de HTTP-aanvraagheader worden verzameld. | text |
| **`ch_js`** | Clienttips die zijn verzameld via de JavaScript-API voor client-tips voor de gebruikersagent. | text |
| **`channel`** | De [Site-secties](/help/components/dimensions/site-section.md) dimensie. | varchar(100) |
| **`clickmaplink`** | Koppeling naar Activity Map | varchar(255) |
| **`clickmaplinkbyregion`** | Activity Map per regio | varchar(255) |
| **`clickmappage`** | Activity Map pagina | varchar(255) |
| **`clickmapregion`** | Activity Map | varchar(255) |
| **`code_ver`** | API- of client-SDK-versie die wordt gebruikt om de afbeeldingsaanvraag te compileren en te verzenden. | teken(16) |
| **`color`** | ID kleurdiepte gebaseerd op de waarde van de `c_color` kolom. Verwijst naar de `color_depth.tsv` opzoektabel. | small int zonder teken |
| **`connection_type`** | Een numerieke id die het verbindingstype vertegenwoordigt. De [Verbindingstype](/help/components/dimensions/connection-type.md) dimensie. Verwijst naar de `connection_type.tsv` opzoektabel. | tinyint zonder teken |
| **`cookies`** | De [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) dimensie.<br>Y: Enabled<br>N: Uitgeschakeld<br>U: Onbekend | teken(1) |
| **`country`** | Een numerieke id die het land van de bezoeker vertegenwoordigt. Verwijst naar de `country.tsv` opzoektabel. | small int zonder teken |
| **`ct_connect_type`** | Met betrekking tot de `connection_type` kolom. De meest voorkomende waarden zijn LAN/Wifi, Mobile Carrier en Modem. | teken(20) |
| **`curr_factor`** | Bepaalt de decimale valutapositie en wordt gebruikt voor valutaomrekening. In USD worden bijvoorbeeld twee decimalen gebruikt, zodat deze kolomwaarde `2`. | tinyint |
| **`curr_rate`** | De wisselkoers op het tijdstip van de transactie. De partners van de Adobe met XE om de wisselkoers van de huidige dag te bepalen. | decimaal (24,12) |
| **`currency`** | De valutacode die tijdens de transactie werd gebruikt. Instellen met [`currencyCode`](/help/implement/vars/config-vars/currencycode.md). | teken(8) |
| **`cust_hit_time_gmt`** | Alleen voor tijdstempels geschikte rapportsuites. De tijdstempel die met de hit wordt verzonden, gebaseerd in UNIX®-tijd. | int |
| **`cust_visid`** | De aangepaste bezoeker-id, indien ingesteld met [`visitorID`](/help/implement/vars/config-vars/visitorid.md). | Varchar (255) |
| **`daily_visitor`** | Een vlag die bepaalt of de hit een nieuwe dagelijkse bezoeker is. | tinyint zonder teken |
| **`dataprivacyconsentoptin`** | De [Optie voor beheer van toestemming](/help/components/dimensions/cm-opt-in.md) dimensie. Er kunnen meerdere waarden aanwezig zijn per hit, gescheiden door een pipe (`\|`). Geldige waarden zijn `DMP` en `SELL`. | varchar(100) |
| **`dataprivacyconsentoptout`** | De [Weigering van toegang voor beheer](/help/components/dimensions/cm-opt-out.md) dimensie. Meerdere waarden kunnen aanwezig zijn per treffer, gescheiden door een pijp (`\|`). Geldige waarden zijn `SSF`, `DMP`, en `SELL`. | varchar(100) |
| **`dataprivacydmaconsent`** | Een waarde die aangeeft als toestemming is verkregen voor het verzenden van gegevens van Adobe Analytics via Adobe Advertising naar externe advertentieproviders (zoals Google). Zie [Toestemming voor advertenties](/help/components/dimensions/ad-consent.md) voor meer informatie. | varchar(100) |
| **`date_time`** | De tijd van de treffer in leesbare formaat, die op de tijdzone van de rapportreeks wordt gebaseerd. | datetime |
| **`domain`** | De [Domein](/help/components/dimensions/domain.md) dimensie. Gebaseerd op het toegangspunt van Internet van de bezoeker. | varchar(100) |
| **`duplicate_events`** | Vermeldt elke gebeurtenis die als een duplicaat is geteld. | varchar(255) |
| **`duplicate_purchase`** | Een markering die bepaalt of de aankoopgebeurtenis voor deze hit wordt genegeerd omdat het een duplicaat is. | tinyint zonder teken |
| **`duplicated_from`** | Wordt alleen gebruikt in rapportsuites die de VISTA-regels voor raakkopieën bevatten. Geeft aan uit welke rapportsuite de treffer is gekopieerd. | varchar(40) |
| **`ef_id`** | De `ef_id` worden gebruikt in Adobe Advertising-integraties. | varchar(255) |
| **`evar1 - evar250`** | Aangepaste variabelen 1-250. Gebruikt in [eVar](/help/components/dimensions/evar.md) afmetingen. Elke organisatie gebruikt eVars anders. De beste plaats voor meer informatie over hoe uw organisatie respectieve eVars bevolkt zou zijn [document ontwerp oplossing](/help/implement/prepare/solution-design.md) specifiek voor uw organisatie. | varchar(255) |
| **`event_list`** | Lijst met door komma&#39;s gescheiden numerieke id&#39;s die gebeurtenissen vertegenwoordigen die tijdens de hit worden geactiveerd. Bevat zowel standaardgebeurtenissen als [aangepaste gebeurtenissen 1-1000](/help/components/metrics/custom-events.md). Gebruiksmiddelen `event.tsv` opzoeken. | text |
| **`exclude_hit`** | Een vlag die bepaalt of de treffer van rapportering wordt uitgesloten. De `visit_num` wordt niet verhoogd voor uitgesloten treffers.<br>1: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>2: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>3: Niet meer gebruikt. Uitsluiting van gebruikersagent<br>4: Uitsluiting op basis van IP-adres<br>5: Er ontbreekt informatie over digitale raakpunten, zoals `page_url`, `pagename`, `page_event`, of `event_list`<br>6: JavaScript heeft het proces niet correct uitgevoerd<br>7: Accountspecifieke uitsluiting, zoals in een VISTA-regeling<br>8: Niet gebruikt. Alternatieve accountspecifieke uitsluiting.<br>9: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>10: Ongeldige valutacode<br>11: Als een tijdstempel ontbreekt in een alleen-tijdstempelrapportsuite, of als een hit een tijdstempel bevat in een niet-tijdstempelrapportsuite<br>12: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>13: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>14: Doeltreffer die niet overeenkomt met een analyseresultaten<br>15: Momenteel niet gebruikt.<br>16: Advertising Cloud-hit die niet overeenkomt met een Analytics-hit | tinyint zonder teken |
| **`first_hit_page_url`** | De allereerste URL van de bezoeker. | varchar(255) |
| **`first_hit_pagename`** | De [Invoerpagina origineel](/help/components/dimensions/entry-dimensions.md) dimensie. De oorspronkelijke naam van de ingangspagina van de bezoeker. | varchar(100) |
| **`first_hit_ref_domain`** | De [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md) dimensie. Gebaseerd op `first_hit_referrer`. Het allereerste verwijzende domein van de bezoeker. | varchar(100) |
| **`first_hit_ref_type`** | Een numerieke id die het referentietype van de allereerste referentie van de bezoeker vertegenwoordigt. Verwijst naar de `referrer_type.tsv` opzoektabel. | tinyint zonder teken |
| **`first_hit_referrer`** | De allereerste verwijzende URL van de bezoeker. | varchar(255) |
| **`first_hit_time_gmt`** | Tijdstempel van de allereerste hit van de bezoeker in UNIX®-tijd. | int |
| **`geo_city`** | De naam van de stad waar de hit vandaan kwam, op basis van IP. Gebruikt in de [Plaatsen](/help/components/dimensions/cities.md) dimensie. | teken(32) |
| **`geo_country`** | De afkorting van het land waar de treffer vandaan kwam, gebaseerd op IP. Gebruikt in de [Landen](/help/components/dimensions/countries.md) dimensie. | teken(4) |
| **`geo_dma`** | Een numerieke id van het demografische gebied waar de hit vandaan kwam, gebaseerd op IP. Gebruikt in de [Amerikaanse DMA-dimensie](/help/components/dimensions/us-dma.md) . | niet ondertekend |
| **`geo_region`** | De naam van de staat of regio waar de treffer vandaan kwam, gebaseerd op IP. Gebruikt in de [Regio&#39;s](/help/components/dimensions/regions.md) dimensie. | teken(32) |
| **`geo_zip`** | De postcode waaruit de hit afkomstig was, gebaseerd op IP. Hiermee kunt u de [Postcode](/help/components/dimensions/zip-code.md) dimensie. Zie ook `zip`. | Varchar (16) |
| **`hit_source`** | De bron waar de hit vandaan kwam. De bronnen 1, 2 en 6 van de it worden gefactureerd. <br>1: standaardverzoek om afbeelding zonder tijdstempel <br>2: standaard verzoek om afbeelding met tijdstempel <br>3: Live uploaden van gegevensbron met tijdstempels <br>4: Niet gebruikt <br>5: uploaden van algemene gegevensbron <br>6: uploaden van gegevensbron voor volledige verwerking <br>7: TransactieID-gegevensbron uploaden <br>8: Niet meer gebruikt; eerdere versies van Adobe Advertising Cloud-gegevensbronnen <br>9: Niet meer gebruikt; Adobe Social summary metrics <br>10: Audience Manager server-kant het door:sturen gebruikt | tinyint zonder teken |
| **`hit_time_gmt`** | De timestamp van de servers van de de inzamelingsgegevens van de Adobe van de slag ontvingen de slag, die in tijd UNIX® wordt gebaseerd. | int |
| **`hitid_high`** | Gebruikt met `hitid_low` om een treffer te identificeren. | bigint zonder teken |
| **`hitid_low`** | Gebruikt met `hitid_high` om een treffer te identificeren. | bigint zonder teken |
| **`hourly_visitor`** | Een vlag die bepaalt als de slag een nieuwe uurbezoeker is. | tinyint zonder teken |
| **`ip`** | Het IPv4-adres, gebaseerd op de HTTP-header van de afbeeldingsaanvraag. Wederzijdse uitsluitingen aan `ipv6`; als deze kolom een niet verduisterd IP adres bevat, `ipv6` is leeg. | teken(20) |
| **`ipv6`** | Het gecomprimeerde IPv6-adres, indien beschikbaar. Wederzijdse uitsluitingen aan `ip`; als deze kolom een niet verduisterd IP adres bevat, `ip` is leeg. | varchar(40) |
| **`j_jscript`** | Versie van JavaScript wordt ondersteund door de browser. | teken(5) |
| **`java_enabled`** | De [[!UICONTROL Java enabled]](/help/components/dimensions/java-enabled.md). <br>Y: Enabled <br>N: Uitgeschakeld <br>U: Onbekend | teken(1) |
| **`javascript`** | Een opzoekings-id van de JavaScript-versie, gebaseerd op `j_jscript`. Verwijst naar de `javascript_version` opzoektabel. | tinyint zonder teken |
| **`language`** | Een numerieke id die de taal van de bezoeker vertegenwoordigt. Verwijst naar de `languages.tsv` opzoektabel. | small int zonder teken |
| **`last_hit_time_gmt`** | Tijdstempel (in UNIX®-tijd) van de voorgaande hit. Wordt gebruikt om de [[!UICONTROL Days since last visit]](/help/components/dimensions/days-since-last-visit.md) dimensie. | int |
| **`last_purchase_num`** | De [Klantenloyaliteit](/help/components/dimensions/customer-loyalty.md) dimensie. Het aantal eerdere aankopen dat de bezoeker heeft gedaan. <br>0: Geen eerdere aankopen (geen klant) <br>1: 1 aankoop vooraf (nieuwe klant) <br>2: 2 eerdere aankopen (retourklant) <br>3: 3 of meer eerdere aankopen (loyale klant) | int zonder teken |
| **`last_purchase_time_gmt`** | Gebruikt in de [[!UICONTROL Days since last purchase]](/help/components/dimensions/days-since-last-purchase.md) dimensie. Tijdstempel (in UNIX®-tijd) van de laatste aanschaf. Voor eerste aankopen en bezoekers die nog geen aankoop hebben gedaan, is deze waarde `0`. | int |
| **`latlon1`** | Locatie (tot 10 km) | varchar(255) |
| **`latlon23`** | Locatie (tot 100 m) | varchar(255) |
| **`latlon45`** | Locatie (tot 1 m) | varchar(255) |
| **`mc_audiences`** | Lijst met Audience Manager segment-id&#39;s waartoe de bezoeker behoort. De `post_mc_audiences` kolom wijzigt het scheidingsteken in `--**--`. | text |
| **`mcvisid`** | Bezoeker-id van Experience Cloud. 128-bits getal dat bestaat uit twee samengevoegde 64-bits getallen opgevuld tot 19 cijfers. | varchar(255) |
| **`mobile_id`** | Als de gebruiker een mobiel apparaat gebruikt, is dit de numerieke id van het apparaat. De sleutelwaarde voor `mobile_attributes.tsv` [Dynamische zoekopdracht](dynamic-lookups.md). | int |
| **`mobileaction`** | Mobiele handeling. Automatisch verzameld bij `trackAction` wordt aangeroepen in mobiele implementaties. Hiermee kunt u in de app automatisch tekenen met handelingen. | varchar(100) |
| **`mobileappid`** | Mobiele toepassings-id. Hiermee slaat u de toepassingsnaam en -versie op in de volgende indeling: `[AppName] [BundleVersion]` | varchar(255) |
| **`mobileappperformanceappid`** | Wordt gebruikt in de Apteligent-gegevensconnector. De toepassings-id die in Apteligent wordt gebruikt. | varchar(255) |
| **`mobileappperformancecrashid`** | Wordt gebruikt in de Apteligent-gegevensconnector. De crash-id die in Apteligent wordt gebruikt. | varchar(255) |
| **`mobileappstoreobjectid`** | Gebruikt in de [!DNL Appfigures] gegevensaansluiting. Object-id van App store. | varchar(255) |
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
| **`mobiledeeplinkid`** | Verzameld op basis van de variabele contextgegevens `a.deeplink.id`. Wordt gebruikt in overnamerapporten als een identifier voor een koppeling naar een mobiele overname. | varchar(255) |
| **`mobiledevice`** | Naam van mobiel apparaat. In iOS wordt de notatie opgeslagen als een door komma&#39;s gescheiden tekenreeks van 2 cijfers. Het eerste getal vertegenwoordigt de apparaatgeneratie en het tweede getal vertegenwoordigt de apparaatfamilie. | varchar(255) |
| **`mobilehourofday`** | Definieert het uur van de dag waarop de app is gestart. Volg de numerieke notatie van 24 uur. | varchar(255) |
| **`mobileinstalldate`** | Datum mobiele installatie. Vermeldt de datum van de eerste keer dat een gebruiker de mobiele app opent. | varchar(255) |
| **`mobilelaunchnumber`** | Elke keer dat de mobiele app wordt gestart, neemt deze met één toe. | varchar(255) |
| **`mobilemessagebuttonname`** | Verzameld uit de variabele `a.message.button.id`van de contextgegevens. Wordt gebruikt voor in-app berichten om de knop te identificeren waarmee het bericht is gesloten. | varchar(100) |
| **`mobilemessageid`** | Bericht-id in de app | Varchar (255) |
| **`mobilemessageonline`** | In-app bericht online | varchar(255) |
| **`mobilemessagepushoptin`** | Verzameld op basis van de variabele contextgegevens `a.push.optin`. Stel dit in op &quot;true&quot; wanneer de gebruiker op Push Messaging klikt; anders is de waarde &quot;false&quot;. | varchar(255) |
| **`mobilemessagepushpayloadid`** | Verzameld op basis van de variabele contextgegevens `a.push.payloadid`. Gebruikt in duw overseinen als nuttige ladings herkenningsteken. | varchar(255) |
| **`mobileosversion`** | Versie van besturingssysteem voor mobiele services | varchar(255) |
| **`mobileplaceaccuracy`** | Verzameld op basis van de variabele contextgegevens `a.loc.acc`. Geeft de nauwkeurigheid van de GPS in meters aan op het moment van verzameling. | varchar(255) |
| **`mobileplacecategory`** | Verzameld op basis van de variabele contextgegevens `a.loc.category`. Beschrijft de categorie van een specifieke plaats. | varchar(255) |
| **`mobileplaceid`** | Verzameld op basis van de variabele contextgegevens `a.loc.id`. Identificatiecode voor een bepaald aandachtspunt. | varchar(255) |
| **`mobilepushoptin`** | Push-optie voor mobiele services | varchar(255) |
| **`mobilepushpayloadid`** | Mobiele services - Push-lading-id | varchar(255) |
| **`mobilerelaunchcampaigncontent`** | Inhoud voor mobiele services starten | varchar(255) |
| **`mobilerelaunchcampaignmedium`** | Mobiele services, startmedium | varchar(255) |
| **`mobilerelaunchcampaignsource`** | Bron voor mobiele services | varchar(255) |
| **`mobilerelaunchcampaignterm`** | Starten van mobiele services | varchar(255) |
| **`mobilerelaunchcampaigntrackingcode`** | Verzameld op basis van de variabele contextgegevens `a.launch.campaign.trackingcode`. Wordt gebruikt in aankopen als de code voor het bijhouden van de opstartiecampagne. | varchar(255) |
| **`mobileresolution`** | Resolutie van het mobiele apparaat. `[Width] x [Height]` in pixels. | varchar(255) |
| **`monthly_visitor`** | Een markering die bepaalt of de bezoeker uniek is voor de huidige maand. | tinyint zonder teken |
| **`mvvar1`** - `mvvar3` | [Variabele List](/help/implement/vars/page-vars/list.md) waarden. Bevat een lijst met gescheiden waarden, afhankelijk van de implementatie. De `post_mvvar1` - `post_mvvar3` kolommen vervangen door het originele scheidingsteken `--**--`. | text |
| **`mvvar1_instances`** - `mvvar3_instances` | De waarden van de lijstvariabele die op de huidige treffer werden geplaatst. Hiermee vervangt u het oorspronkelijke scheidingsteken door `--**--`. Heeft geen `post` kolom. | text |
| **`new_visit`** | Een vlag die bepaalt als de huidige slag een nieuw bezoek is. Wordt ingesteld door Adobe na 30 minuten inactiviteit van het bezoek. | tinyint zonder teken |
| **`os`** | Een numerieke id die het besturingssysteem van de bezoeker vertegenwoordigt. Op basis van de `user_agent` kolom. De sleutelwaarde voor `operating_system.tsv` standaardopzoekhandeling en `operating_system_type.tsv` [Dynamische zoekopdracht](dynamic-lookups.md). | int zonder teken |
| **`page_event`** | Het type hit dat wordt verzonden in de aanvraag voor de afbeelding (standaardhit, downloadkoppeling, aangepaste koppeling, afsluitkoppeling). Zie [Opzoeken van paginagebeurtenissen](datafeeds-page-event.md). | tinyint zonder teken |
| **`page_event_var1`** | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De URL van de downloadkoppeling, exit-koppeling of aangepaste koppeling waarop is geklikt. | text |
| **`page_event_var2`** | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De aangepaste naam (indien opgegeven) van de koppeling. Hiermee stelt u de [Aangepaste koppeling](/help/components/dimensions/custom-link.md), [Koppeling downloaden](/help/components/dimensions/download-link.md), of [Koppeling afsluiten](/help/components/dimensions/exit-link.md) afhankelijk van de waarde in `page_event`. | varchar(100) |
| **`page_type`** | De [dimensie Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) , die doorgaans wordt gebruikt voor 404 pagina&#39;s. | char (20) |
| **`page_url`** | De URL van de hit. Opmerking: deze `post_page_url` optie is gestript voor aanvragen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)) en gebruikt een gegevenstype varchar(255). | text |
| **`pagename`** | De [Pagina](/help/components/dimensions/page.md) dimensie. Als de [`pagename`](/help/implement/vars/page-vars/pagename.md) variabele is leeg, Analytics gebruikt `page_url` in plaats daarvan. | varchar(100) |
| **`pagename_no_url`** | Vergelijkbaar met `pagename`, behalve dat het niet terugvalt naar `page_url`. Alleen de `post` is beschikbaar. | varchar(100) |
| **`paid_search`** | Een vlag die bepaalt als de treffer betaalde onderzoeksopsporing aanpast. | tinyint zonder teken |
| **`persistent_cookie`** | Gebruikt in de [Permanente ondersteuning voor cookies](/help/components/dimensions/persistent-cookie-support.md) dimensie. Geeft aan of de bezoeker cookies ondersteunt die na elke hit niet worden verwijderd. | teken(1) |
| **`pointofinterest`** | Naam van interesepunt voor mobiele services | varchar(255) |
| **`pointofinterestdistance`** | Afstand van mobiele services tot belangencentrum | varchar(255) |
| **`post_`** kolommen | Bevat de waarde die uiteindelijk in rapporten wordt gebruikt. Elke postkolom wordt bevolkt na server-zijlogica, verwerkingsregels, en regels VISTA. Adobe raadt in de meeste gevallen aan postkolommen te gebruiken. | Zie de desbetreffende niet-postkolom |
| **`product_list`** | De [`products`](/help/implement/vars/page-vars/products.md) paginavariabele. Hiermee kunt u verschillende afmetingen en maatstaven vullen, waaronder [Categorie](/help/components/dimensions/category.md), [Product](/help/components/dimensions/product.md), [Eenheden](/help/components/metrics/units.md), en [Ontvangsten](/help/components/metrics/revenue.md). | text |
| **`prop1`** - `prop75` | Aangepaste verkeersvariabelen 1-75. Gebruikt in [Prop](/help/components/dimensions/prop.md) afmetingen. | varchar(100) |
| **`purchaseid`** | Unieke id voor een aankoop, zoals ingesteld met de [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) variabele. Wordt gebruikt door de `duplicate_purchase` kolom. | teken(20) |
| **`quarterly_visitor`** | Een vlag die bepaalt als de treffer een nieuwe driemaandelijkse bezoeker is. | tinyint zonder teken |
| **`ref_domain`** | De [Verwijzen naar domein](/help/components/dimensions/referring-domain.md) dimensie. Op basis van de `referrer` kolom. | varchar(100) |
| **`ref_type`** | Een numerieke id die het verwijzingstype voor de treffer vertegenwoordigt. Gebruikt in de [Type referentie](/help/components/dimensions/referrer-type.md) dimensie. <br>1: Binnen uw site<br>2: Andere websites <br>3: Zoekprogramma&#39;s <br>4: Harde schijf <br>5: GEBRUIKER <br>6: getypt/bladwijzer (geen referentie) <br>7: E-mail <br>8: Geen JavaScript <br>9: Sociale netwerken | tinyint zonder teken |
| **`referrer`** | De [Referenter](/help/components/dimensions/referrer.md) dimensie. Merk op dat wanneer `referrer` u een gegevenstype varchar gebruikt (255), `post_referrer` het gegevenstype varchar gebruikt (244). | Varchar (255) |
| **`resolution`** | Een numerieke id die de resolutie van de monitor aangeeft. Gebruikt in de [afmeting Monitorresolutie](/help/components/dimensions/monitor-resolution.md) . Gebruikt `resolution.tsv` een opzoektabel. | small int zonder teken |
| **`s_kwcid`** | Trefwoord-id die wordt gebruikt in Adobe Advertising-integraties. | Varchar (255) |
| **`s_resolution`** | Waarde voor raw-schermresolutie. Verzameld met de JavaScript-functie `screen.width x screen.height`. | char (20) |
| **`search_engine`** | Een numerieke id die de zoekmachine vertegenwoordigt die de bezoeker naar uw site heeft doorverwezen. Gebruikt in [Zoekmachine](/help/components/dimensions/search-engine.md) afmetingen. Verwijst naar de `search_engines.tsv` opzoektabel. | small int zonder teken |
| **`search_page_num`** | Wordt gebruikt door de [Alle zoekpaginanummers](/help/components/dimensions/all-search-page-rank.md) dimensie. Hiermee geeft u aan op welke pagina met zoekresultaten uw site is weergegeven voordat de gebruiker op uw site heeft geklikt. | small int zonder teken |
| **`secondary_hit`** | Een vlag die bepaalt als de slag een secundaire slag is. Deze markering is doorgaans afkomstig van taggen met meerdere suite- en VISTA-regels die treffers kopiëren. | tinyint zonder teken |
| **`sourceid`** | Source-id | int zonder teken |
| **`state`** | Staatvariabele. | Varchar(50) |
| **`stats_server`** | Niet van gebruik. Interne server van Adobe die de hit heeft verwerkt. | teken(30) |
| **`t_time_info`** | Lokale tijd voor de bezoeker. De indeling is: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| **`tnt`** | Wordt gebruikt in Adobe Target-integratie. Vertegenwoordigt alle tests momenteel gekwalificeerd voor. Indeling is: `TargetCampaignID:TargetRecipeID:TargetType\|Event/Action`. | text |
| **`tnt_action`** | Wordt gebruikt in Adobe Target-integratie. Geeft alle tests aan waarvoor de hit geschikt is. | text |
| **`tnt_instances`** | Wordt gebruikt in Adobe Target-integratie. Variabele voor doelinstanties. | text |
| **`transactionid`** | Een unieke id waarbij verschillende gegevenspunten later via gegevensbronnen kunnen worden geüpload. Verzameld met de [`transactionID`](/help/implement/vars/page-vars/transactionid.md) variabele. | text |
| **`truncated_hit`** | Een vlag die erop wijst dat het beeldverzoek werd beknot. Geeft aan dat een gedeeltelijke hit is ontvangen. <br>Y: Hit is afgekapt; gedeeltelijke hit ontvangen <br>N: Hit is niet afgekapt; full hit ontvangen | teken(1) |
| **`user_agent`** | De userAgent-tekenreeks die wordt verzonden in de HTTP-header van de afbeeldingsaanvraag. | text |
| **`user_hash`** | Niet gebruiken. Hash op de rapportsuite-id. Gebruiken `username` in plaats daarvan. | int zonder teken |
| **`user_server`** | Gebruikt in de [Server](/help/components/dimensions/server.md) dimensie. | varchar(100) |
| **`userid`** | Niet gebruiken. De numerieke id voor de rapportsuite-id. Gebruiken `username` in plaats daarvan. | int zonder teken |
| **`username`** | De rapportsuite-id voor de hit. | teken(40) |
| **`va_closer_detail`** | De [Laatste aanraakdetail](/help/components/dimensions/last-touch-detail.md) dimensie. | varchar(255) |
| **`va_closer_id`** | Een numerieke id die de [Laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md) dimensie. De zoekopdracht voor deze id vindt u in de Manager voor marketingkanalen. | tinyint zonder teken |
| **`va_finder_detail`** | De [Eerste aanraakdetail](/help/components/dimensions/first-touch-detail.md) dimensie. | varchar(255) |
| **`va_finder_id`** | Een numerieke id die de [Eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md) dimensie. De zoekopdracht voor deze id vindt u in de Manager voor marketingkanalen. | tinyint niet ondertekend |
| **`va_instance_event`** | Een vlag die instanties van het Marketingkanaal [identificeert](/help/components/metrics/instances.md). | tinyint niet ondertekend |
| **`va_new_engagement`** | Een vlag die nieuwe engagementen voor Marketing Channel [identificeert](/help/components/metrics/new-engagements.md). | tinyint zonder teken |
| **`video`** | Video-inhoud | varchar(255) |
| **`videoad`** | Naam videoadvertentie | Varchar (255) |
| **`videoadinpod`** | Videoadvertentie in podpositie | varchar(255) |
| **`videoadlength`** | Video en lengte | integer |
| **`videoadload`** | Video en laden | varchar(255) |
| **`videoadname`** | Video en naam | varchar(255) |
| **`videoadplayername`** | Naam van video en speler | varchar(255) |
| **`videoadpod`** | Video en pod | varchar(255) |
| **`videoadvertiser`** | Video-adverteerder | Varchar (255) |
| **`videoaudioalbum`** | Audioalbum video | Varchar (255) |
| **`videoaudioartist`** | Videoontwerper | varchar(255) |
| **`videoaudioauthor`** | Video audio-auteur | varchar(255) |
| **`videoaudiolabel`** | Video, audiolabel | varchar(255) |
| **`videoaudiopublisher`** | Video-uitgever | varchar(255) |
| **`videoaudiostation`** | Videoaudiostation | varchar(255) |
| **`videocampaign`** | Videocampagne | varchar(255) |
| **`videochannel`** | Videokanaal | varchar(255) |
| **`videochapter`** | Naam van videohoofdstuk | varchar(255) |
| **`videocontenttype`** | Type video-inhoud. Automatisch instellen op Video voor alle videoweergaven | varchar(255) |
| **`videodaypart`** | Dagdeel van video | varchar(255) |
| **`videoepisode`** | Video-aflevering | varchar(255) |
| **`videofeedtype`** | Type videofeed | varchar(255) |
| **`videogenre`** | Videogenre | text |
| **`videolength`** | Videolengte | integer |
| **`videomvpd`** | Video MVPD | varchar(255) |
| **`videoname`** | Videonaam | varchar(255) |
| **`videonetwork`** | Videonetwerk | varchar(255) |
| **`videopath`** | Videopad | varchar(100) |
| **`videoplayername`** | Naam videospeler | Varchar (255) |
| **`videotime`** | Videotijd | integer |
| **`videoqoebitrateaverageevar`** | Gemiddelde bitsnelheid videokwaliteit | varchar(255) |
| **`videoqoebitratechangecountevar`** | Aantal wijzigingen videokwaliteit | Varchar (255) |
| **`videoqoebuffercountevar`** | Aantal buffers van videokwaliteit | varchar(255) |
| **`videoqoebuffertimeevar`** | Buffertijd videokwaliteit | varchar(255) |
| **`videoqoedroppedframecountevar`** | Aantal gedropte frames videokwaliteit | varchar(255) |
| **`videoqoeerrorcountevar`** | Aantal fouten in videokwaliteit | varchar(255) |
| **`videoqoeextneralerrors`** | Externe fouten in videokwaliteit | text |
| **`videoqoeplayersdkerrors`** | SDK-fouten videokwaliteit | text |
| **`videoqoetimetostartevar`** | Begintijd voor videokwaliteit | Varchar (255) |
| **`videoseason`** | Videoseizoen | Varchar (255) |
| **`videosegment`** | Videosegment | varchar(255) |
| **`videoshow`** | Videoshow | varchar(255) |
| **`videoshowtype`** | Type video-presentatie | varchar(255) |
| **`videostreamtype`** | Type videostream | varchar(255) |
| **`visid_high`** | Gebruikt met `visid_low` om een bezoeker op unieke wijze te identificeren. | bigint zonder teken |
| **`visid_low`** | Gebruikt met `visid_high` om een bezoeker op unieke wijze te identificeren. | bigint niet ondertekend |
| **`visid_new`** | Een vlag die bepaalt of de hit een nieuw gegenereerde bezoekers-id bevat. | teken(1) |
| **`visid_timestamp`** | Als een bezoekersidentiteitskaart nieuw wordt geproduceerd, verstrekt timestamp in de tijd van UNIX® van toen bezoekersidentiteitskaart werd geproduceerd. | int |
| **`visid_type`** | Niet voor extern gebruik; intern gebruikt door Adobe voor verwerkingsoptimalisaties. Een numerieke id die staat voor de methode waarmee de bezoeker wordt geïdentificeerd.<br>`0`: Aangepaste bezoekers-ID of Onbekend/niet van toepassing<br>`1`: IP en gebruikersagent terugvaloptie <br>`2`: HTTP Mobile Subscriber Header <br>`3`: Verouderde cookiewaarde (`s_vi`) <br>`4`: Terugvalwaarde voor cookie (`s_fid`) <br>`5`: Identity Service | tinyint niet ondertekend |
| **`visit_keywords`** | De [dimensie van het zoekwoord](/help/components/dimensions/search-keyword.md) . In deze kolom wordt een niet-standaard tekenlimiet van varchar(244) gebruikt voor back-endlogica die door Adobe wordt gebruikt. | Varchar(244) |
| **`visit_num`** | De [Bezoek nummer](/help/components/dimensions/visit-number.md) dimensie. Begint bij 1, en verhoogt telkens als een nieuw bezoek per bezoeker begint. | int zonder teken |
| **`visit_page_num`** | De [Hoogte](/help/components/dimensions/hit-depth.md) dimensie. Verhoogt met 1 voor elke hit die de bezoeker genereert. Hiermee herstelt u elk bezoek. | int zonder teken |
| **`visit_ref_domain`** | Op basis van de `visit_referrer` kolom. Het eerste verwijzende domein van het bezoek. | varchar(100) |
| **`visit_ref_type`** | Een numerieke id die het referentietype van de eerste referentie van het bezoek vertegenwoordigt. Verwijst naar de `referrer_type.tsv` opzoektabel. | tinyint zonder teken |
| **`visit_referrer`** | De eerste referentie van het bezoek. | varchar(255) |
| **`visit_search_engine`** | Een numerieke id die de eerste zoekfunctie van het bezoek vertegenwoordigt. Verwijst naar de `search_engines.tsv` opzoektabel. | small int zonder teken |
| **`visit_start_page_url`** | De eerste URL van het bezoek. | varchar(255) |
| **`visit_start_pagename`** | De waarde Paginanaam in de eerste hit van het bezoek. | varchar(100) |
| **`visit_start_time_gmt`** | Tijdstempel (in UNIX®-tijd) van de eerste hit van het bezoek. | int |
| **`weekly_visitor`** | Een vlag die bepaalt als de slag een nieuwe wekelijkse bezoeker is. | tinyint zonder teken |
| **`yearly_visitor`** | Een vlag die bepaalt als de klap een nieuwe jaarlijkse bezoeker is. | tinyint zonder teken |
| **`zip`** | Hiermee kunt u de [Postcode](/help/components/dimensions/zip-code.md) dimensie. Zie ook `geo_zip`. | varchar(50) |

{style="table-layout:auto"}

## Ongebruikte of gepensioneerde kolommen

De volgende lijst met kolommen wordt niet gebruikt en bevat doorgaans geen gegevens. Kolommen die wel gegevens bevatten, worden niet ondersteund door de huidige bibliotheken voor gegevensverzameling en zijn niet beschikbaar in Analysis Workspace.

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
