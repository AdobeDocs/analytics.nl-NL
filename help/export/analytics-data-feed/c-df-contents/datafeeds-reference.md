---
description: Tabelgegevens die de kolommen in de gegevensinvoer beschrijven.
keywords: Gegevensfeed;kolommen
subtopic: data feeds
title: Referentie gegevenskolom
feature: Reports & Analytics Basics
uuid: 9042a274-7124-4323-8cd6-5c84ab3eef6d
exl-id: e1492147-6e7f-4921-b509-898e7efda596
source-git-commit: 20a4ee51d0eace9cdcb5e0aeff5704b9a757a1eb
workflow-type: tm+mt
source-wordcount: '3432'
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
>De meeste kolommen bevatten een vergelijkbare kolom met een voorvoegsel van `post_`. Post kolommen bevatten waarden na server-zijlogica, verwerkingsregels, en regels VISTA. Adobe raadt in de meeste gevallen aan postkolommen te gebruiken. Zie [Veelgestelde vragen over gegevensfeeds](../df-faq.md) voor meer informatie .

| Kolomnaam | Kolombeschrijving | Gegevenstype |
| --- | --- | --- |
| `accept_language` | Hiermee worden alle geaccepteerde talen weergegeven, zoals wordt aangegeven in de HTTP-header Accept-Language in een afbeeldingsaanvraag. | teken(20) |
| `aemassetid` | Een variabele met meerdere waarden die overeenkomt met de elementen van de id&#39;s (GUID) van een set Adobe Experience Manager-elementen. Incrementele indrukgebeurtenissen. | text |
| `aemassetsource` | Identificeert de bron van de gebeurtenis asset. Wordt gebruikt in Adobe Experience Manager. | varchar(255) |
| `aemclickedassetid` | Element-id van een Adobe Experience Manager-element. De verhogingen klikken Gebeurtenissen. | varchar(255) |
| `browser` | Numerieke id van de browser. Verwijst naar de `browser.tsv` opzoektabel. | int zonder teken |
| `browser_height` | Hoogte in pixels van het browservenster. | small int zonder teken |
| `browser_width` | Breedte in pixels van het browservenster. | small int zonder teken |
| `c_color` | Bitdiepte van het kleurenpalet. Wordt gebruikt als onderdeel van de berekening van de [Kleurdiepte](/help/components/dimensions/color-depth.md) dimensie. AppMeasurement gebruikt de JavaScript-functie `screen.colorDepth()`. | teken(20) |
| `campaign` | Variabele gebruikt in de [Trackingcode](/help/components/dimensions/tracking-code.md) dimensie. | varchar(255) |
| `carrier` | Adobe Advertising Cloud-integratievariabele. Geeft de mobiele drager aan. Verwijst naar de `carrier` opzoektabel. | varchar(100) |
| `channel` | Variabele gebruikt in de [Site-secties](/help/components/dimensions/site-section.md) dimensie. | varchar(100) |
| `click_action` | Niet meer gebruikt. Adres van verbonden klikte in het hulpmiddel van de erfenisKaart. | varchar(100) |
| `click_action_type` | Niet meer gebruikt. Het type van verbinding van het erfenis hulpmiddel Clickmap.<br>0: HREF-URL<br>1: Aangepaste id<br>2: JavaScript-gebeurtenis onClick<br>3: Formulierelement | tinyint zonder teken |
| `click_context` | Niet meer gebruikt. De paginanaam waar de verbinding voorkwam. Deel van het oude Clickmap-gereedschap. | varchar(255) |
| `click_context_type` | Niet meer gebruikt. Geeft aan of click_context een paginanaam heeft of standaard de pagina-URL heeft.<br>0: Pagina-URL<br>1: Paginanaam | tinyint zonder teken |
| `click_sourceid` | Niet meer gebruikt. Numerieke id voor de locatie op de pagina van de aangeklikte koppeling. Deel van het oude Clickmap-gereedschap. | int zonder teken |
| `click_tag` | Niet meer gebruikt. Type HTML-element waarop is geklikt. | teken(10) |
| `clickmaplink` | Koppeling naar Activity Map | varchar(255) |
| `clickmaplinkbyregion` | Activity Map per regio | varchar(255) |
| `clickmappage` | Activity Map pagina | varchar(255) |
| `clickmapregion` | Activity Map | varchar(255) |
| `code_ver` | AppMeturement Library-versie die wordt gebruikt om de afbeeldingsaanvraag te compileren en te verzenden. | teken(16) |
| `color` | Kleurdiepte-id op basis van de waarde van de `c_color` kolom. Verwijst naar de `color_depth.tsv` opzoektabel. | small int zonder teken |
| `connection_type` | Numerieke id die het verbindingstype vertegenwoordigt. Variabele gebruikt in de [Verbindingstype](/help/components/dimensions/connection-type.md) dimensie. Verwijst naar de `connection_type.tsv` opzoektabel. | tinyint zonder teken |
| `cookies` | Variabele gebruikt in de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) dimensie.<br>Y: Ingeschakeld<br>N: Uitgeschakeld<br>U: Onbekend | teken(1) |
| `country` | Numerieke id die de waarden vertegenwoordigt die worden gevonden in het dialoogvenster `country.tsv` opzoeken. Gebruikt in het Hoogste niveaudomeinen rapporteren in Rapporten &amp; Analytics. | small int zonder teken |
| `ct_connect_type` | Met betrekking tot de `connection_type` kolom. De meest voorkomende waarden zijn LAN/Wifi, Mobile Carrier en Modem. | teken(20) |
| `curr_factor` | Bepaalt de decimale valutapositie en wordt gebruikt voor valutaomrekening. In USD worden bijvoorbeeld twee decimalen gebruikt, zodat deze kolomwaarde 2 is. | tinyint |
| `curr_rate` | De wisselkoers op het tijdstip van de transactie. Adobe werkt samen met XE om de wisselkoers van de huidige dag te bepalen. | decimaal (24,12) |
| `currency` | De valutacode die tijdens de transactie werd gebruikt. | teken(8) |
| `cust_hit_time_gmt` | Alleen voor tijdstempels geschikte rapportsuites. De tijdstempel die met de hit wordt verzonden, uitgedrukt in Unix-tijd. | int |
| `cust_visid` | Als een aangepaste bezoeker-id is ingesteld, wordt deze in deze kolom ingevuld. | varchar(255) |
| `daily_visitor` | Markering om te bepalen of de treffer een nieuwe dagelijkse bezoeker is. | tinyint zonder teken |
| `date_time` | De tijd van de treffer in leesbare formaat, die op de tijdzone van de rapportreeks wordt gebaseerd. | datetime |
| `domain` | Variabele gebruikt in de [Domein](/help/components/dimensions/domain.md) dimensie. Gebaseerd op het internettoegangspunt van de bezoeker. | varchar(100) |
| `duplicate_events` | Vermeldt elke gebeurtenis die als een duplicaat is geteld. | varchar(255) |
| `duplicate_purchase` | Markering die aangeeft dat de aankoopgebeurtenis voor deze hit moet worden genegeerd omdat deze een duplicaat is. | tinyint zonder teken |
| `duplicated_from` | Wordt alleen gebruikt in rapportsuites die de VISTA-regels voor raakkopieën bevatten. Geeft aan uit welke rapportsuite de treffer is gekopieerd. | varchar(40) |
| `ef_id` | De `ef_id` gebruikt in Adobe Advertising Cloud-integraties. | varchar(255) |
| `evar1 - evar250` | Aangepaste variabelen 1-250. Gebruikt in [eVar](/help/components/dimensions/evar.md) afmetingen. Elke organisatie gebruikt eVars anders. De beste plaats voor meer informatie over hoe uw organisatie respectieve eVars bevolkt zou een document van het oplossingsontwerp specifiek voor uw organisatie zijn. | varchar(255) |
| `event_list` | Door komma&#39;s gescheiden lijst met numerieke id&#39;s die gebeurtenissen vertegenwoordigen die tijdens de hit worden geactiveerd. Bevat zowel standaardgebeurtenissen als aangepaste gebeurtenissen 1-1000. Gebruiksmiddelen `event.tsv` opzoeken. | text |
| `exclude_hit` | Markering die aangeeft dat de treffer van rapportage is uitgesloten. De `visit_num` wordt niet verhoogd voor uitgesloten treffers.<br>1: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>2: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>3: Niet meer gebruikt. Uitsluiting van gebruikersagent<br>4: Uitsluiting op basis van IP-adres<br>5: Ontbrekende informatie over digitale raakgeluiden, zoals `page_url`, `pagename`, `page_event`, of `event_list`<br>6: JavaScript heeft hit bij proces niet correct verwerkt<br>7: Accountspecifieke uitsluiting, zoals in een VISTA-regeling<br>8: Niet gebruikt. Alternatieve accountspecifieke uitsluiting.<br>9: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>10: Ongeldige valutacode<br>11: Druk op het ontbreken van een tijdstempel in een rapportsuite met alleen een tijdstempel of op een hit die een tijdstempel bevat in een rapportsuite zonder een tijdstempel<br>12: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>13: Niet gebruikt. Onderdeel van een gesloopt onderdeel.<br>14: Doeltreffer die niet overeenkomt met een treffer voor Analytics<br>15: Momenteel niet gebruikt.<br>16: Advertising Cloud-hit die niet overeenkomt met een Analytics-hit | tinyint zonder teken |
| `first_hit_page_url` | De allereerste URL van de bezoeker. | varchar(255) |
| `first_hit_pagename` | Variabele gebruikt in de [Invoerpagina origineel](/help/components/dimensions/entry-dimensions.md) dimensie. De oorspronkelijke naam van de ingangspagina van de bezoeker. | varchar(100) |
| `first_hit_ref_domain` | Variabele gebruikt in de [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md) dimensie. Gebaseerd op `first_hit_referrer`. Het allereerste verwijzende domein van de bezoeker. | varchar(100) |
| `first_hit_ref_type` | Numerieke id die het referentietype van de allereerste referentie van de bezoeker vertegenwoordigt. Gebruiksmiddelen `referrer_type.tsv` opzoeken. | tinyint zonder teken |
| `first_hit_referrer` | De allereerste verwijzende URL van de bezoeker. | varchar(255) |
| `first_hit_time_gmt` | Tijdstempel van de allereerste hit van de bezoeker in Unix-tijd. | int |
| `geo_city` | De naam van de stad waar de hit vandaan kwam, op basis van IP. Gebruikt in de [Plaatsen](/help/components/dimensions/cities.md) dimensie. | teken(32) |
| `geo_country` | Afkorting van het land waar de treffer vandaan kwam, gebaseerd op IP. Gebruikt in de [Landen](/help/components/dimensions/countries.md) dimensie. | teken(4) |
| `geo_dma` | Numerieke id van het demografische gebied waar de hit vandaan komt, gebaseerd op IP. Gebruikt in de [US DMA](/help/components/dimensions/us-dma.md) dimensie. | int zonder teken |
| `geo_region` | De naam van de staat of regio waar de treffer vandaan kwam, op basis van IP. Gebruikt in de [Regio&#39;s](/help/components/dimensions/regions.md) dimensie. | teken(32) |
| `geo_zip` | De postcode waar de hit vandaan kwam, gebaseerd op IP. Hiermee kunt u de [Postcode](/help/components/dimensions/zip-code.md) dimensie. Zie ook `zip`. | varchar(16) |
| `hier1 - hier5` | Wordt gebruikt door hiërarchievariabelen. Bevat een lijst met gescheiden waarden. Het scheidingsteken wordt gekozen onder de instellingen van de rapportsuite. | varchar(255) |
| `hit_source` | Geeft aan uit welke bron de treffer afkomstig is. De bronnen 1, 2 en 6 van de it worden gefactureerd. <br>1: Standaardverzoek om afbeelding zonder tijdstempel <br>2: Standaardverzoek om afbeelding met tijdstempel <br>3: Live uploaden van gegevensbron met tijdstempels <br>4: Niet gebruikt <br>5: Generieke gegevensbron uploaden <br>6: Uploaden gegevensbron volledige verwerking <br>7: TransactieID-gegevensbron uploaden <br>8: niet meer gebruikt; Eerdere versies van Adobe Advertising Cloud-gegevensbronnen <br>9: niet meer gebruikt; Samenvattingscijfers voor Adobe Social <br>10: Audience Manager server-kant gebruikt door:sturen | tinyint zonder teken |
| `hit_time_gmt` | De timestamp van de de gegevensverzamelingsservers van de hit Adobe ontvingen de slag, die in Unix tijd wordt gebaseerd. | int |
| `hitid_high` | Wordt gebruikt in combinatie met `hitid_low` om een treffer te identificeren. | bigint zonder teken |
| `hitid_low` | Wordt gebruikt in combinatie met `hitid_high` om een treffer te identificeren. | bigint zonder teken |
| `homepage` | Niet meer gebruikt. Geeft aan of de huidige URL de homepage van de browser is. | teken(1) |
| `hourly_visitor` | Markering om te bepalen of de treffer een nieuwe uurbezoeker is. | tinyint zonder teken |
| `ip` | IP Adres, dat op de kopbal van HTTP van het beeldverzoek wordt gebaseerd. | teken(20) |
| `ip2` | Niet gebruikt. De verwijzingsvariabele van de steun voor rapportreeksen die regels bevatten VISTA die op IP adres worden gebaseerd. | teken(20) |
| `j_jscript` | Versie van JavaScript wordt ondersteund door de browser. | teken(5) |
| `java_enabled` | Markering die aangeeft of Java is ingeschakeld. <br>Y: Ingeschakeld <br>N: Uitgeschakeld <br>U: Onbekend | teken(1) |
| `javascript` | Opzoeken-id van JavaScript-versie, gebaseerd op `j_jscript`. Gebruikt opzoektabel. | tinyint zonder teken |
| `language` | Numerieke id van taal. Gebruiksmiddelen `languages.tsv` opzoektabel. | small int zonder teken |
| `last_hit_time_gmt` | Tijdstempel (in Unix-tijd) van de voorgaande hit. Wordt gebruikt om de [Dagen sinds laatste bezoek](/help/components/dimensions/days-since-last-visit.md) dimensie. | int |
| `last_purchase_num` | Variabele gebruikt in de [Klantenloyaliteit](/help/components/dimensions/customer-loyalty.md) dimensie. Het aantal eerdere aankopen dat de bezoeker heeft gedaan. <br>0: Geen eerdere aankopen (geen klant) <br>1: 1 eerdere aankoop (nieuwe klant) <br>2: 2 eerdere aankopen (retourklant) <br>3: 3 of meer eerdere aankopen (loyale klant) | int zonder teken |
| `last_purchase_time_gmt` | Gebruikt in de [Dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md) dimensie. Tijdstempel (in Unix-tijd) van de laatste aanschaf. Voor eerste aankopen en bezoekers die nog niet eerder een aankoop hebben gedaan, is deze waarde `0`. | int |
| `latlon1` | Locatie (tot 10 km) | varchar(255) |
| `latlon23` | Locatie (tot 100 m) | varchar(255) |
| `latlon45` | Locatie (tot 1 m) | varchar(255) |
| `mc_audiences` | Lijst met Audience Manager segment-id&#39;s waartoe de bezoeker behoort. | text |
| `mcvisid` | Experience Cloud-bezoeker-id. 128-bits getal dat bestaat uit twee samengevoegde 64-bits getallen opgevuld tot 19 cijfers. | varchar(255) |
| `mobile_id` | Als de gebruiker een mobiel apparaat gebruikt, is dit de numerieke id van het apparaat. | int |
| `mobileaction` | Mobiele handeling. Automatisch verzameld bij `trackAction` wordt opgeroepen in Mobiele services. Hiermee kunt u in de app automatisch tekenen met handelingen. | varchar(100) |
| `mobileappid` | Mobiele toepassings-id. Hiermee slaat u de toepassingsnaam en -versie op in de volgende indeling: `[AppName] [BundleVersion]` | varchar(255) |
| `mobileappperformanceappid` | Wordt gebruikt in de Apteligent-gegevensconnector. De toepassings-id die in Apteligent wordt gebruikt. | varchar(255) |
| `mobileappperformancecrashid` | Wordt gebruikt in de Apteligent-gegevensconnector. De crash-id die in Apteligent wordt gebruikt. | varchar(255) |
| `mobileappstoreobjectid` | Wordt gebruikt in de gegevensaansluiting AppFigures. Object-id van App store. | varchar(255) |
| `mobilebeaconmajor` | Belangrijkste baken voor mobiele services | varchar(100) |
| `mobilebeaconminor` | Kleine beperking van het baken voor mobiele services | varchar(100) |
| `mobilebeaconproximity` | Bandennabijheid mobiele services | varchar(255) |
| `mobilebeaconuuid` | Mobile Services-baken UUID | varchar(100) |
| `mobilecampaigncontent` | De naam of id van de inhoud die de koppeling heeft weergegeven. Bevolkt door Mobile App Acquisition. | varchar(255) |
| `mobilecampaignmedium` | Marketing medium, zoals banner of e-mail. Bevolkt door Mobile App Acquisition. | varchar(255) |
| `mobilecampaignname` | Naam van de campagne, die ook in de campagnevariabele wordt opgeslagen. Bevolkt door Mobile App Acquisition. | varchar(255) |
| `mobilecampaignsource` | Originele referentie, zoals nieuwsbrief of sociaal medianetwerk. Bevolkt door Mobile App Acquisition. | varchar(255) |
| `mobilecampaignterm` | Betaalde trefwoorden of andere termen die u met deze overname wilt bijhouden. Bevolkt door Mobile App Acquisition. | varchar(255) |
| `mobiledayofweek` | Het nummer van de weekdag waarop de app is gestart. | varchar(255) |
| `mobiledayssincefirstuse` | Aantal dagen sinds de app voor de eerste keer is uitgevoerd. | varchar(255) |
| `mobiledayssincelastupgrade` | Verzameld van de variabele van contextgegevens a.DaysSinceLastUpgrade. Het aantal dagen dat is verstreken sinds de vorige sessie. | varchar(255) |
| `mobiledayssincelastuse` | Aantal dagen sinds de app voor de laatste keer is uitgevoerd. | varchar(255) |
| `mobiledeeplinkid` | Verzameld op basis van de variabele contextgegevens `a.deeplink.id`. Wordt gebruikt in overnamerapporten als een identifier voor een koppeling naar een mobiele overname. | varchar(255) |
| `mobiledevice` | Naam van mobiel apparaat. In iOS wordt de notatie opgeslagen als een door komma&#39;s gescheiden tekenreeks van 2 cijfers. Het eerste getal vertegenwoordigt de apparaatgeneratie en het tweede getal vertegenwoordigt de apparaatfamilie. | varchar(255) |
| `mobilehourofday` | Definieert het uur van de dag waarop de app is gestart. Volg de numerieke notatie van 24 uur. | varchar(255) |
| `mobileinstalldate` | Datum mobiele installatie. Verstrekt de datum van de eerste keer een gebruiker de mobiele app opent. | varchar(255) |
| `mobilelaunchessincelastupgrade` | Verzameld van de variabele van contextgegevens a.LaunchesSinceUpgrade. Meldt het aantal keren dat de installatie is gestart sinds de laatste upgrade. | varchar(255) |
| `mobilelaunchnumber` | Elke keer dat de mobiele app wordt gestart, neemt deze met één toe. | varchar(255) |
| `mobileltv` | Niet meer gebruikt. Bevolkt door trackLifetimeValue-methoden. | varchar(255) |
| `mobilemessagebuttonname` | Verzameld op basis van de variabele contextgegevens `a.message.button.id`. Wordt gebruikt voor in-app berichten om de knop te identificeren waarmee het bericht is gesloten. | varchar(100) |
| `mobilemessageid` | Berichtings-id in de app | varchar(255) |
| `mobilemessageonline` | Bericht online in de app | varchar(255) |
| `mobilemessagepushoptin` | Verzameld op basis van de variabele contextgegevens `a.push.optin`. Stel dit in op &quot;true&quot; wanneer de gebruiker het verzenden via pushberichten inschakelt. anders is de waarde &quot;false&quot;. | varchar(255) |
| `mobilemessagepushpayloadid` | Verzameld op basis van de variabele contextgegevens `a.push.payloadid`. Gebruikt in duw overseinen als nuttige ladings herkenningsteken. | varchar(255) |
| `mobileosenvironment` | Verzameld op basis van de variabele contextgegevens `a.OSEnvironment`. Frames in de OS-omgeving, zoals Android of iOS. | varchar(255) |
| `mobileosversion` | Versie van besturingssysteem voor mobiele services | varchar(255) |
| `mobileplaceaccuracy` | Verzameld op basis van de variabele contextgegevens `a.loc.acc`. Geeft de nauwkeurigheid van de GPS in meters aan op het moment van verzameling. | varchar(255) |
| `mobileplacecategory` | Verzameld op basis van de variabele contextgegevens `a.loc.category`. Beschrijft de categorie van een specifieke plaats. | varchar(255) |
| `mobileplaceid` | Verzameld op basis van de variabele contextgegevens `a.loc.id`. Identificatiecode voor een bepaald aandachtspunt. | varchar(255) |
| `mobilerelaunchcampaigncontent` | Inhoud voor mobiele services starten | varchar(255) |
| `mobilerelaunchcampaignmedium` | Mobiele services, startmedium | varchar(255) |
| `mobilerelaunchcampaignsource` | Bron voor mobiele services | varchar(255) |
| `mobilerelaunchcampaignterm` | Starten van mobiele services | varchar(255) |
| `mobilerelaunchcampaigntrackingcode` | Verzameld op basis van de variabele contextgegevens `a.launch.campaign.trackingcode`. Wordt gebruikt in aankopen als de code voor het bijhouden van de opstartiecampagne. | varchar(255) |
| `mobileresolution` | Resolutie van het mobiele apparaat. `[Width] x [Height]` in pixels. | varchar(255) |
| `monthly_visitor` | Markering die aangeeft dat de bezoeker uniek is voor de huidige maand. | tinyint zonder teken |
| `mvvar1` - `mvvar3` | Variabele waarden weergeven. Bevat een lijst met gescheiden waarden, afhankelijk van de implementatie. | text |
| `namespace` | Niet gebruikt. Onderdeel van een gesloopt onderdeel. | varchar(50) |
| `new_visit` | Markering die bepaalt of de huidige treffer een nieuw bezoek is. Wordt ingesteld door Adobe-servers na 30 minuten inactiviteit van het bezoek. | tinyint zonder teken |
| `os` | Numerieke id die het besturingssysteem van de bezoeker vertegenwoordigt. Op basis van de `user_agent` kolom. Gebruiksmiddelen `os` opzoeken. | int zonder teken |
| `p_plugins` | Niet meer gebruikt. Lijst met plug-ins die beschikbaar zijn voor de browser. De JavaScript-functie gebruiken `navigator.plugins()`. | text |
| `page_event` | Het type hit dat wordt verzonden in de aanvraag voor de afbeelding (standaardhit, downloadkoppeling, aangepaste koppeling, afsluitkoppeling). Zie [Opzoeken van paginagebeurtenissen](datafeeds-page-event.md). | tinyint zonder teken |
| `page_event_var1` | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De URL van de downloadkoppeling, exit-koppeling of aangepaste koppeling waarop is geklikt. | text |
| `page_event_var2` | Wordt alleen gebruikt in aanvragen voor het bijhouden van koppelingen. De aangepaste naam (indien opgegeven) van de koppeling. | varchar(100) |
| `page_event_var3` | Niet meer gebruikt. Bevat gegevens van de module Enquête en Media. Bevolkt oudere videoverslagen in vorige versies van Adobe Analytics. | text |
| `page_type` | Wordt gebruikt om de [Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) dimensie. Wordt uitsluitend gebruikt voor 404 pagina&#39;s. Deze variabele moet leeg zijn of de waarde bevatten `ErrorPage`. | teken(20) |
| `page_url` | De URL van de hit. Let op: `post_page_url` wordt gestript voor het volgen van verbinding beeldverzoeken en gebruikt een gegevenstype van varchar (255). | text |
| `pagename` | Wordt gebruikt om de [Pagina](/help/components/dimensions/page.md) dimensie. Als de [`pagename`](/help/implement/vars/page-vars/pagename.md) variabele is leeg, Analytics gebruikt `page_url` in plaats daarvan. | varchar(100) |
| `paid_search` | Markering die wordt ingesteld als de treffer overeenkomt met de detectie van betaalde zoekopdrachten. | tinyint zonder teken |
| `partner_plugins` | Niet gebruikt. Onderdeel van een gesloopt onderdeel. | varchar(255) |
| `persistent_cookie` | Gebruikt in de [Permanente ondersteuning voor cookies](/help/components/dimensions/persistent-cookie-support.md) dimensie. Geeft aan of de bezoeker cookies ondersteunt die na elke hit niet worden verwijderd. | teken(1) |
| `plugins` | Niet meer gebruikt. Lijst met numerieke id&#39;s die overeenkomen met plug-ins die beschikbaar zijn in de browser. Gebruiksmiddelen `plugins.tsv` opzoeken. | varchar(180) |
| `pointofinterest` | Naam van interesepunt voor mobiele services | varchar(255) |
| `pointofinterestdistance` | Afstand van mobiele services tot belangencentrum | varchar(255) |
| `post_` kolommen | Bevat de waarde die uiteindelijk in rapporten wordt gebruikt. Elke postkolom wordt bevolkt na server-zijlogica, verwerkingsregels, en regels VISTA. Adobe raadt in de meeste gevallen aan postkolommen te gebruiken. | Zie de desbetreffende niet-postkolom |
| `prev_page` | Niet gebruikt. Door Adobe aan eigendomsrechten gebonden id van de vorige pagina. | int zonder teken |
| `product_list` | Productlijst zoals doorgegeven via de [`products`](/help/implement/vars/page-vars/products.md) variabele. Producten worden gescheiden door komma&#39;s, terwijl afzonderlijke producteigenschappen worden gescheiden door puntkomma&#39;s. | text |
| `product_merchandising` | Niet gebruikt. Gebruiken `product_list` in plaats daarvan. | text |
| `prop1` - `prop75` | Aangepaste verkeersvariabelen 1-75. Gebruikt in [Prop](/help/components/dimensions/prop.md) afmetingen. | varchar(100) |
| `purchaseid` | Unieke id voor een aankoop, zoals ingesteld met de [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) variabele. Wordt gebruikt door de `duplicate_purchase` kolom. | teken(20) |
| `quarterly_visitor` | Markering om te bepalen of de treffer een nieuwe kwartaalbezoeker is. | tinyint zonder teken |
| `ref_domain` | Gebaseerd op de verwijzende kolom. Het verwijzende domein van de treffer. Gebruikt in de [Verwijzen naar domein](/help/components/dimensions/referring-domain.md) dimensie. | varchar(100) |
| `ref_type` | Een numerieke id die het verwijzingstype voor de treffer vertegenwoordigt. Gebruikt in de [Type referentie](/help/components/dimensions/referrer-type.md) dimensie. <br>1: Binnen uw site<br>2: Andere websites <br>3: Zoekprogramma&#39;s <br>4: Vaste schijf <br>5: GEBRUIKER <br>6: Typed/Bookmark (geen referentie) <br>7: E-mail <br>8: Geen JavaScript <br>9: Sociale netwerken | tinyint zonder teken |
| `referrer` | Pagina-URL van de vorige pagina. Gebruikt in de [Referenter](/help/components/dimensions/referrer.md) dimensie. Let op: `referrer` gebruikt een gegevenstype van varchar(255); `post_referrer` gebruikt een gegevenstype van varchar (244). | varchar(255) |
| `resolution` | Numerieke id die de resolutie van de monitor vertegenwoordigt. Gebruikt in de [Monitorresolutie](/help/components/dimensions/monitor-resolution.md) dimensie. Gebruiksmiddelen `resolution.tsv` opzoektabel. | small int zonder teken |
| `s_kwcid` | Trefwoord-id gebruikt in Adobe Advertising Cloud-integratie. | varchar(255) |
| `s_resolution` | Waarde van resolutie voor onbewerkt scherm. Opgenomen met de JavaScript-functie `screen.width x screen.height`. | teken(20) |
| `search_engine` | Numerieke id die staat voor de zoekengine die de bezoeker naar uw site heeft doorverwezen. Gebruiksmiddelen `search_engines.tsv` opzoeken. | small int zonder teken |
| `search_page_num` | Wordt gebruikt door de [Alle zoekpaginanummers](/help/components/dimensions/all-search-page-rank.md) dimensie. Hiermee geeft u aan op welke pagina met zoekresultaten uw site is weergegeven voordat de gebruiker op uw site heeft geklikt. | small int zonder teken |
| `secondary_hit` | Markering die secundaire treffers volgt. Doorgaans zijn deze regels afkomstig van taggen met meerdere suite en VISTA-regels die treffers kopiëren. | tinyint zonder teken |
| `service` | Niet gebruikt. Gebruiken `page_event` in plaats daarvan. | teken(2) |
| `socialaccountandappids` | Niet meer gebruikt. Sociale account en toepassings-id&#39;s | varchar(255) |
| `socialassettrackingcode` | Niet meer gebruikt. Variabele voor sociale campagne | varchar(255) |
| `socialauthor` | Niet meer gebruikt. Variabele voor sociale auteurs | varchar(255) |
| `socialcontentprovider` | Niet meer gebruikt. Sociale Platforms/eigenschappen | varchar(255) |
| `socialinteractiontype` | Niet meer gebruikt. Type sociale interactie | varchar(255) |
| `sociallanguage` | Niet meer gebruikt. Sociale taal | varchar(255) |
| `sociallatlong` | Niet meer gebruikt. Sociale breedtegraad/lengtegraad | varchar(255) |
| `socialowneddefinitioninsighttype` | Niet meer gebruikt. Type inzicht in sociale definitie | varchar(255) |
| `socialowneddefinitioninsightvalue` | Niet meer gebruikt. Waarde van inzicht in sociale definitie | varchar(255) |
| `socialowneddefinitionmetric` | Niet meer gebruikt. Metrisch met definitie van sociale aard | varchar(255) |
| `socialowneddefinitionpropertyvspost` | Niet meer gebruikt. Eigendom van sociale definitie versus post | varchar(255) |
| `socialownedpostids` | Niet meer gebruikt. ID&#39;s van sociale post | varchar(255) |
| `socialownedpropertyid` | Niet meer gebruikt. ID sociale eigendom | varchar(255) |
| `socialownedpropertyname` | Niet meer gebruikt. Naam van sociale eigendom | varchar(255) |
| `socialownedpropertypropertyvsapp` | Niet meer gebruikt. Eigendom van sociale media versus app | varchar(255) |
| `state` | Staatvariabele. | varchar(50) |
| `stats_server` | Niet gebruiken. Adobe interne server die de hit heeft verwerkt. | teken(30) |
| `t_time_info` | Lokale tijd voor de bezoeker. Indeling is: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| `tnt` | Wordt gebruikt in Adobe Target-integratie. Vertegenwoordigt alle tests momenteel gekwalificeerd voor. Indeling is: `TargetCampaignID:TargetRecipeID:TargetType|Event/Action`. | text |
| `tnt_action` | Wordt gebruikt in Adobe Target-integratie. Geeft alle tests aan waarvoor de hit geschikt is. | text |
| `tnt_post_vista` | Niet meer gebruikt. Gebruiken `post_tnt` in plaats daarvan. | text |
| `transactionid` | Een unieke id waarbij verschillende gegevenspunten later via gegevensbronnen kunnen worden geüpload. Verzameld met de [`transactionID`](/help/implement/vars/page-vars/transactionid.md) variabele. | text |
| `truncated_hit` | Een markering die aangeeft dat de afbeeldingsaanvraag is afgebroken. Geeft aan dat een gedeeltelijke hit is ontvangen. <br>Y: Hit was afgekapt; gedeeltelijke treffer ontvangen <br>N: Hit is niet afgekapt; volledige hit ontvangen | teken(1) |
| `ua_color` | Niet meer gebruikt. Eerder gebruikt als fallback voor kleurdiepte. | teken(20) |
| `ua_os` | Niet meer gebruikt. Voorheen gebruikt als fallback voor besturingssysteem. | teken(80) |
| `ua_pixels` | Niet meer gebruikt. Vroeger gebruikt als fallback voor browserhoogte en -breedte. | teken(20) |
| `user_agent` | user agent string sent in the HTTP header of the image request. | text |
| `user_hash` | Niet gebruiken. Hash op de rapportsuite-id. Gebruiken `username` in plaats daarvan. | int zonder teken |
| `user_server` | Gebruikt in de [Server](/help/components/dimensions/server.md) dimensie. | varchar(100) |
| `userid` | Niet gebruiken. De numerieke id voor de rapportsuite-id. Gebruiken `username` in plaats daarvan. | int zonder teken |
| `username` | De rapportsuite-id voor de hit. | teken(40) |
| `va_closer_detail` | Variabele gebruikt in de [Laatste aanraakdetail](/help/components/dimensions/last-touch-detail.md) dimensie. | varchar(255) |
| `va_closer_id` | Numerieke id die de [Laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md) dimensie. U kunt deze id opzoeken in de Manager voor marketingkanalen. | tinyint zonder teken |
| `va_finder_detail` | Variabele gebruikt in de [Eerste aanraakdetail](/help/components/dimensions/first-touch-detail.md) dimensie. | varchar(255) |
| `va_finder_id` | Numerieke id die de [Eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md) dimensie. U kunt deze id opzoeken in de Manager voor marketingkanalen. | tinyint zonder teken |
| `va_instance_event` | Markering om marketingkanaal te identificeren [Instanties](/help/components/metrics/instances.md). | tinyint zonder teken |
| `va_new_engagement` | Markering om marketingkanaal te identificeren [Nieuwe contracten](/help/components/metrics/new-engagements.md). | tinyint zonder teken |
| `video` | Video-inhoud | varchar(255) |
| `videoad` | Video en naam | varchar(255) |
| `videoadinpod` | Video en audio in podpositie | varchar(255) |
| `videoadlength` | Video en lengte | varchar(255) |
| `videoadload` | Video en laden | varchar(255) |
| `videoadname` | Video en naam | varchar(255) |
| `videoadplayername` | Naam van video en speler | varchar(255) |
| `videoadpod` | Video en pod | varchar(255) |
| `videoadvertiser` | Videoadverteerder | varchar(255) |
| `videoaudioalbum` | Videoaudioalbum | varchar(255) |
| `videoaudioartist` | Videoontwerper | varchar(255) |
| `videoaudioauthor` | Video audio-auteur | varchar(255) |
| `videoaudiolabel` | Video, audiolabel | varchar(255) |
| `videoaudiopublisher` | Video-uitgever | varchar(255) |
| `videoaudiostation` | Videoaudiostation | varchar(255) |
| `videocampaign` | Videocampagne | varchar(255) |
| `videochannel` | Videokanaal | varchar(255) |
| `videochapter` | Naam van videohoofdstuk | varchar(255) |
| `videocontenttype` | Type video-inhoud. Automatisch instellen op &#39;Video&#39; voor alle videoweergaven | varchar(255) |
| `videodaypart` | Dagdeel van video | varchar(255) |
| `videoepisode` | Video-aflevering | varchar(255) |
| `videofeedtype` | Type videofeed | varchar(255) |
| `videogenre` | Videogenre | text |
| `videolength` | Videolengte | varchar(255) |
| `videomvpd` | Video MVPD | varchar(255) |
| `videoname` | Videonaam | varchar(255) |
| `videonetwork` | Videonetwerk | varchar(255) |
| `videopath` | Videopad | varchar(100) |
| `videoplayername` | Naam videospeler | varchar(255) |
| `videoqoebitrateaverageevar` | Gemiddelde bitsnelheid videokwaliteit | varchar(255) |
| `videoqoebitratechangecountevar` | Aantal wijzigingen in videokwaliteit | varchar(255) |
| `videoqoebuffercountevar` | Aantal buffer voor videokwaliteit | varchar(255) |
| `videoqoebuffertimeevar` | Buffertijd videokwaliteit | varchar(255) |
| `videoqoedroppedframecountevar` | Aantal gedropte frames videokwaliteit | varchar(255) |
| `videoqoeerrorcountevar` | Aantal fouten in videokwaliteit | varchar(255) |
| `videoqoeextneralerrors` | Externe fouten in videokwaliteit | text |
| `videoqoeplayersdkerrors` | SDK-fouten videokwaliteit | text |
| `videoqoetimetostartevar` | Tijd van videokwaliteit om te beginnen | varchar(255) |
| `videoseason` | Videoseizoen | varchar(255) |
| `videosegment` | Videosegment | varchar(255) |
| `videoshow` | Videoshow | varchar(255) |
| `videoshowtype` | Type video-presentatie | varchar(255) |
| `videostreamtype` | Type videostream | varchar(255) |
| `visid_high` | Wordt gebruikt in combinatie met `visid_low` om een bezoeker op unieke wijze te identificeren. | bigint zonder teken |
| `visid_low` | Wordt gebruikt in combinatie met `visid_high` om een bezoeker op unieke wijze te identificeren. | bigint zonder teken |
| `visid_new` | Markering om te bepalen of de treffer een onlangs gegenereerde bezoeker-id bevat. | teken(1) |
| `visid_timestamp` | Als de bezoeker-id pas is gegenereerd, geeft u het tijdstempel (in Unix-tijd) op van het tijdstip waarop de bezoeker-id is gegenereerd. | int |
| `visid_type` | Niet voor extern gebruik; intern gebruikt door Adobe voor verwerkingsoptimalisaties. Numerieke id die de methode vertegenwoordigt die wordt gebruikt om de bezoeker te identificeren.<br>0: Aangepaste bezoeker-id of onbekend/niet van toepassing<br>1: IP en gebruikersagent fallback <br>2: Koptekst van HTTP Mobile-abonnee <br>3: Verouderde cookie-waarde (`s_vi`) <br>4: Waarde van fallback-cookie (`s_fid`) <br>5: Identiteitsservice | tinyint zonder teken |
| `visit_keywords` | Variabele gebruikt in de [Trefwoord zoeken](/help/components/dimensions/search-keyword.md) dimensie. Deze kolom gebruikt een niet-standaard karaktergrens van varchar (244) om achterste die logica aan te passen door Adobe wordt gebruikt. | varchar(244) |
| `visit_num` | Variabele gebruikt in de [Bezoek nummer](/help/components/dimensions/visit-number.md) dimensie. Begint bij 1, en verhoogt telkens als een nieuw bezoek per bezoeker begint. | int zonder teken |
| `visit_page_num` | Variabele gebruikt in de [Hoogte](/help/components/dimensions/hit-depth.md) dimensie. Verhoogt met 1 voor elke hit die de gebruiker genereert. Hiermee herstelt u elk bezoek. | int zonder teken |
| `visit_ref_domain` | Op basis van de `visit_referrer` kolom. Het eerste verwijzende domein van het bezoek. | varchar(100) |
| `visit_ref_type` | Numerieke id die het referentietype van de eerste referentie van het bezoek vertegenwoordigt. Gebruikt de `referrer_type.tsv` opzoektabel. | tinyint zonder teken |
| `visit_referrer` | De eerste referentie van het bezoek. | varchar(255) |
| `visit_search_engine` | Numerieke id van de eerste zoekfunctie van het bezoek. Gebruiksmiddelen `search_engines.tsv` opzoeken. | small int zonder teken |
| `visit_start_page_url` | De eerste URL van het bezoek. | varchar(255) |
| `visit_start_pagename` | De waarde Paginanaam in de eerste hit van het bezoek. | varchar(100) |
| `visit_start_time_gmt` | Tijdstempel (in Unix-tijd) van de eerste hit van het bezoek. | int |
| `weekly_visitor` | Markering om te bepalen of de treffer een nieuwe wekelijkse bezoeker is. | tinyint zonder teken |
| `yearly_visitor` | Markering om te bepalen of de treffer een nieuwe jaarlijkse bezoeker is. | tinyint zonder teken |
| `zip` | Hiermee kunt u de [Postcode](/help/components/dimensions/zip-code.md) dimensie. Zie ook `geo_zip`. | varchar(50) |

## Lege kolommen

De volgende lijst met kolommen wordt niet gebruikt en bevat geen gegevens:

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
* `mobiledeeplinkid.name`
* `mobileinstalls`
* `mobilelaunches`
* `mobileltvtotal`
* `mobilemessageclicks`
* `mobilemessageid.dest`
* `mobilemessageid.name`
* `mobilemessageid.type`
* `mobilemessageimpressions`
* `mobilemessagepushpayloadid.name`
* `mobilemessageviews`
* `mobilemonthlyengagedusers`
* `mobileplacedwelltime`
* `mobileplaceentry`
* `mobileplaceexit`
* `mobileprevsessionlength`
* `mobilerelaunchcampaigntrackingcode.name`
* `mobileupgrades`
* `socialaveragesentiment`
* `socialaveragesentiment (deprecated)`
* `socialfbstories`
* `socialfbstorytellers`
* `socialinteractioncount`
* `sociallikeadds`
* `sociallink`
* `sociallink (deprecated)`
* `socialmentions`
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
* `sourceid`
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
