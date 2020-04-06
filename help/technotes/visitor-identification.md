---
description: Adobe gebruikt een cookie om unieke browsers/apparaten bij te houden.
keywords: Analytics Implementation
subtopic: Visitors
title: Unieke bezoekers identificeren
topic: Developer and implementation
uuid: ed4dee75-ecfb-4715-8122-461983c7dd8f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Unieke bezoekers identificeren

Adobe gebruikt een cookie om unieke browsers/apparaten bij te houden.

## Bestelling van Bezoeker-id voor analyse {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics biedt verschillende methoden om bezoekers te identificeren. In de volgende tabel worden de verschillende manieren weergegeven waarop een bezoeker kan worden geïdentificeerd in Analytics (in volgorde van voorkeur):

| Volgorde gebruikt | Query-parameter (verzamelingsmethode) | presenteren als |
|---|---|---|
| 1 | vid (s.bezoekerID) | s.bezoekerID is ingesteld |
| 2 | aid (s_vi cookie) | De bezoeker had een bestaand s_vi koekje alvorens u de dienst van identiteitskaart van de Bezoeker uitvoerde, of u hebt een gevormde periode van de gratieperiode van bezoekersidentiteitskaart |
| 3 | mid (AMCV_ cookie ingesteld door Experience Cloud Visitor ID service) | De browser van de bezoeker accepteert cookies (eerste partij) |
| 4 | fid (fallback cookie) | De browser van de bezoeker accepteert cookies (eerste partij) |
| 5 | IP Adres, de Agent van de Gebruiker, IP van de Gateway Adres | De browser van de bezoeker accepteert geen cookies. |

In veel scenario&#39;s zou u 2 of 3 verschillende IDs op een vraag kunnen zien, maar de Analytics zal eerste identiteitskaart van de vorige lijst als officiële bezoekersidentiteitskaart gebruiken. Als u bijvoorbeeld een aangepaste bezoeker-id instelt (opgenomen in de query-parameter &quot;vid&quot;), wordt die id gebruikt vóór andere id&#39;s die op dezelfde hit aanwezig kunnen zijn.

>[!NOTE] Elke Analytics-bezoeker-id is gekoppeld aan een bezoekersprofiel op Adobe-servers. Bezoekersprofielen worden na ten minste 13 maanden inactiviteit verwijderd, ongeacht de vervaldatum van de cookie van de bezoeker.

## Aangepaste bezoeker-id

U kunt een douanemethode uitvoeren om bezoekers te identificeren door de variabele s.bezoekorID te plaatsen.

Een aangepaste bezoeker-id kan worden gebruikt op sites waar bezoekers op een unieke manier kunnen worden geïdentificeerd. Een voorbeeld hiervan is een id die wordt gegenereerd wanneer een gebruiker zich bij de website aanmeldt met een gebruikersnaam en wachtwoord.

Als u de mogelijkheid hebt om de gegevens [!UICONTROL visitor IDs] van uw gebruikers af te leiden en te beheren, kunt u de volgende methoden gebruiken om de id in te stellen:

| Methode | Beschrijving |
|---|---|
| [s.bezoekerID](../implement/vars/config-vars/visitorid.md) variabele | Als JavaScript wordt gebruikt op browser, of als u een andere bibliotheek AppMeasurement gebruikt, kunt u bezoekersidentiteitskaart in een variabele van de gegevensinzameling plaatsen. |
| De tekenreeksparameter van de vraag op het beeldverzoek | Hiermee kunt u de afbeelding [!UICONTROL visitor ID] aan Adobe doorgeven via de [!UICONTROL vid query string] parameter op een aanvraag voor een afbeelding met harde code. |
| API voor gegevensinvoer | Op apparaten die draadloze protocollen gebruiken die JavaScript niet accepteren, kunt u een XML-bericht met het `<visitorid/>` XML-element vanuit uw servers verzenden naar Adobe-verzamelingsservers. |
| URL herschrijven en VISTA | Sommige implementatiearchitecturen bieden ondersteuning voor het herschrijven van URL&#39;s om de sessiestatus te behouden wanneer een cookie niet kan worden ingesteld. In dergelijke gevallen kunnen de technische services van Adobe een [!DNL VISTA] regel implementeren die naar de sessiewaarde in de URL van de pagina zoekt en deze vervolgens opmaakt en in de [!UICONTROL visid] waarden plaatst. |
>[!CAUTION]
>**De aangepaste bezoeker-id&#39;s moeten voldoende korrelig/uniek **zijn: Een ongeldige implementatie van aangepaste Bezoeker-id&#39;s kan leiden tot onjuiste gegevens en slechte rapportprestaties. Als de aangepaste bezoeker-id niet uniek of korrelig genoeg is of onjuist is ingesteld op een algemene standaardwaarde, zoals de tekenreeks &quot;NULL&quot; of &quot;0&quot;, worden de treffers van veel verschillende bezoekers door Adobe Analytics als één bezoeker beschouwd. Deze situatie resulteert in onjuiste gegevens, met bezoekersaantallen te laag zijn en de segmenten werken correct voor die bezoeker. Een onvoldoende korrelige aangepaste bezoeker-id voorkomt ook dat de gegevens op de juiste wijze worden verspreid over knooppunten in de analytische rapportagecluster. In deze situatie, wordt één knoop overbelast en kan rapportverzoeken niet tijdig verwerken. Uiteindelijk zal alle rapportering voor de rapportreeks ontbreken.<br>Slecht geïmplementeerde aangepaste Bezoeker-id&#39;s hebben mogelijk niet direct invloed op de rapportprestaties omdat Analytics vaak een aantal maanden ongebalanceerde gegevens kan verwerken. in de loop der tijd kan een slecht geïmplementeerde aangepaste Bezoeker-id-waarde echter problematisch worden, zodat Analytics de verwerking voor de desbetreffende rapportsuites moet uitschakelen.</br><br>Implementers moeten de richtlijn volgen dat één enkele waarde van identiteitskaart van de douaneBezoeker nooit voor meer dan 1% van het verkeer van uw rapportreeks zou moeten worden gecrediteerd. Hoewel het richtsnoer van 1% voldoende is voor de meeste rapportagevakes, kan de werkelijke limiet die invloed kan hebben op de rapportprestaties lager zijn dan 1% voor zeer grote rapportsuites.</br>

## Bezoeker-id voor analyse

Wanneer een gebruiker uw site bezoekt, wordt een permanente cookie door de Adobe-webserver ingesteld door deze op te nemen in het HTTP-antwoord op de browser. Dit cookie wordt ingesteld op het opgegeven domein voor gegevensverzameling.

Wanneer een aanvraag naar de Adobe-gegevensverzamelingsserver wordt verzonden, wordt de header gecontroleerd op het cookie van de bezoeker-id ( `s_vi`). Als deze cookie in de aanvraag staat, wordt deze gebruikt om de bezoeker te identificeren. Als het cookie zich niet in de aanvraag bevindt, genereert de server een unieke bezoeker-id, stelt deze in als een cookie in de HTTP-antwoordheader en stuurt deze terug met de aanvraag. Het cookie wordt opgeslagen in de browser en wordt teruggestuurd naar de server voor gegevensverzameling tijdens volgende bezoeken aan de site, zodat de bezoeker kan worden geïdentificeerd tijdens verschillende bezoeken.

### Cookies en CNAME-records van derden {#section_61BA46E131004BB2B75929C1E1C93139}

Sommige browsers, zoals Apple Safari, slaan geen cookies meer op die zijn ingesteld in de HTTP-header vanuit domeinen die niet overeenkomen met het domein van de huidige website (dit is een cookie die wordt gebruikt in een context van derden of een cookie van derden). Bijvoorbeeld, als u bent `mysite.com` en uw server van de gegevensinzameling is `mysite.omtrdc.net`, zou het koekje dat in de kopbal van HTTP van is teruggekeerd door browser `mysite.omtrdc.net` kunnen worden verworpen.

Om dit te vermijden, hebben vele klanten CNAME verslagen voor hun servers van de gegevensinzameling als deel van een [eerste-partijkoekjesimplementatie](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/)uitgevoerd. Als een CNAME-record is geconfigureerd om een hostnaam op het domein van de klant toe te wijzen aan de server voor gegevensverzameling (bijvoorbeeld toewijzing `metrics.mysite.com` aan `mysite.omtrdc.net`), wordt het cookie van de bezoeker-id opgeslagen omdat het domein van de gegevensverzameling nu overeenkomt met het domein van de website. Dit verhoogt de waarschijnlijkheid dat het koekje van bezoekersidentiteitskaart zal worden opgeslagen, maar het introduceert wat overheadkosten aangezien u CNAME- verslagen moet vormen en SSL certificaten voor de servers van de gegevensinzameling handhaven.

### Cookies op mobiele apparaten {#section_7D05AE259E024F73A95C48BD1E419851}

Wanneer mobiele apparaten met behulp van cookies worden bijgehouden, kunt u bepaalde instellingen gebruiken om de manier waarop de meting plaatsvindt te wijzigen. Het standaardleven van het cookie is 5 jaar, maar u kunt de variabele van het CL vraagparam ( `s.cookieLifetime`) gebruiken om dit gebrek te veranderen. Gebruik de CDP-queryreeks om de cookielocatie voor naamimplementaties in te stellen `s.cookieDomainPeriods`. De standaardwaarde is 2 als er geen waarde is opgegeven. en de standaardlocatie is domain.com. Voor implementaties die geen CNAME gebruiken, is de het koekjesplaats van bezoekersidentiteitskaart bij het domein 207.net.

## Identiteitsservice

De Identity Service vervangt het oude mechanisme voor de ID van de bezoeker van Analytics en wordt vereist door [!UICONTROL Heartbeat] videometingen, Analytics voor Target en toekomstige Experience Cloud core-services en -integratie.

Zie [Identiteitsservice](https://marketing.adobe.com/resources/help/en_US/mcvid/) voor productdocumentatie over deze service.

## Mobiele apparaten identificeren

De meeste mobiele apparaten accepteren browsercookies. Wanneer apparaten cookies echter niet accepteren, wordt een andere methode gebruikt om draadloze apparaten op unieke wijze te identificeren.

Adobe heeft een aantal HTTP-headers geïdentificeerd die een groot deel van de mobiele apparaten op unieke wijze identificeren. Die kopballen omvatten vaak het aantal van de apparatentelefoon (of een gehakte versie van het aantal), of andere herkenningstekens. De meeste huidige apparaten hebben een of meer headers die het apparaat uniek identificeren, en alle servers van de gegevensverzameling van Adobe gebruiken deze headers automatisch in plaats van een Bezoeker-id.

In een standaard afbeeldingsverzoek zorgen een &#39;1&#39; in het pad ( `/b/ss/rsid/1`) ervoor dat Adobe-servers een GIF-afbeelding retourneren en proberen een blijvend [!UICONTROL visitor ID] cookie ( `AMCV_` of `s_vi`) in te stellen. Als het apparaat echter wordt herkend als een mobiel apparaat dat is gebaseerd op de HTTP-headers, wordt &#39;5&#39; doorgegeven in plaats van &#39;1&#39;, wat aangeeft dat een afbeelding in de wbmp-indeling moet worden geretourneerd en dat onze lijst met herkende draadloze headers (geen cookie) moet worden gebruikt om het apparaat te identificeren.

In de volgende tabel wordt de volgorde weergegeven van de ID-methoden die worden gebruikt op basis van de waarde voor het retourneringstype (&#39;1&#39; of &#39;5&#39;) in het pad:

<table id="table_07B0E55D5DAA4552A5CBC6937D47A857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Instelling </th> 
   <th colname="col2" class="entry"> Volgorde van ID-methode </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code> /1/</code> </td> 
   <td colname="col2"> <p>Standaard: </p> 
    <ul id="ul_E37E9919658A492C92187BAA18D33AB6"> 
     <li id="li_1A9E39C7CFB24C68AA07C8E85D33A858">Aangepaste bezoeker-id </li> 
     <li id="li_0DC8D17828C848BEB614C6E47C090064">Cookie </li> 
     <li id="li_52706792FAD14F459266E3A672F92EA1">Koptekst abonnee-id </li> 
     <li id="li_ECAD713D22314338BB5C92167DC0BB02"> IP van het adres-GebruikerAgent-Gateway IP Adres </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> /5/ /5.1/ /5.5/</code> </td> 
   <td colname="col2"> <p>Apparaat werd geïdentificeerd als draadloos apparaat, of <code> /5/</code> werd manueel verzonden in het beeldverzoek: </p> 
    <ul id="ul_624BEDFA3E1243CF9B42081D8B8EFFFB"> 
     <li id="li_D65761D23B684DB59BC23E92C9098122">Aangepaste bezoeker-id </li> 
     <li id="li_ADBA806B74CA43EFA8612301E06106C6">Koptekst abonnee-id </li> 
     <li id="li_79DFD0DEAA1242C09A03E8134A40F799">Cookie </li> 
     <li id="li_A462B9120FC6443480D62F37D456747E">IP van de adres-Gebruiker Agent-Gateway IP Adres </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

U kunt ook een &#39;1&#39; of een &#39;5&#39; doorgeven in handmatige afbeeldingsaanvragen, maar houd er rekening mee dat deze codes elkaar uitsluiten. Daarom gebruikt het doorgeven van &#39;5&#39; altijd geen cookie wanneer dit wordt ondersteund. U kunt uw eigen mechanisme opnemen om te bepalen of een apparaat cookies ondersteunt en zo ja, geef een &#39;1&#39; in de afbeelding door in plaats van een &#39;5&#39;. De verbetering van de nauwkeurigheid in deze situatie is beperkt tot het aantal mobiele apparaten dat cookies ondersteunt.

### Kopteksten abonnee-id {#section_60D6EAC0D16945A89DD5A7ADF3B8298D}

De methode van abonneeID is over het algemeen betrouwbaarder dan een cookie voor gebruikersidentificatie vanwege het verwijderen van cookies, problemen met de acceptatie van cookies en problemen met het beheer van gatewaycookies.

U kunt wijzigingen in de identificatie van een bezoeker verbeteren door deze toe te voegen aan de witte lijst voor de provider die uw mobiele bezoekers gebruiken. Als u toegang wilt tot de bezoeker-id van de vervoerder, neemt u contact op met de provider om uw domein toe te voegen aan de witte lijst. Als u op de witte lijst van een drager bent, hebt u ook toegang tot de kopballen van abonneeidentiteitskaart die u anders niet kunt toegang hebben.

De volgende lijst van kopballen wordt gebruikt om draadloze apparaten te identificeren. Het algoritme voor het verwerken van de kopteksten is:

1. extraheer de HTTP-headersleutel (de naam van de header, bijvoorbeeld &quot;X-Up-Calling-Line-ID&quot;)
1. Alle niet-alpha (A-Z en a-z) tekens bijsnijden
1. de headersleutel omzetten in kleine letters
1. vergelijk het einde van de sleutel met die in de volgende tabel om een overeenkomst te vinden:

| Koptekst | Type | Voorbeeld |
|---|---|---|
| callinglineid | ID | X-Up-Calling-Line-ID: 8613802423312 |
| subno | ID | x-up-subno: swm_10448371100_vmag.mycingular.net |
| clientid | ID | ClientID: eGtUpsqEO19zVHmbOkgaPVI-@sprintpcs.com |
| uid | ID | x-jphone-uid: a2V4EE21XQH9ECNN |
| clid | ID | X-Hts_clid: 595961714786 |
| devicide | ID | velg-apparaat-id: 200522ae |
| doorsturen voor | ID of IP-adres | X-Forwarded-For: 127.0.0.1 |
| msisdn | ID of IP-adres | X-Wap-msisdn: 8032618185 |
| clientip | IP-adres | Client-ip: 10.9.41.2 |
| wapipaddr | IP-adres | X-WAPIPADDR: 10.48.2013.162 |
| huaweinasië | IP-adres | x-huawei-NASIP: 211 139 172 70 |
| userip | IP-adres | GebruikerIP: 70 214 81 241 |
| ipaddress | IP-adres | X-Nokia-ipaddress: 212 97 227 125 |
| subscriberinfo | IP-adres | X-SUBSCRIBER-INFO: IP=10.103.132.128 |

Bijvoorbeeld &quot;callinglineid&quot;zou &quot;x-Up-Calling-lijn-identiteitskaart&quot;en &quot;nokia-callinglineid&quot;aanpassen. Het headertype vertelt ons wat we in de koptekst moeten verwachten. De volgorde van headerprioriteit wordt hier weergegeven (als een header &quot;callinglineid&quot; aanwezig is, wordt deze gebruikt in plaats van &quot;subno&quot;).

Met [dynamische variabelen](../implement/vars/page-vars/dynamic-variables.md) kunt u specifieke waarden uit een koptekst extraheren.

## Methoden van Fallback-id

Als andere methoden voor de bezoeker-id mislukken, stelt Adobe een fallback-cookie in of gebruikt het een combinatie van IP-adres en een gebruikersagent om de bezoeker te identificeren.

### Identificatiemethode van Fallback Visitor {#section_2BA15E4FA6034C3EBF43859406343EB6}

AppMeasurement voor JavaScript 1.x en JavaScript H.25.3 (uitgebracht in januari 2013) bevat een nieuwe fallback-identificatiemethode voor bezoekers wier browser het cookie blokkeert dat is ingesteld door de gegevensverzamelingsservers van Adobe (genoemd `s_vi`). Eerder, als een koekje niet kon worden geplaatst, werden de bezoekers geïdentificeerd gebruikend een combinatie van het IP adres en het koord van de gebruikersagent tijdens gegevensinzameling.

Als de standaardcookie niet beschikbaar is in deze update, wordt een fallback-cookie gemaakt op het domein van de website met een willekeurig gegenereerde unieke id. `s_vi` Dit cookie, genaamd `s_fid`, wordt ingesteld met een vervaldatum van 2 jaar en wordt gebruikt als de fallback-identificatiemethode die wordt uitgevoerd. Deze wijziging moet resulteren in een grotere nauwkeurigheid van het bezoek en het aantal bezoekers in situaties waarin het primaire cookie ( `AMCV_` of `s_vi`) niet kan worden ingesteld.

Het totaal van bezoeken omvat alle bezoekers die door het `s_vi` koekje of door een reservemethode worden geïdentificeerd.

### IP Adres, de Agent van de Gebruiker, IP van de Gateway Adres {#section_104819D74C594ECE879144FCC5DEF4BF}

. Als het `AMCV_` of `s_vi` en de `s_fid` koekjes niet kunnen worden geplaatst, worden de bezoekers geïdentificeerd gebruikend een combinatie IP adres en de Agent van de Gebruiker.
