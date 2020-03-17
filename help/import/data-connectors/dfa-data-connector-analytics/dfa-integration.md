---
description: 'Het vormen van de integratie DFA impliceert de volgende taken '
keywords: DFA
title: DFA-integratie
topic: Data connectors
uuid: 972a9d62-24fd-4463-a34c-5ec0b926e81e
translation-type: tm+mt
source-git-commit: ''

---


# DFA-integratie{#dfa-integration}

Het vormen van de integratie DFA impliceert de volgende taken:

## De DFA-integratie configureren{#configure-the-dfa-integration}

Stap door de Integratie van DFA-gegevensconnectors.

De configuratiepagina&#39;s bieden een overzicht van de integratie, samen met nuttige koppelingen voor meer informatie. Aan deze integratie zijn Adobe- en DoubleClick-kosten gekoppeld. Neem contact op met de desbetreffende vertegenwoordigers van de verkoper voor beide organisaties en zorg ervoor dat u de structuur van de kosten begrijpt.

1. Meld u aan bij de [!DNL Adobe Analytics].
1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**.

   ![](assets/data_connectors.png)

1. Zoek **[!UICONTROL DoubleClick DFA]** en klik op **[!UICONTROL Add New]**.

   ![Stap resultaat](assets/wizard-01.png)

   Voor elke pagina van de Tovenaar van de Integratie, verstrek de vereiste informatie, dan klik **[!UICONTROL Next]**. De volgende lijst verklaart de informatie u de integratie door de tovenaar moet voltooien.

<table id="table_8F6F7F304C36431DA5FD6E5D54F60FC0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wizard Paginanummer </th> 
   <th colname="col2" class="entry"> Veld </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> Integratienaam </td> 
   <td colname="col3"> De integratienaam die Genesis in de Actieve Lijst van de Integratie van de rapportreeks toont. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> E-mailadres voor integratie </td> 
   <td colname="col3"> Het e-mailadres dat alle meldingen met betrekking tot deze integratie ontvangt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Gebruikersnaam </td> 
   <td colname="col3"> De DFA API-gebruikersnaam die bij deze integratie moet worden gebruikt. Als u een gebruiker wilt inschakelen voor de API-aanmelding, controleert u het API-kenmerk in de DFA-interface. Nadat u de API-aanmelding hebt ingeschakeld, wordt een wachtwoordveld weergegeven met een wachtwoord voor de gebruiker. Dit wachtwoord wordt samen met de gebruikersnaam ingevoerd in de wizard voor verificatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Wachtwoord </td> 
   <td colname="col3"> Het DFA API-wachtwoord. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Adverteerder-id </td> 
   <td colname="col3"> <p>De DFA-adverteerder-id of de bovenliggende Floodlight Configuration-id. Gegevensconnectors gebruiken deze id om de DFA-adverteerder te identificeren die moet worden bijgehouden (versie 1.5 van de integratie). Deze Advertiser-id wordt niet gebruikt in versie 2.0 van de integratie. De bovenliggende Floodlight-configuratie-id wordt opgezocht en gebruikt. Zie de instructies op het scherm </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 </td> 
   <td colname="col2"> DFA Ad Variable </td> 
   <td colname="col3"> De Analyse Var die DFA campagnerekenmerk, impressions, ontvangt en gegevens klikt. Doorgaans is dit de eVar van de Code van het Volgen ( <span class="varname"> s.campagne </span>), maar u kunt om het even welke beschikbare eVar kiezen. Gegevensconnectors voegen ook de volgende DFA-gerelateerde classificaties toe aan de geselecteerde eVar: <p><b>Campagnes</b>: Een inzameling van advertenties die aan veelvoudige plaatsen worden gediend die gemeenschappelijk overseinen dragen. </p> <p><b>Sitenaam</b>: De locatie waar de advertentie werd aangeboden. </p> <p><b>Advertentienaam</b>: De Advertentienaam, zoals die in uw DFA rekening wordt bepaald. </p> <p><b>Naam</b>plaatsing site: De website en de pagina waarop de advertentie is geplaatst. </p> <p><b>Leveringsgereedschap</b>: Dubbelklik voor adverteerders. </p> <p><b>Kanaal</b>: Banner Ad. </p> <p><b>Kostenstructuur</b>: CPM, CPC, of Vast, die op de kostenstructuur van de advertentie wordt gebaseerd. </p> <p><b>Creatieve naam</b>: De naam van de creatieve id die is gekoppeld aan een advertentie-/plaatsing-/creatieve id. </p> <p><b>DFA &gt; Zoekmiddeldeduplicatie</b>: Geeft aan dat DFA waarden moet plaatsen in variabelen van het zoekcentrum wanneer DFA-doorklikbewerkingen of View-through plaatsvinden. </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Impressies </td> 
   <td colname="col3"> De gebeurtenis van de Douane die DFA Impressions metrische gegevens ontvangt. De beelden wijzen op het aantal tijden de advertentie werd gediend. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Klikken </td> 
   <td colname="col3"> Selecteer de douaneGebeurtenis die DFA ontvangt klikt metrische gegevens. Klik op het aantal keren dat bezoekers op de advertentie hebben geklikt, gemeten aan de hand van de omleiding van DFA. De metrische correleert van Klik met metrische analytische kringloop. <p>Opmerking:  DFA-klikken en analytische doorklikbewerkingen komen mogelijk niet exact overeen vanwege verschillen in de manier waarop gegevens worden verzameld.  </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Doorkijkvariabele </td> 
   <td colname="col3"> <p>De Analyse Var die DFA mening-door gegevens ontvangt. Met de variabele Weergave-via kunt u zien hoe weergaven de conversietarieven op uw site beïnvloeden. </p> <p>Gegevensconnectors voegen dezelfde DFA-gerelateerde classificaties toe aan deze eVar als aan de DFA Ad Variable (zie hierboven). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Tijd sinds laatste mening (mening-door tijdsegment variabele) </td> 
   <td colname="col3"> De analytische variabele die DFA-tijd vanaf laatste weergavegegevens ontvangt. De tijd sinds Laatste Mening wijst op de hoeveelheid tijd die sinds laatste en mening-door is verlopen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Weergavedoorvoer </td> 
   <td colname="col3"> De gebeurtenis van de Douane die DFA mening-door metrische gegevens ontvangt. Gebruik de mening-door gebeurtenis met de Beeld-door Variabele om te zien welke campagnes geen directe doorklikken-door beïnvloedden, maar een rol in het drijven van verkeer aan de plaats in één of andere verdere tijd kunnen hebben gespeeld. <p>Gegevensconnectors wijzigen de naam van de geselecteerde aangepaste gebeurtenis in 'Doorheen kijken'. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> DFA-query mislukt </td> 
   <td colname="col3"> (Optioneel) De Analyse Var die berichtcodes voor DFA-queryfouten ontvangt. Mogelijke DFA-berichtcodes zijn: 
    <ul id="ul_85FC7FB19F7F4ADF83ABCA6DDB44CE19"> 
     <li id="li_0A3181DED5A149588A0D3F1584E2FE8B"><b>nc</b>: Geen dubbelklikken op cookie. </li> 
     <li id="li_D397AA73AD5E4086A18B87F271E4EC14"><b>o</b>: Gebruiker heeft zich afgemeld. </li> 
     <li id="li_5AC1D0C8049340B4AD857D88E275CBD6"><b>nh</b>: Geen campagnegeschiedenis. </li> 
     <li id="li_73A8C5E905C54E2BB531A1FCDBC6AA1A"><b>qe</b>: Query-fout (time-out, server-down, enz.) </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> Timeout-gebeurtenis </td> 
   <td colname="col3"> <p>De gebeurtenis van de Teller van de Analyse die elke keer stijgt de <span class="varname"> s.maxDelay </span> tijdopnemer verloopt, en geen reactie werd ontvangen van de servers DFA. Gebruik deze gebeurtenis om de <span class="varname"> s.maxDelay </span> veranderlijke het Tunnen s.maxDelay </a>. te vormen) </p> </td> 
  </tr> 
 </tbody> 
</table>

## De Updates van de Website voor de Integratie DFA{#web-site-updates-for-the-dfa-integration}

Zodra Genesis uw het rapportreeks van Analytics voor de integratie DFA heeft gevormd, moet u het volgende doen om uw Website en milieu te vormen DFA om de integratie te steunen:

### Cookie-ruimte verifiëren op het domein{#verify-cookie-space-on-the-domain}

Voor de integratie van gegevensconnectors voor DFA moet u een cookie instellen op het domein van de pagina.

Hoewel het zeldzaam is, hebben sommige domeinen de maximumkoekjescapaciteit voor sommige browsers van het Web bereikt. Vermijd beïnvloedend het doorbladeren van een bezoeker ervaring op uw Website, raadpleeg uw netwerkverrichtingen, ontwikkelingsteam, of techniekgroep om te verifiëren dat het toevoegen van een ander koekje aan het domein van de pagina&#39;s die voor de integratie worden gebruikt DFA niet de gebruikerservaring zal beïnvloeden. U moet ook een naam voor het cookie selecteren.

### Werk uw DFA Vraag-Koord Parameter bij{#update-your-dfa-query-string-parameter}

Als u al Ad-campagnes hebt bijgehouden met Adobe Analytics vóór de DFA-integratie, is het mogelijk dat alle campagnes (e-mail, zoekopdracht of banner) dezelfde querytekenreeksparameter gebruiken om de verwijzende campagne-id op de landingspagina te identificeren.

Om te begrijpen wanneer om mening-door en klikgegevens van DFA gegevens voor uw campagnes te verzoeken DFA Ad, moeten de Verbinders van Gegevens identificeren wanneer een bezoeker op een DFA de banneradvertentie van de campagnebanner heeft geklikt. Om dit mogelijk te maken, moet u een onderscheiden vraag-koordparameter aan de het landende pagina URL van de campagne toevoegen DFA Ad zodat kunnen de Verbinders van Gegevens tussen DFA Ad campagnepagina&#39;s en andere pagina&#39;s van de advertentiecampagne onderscheiden die u op uw Website zou kunnen hebben. De `dfa_overrideParam` insteekmodule in JavaScript die wordt gebruikt voor DFA.

>[!CAUTION]
>
>Hoewel de variabele Campagne voor andere campagnes kan worden gebruikt, gebruik het niet voor campagnes DFA. Als u de campagnevariabele op een DFA campagne landende pagina plaatst, kan Adobe geen impressies binden en aan DFA campagne klikken doorklikt. Eenmaal per bezoek controleren Adobe-verzamelingsservers DFA-servers op een eerdere klik- of view-through. Daarom neemt u de DFA-insteekcode alleen op gemeenschappelijke bestemmingspagina&#39;s op om onnodige omleidingen te voorkomen die het laden van pagina&#39;s kunnen vertragen, met name voor gebruikers met tragere internetverbindingen.

## De code van de Gegevensverzameling van uw website bijwerken{#update-your-web-site-s-data-collection-code}

De integratie van Genesis voor DFA maakt gebruik van de DFA Floodlight Configuration ID (dfa_SPOTID), die de consistentie van rapporten tussen DFA en het systeem van de de gegevensinzameling van Adobe verbetert.

> [!NOTE] In een recente release van Google DFA werd de term Spotlight gewijzigd in Floodlight. De JavaScript-parameter `dfa_SPOTID` is benoemd op basis van de Spotlight-terminologie, maar wordt voor beide versies gebruikt.

Om de integratie DFA op uw Website toe te laten, moet u uw code van de gegevensinzameling JavaScript bijwerken door het volgende toe te voegen:

* Module voor DFA integreren
* Toevoeging aan uw Code van de Inzameling

### Module voor DFA integreren {#section-fa00e42a732a4e27a4ab3dfcfeae1a5b}

De DFA-integratie maakt gebruik van de Adobe Experience Cloud Integrate Module, die functionaliteit toevoegt aan uw kerncode voor het verzamelen van JavaScript-gegevens ( `s_code.js`). De module Integrate maakt deel uit van het ZIP-bestand wanneer u de AppMeasurement for Javascript-code downloadt van de codecanager. Neem alleen contact op met uw Adobe Consultant als u meer hulp nodig hebt.

Voeg de integrate Module-code in de `Modules` sectie van het `s_code.js` bestand van uw website in.

### Toevoeging aan uw Code van de Inzameling {#section-8f98c727f1ba414fb8b4f02d696b8791}

Op basis van uw selecties tijdens het activeren van de DFA-integratie in de wizard Integratie, genereren gegevensconnectors een aangepaste toevoeging aan uw JavaScript-code voor gegevensverzameling en e-mailen deze. Voeg deze code in de hoofdsectie van het `s_code.js` bestand in (niet in de `doPlugins` functie of een andere functie).

De voorbeeldcode hieronder is alleen ter illustratie; gebruik de code die aan u werd gemaild nadat u de Tovenaar van de Integratie van Verbindingen van Gegevens voltooide.

De verzamelingscode bestaat uit de volgende componenten:

* Instellingen DFA-integratie
* Vereiste insteekmodules voor integratie

**Instellingen DFA-integratie**

```
/************************** DFA VARIABLES **************************/ 
var dfaConfig = { 
   CSID:              "1234567", 
   SPOTID:            "29876543", 
   tEvar:             "eVar17", 
   errorEvar:         "eVar59", 
   timeoutEvent:      "event76", 
   requestURL:         "http://fls.doubleclick.net/ 
json?spot=[SPOTID]&src=[CSID]&var=[VAR]&host=integrate.112.2o7.net%2 
Fdfa_echo%3Fvar%3D[VAR]%26AQE%3D1%26A2S%3D1&ord=[RAND]", 
 
   maxDelay:          "1500", 
   visitCookie:       "s_dfa", 
   clickThroughParam: "CID", 
   searchCenterParam: "s_kwcid", 
   newRsidsProp:      undefined 
}; 
/************************ END DFA Variables ************************/ 
```

Het DFA Integate Instellingenblok stelt variabelen in die vereist zijn voor de DFA-integratie. De waarden voor elk van deze variabelen zijn afkomstig uit de volgende bronnen:

**CSID**: Client Side ID. Gegenereerd door DFA zodra u de Tovenaar van de Integratie voltooit. Gegevensconnectors vullen deze variabele vooraf met uw DFA CS-id in en sturen u deze waarde ook in de e-mail met setup nadat u de wizard Integratie hebt voltooid. Deze variabele is niet vereist als Advanced Ad Serving is ingeschakeld voor uw account.

**SPOTID**: Vullight-configuratie (voorheen Spotlight-id). Gegevensconnectors vullen deze variabele vooraf in met uw DFA Floodlight Configuration-id, op basis van de DFA-accountinformatie die u hebt opgegeven in de wizard Integratie.

**Gebeurtenis**: Overdrachtsvariabele. De Verbindingen van gegevens vullen deze variabele met de veranderlijke naam van Analytics vooraf in u voor de Mening-Door variabele in de Tovenaar van de Integratie specificeerde. Wijzig deze waarde niet zonder zorgvuldige coördinatie met Adobe Engineering of Engineering Services.

**errorEvar**: Foutvariabele. Gegevensconnectors vullen deze variabele vooraf in met de variabelenaam Analytics die u voor de variabele DFA-query-fout hebt opgegeven in de wizard Integratie.

**timeoutEvent**: Time-outgebeurtenis. Gegevensconnectors vullen deze variabele vooraf met de variabelenaam Analytics die u voor de variabele Timeout Event in de Tovenaar van de Integratie hebt opgegeven.

**requestURL**: De externe DFA-host waarop kan worden gezocht naar advertentiegegevens. Wijzig deze waarde alleen in opdracht van Adobe.

**maxDelay**: Hier geeft u op hoe lang de JavaScript-code voor gegevensverzameling wacht op een reactie van de DFA Floodlight-server, in milliseconden. Adobe raadt u aan met deze waarde te experimenteren om de optimale waarde te vinden op basis van het verkeer van uw site. Als u deze waarde verhoogt, worden over het algemeen meer DFA-gegevens verzameld, maar neemt het risico toe dat de gegevens van de basisbezoeker verloren gaan als de bezoeker de site verlaat tijdens de vertragingsperiode. Als u deze waarde verlaagt, loopt u minder risico dat raakgegevens verloren gaan, maar wordt minder DFA-gegevens verzonden met de raakgegevens van Adobe.

**visitCookie**: De naam van het cookie dat wordt gebruikt om DFA-aanroepen te beperken tot eenmaal per bezoek.

**clickThroughParam**: Een queryreeks, die doorgaans wordt opgenomen op alle advertenties, die de module Integrate meedeelt dat er zojuist een klik heeft plaatsgevonden. De aanwezigheid van deze parameter in de querytekenreeks zorgt ervoor dat het verzoek wordt uitgevoerd op DFA Floodlight-servers, ongeacht of de bezoeker al in de laatste 30 minuten was gevraagd.

**newRsidsProp**: (Optioneel) Toegewezen aan een ongebruikte variabele van het type Traffic-eigenschap. De integratie DFA verzamelt en slaat deze waarde in het bezoekcookie op om de rapportsuites te identificeren die gegevens voor een bepaalde bezoeker verzamelden. Deze eigenschap is alleen nodig bij aangepaste implementaties met Adobe Engineering-services.

**Vereiste plug-ins voor integratie**

De toevoeging van de Code van de Inzameling omvat extra stop-ins die de verrichting van de integratie DFA verbeteren:

* Beperkt DFA-query&#39;s tot eenmaal per bezoek
* Biedt flexibiliteit voor cookienamen. Hoewel de meeste organisaties s_dfa gebruiken, kunt u om het even welke geldige koekjesnaam voor de integratie gebruiken DFA.
* Hiermee verwijdert u overbodige omleidingen. Omdat doorkijkgegevens in real time worden verzameld, zouden de inzamelingsservers van Adobe en DFA gegevens over elke paginamening potentieel kunnen ruilen. De insteekmodule blokkeert deze gegevensuitwisseling wanneer de informatie niet nodig is.

>[!CAUTION]
>
>Een van de mechanismen die de plug-in gebruikt om onnodige DFA-query&#39;s te voorkomen, is een op domeinen gebaseerd bezoekcookie. Een reeks van het integratierapport die veelvoudige domeinen overspant breidt klik-door en mening-door gegevens uit wanneer de bezoekers domeinen na een DFA-Beïnvloed mening-door of klik-door kruisen.

## Bevestiging een Succesvolle Integratie DFA{#confirming-a-successful-dfa-integration}

Nadat u alle noodzakelijke updates van de Website hebt gemaakt, kunt u een kijker van het netwerkverkeer, zoals Charles*, de Hulpmiddelen van de Ontwikkelaar van Chrome, of Firebug*, gebruiken om te bevestigen DFA met de inzamelingsservers van Adobe communiceert.

Nadat u het DFA-Toegelaten `s_code.js` dossier hebt opgesteld, gebruik de kijker van het netwerkverkeer om de verzoeken tussen DFA en de servers van de de gegevensinzameling van Adobe te bekijken, zoekend het volgende:

* Een verzoek aan de `fls.doubleclick.net/json` dienst van DFA. Deze service reageert mogelijk anders, afhankelijk van de versie van DFA die u gebruikt. Met DFA Integration versie 1.5:

   * Een HTTP 302-omleiding naar [!DNL ad.doubleclick.net]. Hiermee wordt een locatie verzonden: -tag in de reactie met informatie over de advertentiebezoeker.
   * Deze tag Location leidt tot omleiding naar [!DNL integrate.112.2o7.net/dfa_echo]. Deze service vertaalt de informatie over de advertentiebezoeker naar een met JSON (JavaScript Object Notati on) gecodeerde tekenreeks. Deze gegevens worden geretourneerd met een HTTP-respons van 200 OK.

* Met DFA Integration versie 2.0 (Advanced Ad Serving enabled):

   * [!DNL fls.doubleclick.net] zal direct met 200 O.K. antwoorden.

In beide gevallen resulteert een geslaagde aanvraag in een aanvraag naar de Adobe-servers voor gegevensverzameling die de parameter vX bevat, waarbij X uw View-Through Var-nummer is. Deze parameterwaarde heeft de vorm: DFA-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX. Deze tekenreeks bevat gegevens over de laatste klik en de laatste indruk voor de huidige bezoeker.

## Afstemmen s.maxDelay{#tuning-s-maxdelay}

Voor een geslaagde DFA-implementatie moet s.maxDelay voor uw specifieke site worden geoptimaliseerd.

In het algemeen houdt het besluit om meer of minder gegevens te verzamelen een ruil in tussen het verkrijgen van meer DFA-bezoekersgegevens en het in gevaar brengen van het verzamelen van Adobe-bezoekersgegevens. *`s.maxDelay`* Bij een hogere waarde worden meer DFA-bezoekersgegevens *`s.maxDelay`* verkregen, maar (dat te hoog wordt geplaatst) kan de verzameling van Adobe-bezoekersgegevens in gevaar komen. Door de waarde van s.maxDelay te verlagen, worden de gegevens van Adobe-bezoekers verzameld, maar kunnen gegevens van DFA-bezoekers verloren gaan.

*`s.maxDelay`* kapselt meer dan enkel de tijd in netwerkmededeling aan contact DFA in; het staat ook voor browservertragingen bij het branden en evalueren van het JavaScript waarop deze communicatie is gebaseerd. Dit komt omdat de module Integrate de *`s.maxDelay`* tijdopnemer begint nadat het element van HTML in aan DOM heeft opgenomen die de gegevens van de server DFA Floodlight trekt. De hoeveelheid tijd die nodig is om de browser de HTTP-aanvraag te laten starten op basis van dit nieuwe HTML-element, is afhankelijk van andere afbeeldingen of JavaScript-bestanden die tegelijkertijd worden geladen, de snelheid van de bezoekercomputer en specifieke browserimplementaties. Wanneer de JSON-gegevens worden opgehaald van de DFA Floodlight-server, moet het JavaScript bovendien door de browser worden geëvalueerd. Dit wordt opnieuw volledig gecontroleerd door browser en kan worden vertraagd als er grote hoeveelheden code JavaScript gelijktijdig of vele asynchrone verzoeken JavaScript lopen.

Met dit in gedachten, *`s.maxDelay`* moet worden geplaatst afhankelijk van de ingewikkeldheid van de landingspagina plus de hoeveelheid netwerkvertraging met DFA. Op sommige sites kan een manier om de complexiteit te verminderen, de Adobe-verzamelingscode vroeg in het laden van pagina&#39;s afvuren, zodat er minder gebeurt in de browser op het moment dat de Floodlight-server wordt aangevraagd.

De variabele van de Onderbreking wordt absoluut vereist wanneer het stemmen *`s.maxDelay`*, omdat het elke keer wordt verhoogd wanneer de s.maxDelay onderbreking wordt bereikt. Als *`s.maxDelay`* we besluiten of we de waarde willen verhogen of verlagen, raden we u aan dit proces te volgen:

1. Verzamel meerdere dagen gegevens met een bepaalde waarde *`s.maxDelay`* ingesteld.
1. Voer een [!DNL Daily Unique Visitors Report] voor het tijdbereik uit.
1. Voer de procedure uit [!DNL Timeout Event Report] om het aantal time-outs te controleren dat wordt doorlopen. Een time-out wordt slechts eenmaal per bezoeker verzameld.

Nu de cijfers in handen zijn, berekenen

```
Timeout Percentage = [Step 3] / [Step 2] * 100
```

Let op: het time-outpercentage houdt eigenlijk rekening met alle bezoekers van de site. Sommige van deze bezoekers zouden helemaal niet aan DFA gebonden zijn, en daarom is de time-out misleidend. Om deze berekening te verbeteren, zou een andere analyse slechts unieke bezoekers aan pagina&#39;s met de `clickThroughParam` reeks (bijvoorbeeld, `?CID=1`) kunnen overwegen. Dit zal nauwkeuriger zijn.

Als het percentage voor de time-out erg laag is, kunt u het beste verlagen *`s.maxDelay`*. Als het erg hoog is, moet u de waarde verhogen *`s.maxDelay`*. Als u afneemt, *`s.maxDelay`* wilt u het programma opnieuw uitvoeren [!DNL Timeout Report] om ervoor te zorgen dat de time-outs niet drastisch zijn toegenomen. Als u een hogere waarde opgeeft, *`s.maxDelay`* wilt u een pagina uitvoeren [!DNL Page Views Report] om ervoor te zorgen dat de paginaweergaven niet uitvallen als gevolg van verloren gegevens. Telkens wanneer de gegevens *`s.maxDelay`* worden gewijzigd, worden de gegevens gedurende enkele dagen in acht genomen om ervoor te zorgen dat de gegevens een trend vormen, en niet alleen een dagelijkse fluctuatie.

De optimale instelling voor *`s.maxDelay`* is het punt waarop het time-outpercentage wordt geminimaliseerd terwijl Paginaweergaven niet worden uitgeschakeld.

De time-outs zullen naar verwachting afnemen wanneer u naar versie 2.0 van de integratie gaat, vanwege de eliminaties van 302 omleidingen. Aanvankelijke bevindingen met bèta-clients hebben een consistente reductie van de time-outs aangetoond, waardoor meer DFA-gegevens worden verzameld
