---
title: Compatibiliteit met Analytics-afmetingen
description: Referentie voor Analytics-afmetingen en -rapporten.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 8%

---


# Compatibiliteit met Analytics-afmetingen

Deze pagina bevat een overzicht van de afmetingen die worden ondersteund door de respectievelijke Analytics-mogelijkheden.

>[!NOTE]
>
>Namen, classificaties en kenmerken van aangepaste variabelen worden in deze lijst weggelaten. Deze waarden zijn specifiek voor individuele rapportreeksen.

>[!NOTE]
>
>Er zijn enkele overlappingen waarbij Analytics-gereedschappen verschillende termen gebruiken voor vergelijkbare dimensies. Rapporten en Analytics gebruiken bijvoorbeeld `browserwidth` terwijl Analysis Workspace dit gebruikt `browserwidthbucketed`.

## Dimensies die worden ondersteund in zowel Rapporten als Analytics en Analysis Workspace

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|---|---|
| Analytics voor Target | `targetraw` |
| Soorten publiek-id | `mcaudiences` |
| Browser | `browser` |
| Browsertype | `browsertype` |
| Categorie | `category` |
| Plaatsen | `geocity` |
| Kleurdiepte | `colordepth` |
| Verbindingstype | `connectiontype` |
| Cookie-ondersteuning | `cookie` |
| Landen | `geocountry` |
| Klantloyaliteit | `customerloyalty` |
| Aangepaste conversievars | `evar1`, `evar2`enz. |
| Custom Insight Vars | `prop1`, `prop2`enz. |
| Aangepaste koppeling | `customlink` |
| Dagen vóór eerste aankoop | `daysbeforefirstpurchase` |
| Dagen sinds laatste aankoop | `dayssincelastpurchase` |
| Domein | `filtereddomain` |
| Koppeling downloaden | `downloadlink` |
| Itempagina | `entrypage` |
| Oorspronkelijke invoerpagina | `entrypageoriginal` |
| Koppeling afsluiten | `exitlink` |
| Eerste aanraakkanaal | `firsttouchchannel` |
| Details eerste aanraakkanaal | `firsttouchchanneldetail` |
| Java ingeschakeld | `javaenabled` |
| Taal | `language` |
| Laatste aanraakkanaal | `lasttouchchannel` |
| Details laatste aanraakkanaal | `lasttouchchanneldetail` |
| Variabelen weergeven | `listvariables` |
| Marketingkanaal | `marketingchannel` |
| Ondersteuning voor mobiele audio | `mobileaudiosupport` |
| Mobiele aanbieder | `mobilecarrier` |
| Kleurdiepte mobiel | `mobilecolordepth` |
| Ondersteuning voor mobiele cookies | `mobilecookiesupport` |
| Mobiel apparaat | `mobiledevicename` |
| Type mobiel apparaat | `mobiledevicetype` |
| Maximale e-maillengte voor mobiele apparaten | `mobileemaillength` |
| Ondersteuning voor mobiele images | `mobileimagesupport` |
| Mobiele fabrikant | `mobilemanufacturer` |
| Mobiel besturingssysteem (afgekeurd) | `mobileos` |
| Hoogte mobiel scherm | `mobilescreenheight` |
| Grootte mobiel scherm | `mobilescreensize` |
| Breedte mobiel scherm | `mobilescreenwidth` |
| Maximale URL browser voor mobiel | `mobileurllength` |
| Ondersteuning voor mobiele video | `mobilevideosupport` |
| Monitorresolutie | `monitorresolution` |
| Besturingssystemen | `operatingsystem` |
| Origineel verwijzingsdomein | `referringdomainoriginal` |
| Pagina | `page` |
| Pagina&#39;s niet gevonden | `pagesnotfound` |
| Product | `product` |
| Referrer | `referrer` |
| Type referrer | `referrertype` |
| Referentiedomein | `referringdomain` |
| Regio&#39;s | `georegion` |
| Retourfrequentie | `returnfrequency` |
| SC-TnT | `tntbase` |
| Zoekmachine | `searchengine` |
| Trefwoord zoeken | `searchenginekeyword` |
| Zoekmachine - Natuurlijk | `searchenginenatural` |
| Zoekmachine - Betaald | `searchenginepaid` |
| Trefwoord zoeken - Natuurlijk | `searchenginenaturalkeyword` |
| Trefwoord zoeken - Betaald | `searchenginepaidkeyword` |
| Alle zoekpaginanummers | `searchenginepagerank` |
| Server | `server` |
| Bezoeken van één pagina | `singlepagevisits` |
| Sectie Site | `sitesections` |
| Tijd besteed per bezoek - korrelig | `sitetime` |
| Trackingcode | `campaign` |
| US DMA | `geodma` |
| VS | `state` |
| Tijd voorafgaand aan gebeurtenis | `timeprior` |
| Tijd besteed per bezoek - Emmerd | `timespent` |
| Diepte bezoeken | `pathlength` |
| Bezoeknummer | `visitnumber` |
| Postcode | `zip` |

## Afmetingen worden alleen ondersteund in Analysis Workspace

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AM/PM | `timepartampm` |
| Browserhoogte - Emmerd | `browserheightbucketed` |
| Browserbreedte - Emmerd | `browserwidthbucketed` |
| Dag | `daterangeday` |
| Dag van Maand | `timepartdayofmonth` |
| Weekdag | `dayofweek` |
| Weekdag | `timepartdayofweek` |
| Dag van het Jaar | `timepartdayofyear` |
| Dagen sinds laatste bezoek | `dayssincelastvisit` |
| Aangepaste informatie invoeren | `entryprops` |
| Itemlijstvariabelen | `entrylistvariables` |
| Entry-server | `entryserver` |
| Sectie voor invoersite | `entrysitesections` |
| Aangepaste inzichten afsluiten | `exitprops` |
| Lijstvariabelen afsluiten | `exitlistvariables` |
| Pagina afsluiten | `exitpage` |
| Server afsluiten | `exitserver` |
| Site-sectie afsluiten | `exitsitesections` |
| Hit Depth | `hitdepth` |
| Type hit | `hittype` |
| Uur | `daterangehour` |
| Uur van dag | `timeparthourofday` |
| Detail marketingkanaal | `marketingchanneldetail` |
| Minuut | `daterangeminute` |
| Maximale bladwijzerlengte voor mobiel | `mobilebookmarklength` |
| Mobiel apparaatnummer | `mobiledevicenumber` |
| Mobiele DRM | `mobiledrm` |
| Mobiele informatiediensten | `mobileinformationservices` |
| Mobile Java VM | `mobilejavavm` |
| Decoratie van mobiele e-mail | `mobilemaildecoration` |
| Mobiele netprotocollen | `mobilenetprotocols` |
| Mobiel pushbericht om te spreken | `mobilepushtotalk` |
| Maand | `daterangemonth` |
| Maand van jaar | `timepartmonthofyear` |
| Typen besturingssystemen | `operatingsystemgroup` |
| Betaalde zoekopdracht | `paidsearch` |
| Ondersteuning voor continue cookies | `persistentcookie` |
| Kwart | `daterangequarter` |
| Kwartaal van jaar | `timepartquarterofyear` |
| Enquête | `surveybase` |
| Tijd besteed op pagina - Emmerd | `averagepagetime` |
| Tijd besteed op pagina - korrelig | `pagetimeseconds` |
| Reden voor reeksspatiëring | `optoutreason` |
| Weekdag/Weekend | `timepartweekdayweekend` |
| Week | `daterangeweek` |
| Jaar | `daterangeyear` |

## Afmetingen met behoud van inhoud worden alleen ondersteund in Analysis Workspace

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| Mediasessie-id | `videosessionid` |
| Nielsen Access-methode | `nielsenaccmethod` |
| Nielsen App ID | `nielsenappid` |
| Nielsen Channel Asset | `nielsenchannelasset` |
| Nielsen-inhoudstype | `nielsencontenttype` |

## Afmetingen worden alleen ondersteund in Rapporten en Analytics

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Browserhoogte | `browserheight` |
| Browserbreedte | `browserwidth` |
| Dagelijkse unieke klanten | `dailyuniquecustomers` |
| JavaScript | `javascriptsupport` |
| JavaScript-versie | `javascriptversion` |
| Maandelijkse unieke klanten | `monthlyuniquecustomers` |
| Driemaandelijkse unieke klanten | `quarterlyuniquecustomers` |
| Tijdzones | `timezone` |
| Domeinen op hoogste niveau | `topleveldomain` |
| Bezoekende staat | `legacystate` |
| Wekelijks unieke klanten | `weeklyuniquecustomers` |
| Jaarlijkse unieke klanten | `yearlyuniquecustomers` |

## Afmetingen waarbij de inhoud behouden blijft, worden ondersteund door zowel Rapporten als Analytics en Analysis Workspace

### Video (Media Analytics)

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Inhoud | `video` |
| Segment Inhoud | `videosegment` |
| Inhoudstype | `videocontenttype` |
| Naam van advertentiespeler | `videoadplayername` |
| Positie advertentie in pod | `videoadinpod` |
| Gedropte frames | `videoqoedroppedframecountevar` |
| Fouten | `videoqoeerrorcountevar` |
| Gemiddelde bitsnelheid | `videoqoebitrateaverageevar` |
| Wijzigingen in bitsnelheid | `videoqoebitratechangecountevar` |
| Totale bufferduur | `videoqoebuffertimeevar` |
| Buffergebeurtenissen | `videoqoebuffercountevar` |
| Te starten tijd | `videoqoetimetostartevar` |
| Advertentiepod | `videoadpod` |
| Mediapad | `videopath` |
| Advertentie | `videoad` |
| Naam van inhoudspeler | `videoplayername` |
| Inhoudskanaal | `videochannel` |
| Hoofdstuk | `videochapter` |
| Inhoudsnaam (variabele) | `videoname` |
| Content Length (variable) | `videolength` |
| Advertentienaam (variabele) | `videoadname` |
| Ad Length (variabel) | `videoadlength` |
| Tonen | `videoshow` |
| Seizoen | `videoseason` |
| Episode | `videoepisode` |
| Netwerk | `videonetwork` |
| Tekst tonen | `videoshowtype` |
| Advertentieladingen | `videoadload` |
| MVPD | `videomvpd` |
| Dagdeel | `videodaypart` |
| Adverteerder | `videoadadvertiser` |
| Campagne-id | `videoadcampaign` |
| Genre | `videogenre` |
| Type stream | `videostreamtype` |
| Fout-id&#39;s van speler-SDK | `videoqoeplayersdkerrors` |
| Externe fout-id&#39;s | `videoqoeextneralerrors` |
| Type mediafeed | `videofeedtype` |
| Pad naar instapmedium | `entryvideopath` |
| Mediapad afsluiten | `exitvideopath` |
| Genre item | `entryvideogenre` |
| Exit Genre | `exitvideogenre` |
| Invoer Player SDK-foutmeldingen | `entryvideoqoeplayersdkerrors` |
| Fout-id&#39;s van speler-SDK afsluiten | `exitvideoqoeplayersdkerrors` |
| Externe fout-id&#39;s invoeren | `entryvideoqoeextneralerrors` |
| Externe fout-id&#39;s afsluiten | `exitvideoqoeextneralerrors` |

### Adobe Social

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Voorwaarden | `socialterm` |
| Sociale Platforms/eigenschappen | `socialcontentprovider` |
| Auteurs | `socialauthor` |
| Taal | `sociallanguage` |
| Breedtegraad/lengtegraad | `sociallatlong` |
| Codes voor het bijhouden van elementen | `socialassettrackingcode` |
| Eigendom van sociale eigenschappen | `socialaccountandappids` |
| ID&#39;s van eigenlijke berichten | `socialownedpostids` |
| Eigendom van sociale definities | `socialinteractiontype` |
| Eigenschap-id&#39;s in eigendom | `socialownedpropertyid` |
| Eigendom van eigenschap versus toepassing | `socialownedpropertypropertyvsapp` |
| Eigenschapnaam in eigendom | `socialownedpropertyname` |
| Eigendom van definitie versus Post | `socialowneddefinitionpropertyvspost` |
| Eigen definitietype | `socialowneddefinitioninsighttype` |
| Waarde van eigen definitietoezicht | `socialowneddefinitioninsightvalue` |
| Eigen definitiemetrisch | `socialowneddefinitionmetric` |
| Element | `socialmediaid` |

### Mobile SDK

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Eerste startdatum | `mobileinstalldate` |
| Toepassings-id | `mobileappid` |
| Startnummer | `mobilelaunchnumber` |
| Dagen sinds eerste gebruik | `mobiledayssincefirstuse` |
| Dagen sinds laatste gebruik | `mobiledayssincelastuse` |
| Uur van de Dag (SDK) | `mobilehourofday` |
| Dag van de week (SDK) | `mobiledayofweek` |
| Besturingssysteem (SDK) | `mobileosenvironment` |
| Dagen sinds laatste upgrade | `mobiledayssincelastupgrade` |
| Starten vanaf laatste upgrade | `mobilelaunchessincelastupgrade` |
| Apparaatnaam (SDK) | `mobiledevice` |
| Versie besturingssysteem (SDK) | `mobileosversion` |
| Beacon Major | `mobilebeaconmajor` |
| Beacon Minor | `mobilebeaconminor` |
| Beacon UUID | `mobilebeaconuuid` |
| Beacon-nabijheid | `mobilebeaconproximity` |
| Locatie (tot 10 km) | `latlon1` |
| Locatie (tot 100 m) | `latlon23` |
| Locatie (tot 1 m) | `latlon45` |
| Naam van belangenpunt | `pointofinterest` |
| Afstand tot belangencentrum | `pointofinterestdistance` |
| Nauwkeurigheid van locatie | `mobileplaceaccuracy` |
| Categorie plaatsen | `mobileplacecategory` |
| Id plaatsen | `mobileplaceid` |
| Entry Beacon Major | `entrymobilebeaconmajor` |
| Bandbakenmais afsluiten | `exitmobilebeaconmajor` |
| Invoerbaken, klein | `entrymobilebeaconminor` |
| Minder baken afsluiten | `exitmobilebeaconminor` |
| Entry Beacon UUID | `entrymobilebeaconuuid` |
| UUID van Beacon afsluiten | `exitmobilebeaconuuid` |
| Invoerbaken nabijheid | `entrymobilebeaconproximity` |
| Nabijheid van baken afsluiten | `exitmobilebeaconproximity` |

### Adobe Advertising Cloud (AMO)

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AMO EF-ID | `amo_ef_id` |
| AMO-id | `amo_cid` |

### Activity Map

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Koppeling Activity Mappen per regio | `clickmaplinkbyregion` |
| Activity Map | `clickmapregion` |
| Activity Map-koppeling | `clickmaplink` |
| Activity Map-pagina | `clickmappage` |

### Nielsen Integration

Raadpleeg de extensie [Nielsen voor meer informatie over het implementeren van deze integratie](https://exchange.adobe.com/experiencecloud.details.101361.html).

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
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

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Element-id | `aemassetid` |
| Middelbron | `aemassetsource` |
| Id van geklikt element | `aemclickedassetid` |
| Item-id | `entryaemassetid` |
| Element-id afsluiten | `exitaemassetid` |

### Adobe Campaign

| Naam van dimensie (zichtbaar in gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Uitgevoerde levering-id van Adobe Campaign | `ac_delivery_internal_name` |
