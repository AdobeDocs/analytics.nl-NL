---
title: Compatibiliteit met analytische afmetingen
description: Referentie voor analytische afmetingen en rapporten.
feature: Dimensions
exl-id: 1884bc20-b04d-4f9a-b057-2b2fbe53190d
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 6%

---

# Compatibiliteit met analytische afmetingen

Deze pagina maakt een lijst van [&#x200B; dimensies &#x200B;](overview.md) die in hun respectieve mogelijkheden van Analytics worden gesteund.

>[!NOTE]
>
>Namen, classificaties en kenmerken van aangepaste variabelen worden in deze lijst weggelaten. Deze dimensiepunten zijn specifiek voor individuele rapportreeksen.

## Dimensies die worden ondersteund in Analysis Workspace

| Dimension-naam (zichtbaar in de gebruikersinterface van Analytics) | Dimension-id (wordt gebruikt in API-aanvragen) |
|---|---|
| Analyses voor doel | `targetraw` |
| Soorten publiek-id | `mcaudiences` |
| [Browser](browser.md) | `browser` |
| [&#x200B; Browser Type &#x200B;](browser-type.md) | `browsertype` |
| [Categorie](category.md) | `category` |
| [&#x200B; Steden &#x200B;](cities.md) | `geocity` |
| [Kleurdiepte](color-depth.md) | `colordepth` |
| [Verbindingstype](connection-type.md) | `connectiontype` |
| [&#x200B; Steun van het Koekje &#x200B;](cookie-support.md) | `cookie` |
| [&#x200B; Landen &#x200B;](countries.md) | `geocountry` |
| [Klantloyaliteit](customer-loyalty.md) | `customerloyalty` |
| [&#x200B; de Omzetting Vars van de Douane van de Omzetting &#x200B;](evar.md) | `evar1` , `evar2` , enzovoort. |
| [&#x200B; Custom Insight Vars &#x200B;](prop.md) | `prop1` , `prop2` , enzovoort. |
| [Aangepaste koppeling](custom-link.md) | `customlink` |
| [Dagen vóór eerste aankoop](days-before-first-purchase.md) | `daysbeforefirstpurchase` |
| [Dagen sinds laatste aankoop](days-since-last-purchase.md) | `dayssincelastpurchase` |
| [&#x200B; Domein &#x200B;](domain.md) | `filtereddomain` |
| [&#x200B; Verbinding van de Download &#x200B;](download-link.md) | `downloadlink` |
| [&#x200B; Pagina van de Ingang &#x200B;](entry-dimensions.md) | `entrypage` |
| [&#x200B; Origineel van de Pagina van de Ingang van de Ingang &#x200B;](entry-dimensions.md) | `entrypageoriginal` |
| [&#x200B; Verbinding van de uitgang &#x200B;](exit-link.md) | `exitlink` |
| [&#x200B; Eerste Aanraakkanaal &#x200B;](first-touch-channel.md) | `firsttouchchannel` |
| [&#x200B; Eerste het Detail van het Kanaal van de Aanraak &#x200B;](first-touch-detail.md) | `firsttouchchanneldetail` |
| [&#x200B; toegelaten Java &#x200B;](java-enabled.md) | `javaenabled` |
| [Taal](language.md) | `language` |
| [&#x200B; het Laatste Kanaal van de Aanraking &#x200B;](last-touch-channel.md) | `lasttouchchannel` |
| [&#x200B; het Laatste Detail van het Kanaal van de Aanraak &#x200B;](last-touch-detail.md) | `lasttouchchanneldetail` |
| Variabelen weergeven | `listvariables` |
| [&#x200B; het Marketing Kanaal &#x200B;](marketing-channel.md) | `marketingchannel` |
| [&#x200B; Mobiele AudioSteun &#x200B;](mobile-dimensions.md) | `mobileaudiosupport` |
| [Mobiele aanbieder](mobile-dimensions.md) | `mobilecarrier` |
| [&#x200B; Mobiele Diepte van de Kleur &#x200B;](mobile-dimensions.md) | `mobilecolordepth` |
| [&#x200B; Mobiele Steun van het Koekje &#x200B;](mobile-dimensions.md) | `mobilecookiesupport` |
| [&#x200B; Mobiel Apparaat &#x200B;](mobile-dimensions.md) | `mobiledevicename` |
| [&#x200B; Mobiel Type van Apparaat &#x200B;](mobile-dimensions.md) | `mobiledevicetype` |
| [&#x200B; Mobiele Maximum E-maillengte &#x200B;](mobile-dimensions.md) | `mobileemaillength` |
| [&#x200B; Mobiele Steun van het Beeld &#x200B;](mobile-dimensions.md) | `mobileimagesupport` |
| [&#x200B; Mobiele Fabrikant &#x200B;](mobile-dimensions.md) | `mobilemanufacturer` |
| [&#x200B; Mobiel Werkende Systeem (afgekeurd) &#x200B;](mobile-dimensions.md) | `mobileos` |
| [&#x200B; Mobiele Hoogte van het Scherm &#x200B;](mobile-dimensions.md) | `mobilescreenheight` |
| [&#x200B; Mobiele Grootte van het Scherm &#x200B;](mobile-dimensions.md) | `mobilescreensize` |
| [&#x200B; Mobiele Breedte van het Scherm &#x200B;](mobile-dimensions.md) | `mobilescreenwidth` |
| [&#x200B; Mobiele Maximum Browser URL Lengte &#x200B;](mobile-dimensions.md) | `mobileurllength` |
| [&#x200B; Mobiele VideoSteun &#x200B;](mobile-dimensions.md) | `mobilevideosupport` |
| [&#x200B; Resolutie van de Monitor &#x200B;](monitor-resolution.md) | `monitorresolution` |
| [Besturingssystemen](operating-systems.md) | `operatingsystem` |
| [&#x200B; Origineel Verwijzend Domein &#x200B;](original-referring-domain.md) | `referringdomainoriginal` |
| [&#x200B; Pagina &#x200B;](page.md) | `page` |
| [Pagina&#39;s niet gevonden](pages-not-found.md) | `pagesnotfound` |
| [&#x200B; Product &#x200B;](product.md) | `product` |
| [&#x200B; Referrer &#x200B;](referrer.md) | `referrer` |
| [Type referrer](referrer-type.md) | `referrertype` |
| [&#x200B; Verwijzend Domein &#x200B;](referring-domain.md) | `referringdomain` |
| [&#x200B; Gebieden &#x200B;](regions.md) | `georegion` |
| [Retourfrequentie](return-frequency.md) | `returnfrequency` |
| SC-TnT | `tntbase` |
| [&#x200B; Motor van het Onderzoek &#x200B;](search-engine.md) | `searchengine` |
| [&#x200B; Sleutelwoord van het Onderzoek &#x200B;](search-keyword.md) | `searchenginekeyword` |
| [&#x200B; Motor van het Onderzoek - Natuurlijk &#x200B;](search-engine.md) | `searchenginenatural` |
| [&#x200B; Motor van het Onderzoek - Betaalde &#x200B;](search-engine.md) | `searchenginepaid` |
| [&#x200B; het Trefwoord van het Onderzoek - Natuurlijk &#x200B;](search-keyword.md) | `searchenginenaturalkeyword` |
| [&#x200B; het Trefwoord van het Onderzoek - Betaalde &#x200B;](search-keyword.md) | `searchenginepaidkeyword` |
| [&#x200B; Al Rang van de Pagina van het Onderzoek &#x200B;](all-search-page-rank.md) | `searchenginepagerank` |
| [&#x200B; Server &#x200B;](server.md) | `server` |
| [&#x200B; Enige Bezoeken van de Pagina &#x200B;](single-page-visits.md) | `singlepagevisits` |
| [&#x200B; Sectie van de Plaats &#x200B;](site-section.md) | `sitesections` |
| [&#x200B; Tijd die per Bezoek - Granulair wordt uitgegeven &#x200B;](time-spent-per-visit.md) | `sitetime` |
| [&#x200B; het Volgen Code &#x200B;](tracking-code.md) | `campaign` |
| [&#x200B; DMA van de V.S. &#x200B;](us-dma.md) | `geodma` |
| [&#x200B; Staten van de V.S. &#x200B;](us-states.md) | `state` |
| [Tijd voorafgaand aan gebeurtenis](time-prior-to-event.md) | `timeprior` |
| [&#x200B; Tijd die per Bezoek wordt uitgegeven - Emmerde &#x200B;](time-spent-per-visit.md) | `timespent` |
| [&#x200B; Diepte van het Bezoek &#x200B;](visit-depth.md) | `pathlength` |
| [Bezoeknummer](visit-number.md) | `visitnumber` |
| [&#x200B; Postcode &#x200B;](zip-code.md) | `zip` |
| [&#x200B; AM / PM &#x200B;](am-pm.md) | `timepartampm` |
| [&#x200B; Browser Hoogte - Gesloten &#x200B;](browser-height.md) | `browserheightbucketed` |
| [&#x200B; Browser Breedte - Gesloten &#x200B;](browser-width.md) | `browserwidthbucketed` |
| [&#x200B; Dag &#x200B;](day.md) | `daterangeday` |
| [&#x200B; Dag van Maand &#x200B;](day-of-month.md) | `timepartdayofmonth` |
| [&#x200B; Dag van Week &#x200B;](day-of-week.md) | `dayofweek` |
| [&#x200B; Dag van Week &#x200B;](day-of-week.md) | `timepartdayofweek` |
| [&#x200B; Dag van Jaar &#x200B;](day-of-year.md) | `timepartdayofyear` |
| [Dagen sinds laatste bezoek](days-since-last-visit.md) | `dayssincelastvisit` |
| [&#x200B; Ingang de Inzicht van de Douane &#x200B;](entry-dimensions.md) | `entryprops` |
| [&#x200B; Variabelen van de Lijst van de Ingang &#x200B;](entry-dimensions.md) | `entrylistvariables` |
| [&#x200B; Server van de Ingang &#x200B;](entry-dimensions.md) | `entryserver` |
| [&#x200B; Sectie van de Plaats van de Ingang &#x200B;](entry-dimensions.md) | `entrysitesections` |
| [&#x200B; de Inzichten van de Douane van de uitgang &#x200B;](exit-dimensions.md) | `exitprops` |
| [&#x200B; Uitgang de Variabelen van de Lijst &#x200B;](exit-dimensions.md) | `exitlistvariables` |
| [&#x200B; de Pagina van de uitgang &#x200B;](exit-dimensions.md) | `exitpage` |
| [&#x200B; de Server van de uitgang &#x200B;](exit-dimensions.md) | `exitserver` |
| [&#x200B; sectie van de Plaats van de uitgang &#x200B;](exit-dimensions.md) | `exitsitesections` |
| [&#x200B; Diepte van het Actief &#x200B;](hit-depth.md) | `hitdepth` |
| [Type hit](hit-type.md) | `hittype` |
| [&#x200B; Uur &#x200B;](hour.md) | `daterangehour` |
| [&#x200B; Uur van Dag &#x200B;](hour-of-day.md) | `timeparthourofday` |
| [&#x200B; het Detail van het Kanaal van de Marketing &#x200B;](marketing-detail.md) | `marketingchanneldetail` |
| [&#x200B; Minuut &#x200B;](minute.md) | `daterangeminute` |
| [&#x200B; Mobiele Maximum Lengte van de Referentie &#x200B;](mobile-dimensions.md) | `mobilebookmarklength` |
| [&#x200B; Mobiel Aantal van het Apparaat &#x200B;](mobile-dimensions.md) | `mobiledevicenumber` |
| [&#x200B; Mobiele DRM &#x200B;](mobile-dimensions.md) | `mobiledrm` |
| [&#x200B; Mobiele Diensten van de Informatie &#x200B;](mobile-dimensions.md) | `mobileinformationservices` |
| [&#x200B; Mobiele VM van Java &#x200B;](mobile-dimensions.md) | `mobilejavavm` |
| [&#x200B; Mobiele Decoratie van de Post &#x200B;](mobile-dimensions.md) | `mobilemaildecoration` |
| [&#x200B; Mobiele Netto Protocollen &#x200B;](mobile-dimensions.md) | `mobilenetprotocols` |
| [&#x200B; Mobiel duw om te spreken &#x200B;](mobile-dimensions.md) | `mobilepushtotalk` |
| [&#x200B; Maand &#x200B;](month.md) | `daterangemonth` |
| [&#x200B; Maand van Jaar &#x200B;](month-of-year.md) | `timepartmonthofyear` |
| [Typen besturingssystemen](operating-system-types.md) | `operatingsystemgroup` |
| [&#x200B; Betaald Onderzoek &#x200B;](paid-search.md) | `paidsearch` |
| [&#x200B; Blijvende Steun van het Koekje &#x200B;](persistent-cookie-support.md) | `persistentcookie` |
| [&#x200B; Kwartaal &#x200B;](quarter.md) | `daterangequarter` |
| [&#x200B; Kwartaal van Jaar &#x200B;](quarter-of-year.md) | `timepartquarterofyear` |
| Enquête | `surveybase` |
| [&#x200B; Tijd die op Pagina wordt besteed - Gesloten &#x200B;](time-spent-on-page.md) | `averagepagetime` |
| [&#x200B; Tijd die op Pagina wordt besteed - korrelig &#x200B;](time-spent-on-page.md) | `pagetimeseconds` |
| [&#x200B; het Volgen Opt-out Reden &#x200B;](tracking-opt-out-reason.md) | `optoutreason` |
| [&#x200B; Weekdag/Weekend &#x200B;](weekday-weekend.md) | `timepartweekdayweekend` |
| [&#x200B; Week &#x200B;](week.md) | `daterangeweek` |
| [&#x200B; Jaar &#x200B;](year.md) | `daterangeyear` |

## Afmetingen met behoud van inhoud worden alleen ondersteund in Analysis Workspace

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| Mediasessie-id | `videosessionid` |
| Nielsen Access-methode | `nielsenaccmethod` |
| Nielsen App ID | `nielsenappid` |
| Nielsen Channel Asset | `nielsenchannelasset` |
| Nielsen-inhoudstype | `nielsencontenttype` |

## Afmetingen waarbij de inhoud behouden blijft, ondersteund door Analysis Workspace

### Video (streaming media services)

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [&#x200B; Inhoud &#x200B;](sm-core.md) | `video` |
| [&#x200B; Segment van de Inhoud &#x200B;](sm-core.md) | `videosegment` |
| [&#x200B; Type van Inhoud &#x200B;](sm-core.md) | `videocontenttype` |
| [&#x200B; Add Player Name &#x200B;](sm-ads.md) | `videoadplayername` |
| [&#x200B; Advertentie in Podpositie &#x200B;](sm-ads.md) | `videoadinpod` |
| [&#x200B; gelaten vallen Kaders &#x200B;](sm-quality.md) | `videoqoedroppedframecountevar` |
| [&#x200B; Fouten &#x200B;](sm-quality.md) | `videoqoeerrorcountevar` |
| [&#x200B; Gemiddelde Bitsnelheid &#x200B;](sm-quality.md) | `videoqoebitrateaverageevar` |
| [&#x200B; Veranderingen van de Bitsnelheid &#x200B;](sm-quality.md) | `videoqoebitratechangecountevar` |
| [&#x200B; Totale Duur van de Buffer &#x200B;](sm-quality.md) | `videoqoebuffertimeevar` |
| [&#x200B; Gebeurtenissen van de Buffer &#x200B;](sm-quality.md) | `videoqoebuffercountevar` |
| [&#x200B; Tijd aan Begin &#x200B;](sm-quality.md) | `videoqoetimetostartevar` |
| [&#x200B; Advertentiepod &#x200B;](sm-ads.md) | `videoadpod` |
| [&#x200B; Weg van Media &#x200B;](sm-core.md) | `videopath` |
| [&#x200B; Advertentie &#x200B;](sm-ads.md) | `videoad` |
| [&#x200B; Naam van de Speler van de Inhoud &#x200B;](sm-core.md) | `videoplayername` |
| [&#x200B; Kanaal van de Inhoud &#x200B;](sm-core.md) | `videochannel` |
| [&#x200B; Hoofdstuk &#x200B;](sm-chapters.md) | `videochapter` |
| [&#x200B; Naam van de Inhoud (veranderlijk) &#x200B;](sm-core.md) | `videoname` |
| [&#x200B; Lengte van de Inhoud (veranderlijk) &#x200B;](sm-core.md) | `videolength` |
| [&#x200B; Add Naam (veranderlijk) &#x200B;](sm-ads.md) | `videoadname` |
| [&#x200B; Add Length (veranderlijk) &#x200B;](sm-ads.md) | `videoadlength` |
| [&#x200B; tonen &#x200B;](sm-video-metadata.md) | `videoshow` |
| [&#x200B; Seizoen &#x200B;](sm-video-metadata.md) | `videoseason` |
| [&#x200B; Episode &#x200B;](sm-video-metadata.md) | `videoepisode` |
| [&#x200B; Netwerk &#x200B;](sm-video-metadata.md) | `videonetwork` |
| [&#x200B; toon Type &#x200B;](sm-video-metadata.md) | `videoshowtype` |
| [&#x200B; Advertentie laadt &#x200B;](sm-ads.md) | `videoadload` |
| [&#x200B; MVPD &#x200B;](sm-video-metadata.md) | `videomvpd` |
| [&#x200B; Deel van de Dag &#x200B;](sm-video-metadata.md) | `videodaypart` |
| [&#x200B; Advertiser &#x200B;](sm-ads.md) | `videoadadvertiser` |
| [&#x200B; identiteitskaart van de Campagne &#x200B;](sm-ads.md) | `videoadcampaign` |
| [&#x200B; Genre &#x200B;](sm-video-metadata.md) | `videogenre` |
| [&#x200B; Type van Stroom &#x200B;](sm-core.md) | `videostreamtype` |
| [&#x200B; De Fout IDs van de Fout van de Speler SDK &#x200B;](sm-quality.md) | `videoqoeplayersdkerrors` |
| [&#x200B; Externe Fout IDs &#x200B;](sm-quality.md) | `videoqoeextneralerrors` |
| [&#x200B; Type van Diervoeders van Media &#x200B;](sm-video-metadata.md) | `videofeedtype` |
| [&#x200B; Pad van de Media van de Ingang &#x200B;](entry-dimensions.md) | `entryvideopath` |
| [&#x200B; Uitgang de Weg van Media &#x200B;](exit-dimensions.md) | `exitvideopath` |
| [&#x200B; Genre van de Ingang &#x200B;](entry-dimensions.md) | `entryvideogenre` |
| [&#x200B; Uitgang Genre &#x200B;](exit-dimensions.md) | `exitvideogenre` |
| [&#x200B; De Fout IDs van de Speler van de Ingang SDK &#x200B;](entry-dimensions.md) | `entryvideoqoeplayersdkerrors` |
| [&#x200B; de Fout IDs van de Speler van de Afgang SDK &#x200B;](exit-dimensions.md) | `exitvideoqoeplayersdkerrors` |
| [&#x200B; De Externe van de Ingang identiteitskaarts van de Fout &#x200B;](entry-dimensions.md) | `entryvideoqoeextneralerrors` |
| [&#x200B; Uitgang Externe Fout IDs &#x200B;](exit-dimensions.md) | `exitvideoqoeextneralerrors` |

### Adobe Social

Adobe Social is uitgeschakeld.

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
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
| Insight-type voor eigen definitie | `socialowneddefinitioninsighttype` |
| Insight-waarde voor eigen definitie | `socialowneddefinitioninsightvalue` |
| Eigen definitiemetrisch | `socialowneddefinitionmetric` |
| Element | `socialmediaid` |

### Mobile SDK

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [&#x200B; Eerste Datum van de Lancering &#x200B;](lifecycle-dimensions.md) | `mobileinstalldate` |
| [&#x200B; toepassings identiteitskaart &#x200B;](lifecycle-dimensions.md) | `mobileappid` |
| [&#x200B; Aantal van de Lancering &#x200B;](lifecycle-dimensions.md) | `mobilelaunchnumber` |
| [&#x200B; dagen sinds eerste gebruik &#x200B;](lifecycle-dimensions.md) | `mobiledayssincefirstuse` |
| [&#x200B; dagen sinds laatste Gebruik &#x200B;](lifecycle-dimensions.md) | `mobiledayssincelastuse` |
| [&#x200B; Uur van Dag (SDK) &#x200B;](lifecycle-dimensions.md) | `mobilehourofday` |
| [&#x200B; Dag van Week (SDK) &#x200B;](lifecycle-dimensions.md) | `mobiledayofweek` |
| [&#x200B; Werkend Systeem (SDK) &#x200B;](lifecycle-dimensions.md) | `mobileosenvironment` |
| [&#x200B; dagen sinds laatste verbetering &#x200B;](lifecycle-dimensions.md) | `mobiledayssincelastupgrade` |
| [&#x200B; Lanceringen sinds laatste verbetering &#x200B;](lifecycle-dimensions.md) | `mobilelaunchessincelastupgrade` |
| [&#x200B; Naam van het Apparaat (SDK) &#x200B;](lifecycle-dimensions.md) | `mobiledevice` |
| [&#x200B; Versie van het Werkende Systeem (SDK) &#x200B;](lifecycle-dimensions.md) | `mobileosversion` |
| [&#x200B; Belangrijkste baken &#x200B;](lifecycle-dimensions.md) | `mobilebeaconmajor` |
| [&#x200B; Kleine baken Minder &#x200B;](lifecycle-dimensions.md) | `mobilebeaconminor` |
| [&#x200B; het baken UUID &#x200B;](lifecycle-dimensions.md) | `mobilebeaconuuid` |
| [&#x200B; Beacon Proximity &#x200B;](lifecycle-dimensions.md) | `mobilebeaconproximity` |
| [&#x200B; Plaats (neer aan 10 km) &#x200B;](lifecycle-dimensions.md) | `latlon1` |
| [&#x200B; Plaats (neer aan 100 m) &#x200B;](lifecycle-dimensions.md) | `latlon23` |
| [&#x200B; Plaats (neer aan 1 m) &#x200B;](lifecycle-dimensions.md) | `latlon45` |
| [&#x200B; Punt van de Naam van het Intern &#x200B;](lifecycle-dimensions.md) | `pointofinterest` |
| [&#x200B; Afstand aan Punt van het Centrum van de Rente &#x200B;](lifecycle-dimensions.md) | `pointofinterestdistance` |
| [&#x200B; Nauwkeurigheid van de Plaats &#x200B;](lifecycle-dimensions.md) | `mobileplaceaccuracy` |
| [&#x200B; Plaats Categorie &#x200B;](lifecycle-dimensions.md) | `mobileplacecategory` |
| [&#x200B; identiteitskaart van de Plaats &#x200B;](lifecycle-dimensions.md) | `mobileplaceid` |
| [&#x200B; Invoerbaken Ingang Belangrijk &#x200B;](lifecycle-dimensions.md) | `entrymobilebeaconmajor` |
| [&#x200B; Belangrijkste van het Bebakken van de Uitgang &#x200B;](lifecycle-dimensions.md) | `exitmobilebeaconmajor` |
| [&#x200B; Onderliggend baken van de Ingang 0&rbrace; &#x200B;](lifecycle-dimensions.md) | `entrymobilebeaconminor` |
| [&#x200B; de Kleine Korte Kleine Beacon van de Uitgang &#x200B;](lifecycle-dimensions.md) | `exitmobilebeaconminor` |
| [&#x200B; Ingangsbaken UUID &#x200B;](lifecycle-dimensions.md) | `entrymobilebeaconuuid` |
| [&#x200B; de Beacon UUID van het Beken van de Uitgang &#x200B;](lifecycle-dimensions.md) | `exitmobilebeaconuuid` |
| [&#x200B; Beacon van het Ingang Beacon Proximity &#x200B;](lifecycle-dimensions.md) | `entrymobilebeaconproximity` |
| [&#x200B; Beacon Proximity van de Uitgang &#x200B;](lifecycle-dimensions.md) | `exitmobilebeaconproximity` |

### Adobe Advertising Cloud (AMO)

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AMO EF-ID | `amo_ef_id` |
| AMO-id | `amo_cid` |

### Activity Map

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| [&#x200B; de Verbinding van Activity Map door Gebied &#x200B;](activity-map-link-by-region.md) | `clickmaplinkbyregion` |
| [&#x200B; Activity Map Gebied &#x200B;](activity-map-region.md) | `clickmapregion` |
| [&#x200B; Verbinding van Activity Map &#x200B;](activity-map-link.md) | `clickmaplink` |
| [&#x200B; de Pagina van Activity Map &#x200B;](activity-map-page.md) | `clickmappage` |

### Nielsen Integration

Voor meer informatie over hoe te om deze integratie uit te voeren, zie de [&#x200B; Uitbreiding Nielsen &#x200B;](https://exchange.adobe.com/apps/ec/101361) op Adobe Exchange.

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
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

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Element-id | `aemassetid` |
| Source-element | `aemassetsource` |
| Id van geklikt element | `aemclickedassetid` |
| Item-id | `entryaemassetid` |
| Element-id afsluiten | `exitaemassetid` |

### Adobe Campaign

| Dimension-naam (zichtbaar in analysegebruikersinterface) | Dimension-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Uitgevoerde levering-id van Adobe Campaign | `ac_delivery_internal_name` |
