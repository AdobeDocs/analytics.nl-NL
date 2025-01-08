---
title: Compatibiliteit met analytische Dimensionen
description: Referentie voor analytische afmetingen en rapporten.
feature: Dimensions
exl-id: 1884bc20-b04d-4f9a-b057-2b2fbe53190d
source-git-commit: fd26afc166ada6b1bc1890cbcf1406345c275765
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 6%

---

# Compatibiliteit met analytische Dimensionen

Deze pagina maakt een lijst van [ dimensies ](overview.md) die in hun respectieve mogelijkheden van Analytics worden gesteund.

>[!NOTE]
>
>Namen, classificaties en kenmerken van aangepaste variabelen worden in deze lijst weggelaten. Deze dimensiepunten zijn specifiek voor individuele rapportreeksen.

## Dimensionen ondersteund in Analysis Workspace

| Naam Dimension (zichtbaar in de gebruikersinterface voor analyse) | Dimension-id (wordt gebruikt in API-aanvragen) |
|---|---|
| Analyses voor doel | `targetraw` |
| Soorten publiek-id | `mcaudiences` |
| [Browser](browser.md) | `browser` |
| [ Browser Type ](browser-type.md) | `browsertype` |
| [Categorie](category.md) | `category` |
| [ Steden ](cities.md) | `geocity` |
| [Kleurdiepte](color-depth.md) | `colordepth` |
| [Verbindingstype](connection-type.md) | `connectiontype` |
| [ Steun van het Koekje ](cookie-support.md) | `cookie` |
| [ Landen ](countries.md) | `geocountry` |
| [Klantloyaliteit](customer-loyalty.md) | `customerloyalty` |
| [ de Omzetting Vars van de Douane van de Omzetting ](evar.md) | `evar1` , `evar2` , enzovoort. |
| [ Custom Insight Vars ](prop.md) | `prop1` , `prop2` , enzovoort. |
| [Aangepaste koppeling](custom-link.md) | `customlink` |
| [Dagen vóór eerste aankoop](days-before-first-purchase.md) | `daysbeforefirstpurchase` |
| [Dagen sinds laatste aankoop](days-since-last-purchase.md) | `dayssincelastpurchase` |
| [ Domein ](domain.md) | `filtereddomain` |
| [ Verbinding van de Download ](download-link.md) | `downloadlink` |
| [ Pagina van de Ingang ](entry-dimensions.md) | `entrypage` |
| [ Origineel van de Pagina van de Ingang van de Ingang ](entry-dimensions.md) | `entrypageoriginal` |
| [ Verbinding van de uitgang ](exit-link.md) | `exitlink` |
| [ Eerste Aanraakkanaal ](first-touch-channel.md) | `firsttouchchannel` |
| [ Eerste het Detail van het Kanaal van de Aanraak ](first-touch-detail.md) | `firsttouchchanneldetail` |
| [ toegelaten Java ](java-enabled.md) | `javaenabled` |
| [Taal](language.md) | `language` |
| [ het Laatste Kanaal van de Aanraking ](last-touch-channel.md) | `lasttouchchannel` |
| [ het Laatste Detail van het Kanaal van de Aanraak ](last-touch-detail.md) | `lasttouchchanneldetail` |
| Variabelen weergeven | `listvariables` |
| [ het Marketing Kanaal ](marketing-channel.md) | `marketingchannel` |
| [ Mobiele AudioSteun ](mobile-dimensions.md) | `mobileaudiosupport` |
| [Mobiele aanbieder](mobile-dimensions.md) | `mobilecarrier` |
| [ Mobiele Diepte van de Kleur ](mobile-dimensions.md) | `mobilecolordepth` |
| [ Mobiele Steun van het Koekje ](mobile-dimensions.md) | `mobilecookiesupport` |
| [ Mobiel Apparaat ](mobile-dimensions.md) | `mobiledevicename` |
| [ Mobiel Type van Apparaat ](mobile-dimensions.md) | `mobiledevicetype` |
| [ Mobiele Maximum E-maillengte ](mobile-dimensions.md) | `mobileemaillength` |
| [ Mobiele Steun van het Beeld ](mobile-dimensions.md) | `mobileimagesupport` |
| [ Mobiele Fabrikant ](mobile-dimensions.md) | `mobilemanufacturer` |
| [ Mobiel Werkende Systeem (afgekeurd) ](mobile-dimensions.md) | `mobileos` |
| [ Mobiele Hoogte van het Scherm ](mobile-dimensions.md) | `mobilescreenheight` |
| [ Mobiele Grootte van het Scherm ](mobile-dimensions.md) | `mobilescreensize` |
| [ Mobiele Breedte van het Scherm ](mobile-dimensions.md) | `mobilescreenwidth` |
| [ Mobiele Maximum Browser URL Lengte ](mobile-dimensions.md) | `mobileurllength` |
| [ Mobiele VideoSteun ](mobile-dimensions.md) | `mobilevideosupport` |
| [ Resolutie van de Monitor ](monitor-resolution.md) | `monitorresolution` |
| [Besturingssystemen](operating-systems.md) | `operatingsystem` |
| [ Origineel Verwijzend Domein ](original-referring-domain.md) | `referringdomainoriginal` |
| [ Pagina ](page.md) | `page` |
| [Pagina&#39;s niet gevonden](pages-not-found.md) | `pagesnotfound` |
| [ Product ](product.md) | `product` |
| [ Referrer ](referrer.md) | `referrer` |
| [Type referrer](referrer-type.md) | `referrertype` |
| [ Verwijzend Domein ](referring-domain.md) | `referringdomain` |
| [ Gebieden ](regions.md) | `georegion` |
| [Retourfrequentie](return-frequency.md) | `returnfrequency` |
| SC-TnT | `tntbase` |
| [ Motor van het Onderzoek ](search-engine.md) | `searchengine` |
| [ Sleutelwoord van het Onderzoek ](search-keyword.md) | `searchenginekeyword` |
| [ Motor van het Onderzoek - Natuurlijk ](search-engine.md) | `searchenginenatural` |
| [ Motor van het Onderzoek - Betaalde ](search-engine.md) | `searchenginepaid` |
| [ het Trefwoord van het Onderzoek - Natuurlijk ](search-keyword.md) | `searchenginenaturalkeyword` |
| [ het Trefwoord van het Onderzoek - Betaalde ](search-keyword.md) | `searchenginepaidkeyword` |
| [ Al Rang van de Pagina van het Onderzoek ](all-search-page-rank.md) | `searchenginepagerank` |
| [ Server ](server.md) | `server` |
| [ Enige Bezoeken van de Pagina ](single-page-visits.md) | `singlepagevisits` |
| [ Sectie van de Plaats ](site-section.md) | `sitesections` |
| [ Tijd die per Bezoek - Granulair wordt uitgegeven ](time-spent-per-visit.md) | `sitetime` |
| [ het Volgen Code ](tracking-code.md) | `campaign` |
| [ DMA van de V.S. ](us-dma.md) | `geodma` |
| [ Staten van de V.S. ](us-states.md) | `state` |
| [Tijd voorafgaand aan gebeurtenis](time-prior-to-event.md) | `timeprior` |
| [ Tijd die per Bezoek wordt uitgegeven - Emmerde ](time-spent-per-visit.md) | `timespent` |
| [ Diepte van het Bezoek ](visit-depth.md) | `pathlength` |
| [Bezoeknummer](visit-number.md) | `visitnumber` |
| [ Postcode ](zip-code.md) | `zip` |
| [ AM / PM ](am-pm.md) | `timepartampm` |
| [ Browser Hoogte - Gesloten ](browser-height.md) | `browserheightbucketed` |
| [ Browser Breedte - Gesloten ](browser-width.md) | `browserwidthbucketed` |
| [ Dag ](day.md) | `daterangeday` |
| [ Dag van Maand ](day-of-month.md) | `timepartdayofmonth` |
| [ Dag van Week ](day-of-week.md) | `dayofweek` |
| [ Dag van Week ](day-of-week.md) | `timepartdayofweek` |
| [ Dag van Jaar ](day-of-year.md) | `timepartdayofyear` |
| [Dagen sinds laatste bezoek](days-since-last-visit.md) | `dayssincelastvisit` |
| [ Ingang de Inzicht van de Douane ](entry-dimensions.md) | `entryprops` |
| [ Variabelen van de Lijst van de Ingang ](entry-dimensions.md) | `entrylistvariables` |
| [ Server van de Ingang ](entry-dimensions.md) | `entryserver` |
| [ Sectie van de Plaats van de Ingang ](entry-dimensions.md) | `entrysitesections` |
| [ de Inzichten van de Douane van de uitgang ](exit-dimensions.md) | `exitprops` |
| [ Uitgang de Variabelen van de Lijst ](exit-dimensions.md) | `exitlistvariables` |
| [ de Pagina van de uitgang ](exit-dimensions.md) | `exitpage` |
| [ de Server van de uitgang ](exit-dimensions.md) | `exitserver` |
| [ sectie van de Plaats van de uitgang ](exit-dimensions.md) | `exitsitesections` |
| [ Diepte van het Actief ](hit-depth.md) | `hitdepth` |
| [Type hit](hit-type.md) | `hittype` |
| [ Uur ](hour.md) | `daterangehour` |
| [ Uur van Dag ](hour-of-day.md) | `timeparthourofday` |
| [ het Detail van het Kanaal van de Marketing ](marketing-detail.md) | `marketingchanneldetail` |
| [ Minuut ](minute.md) | `daterangeminute` |
| [ Mobiele Maximum Lengte van de Referentie ](mobile-dimensions.md) | `mobilebookmarklength` |
| [ Mobiel Aantal van het Apparaat ](mobile-dimensions.md) | `mobiledevicenumber` |
| [ Mobiele DRM ](mobile-dimensions.md) | `mobiledrm` |
| [ Mobiele Diensten van de Informatie ](mobile-dimensions.md) | `mobileinformationservices` |
| [ Mobiele VM van Java ](mobile-dimensions.md) | `mobilejavavm` |
| [ Mobiele Decoratie van de Post ](mobile-dimensions.md) | `mobilemaildecoration` |
| [ Mobiele Netto Protocollen ](mobile-dimensions.md) | `mobilenetprotocols` |
| [ Mobiel duw om te spreken ](mobile-dimensions.md) | `mobilepushtotalk` |
| [ Maand ](month.md) | `daterangemonth` |
| [ Maand van Jaar ](month-of-year.md) | `timepartmonthofyear` |
| [Typen besturingssystemen](operating-system-types.md) | `operatingsystemgroup` |
| [ Betaald Onderzoek ](paid-search.md) | `paidsearch` |
| [ Blijvende Steun van het Koekje ](persistent-cookie-support.md) | `persistentcookie` |
| [ Kwartaal ](quarter.md) | `daterangequarter` |
| [ Kwartaal van Jaar ](quarter-of-year.md) | `timepartquarterofyear` |
| Enquête | `surveybase` |
| [ Tijd die op Pagina wordt besteed - Gesloten ](time-spent-on-page.md) | `averagepagetime` |
| [ Tijd die op Pagina wordt besteed - korrelig ](time-spent-on-page.md) | `pagetimeseconds` |
| [ het Volgen Opt-out Reden ](tracking-opt-out-reason.md) | `optoutreason` |
| [ Weekdag/Weekend ](weekday-weekend.md) | `timepartweekdayweekend` |
| [ Week ](week.md) | `daterangeweek` |
| [ Jaar ](year.md) | `daterangeyear` |

## Afmetingen met behoud van inhoud worden alleen ondersteund in Analysis Workspace

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| Mediasessie-id | `videosessionid` |
| Nielsen Access-methode | `nielsenaccmethod` |
| Nielsen App ID | `nielsenappid` |
| Nielsen Channel Asset | `nielsenchannelasset` |
| Nielsen-inhoudstype | `nielsencontenttype` |

## Afmetingen waarbij de inhoud behouden blijft, ondersteund door Analysis Workspace

### Video (de streamingmedia-verzameling)

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [ Inhoud ](sm-core.md) | `video` |
| [ Segment van de Inhoud ](sm-core.md) | `videosegment` |
| [ Type van Inhoud ](sm-core.md) | `videocontenttype` |
| [ Add Player Name ](sm-ads.md) | `videoadplayername` |
| [ Advertentie in Podpositie ](sm-ads.md) | `videoadinpod` |
| [ gelaten vallen Kaders ](sm-quality.md) | `videoqoedroppedframecountevar` |
| [ Fouten ](sm-quality.md) | `videoqoeerrorcountevar` |
| [ Gemiddelde Bitsnelheid ](sm-quality.md) | `videoqoebitrateaverageevar` |
| [ Veranderingen van de Bitsnelheid ](sm-quality.md) | `videoqoebitratechangecountevar` |
| [ Totale Duur van de Buffer ](sm-quality.md) | `videoqoebuffertimeevar` |
| [ Gebeurtenissen van de Buffer ](sm-quality.md) | `videoqoebuffercountevar` |
| [ Tijd aan Begin ](sm-quality.md) | `videoqoetimetostartevar` |
| [ Advertentiepod ](sm-ads.md) | `videoadpod` |
| [ Weg van Media ](sm-core.md) | `videopath` |
| [ Advertentie ](sm-ads.md) | `videoad` |
| [ Naam van de Speler van de Inhoud ](sm-core.md) | `videoplayername` |
| [ Kanaal van de Inhoud ](sm-core.md) | `videochannel` |
| [ Hoofdstuk ](sm-chapters.md) | `videochapter` |
| [ Naam van de Inhoud (veranderlijk) ](sm-core.md) | `videoname` |
| [ Lengte van de Inhoud (veranderlijk) ](sm-core.md) | `videolength` |
| [ Add Naam (veranderlijk) ](sm-ads.md) | `videoadname` |
| [ Add Length (veranderlijk) ](sm-ads.md) | `videoadlength` |
| [ tonen ](sm-video-metadata.md) | `videoshow` |
| [ Seizoen ](sm-video-metadata.md) | `videoseason` |
| [ Episode ](sm-video-metadata.md) | `videoepisode` |
| [ Netwerk ](sm-video-metadata.md) | `videonetwork` |
| [ toon Type ](sm-video-metadata.md) | `videoshowtype` |
| [ Advertentie laadt ](sm-ads.md) | `videoadload` |
| [ MVPD ](sm-video-metadata.md) | `videomvpd` |
| [ Deel van de Dag ](sm-video-metadata.md) | `videodaypart` |
| [ Advertiser ](sm-ads.md) | `videoadadvertiser` |
| [ identiteitskaart van de Campagne ](sm-ads.md) | `videoadcampaign` |
| [ Genre ](sm-video-metadata.md) | `videogenre` |
| [ Type van Stroom ](sm-core.md) | `videostreamtype` |
| [ De Fout IDs van de Fout van de Speler SDK ](sm-quality.md) | `videoqoeplayersdkerrors` |
| [ Externe Fout IDs ](sm-quality.md) | `videoqoeextneralerrors` |
| [ Type van Diervoeders van Media ](sm-video-metadata.md) | `videofeedtype` |
| [ Pad van de Media van de Ingang ](entry-dimensions.md) | `entryvideopath` |
| [ Uitgang de Weg van Media ](exit-dimensions.md) | `exitvideopath` |
| [ Genre van de Ingang ](entry-dimensions.md) | `entryvideogenre` |
| [ Uitgang Genre ](exit-dimensions.md) | `exitvideogenre` |
| [ De Fout IDs van de Speler van de Ingang SDK ](entry-dimensions.md) | `entryvideoqoeplayersdkerrors` |
| [ de Fout IDs van de Speler van de Afgang SDK ](exit-dimensions.md) | `exitvideoqoeplayersdkerrors` |
| [ De Externe van de Ingang identiteitskaarts van de Fout ](entry-dimensions.md) | `entryvideoqoeextneralerrors` |
| [ Uitgang Externe Fout IDs ](exit-dimensions.md) | `exitvideoqoeextneralerrors` |

### Adobe Social

Adobe Social is met pensioen.

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Voorwaarden | `socialterm` |
| Sociale platforms/eigenschappen | `socialcontentprovider` |
| Auteurs | `socialauthor` |
| Taal | `sociallanguage` |
| Breedtegraad/lengtegraad | `sociallatlong` |
| Codes voor het bijhouden van elementen | `socialassettrackingcode` |
| Eigendom van sociale eigenschappen | `socialaccountandappids` |
| ID&#39;s van eigenlijke berichten | `socialownedpostids` |
| Eigendom van sociale definities | `socialinteractiontype` |
| Eigenschap-id&#39;s | `socialownedpropertyid` |
| Eigendom van eigenschap versus toepassing | `socialownedpropertypropertyvsapp` |
| Eigenschapnaam in eigendom | `socialownedpropertyname` |
| Eigendom van definitie versus Post | `socialowneddefinitionpropertyvspost` |
| Eigen definitietype | `socialowneddefinitioninsighttype` |
| Waarde van eigen definitietoezicht | `socialowneddefinitioninsightvalue` |
| Eigen definitiemetrisch | `socialowneddefinitionmetric` |
| Element | `socialmediaid` |

### Mobile SDK

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [ Eerste Datum van de Lancering ](lifecycle-dimensions.md) | `mobileinstalldate` |
| [ toepassings identiteitskaart ](lifecycle-dimensions.md) | `mobileappid` |
| [ Aantal van de Lancering ](lifecycle-dimensions.md) | `mobilelaunchnumber` |
| [ dagen sinds eerste gebruik ](lifecycle-dimensions.md) | `mobiledayssincefirstuse` |
| [ dagen sinds laatste Gebruik ](lifecycle-dimensions.md) | `mobiledayssincelastuse` |
| [ Uur van Dag (SDK) ](lifecycle-dimensions.md) | `mobilehourofday` |
| [ Dag van Week (SDK) ](lifecycle-dimensions.md) | `mobiledayofweek` |
| [ Werkend Systeem (SDK) ](lifecycle-dimensions.md) | `mobileosenvironment` |
| [ dagen sinds laatste verbetering ](lifecycle-dimensions.md) | `mobiledayssincelastupgrade` |
| [ Lanceringen sinds laatste verbetering ](lifecycle-dimensions.md) | `mobilelaunchessincelastupgrade` |
| [ Naam van het Apparaat (SDK) ](lifecycle-dimensions.md) | `mobiledevice` |
| [ Versie van het Werkende Systeem (SDK) ](lifecycle-dimensions.md) | `mobileosversion` |
| [ Belangrijkste baken ](lifecycle-dimensions.md) | `mobilebeaconmajor` |
| [ Kleine baken Minder ](lifecycle-dimensions.md) | `mobilebeaconminor` |
| [ het baken UUID ](lifecycle-dimensions.md) | `mobilebeaconuuid` |
| [ Beacon Proximity ](lifecycle-dimensions.md) | `mobilebeaconproximity` |
| [ Plaats (neer aan 10 km) ](lifecycle-dimensions.md) | `latlon1` |
| [ Plaats (neer aan 100 m) ](lifecycle-dimensions.md) | `latlon23` |
| [ Plaats (neer aan 1 m) ](lifecycle-dimensions.md) | `latlon45` |
| [ Punt van de Naam van het Intern ](lifecycle-dimensions.md) | `pointofinterest` |
| [ Afstand aan Punt van het Centrum van de Rente ](lifecycle-dimensions.md) | `pointofinterestdistance` |
| [ Nauwkeurigheid van de Plaats ](lifecycle-dimensions.md) | `mobileplaceaccuracy` |
| [ Plaats Categorie ](lifecycle-dimensions.md) | `mobileplacecategory` |
| [ identiteitskaart van de Plaats ](lifecycle-dimensions.md) | `mobileplaceid` |
| [ Invoerbaken Ingang Belangrijk ](lifecycle-dimensions.md) | `entrymobilebeaconmajor` |
| [ Belangrijkste van het Bebakken van de Uitgang ](lifecycle-dimensions.md) | `exitmobilebeaconmajor` |
| [ Onderliggend baken van de Ingang 0} ](lifecycle-dimensions.md) | `entrymobilebeaconminor` |
| [ de Kleine Korte Kleine Beacon van de Uitgang ](lifecycle-dimensions.md) | `exitmobilebeaconminor` |
| [ Ingangsbaken UUID ](lifecycle-dimensions.md) | `entrymobilebeaconuuid` |
| [ de Beacon UUID van het Beken van de Uitgang ](lifecycle-dimensions.md) | `exitmobilebeaconuuid` |
| [ Beacon van het Ingang Beacon Proximity ](lifecycle-dimensions.md) | `entrymobilebeaconproximity` |
| [ Beacon Proximity van de Uitgang ](lifecycle-dimensions.md) | `exitmobilebeaconproximity` |

### Adobe Advertising Cloud (AMO)

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AMO EF-ID | `amo_ef_id` |
| AMO-id | `amo_cid` |

### Activity Map

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [ verbinding van de Activity Map door Gebied ](activity-map-link-by-region.md) | `clickmaplinkbyregion` |
| [ Gebied van de Activity Map ](activity-map-region.md) | `clickmapregion` |
| [ Verbinding van de Activity Map ](activity-map-link.md) | `clickmaplink` |
| [ Pagina van de Activity Map ](activity-map-page.md) | `clickmappage` |

### Nielsen Integration

Voor meer informatie over hoe te om deze integratie uit te voeren, zie de [ Uitbreiding Nielsen ](https://exchange.adobe.com/apps/ec/101361) op de Adobe Exchange.

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Nielsen AdModel | `nielsenadmodel` |
| Nielsen Segment C | `nielsensegmentc` |
| Nielsen Segment B | `nielsensegmentb` |
| Nielsen Segment A | `nielsensegmenta` |
| Nielsen Content ID | `nielsencontentid` |
| Nielsen Asset/Program | `nielsenasset` |
| Nielsen VCID | `nielsenvcid` |
| Nielsen Opt Out | `nielsenoptout` |
| Nielsen Client ID + VCID | `nielsenclientidvcid` |
| Nielsen Client ID | `nielsenclientid` |
| Ingang Nielsen Weigeren | `entrynielsenoptout` |
| Nielsen afsluiten Opt Out | `exitnielsenoptout` |
| Ingang Nielsen Client ID + VCID | `entrynielsenclientidvcid` |
| Nielsen Client ID afsluiten + VCID | `exitnielsenclientidvcid` |
| Ingang Nielsen Client ID | `entrynielsenclientid` |
| Nielsen-client-id afsluiten | `exitnielsenclientid` |

### Adobe Experience Manager (AEM)

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Element-id | `aemassetid` |
| Source-element | `aemassetsource` |
| Id van geklikt element | `aemclickedassetid` |
| Item-id | `entryaemassetid` |
| Element-id afsluiten | `exitaemassetid` |

### Adobe Campaign

| Naam van Dimension (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Uitgevoerde levering-id van Adobe Campaign | `ac_delivery_internal_name` |
