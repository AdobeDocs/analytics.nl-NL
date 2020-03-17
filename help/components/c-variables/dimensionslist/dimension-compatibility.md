---
title: Compatibiliteit met analytische afmetingen
description: Referentie voor analytische afmetingen en rapporten.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Compatibiliteit met analytische afmetingen

Dit verwijzingsartikel maakt een lijst van dimensies/rapporten die in zowel de Werkruimte van Rapporten &amp; van de Analyse, als in de Werkruimte van de Analyse slechts, en in Rapporten &amp; van Analyse worden gesteund.

Houd er rekening mee dat

* Dit zijn geen limitatieve lijsten. Voor elke rapportsuite is een bepaalde set productvariabelen al dan niet ingeschakeld. Bovendien kan elk rapport een willekeurig aantal aangepaste variabelen bevatten dat is in- of uitgeschakeld of toegewezen aan productvariabelen. We hebben ook bezoekerskenmerken en -classificaties weggelaten, omdat deze uniek zijn voor elke rapportsuite.

* Er zijn enkele gevallen van overlapping, waarbij de analyseprogramma&#39;s verschillende termen gebruiken voor wat in wezen hetzelfde is, bijvoorbeeld: `browserwidth` en `browserwidthbucketed`.

## Dimensies die worden ondersteund in de werkruimte Rapporten en Analyse

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|---|---|
| Analyses voor doel | doelwit |
| Soorten publiek-id | mcaudieen |
| Browser | browser |
| Browsertype | browsertype |
| Categorie | categorie |
| Plaatsen | geocity |
| Kleurdiepte | colordeptie |
| Verbindingstype | connectiontype |
| Cookie-ondersteuning | koekje |
| Landen | geoland |
| Loyalty van klant | klantentrouw |
| Aangepaste conversievars | evar1, evar2, enz. |
| Aangepaste zichtsvariabelen | prop1, prop2, enz. |
| Aangepaste koppeling | customlink |
| Dagen vóór eerste aankoop | daysbefore firstpurchase |
| Dagen sinds laatste aankoop | dayssincelastaankoop |
| Domein | filtereddomein |
| Koppeling downloaden | downloadlink |
| Itempagina | ingang |
| Oorspronkelijke invoerpagina | entrypageoriginal |
| Koppeling afsluiten | exitlink |
| Eerste aanraakkanaal | firstTouchchannel |
| Details eerste aanraakkanaal | firstTouchchanneldetail |
| Java ingeschakeld | javaenabled |
| Taal | taal |
| Laatste aanraakkanaal | lasttouchchannel |
| Details laatste aanraakkanaal | lastTouchchanneldetail |
| Variabelen weergeven | listvariables |
| Marketingkanaal | marketingkanaal |
| Ondersteuning voor mobiele audio | mobileaudiosupport |
| Mobiele vervoerder | mobiel |
| Kleurdiepte mobiel | mobiel-hoekig |
| Ondersteuning voor mobiele cookies | mobilecookiekiesupport |
| Mobiel apparaat | mobiledevicename |
| Type mobiel apparaat | mobiledevicetype |
| Maximale e-maillengte voor mobiele apparaten | mobiele lengte |
| Ondersteuning voor mobiele images | mobileimagesupport |
| Mobiele fabrikant | mobiele fabrikant |
| Mobiel besturingssysteem (afgekeurd) | mobileos |
| Hoogte mobiel scherm | mobiescreenhoogte |
| Grootte mobiel scherm | mobiescreenformaat |
| Breedte mobiel scherm | mobiescreenbreedte |
| Maximale URL browser voor mobiel | mobiele lengte |
| Ondersteuning voor mobiele video | mobilevideo-ondersteuning |
| Monitorresolutie | monitorresolutie |
| Besturingssystemen | operateringssysteem |
| Origineel verwijzingsdomein | referringdomainoriginal |
| Pagina | page |
| Pagina&#39;s niet gevonden | pagesnotfound |
| Product | product |
| Referenter | referentie |
| Type referentie | referertype |
| Referentiedomein | verwijzingsdomein |
| Regio&#39;s | georegio |
| Geretourneerde frequentie | retourfrequentie |
| SC-TnT | tntbase |
| Zoekmachine | zoekmachine |
| Trefwoord zoeken | searchenginekeyword |
| Zoekmachine - Natuurlijk | zoekmachine |
| Zoekmachine - Betaald | doorzoekster |
| Trefwoord zoeken - Natuurlijk | searchenginenaturaltrefwoord |
| Trefwoord zoeken - Betaald | searchenginepaidtrefwoord |
| Alle zoekpaginanummers | doorzoekenginepagerank |
| Server | server |
| Bezoeken van één pagina | singlepagevisits |
| Sectie Site | plaatsen |
| Tijd besteed per bezoek - korrelig | sitetijd |
| Trackingcode | campagne |
| US DMA | geodma |
| VS | state |
| Tijd voorafgaand aan gebeurtenis | tijdvoorafgaande |
| Tijd besteed per bezoek - Emmerd | tijdsbestek |
| Diepte bezoeken | padlengte |
| Bezoek nummer | bezoeker |
| Postcode | zip |

## Dimensies die alleen worden ondersteund in de analysewerkruimte

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AM/PM | timepartampm |
| Browserhoogte - Emmerd | browserheightbuckted |
| Browserbreedte - Emmerd | browserwidthbuckted |
| Dag | daterangeday |
| Dag van Maand | timepartdayfor |
| Weekdag | dag |
| Weekdag | timepartday-week |
| Dag van het Jaar | tijdsbestek |
| Dagen sinds laatste bezoek | dayssincelastbezoek |
| Aangepaste informatie invoeren | entryprops |
| Itemlijstvariabelen | entrylistvariables |
| Entry-server | entryserver |
| Sectie voor invoersite | entrysitesecties |
| Aangepaste inzichten afsluiten | exitprops |
| Lijstvariabelen afsluiten | exitlistvariabelen |
| Pagina afsluiten | exitpage |
| Server afsluiten | exitserver |
| Site-sectie afsluiten | exitesecties |
| Hit Depth | hittediepte |
| Type hit | hittype |
| Uur | daterangehour |
| Uur van dag | timeparthourofday |
| Detail marketingkanaal | marketingChannelDetail |
| Minuut | daterangeminute |
| Maximale bladwijzerlengte voor mobiel | mobilebookmarklength |
| Mobiel apparaatnummer | mobiledevicenumber |
| Mobiele DRM | mobiledrm |
| Mobiele informatiediensten | mobileinformatieservices |
| Mobile Java VM | mobilejavavm |
| Decoratie van mobiele e-mail | mobilemaildecoratie |
| Mobiele netprotocollen | mobilenetprotocollen |
| Mobiel pushbericht om te spreken | mobiel |
| Maand | daterangemonth |
| Maand van jaar | timepartmonthofyear |
| Typen besturingssystemen | operatingssystemgroup |
| Betaalde zoekopdracht | doorzoeken |
| Ondersteuning voor continue cookies | aanhoudend cookie |
| Kwart | daterangetisch |
| Kwartaal van jaar | tijdparttimetrafjaar |
| Enquête | landmeter |
| Tijd besteed op pagina - Emmerd | gemiddelde pagina |
| Tijd besteed op pagina - korrelig | pagetimeseconds |
| Reden voor reeksspatiëring | optoverraad |
| Weekdag/Weekend | timepartweekagavond |
| Week | daterangeweek |
| Jaar | daterangejaar |

## Afmetingen waarbij de inhoud behouden blijft, worden alleen ondersteund in de analysewerkruimte

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Activiteitenkaart XY | clickMapxy |
| Mediasessie-id | videosessionid |
| Nielsen Access-methode | nielsenaccmethod |
| Nielsen App ID | nielsenappid |
| Nielsen Channel Asset | nielsenchannelelement |
| Nielsen-inhoudstype | nielsencontenttype |

## Afmetingen worden alleen ondersteund in rapporten en analyses

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Browserhoogte | browserhoogte |
| Browserbreedte | browserbreedte |
| Dagelijkse unieke klanten | alleenstaande klanten |
| JavaScript | javascriptsupport |
| JavaScript-versie | javascriptversion |
| Maandelijkse unieke klanten | monthlyuniqueklanten |
| Driemaandelijkse unieke klanten | driekwart-unieke-klanten |
| Tijdzones | tijdzone |
| Domeinen op hoofdniveau | topleveldomain |
| Bezoekende staat | legacystate |
| Wekelijks unieke klanten | weeklyuniqueklanten |
| Jaarlijkse unieke klanten | eenwaardige klanten |

## Vooraf geconfigureerde rapporten in rapporten en analyses

Rapporten &amp; Analytics bevat veelvoudige pre-gevormde rapporten die of niet aan een specifieke dimensie in kaart brengen, of het rapport gebruikt een klasse van dimensies. Deze rapporten worden hier weergegeven:

* URL-lengte bladwijzer
* Browsers
* Browsertypen
* Kampeerconversietrechter
* Kanaal voor omzetting van winkelwagentje
* Plaatsen
* Klikt op pagina
* Landen
* Crossverkoop
* Functie Aangepaste gebeurtenissen
* Ondersteuning voor Decoration Mail
* Apparaatnummeroverdracht (AAN/UIT)
* Domeinen
* DRM
* Itempagina&#39;s
* Pagina&#39;s afsluiten
* Fallout
* Volledige paden
* ICities
* Informatiediensten
* Java-versie
* Talen
* Langste paden
* Mediagelijktijdige viewers
* Media Daypart
* Details media
* Overzicht van media
* Monitorresoluties
* Netto protocollen
* Netscape-plug-ins
* Volgende pagina
* Volgende paginastroom
* Besturingssystemen
* Typen besturingssystemen
* Paginadiepte
* Paginaoverzicht
* PathFinder
* Vorige paginastroom
* Vorige pagina
* PTT
* Producten conversietrechter
* Conversietrechter aanschaffen
* Refererende domeinen
* Regio&#39;s
* Opnieuw laden
* Zoekmotoren - Alles
* Zoekprogramma&#39;s - Natuurlijk
* Zoekmotoren - Betaald
* Trefwoorden zoeken - Alles
* Trefwoorden zoeken - Natuurlijk
* Trefwoorden zoeken - Betaald
* Details doelactiviteit
* Tijd besteed op pagina
* Tijdzones
* Domeinen op hoofdniveau
* U.S. DMA
* Amerikaanse staten
* Bezoek nummer
* Homepage van bezoeker

## De inhoud-bewuste afmetingen die door zowel Rapporten &amp; Analytics als de Werkruimte van de Analyse worden gesteund

### Video (Media Analytics)

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Inhoud | video |
| Segment Inhoud | videosegment |
| Inhoudstype | videocontenttype |
| Naam van advertentiespeler | videoadplayernaam |
| Positie advertentie in pod | videoadinpod |
| Gedropte frames | videoqoedroppedframecountevar |
| Fouten | videoqoeerrorcountevar |
| Gemiddelde bitsnelheid | videoqoebitrateaverageevar |
| Wijzigingen in bitsnelheid | videoqobitratechangecountevar |
| Totale bufferduur | videoqoebuffertimeevar |
| Buffergebeurtenissen | videoqoebuffercountevar |
| Te starten tijd | videoqoetimetostartevar |
| Advertentiepod | videoadpod |
| Mediapad | videopath |
| Advertentie | video |
| Naam van inhoudspeler | videoplayernaam |
| Inhoudskanaal | videokanaal |
| Hoofdstuk | videohoofdstuk |
| Inhoudsnaam (variabele) | videonaam |
| Content Length (variable) | videolengte |
| Advertentienaam (variabele) | videoadname |
| Ad Length (variabel) | videoadlength |
| Tonen | videoshow |
| Seizoen | videoseizoen |
| Episode | videoaflevering |
| Netwerk | videonetwerk |
| Tekst tonen | videoshowtype |
| Advertentieladingen | videoadload |
| MVPD | videomvpd |
| Dagdeel | videodagverblijf |
| Adverteerder | videoadverteerder |
| Campagne-id | videocampagne |
| Genre | videogene |
| Type stream | videostreaming |
| Fout-id&#39;s van speler-SDK | videoqoeplayersdkerrors |
| Externe fout-id&#39;s | videoTextExtendedError |
| Type mediafeed | videofeedtype |
| Pad naar instapmedium | entryvideopath |
| Mediapad afsluiten | exitvideopath |
| Genre item | enteryvideogene |
| Exit Genre | exitvideogene |
| Invoer Player SDK-foutmeldingen | entryvideoPlayPlayerDkerrors |
| Fout-id&#39;s van speler-SDK afsluiten | exitvideoQueplayersdkerrors |
| Externe fout-id&#39;s invoeren | entryvideoExtensionError |
| Externe fout-id&#39;s afsluiten | exitvideoquExtensionError |

### Adobe Social

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Voorwaarden | sociaal |
| Sociale platforms/eigenschappen | socialcontentprovider |
| Auteurs | socialisten |
| Taal | sociaal |
| Breedtegraad/lengtegraad | sociaal |
| Codes voor het bijhouden van elementen | socialassettrackingcode |
| Eigendom van sociale eigenschappen | socialaccountandappels |
| ID&#39;s van eigenlijke berichten | socialisten |
| Eigendom van sociale definities | socialinteractietype |
| Eigenschap-id&#39;s in eigendom | socialownpropertyid |
| Eigendom van eigenschap versus toepassing | socialownpropertyPropertyapp |
| Eigenschapnaam in eigendom | socialownpropertyname |
| Eigendom van definitie versus Post | socialowndefintionpropertyvspost |
| Eigen definitietype | socialowndefinedDefinitionIntentType |
| Waarde van eigen definitietoezicht | socialownDefinitionInghtvalue |
| Eigen definitiemetrisch | socialowndefintionmetrisch |
| Element | sociaal-mediant |

### Mobile SDK

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Eerste startdatum | mobiele installatiedatum |
| Toepassings-id | mobileappid |
| Startnummer | mobilelaunchnumber |
| Dagen sinds eerste gebruik | mobiledayssincefirstuse |
| Dagen sinds laatste gebruik | mobiledayssincelastuse |
| Uur van de Dag (SDK) | mobilehourofday |
| Dag van de week (SDK) | mobiledayofweek |
| Besturingssysteem (SDK) | mobiele omgeving |
| Dagen sinds laatste upgrade | mobiledayssincelastupgrade |
| Starten vanaf laatste upgrade | mobilelaunchessincelastupgrade |
| Apparaatnaam (SDK) | mobileapparaat |
| Versie besturingssysteem (SDK) | mobileosversion |
| Beacon Major | mobilebeaconmajor |
| Beacon Minor | mobilebeaconminor |
| Beacon UUID | mobilebeaconuid |
| Beacon-nabijheid | Moblebeaconproximiteit |
| Locatie (tot 10 km) | latlon1 |
| Locatie (tot 100 m) | latlon23 |
| Locatie (tot 1 m) | latlon45 |
| Naam van belangenpunt | pointofinterest |
| Afstand tot belangencentrum | pointofinterestdistance |
| Nauwkeurigheid van locatie | mobiele plaatsnauwkeurigheid |
| Categorie plaatsen | mobiele-placecategorieën |
| Id plaatsen | mobileplaceid |
| Entry Beacon Major | entrymobilebeaconmajor |
| Bandbakenmais afsluiten | exitmobilebeaconmajor |
| Invoerbaken, klein | entrymobilebeaconminor |
| Minder baken afsluiten | exitmobilebeaconminor |
| Entry Beacon UUID | entrymobilebeaconuid |
| UUID van Beacon afsluiten | exitmobilebeaconuid |
| Invoerbaken nabijheid | entrymobilebeaconproximiteit |
| Nabijheid van baken afsluiten | exitmobilebeaconproximiteit |

### Adobe Advertising Cloud (AMO)

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| AMO EF-ID | amo_ef_id |
| AMO-id | amo_cid |

### Activiteitenkaart

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Koppeling activiteitenoverzicht per regio | clickmaplinkbyregion |
| Activiteitenkaartgebied | clickmapregion |
| Koppeling naar activiteitenoverzicht | klikmaplink |
| Pagina Activiteitenkaart | klikmap |

### Nielsen Integration

Zie [Nielsen-partnerschap](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/nielsen-partnership.html)voor meer informatie over hoe u deze integratie kunt implementeren.

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Nielsen AdModel | nielsenadmodel |
| Nielsen Segment C | nielsensegmentatie |
| Nielsen Segment B | nielsensegmentator |
| Nielsen Segment A | nielsensegmentatie |
| Nielsen Content ID | nielsencontentid |
| Nielsen Asset/Program | nielsenelement |
| Nielsen VCID | nielsenvcid |
| Nielsen Opt Out | nielsenoptout |
| Nielsen Client ID + VCID | nielsenclientidvcid |
| Nielsen Client ID | nielsenclientid |
| Ingang Nielsen Weigeren | entrynielsenoptout |
| Nielsen afsluiten Opt Out | exitnielsenoptout |
| Ingang Nielsen Client ID + VCID | entrynielsenclientidvcid |
| Nielsen Client ID afsluiten + VCID | exitnielsenclientidvcid |
| Ingang Nielsen Client ID | entrynielsenclientid |
| Nielsen-client-id afsluiten | exitnielsenclientid |

### Adobe Experience Manager (AEM)

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Element-id | aemassetië |
| Middelbron | amassetbron |
| Id van geklikt element | aemclickedassetiek |
| Item-id | entryaemassetid |
| Element-id afsluiten | exitatie |

### Adobe-campagne

| Naam van dimensie (zichtbaar in de gebruikersinterface van Analytics) | Dimensie-id (wordt gebruikt in API-aanvragen) |
|--- |--- |
| Leverings-id voor Adobe Campagne uitgevoerd | ac_delivery_internal_name |
