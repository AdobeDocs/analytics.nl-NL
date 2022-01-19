---
title: Einde van levensduur voor bronnen van volledige verwerkingsgegevens
description: Redenen voor het einde van de levensduur en vergelijkingen tussen de API voor het invoegen van gegevens in bulk en de gegevensbronnen voor volledige verwerking.
exl-id: 24a44b7a-64fd-4a99-975f-4887f4638812
source-git-commit: 0b31585f5a928d68083764b80f3a08927b407387
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 5%

---

# Einde van levensduur voor bronnen van volledige verwerkingsgegevens

Gedurende verscheidene jaren, lieten de Volledige Bronnen van Gegevens van de Verwerking u toe om raakvlakke gegevens aan Adobe Analytics voor te leggen. Deze gegevens zijn op dezelfde manier verwerkt als gegevens die zijn verzameld via onze JavaScript-bibliotheken en de SDK van de mobiele app. In 2020 heeft Adobe de [API voor het invoegen van bulkgegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md), die de zelfde functies zoals Volledige Gegevensbronnen van de Verwerking, maar met extra eigenschappen uitvoert. Dit onderwerp verstrekt details over extra functionaliteit die door de Invoeging API van Gegevens van het Bulk wordt verstrekt en schetst verschillen in dossierformaten.

Vanaf 25 maart 2021, verhinderde Adobe nieuwe Volledige verbindingen van de Gegevensbronnen van de Verwerking worden gecreeerd. De bestaande verbindingen werden gesteund tot de dienst volledig werd afgekeurd op 31 Januari, 2022. Naast onze standaarddocumentatie bieden we een doorloop van de [stappen nodig voor het verzenden van gegevens via de API voor het invoegen van gegevens in bulk](https://adobe.ly/aabdia).

## Waarom hebben we deze functie aan het einde van de levensduur?

De BDIA (Bulk Data Insertion API) biedt extra functionaliteit en bestrijkt alle gebruiksgevallen die worden ondersteund door Volledige verwerking. U kunt beter werken met de API voor het invoegen van gegevens in bulk.

## Belangrijkste verschillen tussen de volledige gegevensbronnen van de Verwerking en de Invoeging API van de Gegevens van het Bulk

* Bij het invoegen van bulkgegevens kunnen meerdere bestanden worden verzonden die parallel kunnen worden verwerkt. U kunt Bezoekersgroepen gebruiken om de continuïteit van de bezoeker en de toewijzing van de eVar te garanderen.
* De Invoeging van de Gegevens van het bulk heeft gegevensbevestiging evenals fout behandelende mogelijkheden, zo verwijderend sommige administratieve werk van het voorleggen van klapgegevens.
* Bulk gegevens invoegen ondersteunt verschillende opties voor bezoekers-id&#39;s. U kunt zowel de analyse-id als de Marketing Cloud-id verzenden (zie [Identiteitsservice](https://experienceleague.adobe.com/docs/id-service/using/home.html) voor meer informatie). Bovendien kunt u uw eigen id als een [zaaigoed voor het genereren van een ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds).
* De toevoeging van bulkgegevens steunt de Variabelen van Lijst en van de Context- Gegevens.
* De toevoeging van bulkgegevens steunt geen Activity Map gegevens.

## Belangrijkste verschillen in bestandsindeling en inhoud

* De toevoeging van bulkgegevens heeft een aantal extra vereiste gebieden. Zie de [documentatie](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) voor meer informatie.
* Voor continuïteit en attributie van bezoekers moeten rijen binnen bestanden in chronologische volgorde worden gesorteerd. Zie [Bezoekersgroepen](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups) voor meer informatie over de volgorde van bezoekersactiviteiten in verschillende bestanden.
* Voor het invoegen van bulkgegevens moeten bestanden .csv gecomprimeerd zijn in .gzip-indeling.
* BDIA gebruikt &quot;timestamp&quot;in plaats van &quot;date&quot;.

Voor meer details, zie de volgende vergelijking van de gebiedswaarden beschikbaar in de Invoeging van Gegevens van de Bulk (BDIA) en Volledige Gegevensbronnen van de Verwerking (FPDS).

## Vergelijking van de veldwaarden in BDIA en FPDS

| BDIA-variabele | Variabele voor volledige verwerkingskolom | Beschrijving |
| --- | --- | --- |
| amlh | Niet ondersteund | Tip voor Adobe Audience Manager-locatie. |
| browserHeight | browserHeight | Browserhoogte in pixels (bijvoorbeeld 768) |
| browserWidth | browserWidth | Browserbreedte in pixels (bijvoorbeeld 1024) |
| campaign | campagne | Code voor bijhouden van conversiecampagne |
| channel | kanaal | Kanaaltekenreeks (bijvoorbeeld Sectie Sport) |
| colorDepth | colorDepth | Kleurdiepte van monitor in bits (bijvoorbeeld 24) |
| connectionType | connectionType | Verbindingstype van de bezoeker (LAN of modem) |
| contextData.key | Niet ondersteund | Sleutelwaardeparen worden in opgegeven door de koptekst &quot;contextData.product&quot; of &quot;contextData.color&quot; te noemen |
| cookiesEnabled | cookiesEnabled | `Y` of `N` for if the bezoeker supports first-party session cookies |
| currencyCode | currencyCode | Valutacode inkomsten (bijvoorbeeld `USD`) |
| clientID.[customerIDType].authState | Niet ondersteund | De geverifieerde status van de bezoeker. Ondersteunde waarden zijn: 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT of &#39;&#39; (hoofdlettergevoelig). Twee opeenvolgende enkele citaten (&#39;&#39;) veroorzaken dat de waarde wordt weggelaten van het vraagkoord, dat aan 0 vertaalt wanneer de slag wordt gemaakt. Houd rekening met de ondersteunde numerieke waarden voor authState: 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
| clientID.[customerIDType].id | Niet ondersteund | De klant-id die moet worden gebruikt. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
| clientID.[customerIDType].isMCSeed | Niet ondersteund | Of dit het zaad voor identiteitskaart van de Bezoeker van de Marketing Cloud is of niet. Ondersteunde waarden zijn: 0, 1, TRUE, FALSE, &#39;&#39; (hoofdlettergevoelig). Als u 0, FALSE of twee opeenvolgende enkele aanhalingstekens (&#39;&#39;) gebruikt, wordt de waarde weggelaten uit de querytekenreeks. Het customerIDType kan om het even welke alfanumerieke koord zijn, maar zou als case gevoelig moeten worden beschouwd. |
| eVarN | eVarN, d.w.z. `<eVar2>`...`<eVar>` | Naam van conversie-eVar. U kunt maximaal 75 eVars ( eVar1 - eVar75 ) hebben. U kunt de naam van de eVar (eVar12) of een vriendelijke naam (Advertentiecampagne 3) opgeven. |
| events | gebeurtenissen | [Tekenreeks gebeurtenissen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=en#vars), opgemaakt met dezelfde syntaxis als de variabele s.events. Bijvoorbeeld: scAdd,event1,event7 |
| hierN | hierN, d.w.z. `<hier2>`...`</hier2>` | Hiërarchienaam. U kunt maximaal vijf hiërarchieën gebruiken ( hier1 - hier5 ). U kunt de standaardhiërarchienaam opgeven `hier2` of een vriendelijke naam (Yankees). |
| homePage | homePage | Y of N — is de huidige pagina op de homepage van de bezoeker. |
| ipaddress | Niet ondersteund | Het IP-adres van de bezoeker. |
| javaEnabled | javaEnabled | Y of N — Heeft de bezoeker Java ingeschakeld? |
| javaScriptVersion | javaScriptVersion | JavaScript-versie (bijvoorbeeld 1.3). |
| taal | Niet ondersteund | De door de browser ondersteunde taal. Bijvoorbeeld, `en-us`. |
| linkName | linkName | Naam van koppeling. |
| linkType | linkType | Type koppeling. Tot de ondersteunde waarden behoren: `d: Download link`, `e: Exit link`, `o: Custom link`. |
| linkURL | linkURL | HREF of link. |
| list Bijvoorbeeld list2. | Niet ondersteund | Een gescheiden lijst van waarden die worden doorgegeven aan een variabele, en vervolgens worden gerapporteerd als afzonderlijke regelitems voor rapportage |
| marketingCloudVisitorID | Niet ondersteund | Marketing Cloud-id. Zie [Identificatie bezoeker](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en#id-service-api) en de Marketing Cloud Visitor ID Service |
| Niet ondersteund | charSet | De ondersteunde tekenset voor uw website. Bijvoorbeeld UTF-8, ISO-8859-1 enzovoort. |
| Niet ondersteund | clickAction | Object-id voor bezoeker op kaart klikken (oid) |
| Niet ondersteund | clickActionType | Type object-id voor bezoeker op kaart klikken (punt) |
| Niet ondersteund | clickContext | Pagina-id voor bezoeker klikt op kaart (pid) |
| Niet ondersteund | clickContextType | Type pagina-id voor bezoeker op kaart klikken (pidt) |
| Niet ondersteund | clickSourceID | Bronindex voor bezoeker op kaart klikken (oi) |
| Niet ondersteund | clickTag | Naam van objecttag voor bezoeker op kaart klikken (naar) |
| Niet ondersteund | scXmlVer | Marketingrapporten XML aanvraagversienummer (bijvoorbeeld 1.0). |
| Niet ondersteund | tijdzone | De tijdzone van de bezoeker verschuift van GMT in uren (bijvoorbeeld -8). |
| pageName | pageName | Naam van de pagina |
| pageType | pageType | Type pagina (bijvoorbeeld &quot;Foutpagina&quot;). |
| pageURL | pageURL | Pagina-URL (bijvoorbeeld https://www.example.com/index.html). |
| plug-ins | plug-ins | Lijst met namen van plug-ins van browsers, gescheiden door puntkomma&#39;s. |
| products | producten | Lijst met alle producten op de pagina. Scheid producten met een komma. Bijvoorbeeld: Sport;Ball;1;5.95,Speelgoed; Boven;1:1.99. |
| prop1 - prop75 | propN, d.w.z. `<prop2>`...`</prop2>` | Eigenschapcontrole# (bijvoorbeeld Sportsectie). |
| propN | propN | Eigenschapswaarden voor uw eigenschappen. |
| purchaseID | purchaseID | Aankoop-id-nummer. |
| referrer | referentie | URL voor paginaverwijzing. |
| reportSuiteID | s_account | Hier geeft u de rapportsuites op waarin u gegevens wilt verzenden. U zou veelvoudige rapportreeks IDs met een komma moeten scheiden. |
| resolutie | resolutie | Monitorresolutie (bijvoorbeeld 1024x768). |
| server | server | Servertekenreeks. |
| state | state | Conversiestatekenreeks. |
| timestamp | date | De ISO 8601-datumnotatie van YYY-MM-DDThh gebruiken:mm:ss±UTC_offset (bijvoorbeeld, 2021-09-01T12:00:00-07:00 ) of Unix Time Format (het aantal seconden dat is verstreken sinds 1 januari 1970). |
| trackingServer | Niet ondersteund | Kan alleen via kolomkop worden opgegeven. |
| transactionID | Niet ondersteund | Gemeenschappelijke waarde die wordt gebruikt om multikanaalsgebruikersactiviteiten voor rapportagedoeleinden aan elkaar te koppelen. Zie voor meer informatie de [Gebruikershandleiding voor gegevensbronnen](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=en#data-sources). |
| userAgent | Niet ondersteund | Tekenreeks gebruikersagent |
| visitorID | bezoekerID | Analyse-id van bezoeker. Zie [Identificatie bezoeker](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| zip | zip | ZIP-code conversie. |
