---
title: Opmerkingen bij de release AppMeasurement for JavaScript
description: Cumulatieve releaseopmerkingen voor AppMeasurement for JavaScript.
feature: Appmeasurement Implementation
exl-id: 80b935f0-3ec5-4ffa-9858-f83ae9a6b763
role: Admin, Developer, Leader, User
source-git-commit: 886c6070936275cf1df269a951b87d041fcf7b8c
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 4%

---

# Opmerkingen bij de release AppMeasurement for JavaScript

>[!IMPORTANT]
>
>Vanaf maart 2025 wordt dit artikel niet meer bijgewerkt. U kunt versienota&#39;s voor bekijken en de recentste versie van AppMeasurement van [ GitHub ](https://github.com/adobe/appmeasurement/releases) downloaden.


## Versie 2.27.0

Datum van de versie: **12 augustus, 2024**

* Het `s_ac` -cookie wordt nu geschreven met de `secure` -markering if `writeSecureCookies` is ingeschakeld.
* Initialisatiefout verholpen wanneer de bibliotheek inline is ingesloten.
* Correctie van een fout als `localStorage` of `sessionStorage` is uitgeschakeld.
* De hoge Gebruiker-agent van Entropie Hints zijn nu inbegrepen met verbinding het volgen vraag (`tl`) als `collectHighEntropyUserAgentHints` is toegelaten.

## Versie 2.26.0

Datum van de versie: **Maart 4, 2024**

* AppMeasurement herkent en gebruikt automatisch het hoofddomein voor domeinen op hoofdniveau van landcode, waarvoor eerder specifieke configuraties van het cookiedomein waren vereist. Bijwerken kan gevolgen hebben vanwege deze automatische herkenning. Zie [`cookieDomainPeriods`](/help/implement/vars/config-vars/cookiedomainperiods.md) voor meer informatie.
* De distributie omvat de Bibliotheek van de Dienst van de Identiteit 5.5.0 en Data Integration Library 9.6.

## Versie 2.25.0

Datum van de versie: **12 september, 2023**

* De optionele methode [`bufferRequests()`](vars/functions/bufferrequests.md) is toegevoegd om de betrouwbaarheid van het vastleggen van aanvragen te verbeteren wanneer een browser de API van het baken niet ondersteunt of aanvragen annuleert wanneer een pagina wordt verwijderd.
* Toegevoegde waarborgen om veelvoudige post-spoorcallbacks voor één enkel volgend verzoek te verhinderen.

## Versie 2.24.0

Datum van de versie: **18 juli, 2023**

* De optionele configuratievariabele [`decodeLinkParameters`](vars/config-vars/decodelinkparameters.md) is toegevoegd om koppelings-URL&#39;s met double-byte gecodeerde tekens te decoderen.
* Extra foutafhandeling toegevoegd voor browsers met onjuiste API&#39;s voor client-tips voor gebruikers-agent met hoge entropie.
* De POST Content-Type-header is standaard gewijzigd en gebruikt `x-www-form-urlencoded` .

## Versie 2.23.0

Datum van de versie: **23 September, 2022**

* AppMeasurement biedt nu ondersteuning voor de verzameling van clienttips met een hoge entropie voor gebruikers-agent die Chromium-browsers (Google Chrome en Microsoft Edge) gebruiken om apparaatinformatie te verschaffen. U kunt clienttips configureren via Tags of de configuratievariabele [`collectHighEntropyUserAgentHints`](vars/config-vars/collecthighentropyuseragenthints.md) gebruiken. Verzameling van hints met hoge entropie is standaard uitgeschakeld. Leer meer over gebruiker-agent [ cliëntwenken ](/help/technotes/client-hints.md).

## Versie 2.2.4

Datum van de versie: **18 Januari, 2022**

* De aanroep voor het bijhouden van koppelingen `s.tl()` controleert nu of het object dat eraan wordt doorgegeven, een `href` kenmerk van het type `string` bevat. Als het geen `string` is, negeert het `href` -kenmerk netjes in plaats van te mislukken. Dit scenario kan zich voordoen wanneer u `svg` voorwerpen aan de verbinding het volgen vraag doorgeeft.

## Versie 2.2.2.3

Datum van de versie: **11 Oktober, 2021**

* Bijgewerkte koppelingen in bestanden die verwijzen naar documentatie.

## Versie 2.2.2

Datum van de versie: **7 September, 2021**

* Deze update zorgt ervoor dat `opt.dmp` en `opt.sell` altijd worden opgenomen bij het bijhouden van koppelingen. Zie [ Privacy die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md) meldt in de Admin gebruikersgids voor meer informatie.

## Versie 2.22.1

Datum van de versie: **17 augustus 2021**

* Klanten die opt-out gebruiken hebben de server-side het door:sturen opt-out parameters niet kunnen gezien wanneer het volgen van verbindingen. De correcties in deze release zorgen ervoor dat de markeringen voor niet-deelname worden verzonden als deze aanwezig zijn bij het bijhouden van koppelingen.

## Versie 2.2.2.0

Datum van de versie: **4 augustus 2020**

* Oplossing voor ontbrekende referentie wanneer de eerste melding niet is verzonden vanwege de gebruikersvoorkeuren voor weigeren.

## Versie 2.21.0

Datum van de versie: **24 juni, 2020**

* Probleem verholpen waarbij het Activity Map linkExclusions-filter niet altijd werd toegepast op Firefox.

## Versie 2.20.0

Datum van de versie: **Maart 5, 2020**

* Probleem met betrekking tot beveiliging is opgelost door de Internet Explorer-detectie bij te werken om de JSLint-waarschuwing te onderdrukken.

## Versie 2.19.0

Datum van de versie: **21 februari, 2020**

* Bijgewerkte module Publiek Management naar DIL 9.4. (AN-209341)

## Versie 2.18.0

Datum van de versie: **13 februari, 2020**

* AppMeasurement kan cookies nu dwingen het kenmerk Secure op te nemen door de variabele [`writeSecureCookies`](vars/config-vars/writesecurecookies.md) in te stellen. De vereiste voor deze variabele is dat de gehele clientwebsite veilig wordt aangeboden (HTTPS). (AN-204604)

## Versie 2.17.0

Releasedatum: **zaterdag 23 augustus 2019**

* Toegevoegde ondersteuning voor herschikking van Baidu-queryreeks. (AN-182483)
* Probleem verholpen dat storende bezoekerswaarden veroorzaakte in hits die in de wachtrij stonden terwijl werd gewacht op aanmelden. (AN-184391)

## Versie 2.16.0

Datum van de versie: **15 augustus, 2019**

* Geïmplementeerde `sendBeacon` ondersteuning in [!UICONTROL AppMeasurement] voor afsluitkoppelingen. Als een hit `sendBeacon` gebruikt en de pagina wordt verwijderd, wordt de aanvraag nog steeds voltooid. Dit is zeer nuttig voor uitgangsverbindingen omdat het waarschijnlijker is dat de treffer de servers van de gegevensinzameling bereikt. (AN-175142)
* ECID/fid-waarden worden nu in de cache geplaatst bij de eerste hit, ook al veranderen de instellingen voor OptIn. (AN-175142)
* Bijgewerkte Audience Management Module naar DIL 9.3. (AN-182704)
* De belichte schakelaar binnen `s.ActivityMap.trackScrollReach` om rolbereik het volgen of weg te zetten. (AN-182754)
* Bijgewerkte AppMeasurement voor gebruik van Bezoeker ID Service 4.4.0. (AN-182912)

## Versie 2.15.0

Datum van de versie: **15 Juli, 2019**

* Toegevoegde ActivityMap scroll reach tracking to the Activity Map extension (AN-172949)
* DIL 9.2 toegevoegd aan AppMeasurement (AN-182472)

## Versie 2.14.0

Datum van de versie: **21 mei, 2019**

* Oplossing voor problemen met het beheer van de status van tracker-parameters wanneer meerdere hits in behandeling zijn. (AN-176931, AN-176629, DTM-12758)
* Bijgewerkte AppMeasurement om Visitor.js 4.3.0 (AN-180049) op te nemen

## Versie 2.13.0

Datum van de versie: **10 april, 2019**

* Oplossing voor veel gemelde problemen met clearVars. Het probleem doet zich voor wanneer hits worden verzonden voordat de tracker gereed is. Wanneer de tracker gereed is, kan de bibliotheek variabelen instellen die al zijn gewist of gewijzigd. (AN-176931, AN-176629, DTM-12758)

## Versie 2.12.0

Datum van de versie: **22 februari, 2019**

* Bijgewerkte module Publiek Management naar DIL 9.1. (AN-175255)
* Het GTM-beveiligingsbeleid staat Activity Map Module niet toe. (AN-174679)
* Verbeterde AppMeasurement om de opt-out te respecteren wanneer de Identity Service niet is goedgekeurd in opt-in. (AN-175259)

## Versie 2.11.0

Datum van de versie: **11 februari, 2019**

* Extra ondersteuning voor de nieuwe Adobe Opt-in-services in AppMeasurement. (AN-163546)
* Toegevoegde ondersteuning voor het opslaan van gegevens voor het bijhouden van koppelingen in sessieopslag. (AN-162272)
* Toegevoegde ondersteuning voor het type mediastream voor audioanalyse. (AN-173265)

## Versie 2.10.0

Datum van de versie: **September 20, 2018**

Deze release zorgt ervoor dat de [!DNL AppMeasurement] -bibliotheek cookies correct verzendt voor alle verbindingstypen.

* [!DNL AppMeasurement] blokkeert cookie-verzendingen tijdens POST. (AN-165538)
* Ondersteuning voor XDomainRequest neerzetten. (AN-165733)
* Verlaag de standaardlevensduur van [!DNL AppMeasurement] cookies van vijf tot twee jaar. (AN-158572)
* De mediamodule verwijderen uit Codebeheer ( [!DNL AppMeasurement]) (AN-166590)

## Versie 2.9.0

Datum van de versie: **24 mei, 2018**

>[!NOTE]
>
>Bezoeker-API 3.0 of hoger is vereist voor klanten die de [!DNL Experience Cloud] ID-service gebruiken. Adobe raadt u aan een upgrade uit te voeren naar de nieuwste versie van de API van Visitor wanneer gekoppelde codebibliotheken worden bijgewerkt ( [!DNL at.js] , [!DNL AppMeasurement.js] , enzovoort.)

* Bijgewerkt [!DNL AppMeasurement] om de bijgewerkte Bezoekerinterface te gebruiken voor het aanvragen van id&#39;s. (AN-151483)
* Probleem verholpen waarbij de functie voor het bijhouden van koppelingen steeds wordt weggeschreven nadat het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Probleem verholpen waarbij `registerPreTrackCallback` en `registerPostTrackCallback` de handtekening van de callback-functie afbreken wanneer deze meerdere keren worden aangeroepen. (AN-158566)

## Versie 2.8.2

Datum van de versie: **12 april, 2018**

* Werk [!DNL AppMeasurement] bij om de bijgewerkte bezoekersinterface te gebruiken voor het aanvragen van id&#39;s. (AN-151483)
* De functie voor het bijhouden van koppelingen wordt steeds opnieuw geschreven als het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Verlaag de standaardlevensduur van [!DNL AppMeasurement] cookies van vijf tot twee jaar. (AN-158572)

## Versie 2.8.1

Datum van de versie: **Maart 29, 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

## Versie 2.8.0

Datum van de versie: **Maart 15, 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

* Bundel VAPI v3.1 met [!DNL AppMeasurement] v2.8. (AN-158353)
* Refactor bouwt het eindpunt van de gegevensverzameling om het delen te vergemakkelijken. (AN-156647)
* Voeg de metriek van de verzoekround-trip timing aan [!DNL AppMeasurement] toe. (AN-158343)

## Versie 2.7.0

De datum van de versie: **Januari 18, 2018**

* Ondersteuning voor IE 6 tot en met 9
* Opname van de Bezoeker-API v3.0.0
* Opname van DIL v7.00

## Versie 2.6.0

De datum van de versie: **9 November, 2017**

Probleem verholpen waarbij [!DNL AppMeasurement] library niet altijd de juiste accountcombinatie instelt wanneer s_gl wordt aangeroepen. (AN-152153)

## Versie 2.5.0

De datum van de versie: **21 september, 2017**

* Opname van de module [!DNL dil.js 6.12] ( [!DNL Audience Manager] )
* Opname van de Bezoeker-API 2.5.0.

## Versie 2.4.0

Releasedatum: **vrijdag 17 augustus 2017**

* Inclusief dil.js v6.11
* Inclusief bezoeker-API 2.4.0

## Versie 2.3.0

Releasedatum: **vrijdag 20 juli 2017**

* Correctie van bug waarbij `s.Util.getQueryParam` werd vastgelegd `#`
* Toegevoegd v6.10 van `dil.js` (AN-145701)

## Versie 2.2.0

Releasedatum: **vrijdag 8 juni 2017**

* Toegevoegde ondersteuning voor meerdere [!DNL AppMeasurement] instantiorder. (AN-138237)
* Opname van versie 2.2.0 Bezoeker-API. (AN-144042)

## Versie 2.1.0

De datum van de versie: **20 april, 2017**

* Inclusief de meest recente versie van `dil.js` (AN-140396)
* Toegevoegde ondersteuning voor parameter `adobe_mc_ref` die de paginaverwijzing overschrijft. (AN-131920)
* Opnieuw opgenomen Bezoeker-API 2.1.0. (AN-140873)
* Toegevoegde parameter `mcorgid` . (AN-139586)
* Toegevoegde cp (customerPerspective) parameter. (AN-140897)

## Versie 2.0.0

De datum van de versie: **9 Maart, 2017**

* Verplaatst naar een nieuw bouwstijlproces dat een update van het versieaantal aan 2.0.0 vereist. (AN-137878)
* Verplaatst mboxMCSDID behandeling in de correcte sectieplaats waar de volgende vraag wordt gemaakt. (AN-138483)

## Versie 1.8.0

De datum van de versie: **Januari 19, 2017**

* Include VisitorAPI 2.0.0
* Herhaalde functieaanroepen en controles zodat SDID wordt verbruikt nadat de afbreekcontrole is voltooid. (AN-134364)
* Toegevoegde `s.registerPreTrackCallback` en `s.registerPostTrackCallback` haken. (AN-134567)

## Versie 1.7.0

Bijgewerkt: **11 November, 2016**

* Inclusief Bezoeker-API 1.10.1.
* Werk [!DNL Audience Manager] -module bij met de demdex Integration Library (DIL) 6.6. (AN-132065)
* Opname van de Bezoeker-API 1.9.0. (AN-132072)
* [!DNL AppMeasurement] [!DNL Audience Manager] Module bijwerken met DIL 6.5 en extra configuraties (AN-129411)
* Opname van Bezoeker API 1.8.0 (AN-129887)

## Versie 1.6.4

Bijgewerkt: **vrijdag 18 augustus 2016**

* Bijgewerkt [!DNL AppMeasurement] voor het lezen en schrijven van AMCV-cookies. (AN-127098)
* Opname van de Bezoeker-API 1.7.0.

>[!NOTE]
>
>Zie ook de volgende releaseopmerkingen voor [!DNL JavaScript] versie 1.6.3, die bijgewerkte vereisten voor de Experience Cloud ID-service bevatten.

## Versie 1.6.3

Bijgewerkt: **vrijdag 4 augustus 2016**

* Correctie van een probleem waarbij [!DNL AppMeasurement] vroegtijdig beëindigde aanvraagverbindingen. (AN-126448)

>[!IMPORTANT]
>
>Versie 1.6.0 van de [!DNL Experience Cloud] dienst van identiteitskaart *vereist* [!DNL AppMeasurement] voor [!DNL JavaScript] versie 1.6.3 of hoger. Als u wilt upgraden naar versie 1.6.0 van de Experience Cloud ID-service, moet u AppMeasurement 1.6.3 of hoger gebruiken.

## Versie 1.6.2

Datum van de versie: **21 juli, 2016**

* Opname van de Bezoeker-API 1.6.0.
* Probleem verholpen waarbij [!DNL AppMeasurement] de onjuiste, verduisterde methode aanriep in de Bezoeker-API. (AN-126006)
* Probleem opgelost waarbij de fout [!DNL JavaScript] werd veroorzaakt: &quot;Kenmerk alleen geldig op v:image&quot;. (AN-124009)

## Versie 1.6.1

Releasedatum: **vrijdag 16 juni 2016**

* Opname van de Bezoeker-API 1.5.7.
* Probleem verholpen met het volgen van koppelingen in Firefox die de gebeurtenis complete niet hebben geactiveerd.

## Versie 1.6

Datum van de versie: **21 april 2016**

* De Activity Map-module [!DNL AppMeasurement] is geïntegreerd in de standaardmodule [!DNL AppMeasurement] , zodat u slechts naar één [!DNL .js] -bestand hoeft te verwijzen. Bovendien wordt het bijhouden van Activity Map standaard geactiveerd. (AN-112689)
* Oplossing voor een afbreekprobleem met de volgorde van queryreeksvariabelen in [!DNL AppMeasurement] , zodat *`pageURLRest`* het laatst is. (AN-114647)

## Versie 1.5.4

Datum van de versie: **Maart 17, 2016**

* Opname van de Bezoeker-API 1.5.4
* Ondersteuning voor de opt-out voor bezoekers-API 1.5.4+

## Versie 1.5.3

Datum van de versie: **Januari 21, 2016**

* Vaste afhandeling van de module [!DNL Audience Manager] wanneer POSTs voor het volgen van vraag wordt gebruikt. (AN-115381)
* Verplaatst de rest van de pagina-URL (&quot;-g&quot;) naar het einde van de queryreeks voor het volgende verzoek. (AN-114647)

## Versie 1.5.2

Datum van de versie: **5 November, 2015**

* Opname van de Bezoeker-API 1.5.3.
* Vaste detectie van IE11 voor URL Truncation 2047 (AN-114914)

## Versie 1.5.1

Datum van de versie: **17 september, 2015**

* Opname van de Bezoeker-API 1.5.2
* Bijgewerkte [!DNL Audience Manager] -module voor het gebruik van Adobe Audience Manager DIL 6.2 - getCustomer ID&#39;s van VisitorAPI.js en geef deze door in /event call aan Adobe Audience Manager. (AN-104978)

## Versie 1.5

Datum van de versie: **18 juni, 2015**

* Ondersteuning voor Bezoeker API 1.5, die de methode *`getCustomerIDs`* gebruikt om id&#39;s van klanten en geverifieerde status te verzamelen en de id&#39;s verzendt met verzoeken om gegevensverzameling.
* Oplossing voor een dubbele bestemmings-iframe in de module **[!UICONTROL AudienceManagement]** (DIL 6.1)
* Oplossing voor het bekende probleem dat in release 1.4.5 werd beschreven.

## Versie 1.4.5

Datum van de versie: **21 mei, 2015**

* Vanaf iOS SDK versie 4.5 kunt u met een nieuwe iOS-extensie gebruiksgegevens verzamelen van uw Apple Watch-apps, hedendaagse widgets, widgets voor fotobewerking en alle andere iOS-extensie-apps.
* Vanaf Android SDK versie 4.5 kunt u met een nieuwe Android-extensie gegevens verzamelen van uw mobiele Android-app.
* Opname van de Bezoeker-API 1.4.
* Bijgewerkte module PubliekManagement om DIL versie 6.0 te gebruiken.

>[!NOTE]
>
>**Bekend Kwestie**: In de integratie van de Module van de Bezoeker API / [!DNL AppMeasurement] [!DNL Audience Manager], zijn er twee bestemmings het publiceren iFrame verzoeken die in IE6-9 worden gemaakt: `//fast.<subdomain>.demdex.net/dest5.html` en `//fast.<subdomain>.demdex.net/dest4.html`. Het juiste gedrag, zoals in andere browsers, is om alleen `//fast.<subdomain>.demdex.net/dest5.html` te laden.

## Versie 1.4.4

Datum van de versie: **16 april 2015**

* U kunt nu aangepaste contextgegevensvariabelen opnemen met levenscyclusmetriek.
* De aanroepen `trackBeacon` en `clearCurrentBeacon` zijn nu beschikbaar in PhoneGap.
* Een kleine correctie voor het wissen van de profiel-id van de lichte server na de `trackLight` -aanroep.

## Versie 1.4.3

Datum van de versie: **19 februari, 2015**

* Alle behandeling van vertraagde het volgen vraag verenigbaar gemaakt, die kwesties met gesteunde variabelen tijdens de vertraging, zoals het geklikte voorwerp lost.
* Veranderd in geen automatische verwijzing na de eerste het volgen vraag zodat zal de tweede, derde, enz het volgen vraag (gewoonlijk verbinding het volgen) niet de verwijzer tweemaal tellen wanneer *`s.referrer`* manueel vóór de eerste het volgen vraag werd geplaatst.
* Het ZIP voor distributie is bijgewerkt en bevat Bezoeker API 1.3.5.

## Versie 1.4.2

Datum van de versie: **15 Januari, 2015**

* Correctie van de afhandeling van de WebKit-prerender om te voorkomen dat vooraf weergegeven pagina&#39;s die niet worden weergegeven, worden bijgehouden.
* Het ZIP-bestand voor distributie is bijgewerkt en bevat nu Bezoeker API 1.3.4 en een bijgewerkte **[!UICONTROL AudienceManagement]** -module die DIL versie 5.5 bevat.

## Versie 1.4.1

Datum van de versie: **18 september, 2014**

* Er is een variabele `tagContainerMarker` toegevoegd waarmee de implementatie maximaal 4 tekens kan opgeven die samen met een extra scheidingsteken voor streepjestekens aan de versietekenreeks worden toegevoegd. Dit wordt gebruikt door dynamisch tagbeheer.

  ```js
  // JavaScript
  s.tagContainerMarker = "D1.0";
  
  // Data Collection request
  //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
  ```

  De 4 tekens zijn beperkt tot tekens die zijn toegestaan in URL-bestandspaden, zoals alfanumeriek en punt.

* Op pagina&#39;s met twee labels en H-code heeft u een lus gecorrigeerd die kan optreden tijdens het automatisch bijhouden van koppelingen (downloaden en afsluiten) waarbij geforceerde koppelingen moeten worden bijgehouden (standaard in Webkit-browsers). Daarnaast is er een algemene beveiliging toegevoegd rondom het automatisch bijhouden van koppelingen om vergelijkbare lusbewerkingen te voorkomen. Deze vrijwaringsbeperkingen automatische verbinding het volgen van herhaalde kliks aan het *zelfde* voorwerp aan eens om de 10 seconden. Deze beveiliging is alleen van toepassing op het automatisch bijhouden van koppelingen, zodat oproepen voor het handmatig bijhouden van koppelingen (s.tl) niet beperkt zijn. Klikken op verschillende objecten worden ook niet beïnvloed door deze beveiliging en worden bijgehouden.
* Correctie van afhandeling van geklikt object wanneer een vertraging nodig is.
* Probleem verholpen waarbij een aantal pagina&#39;s werd geteld wanneer s.t werd aangeroepen vanuit een functie klikkoppeling als de bezoeker-API nog niet de vereiste waarden heeft.
* Ondersteuning voor HTTP POST.

  >[!IMPORTANT]
  >
  >Voor een [!DNL Analytics] vraag om de methode van de POST in plaats van de methode van GET in [!DNL AppMeasurement] (een methode om [ afgekapte URLs in IE ](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html) op te lossen) te gebruiken, moet u de recentste implementatie van de Dienst van identiteitskaart van de Bezoeker voor Experience Cloud gebruiken.

## Versie 1.4

Datum van de versie: **Augustus 21, 2014**

* Het verwijderen van het volgen van browser stop-ins (`p` vraagparameter) als stop-ins wordt niet meer gemeld in versie 15.
* Toevoeging van de module **[!UICONTROL AudienceManagement]** in het gecomprimeerde bestand.
* Extra ondersteuning voor extra eVars (76 - 250) en evenementen (101-1000).

>[!NOTE]
>
>H-Code biedt geen ondersteuning voor de extra gebeurtenissen en gebeurtenissen.

## Versie 1.3.2

Datum van de versie: **19 juni, 2014**

* Correctie van de afhandeling van voltooide en wachtende vlaggen voor Bezoeker API-velden, zoals de oudere [!DNL Analytics] Bezoeker-id, die fouten veroorzaakten.
* Ondersteuning voor nieuwe functies in bezoekersidentiteitsservice 1.3.

## Versie 1.3.1

Datum van de versie: **22 mei, 2014**

* [!DNL AppMeasurement] for [!DNL JavaScript] `s_gi` function heeft instanties die met H-code zijn gemaakt, niet correct gevonden `s_gi` . Merk op dat dit probleem slechts invloed had op enkele implementaties van dubbele codering, waarbij [!DNL AppMeasurement] for [!DNL JavaScript] en H code zich op dezelfde pagina bevonden met afzonderlijke instanties, en `s_gi` werd gebruikt om instanties te zoeken op rapportsuite.

## Versie 1.3

Datum van de versie: **17 april 2014**

* Steun voor de [ dienst van identiteitskaart van de Bezoeker van Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Versie 1.2.4

Datum van de versie: **Maart 13, 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.3

Datum van de versie: **20 februari, 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.2

Datum van de versie: **6 Februari, 2014**

* Probleem met compatibiliteit met de DIL-module van [!DNL Audience Manager] opgelost. [!DNL Audience Manager] klanten moeten ook een update naar versie 4.8 van de DIL-module uitvoeren.

## Versie 1.2.1

Datum van de versie: **15 November, 2013**

* Gebeurtenissen voor een vaste pagina die worden gebruikt voor het meten van hartslagvideo.

## Versie 1.2

Datum van de versie: **14 November, 2013**

* Toegevoegde steun voor [ Hartslagvideometing ](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html).
* `VisitorAPI.js` werd toegevoegd om de [ Dienst van identiteitskaart van de Bezoeker ](https://experienceleague.adobe.com/docs/id-service/using/home.html) te steunen.

## Versie 1.1.1

* Er is voorkomen dat een aanroep voor het bijhouden van koppelingen vanuit Opera-browsers wordt verzonden voor koppelingen die beginnen met &quot;opera:&quot; (&quot;opera:&quot; is vergelijkbaar met &quot;about:&quot; en &quot;chrome:&quot; in andere browsers).
* Toegevoegd `alt=""` aan alle voorwerpen van het Beeld om aan Toegankelijke Video en Communicatie Wet te voldoen.

## Versie 1.1

Datum van de versie: **18 september, 2013**

* Correctie van de ondersteuning voor het plaatsen van de bibliotheek- en paginacode in de tag `head` .
* Ondersteuning voor ontbrekende module `onLoad` toegevoegd.

## Versie 1.0.3

Datum van de versie: **15 augustus, 2013**

* Extra ondersteuning voor implementatie via Adobe-tagbeheer.
* Probleem verholpen waarbij werd voorkomen dat hiërarchievariabelen op het [!DNL AppMeasurement] -object werden ingesteld.

## Versie 1.0.2

Datum van de versie: **18 juli, 2013**

* De hash/het fragment wordt nu genegeerd door de koppeling automatisch te volgen. Eerder werd de volgende URL automatisch bijgehouden sinds de volledige `href` eindigde in `.pdf` :

  ```js
  <a href="index.htm#anchor.pdf">Test Link</a>
  ```

  De hash/het fragment wordt nu genegeerd, zodat de koppeling alleen wordt bijgehouden wanneer de bestandsnaam eindigt in een extensie die overeenkomt.

## Versie 1.0.1

Datum van de versie: **23 mei, 2013**

Er is een nieuwe [!DNL JavaScript] [!DNL AppMeasurement] -bibliotheek beschikbaar in Codebeheer. Deze bibliotheek biedt dezelfde kernfunctionaliteit van [!DNL s_code.js], maar is lichter en sneller voor gebruik op zowel mobiele als desktopsites.

* 3-7 keer sneller dan de H.25-code.
* Slechts 21k ongecomprimeerd en 8k gzipped (H.25 code is 33k ongecomprimeerd en 13k gzipped).
* Native ondersteuning voor het ophalen van queryparameters, het lezen en schrijven van cookies en het uitvoeren van geavanceerde koppelingstracering.
* Klein en snel genoeg voor gebruik met mobiele sites en robuust genoeg voor gebruik op het volledige desktopweb, zodat u in alle webomgevingen gebruik kunt maken van één bibliotheek.
