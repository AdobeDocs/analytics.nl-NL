---
title: AppMeasurement voor JavaScript-releaseopmerkingen
description: Cumulatieve releaseopmerkingen voor AppMeasurement voor JavaScript.
feature: Appmeasurement Implementation
exl-id: 80b935f0-3ec5-4ffa-9858-f83ae9a6b763
role: Admin, Developer, Leader, User
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '2614'
ht-degree: 5%

---

# AppMeasurement voor JavaScript-releaseopmerkingen

Cumulatieve releaseopmerkingen voor AppMeasurement voor JavaScript.

<!-- https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log -->

U kunt de nieuwste versie van het AppMeasurement downloaden van [GitHub](https://github.com/adobe/appmeasurement/releases).

## Versie 2.25.0

Releasedatum: **12 september 2023**

* De optionele methode toegevoegd [`bufferRequests()`](vars/functions/bufferrequests.md) om de betrouwbaarheid te verbeteren van het vangen van verzoeken wanneer browser niet de Beacon API steunt of verzoeken annuleert wanneer een pagina leegt.
* Toegevoegde waarborgen om veelvoudige post-spoorcallbacks voor één enkel volgend verzoek te verhinderen.

## Versie 2.24.0

Releasedatum: **18 juli 2023**

* De optionele configuratievariabele toegevoegd [`decodeLinkParameters`](vars/config-vars/decodelinkparameters.md) om koppeling-URL&#39;s met double-byte gecodeerde tekens te decoderen.
* Extra foutafhandeling toegevoegd voor browsers met onjuiste API&#39;s voor client-tips voor gebruikers-agent met hoge entropie.
* Gewijzigde POST Content-Type header voor gebruik `x-www-form-urlencoded` standaard.

## Versie 2.23.0

Releasedatum: **23 september 2022**

* AppMeasurement ondersteunt nu de verzameling van clienttips voor gebruikers/agents met hoge entropie die Chromium browsers (Google Chrome en Microsoft Edge) gebruiken om apparaatinformatie te verschaffen. U kunt cliëntwenken via Markeringen vormen of gebruiken [`collectHighEntropyUserAgentHints`](vars/config-vars/collecthighentropyuseragenthints.md) configuratievariabele. Verzameling van hints met hoge entropie is standaard uitgeschakeld. Meer informatie over gebruikersagent [clienthints](/help/technotes/client-hints.md).

## Versie 2.2.4

Releasedatum: **18 januari 2022**

* De vraag van het verbinden volgen `s.tl()` controleert nu of het object dat eraan wordt doorgegeven, een `href` kenmerk van type `string`. Als het geen `string`en dan negeert het op elegante wijze de `href` in plaats van mislukt. Dit scenario kan zich voordoen wanneer u `svg` objecten naar de aanroep voor het bijhouden van koppelingen.

## Versie 2.2.2.3

Releasedatum: **11 oktober 2021**

* Bijgewerkte koppelingen in bestanden die verwijzen naar documentatie.

## Versie 2.2.2

Releasedatum: **7 september 2021**

* Deze update veroorzaakt `opt.dmp` en `opt.sell` om altijd te worden opgenomen bij het bijhouden van koppelingen. Zie de [Privacy-rapportage](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md) in de gebruikershandleiding voor Admin voor meer informatie.

## Versie 2.22.1

Releasedatum: **17 augustus 2021**

* Klanten die opt-out gebruiken hebben de server-side het door:sturen opt-out parameters niet kunnen gezien wanneer het volgen van verbindingen. De correcties in deze release zorgen ervoor dat de markeringen voor niet-deelname worden verzonden als deze aanwezig zijn bij het bijhouden van koppelingen.

## Versie 2.2.2.0

Releasedatum: **4 augustus 2020**

* Oplossing voor ontbrekende referentie wanneer de eerste melding niet is verzonden vanwege de gebruikersvoorkeuren voor weigeren.

## Versie 2.21.0

Releasedatum: **24 juni 2020**

* Probleem verholpen waarbij het filter Activity Map linkExclusions niet altijd werd toegepast op Firefox.

## Versie 2.20.0

Releasedatum: **5 maart 2020**

* Probleem met betrekking tot beveiliging is opgelost door de Internet Explorer-detectie bij te werken om de JSLint-waarschuwing te onderdrukken.

## Versie 2.19.0

Releasedatum: **21 februari 2020**

* Bijgewerkte module van het Beheer van het Publiek aan DIL 9.4. (AN-209341)

## Versie 2.18.0

Releasedatum: **13 februari 2020**

* AppMeasurement kan cookies nu dwingen het kenmerk Secure op te nemen door de instelling van de [`writeSecureCookies`](vars/config-vars/writesecurecookies.md) variabele. De vereiste voor deze variabele is dat de gehele clientwebsite veilig wordt aangeboden (HTTPS). (AN-204604)

## Versie 2.17.0

Releasedatum: **zaterdag 23 augustus 2019**

* Toegevoegde ondersteuning voor herschikking van Baidu-queryreeks. (AN-182483)
* Probleem verholpen dat storende bezoekerswaarden veroorzaakte in hits die in de wachtrij stonden terwijl werd gewacht op aanmelden. (AN-184391)

## Versie 2.16.0

Releasedatum: **15 augustus 2019**

* Geïmplementeerd `sendBeacon` ondersteuning in [!UICONTROL AppMeasurement] voor afsluitkoppelingen. Als een hit wordt gebruikt `sendBeacon` en de pagina wordt verwijderd, is de aanvraag nog steeds voltooid. Dit is zeer nuttig voor uitgangsverbindingen omdat het waarschijnlijker is dat de treffer de servers van de gegevensinzameling bereikt. (AN-175142)
* ECID/fid-waarden worden nu in de cache geplaatst bij de eerste hit, ook al veranderen de instellingen voor OptIn. (AN-175142)
* Bijgewerkte Module van het Beheer van het Publiek aan DIL 9.3. (AN-182704)
* Uitgeschakelde switch in `s.ActivityMap.trackScrollReach` om het bereiken van het schuifbereik in of uit te schakelen. (AN-182754)
* Bijgewerkt AppMeasurement voor gebruik van Bezoeker ID Service 4.4.0. (AN-182912)

## Versie 2.15.0

Releasedatum: **15 juli 2019**

* Toegevoegde ActivityMap scroll bereiktracking naar de extensie Activity Map (AN-172949)
* DIL 9.2 toegevoegd aan AppMeasurement (AN-182472)

## Versie 2.14.0

Releasedatum: **21 mei 2019**

* Oplossing voor problemen met het beheer van de status van tracker-parameters wanneer meerdere hits in behandeling zijn. (AN-176931, AN-176629, DTM-12758)
* Bijgewerkt AppMeasurement om Visitor.js 4.3.0 (AN-180049) op te nemen

## Versie 2.13.0

Releasedatum: **10 april 2019**

* Oplossing voor veel gemelde problemen met clearVars. Het probleem doet zich voor wanneer hits worden verzonden voordat de tracker gereed is. Wanneer de tracker gereed is, kan de bibliotheek variabelen instellen die al zijn gewist of gewijzigd. (AN-176931, AN-176629, DTM-12758)

## Versie 2.12.0

Releasedatum: **22 februari 2019**

* Bijgewerkte module van het Beheer van de Publiek aan DIL 9.1. (AN-175255)
* GTM-beveiligingsbeleid staat geen Activity Map-module toe. (AN-174679)
* Verbeterd AppMeasurement om de opt-out te respecteren wanneer de Identity Service niet is goedgekeurd in opt-in. (AN-175259)

## Versie 2.11.0

Releasedatum: **11 februari 2019**

* Extra ondersteuning voor de nieuwe Adobe Opt-in-servicefunctionaliteit in AppMeasurement. (AN-163546)
* Toegevoegde ondersteuning voor het opslaan van gegevens voor het bijhouden van koppelingen in sessieopslag. (AN-162272)
* Toegevoegde ondersteuning voor het type mediastream voor audioanalyse. (AN-173265)

## Versie 2.10.0

Releasedatum: **20 september 2018**

Deze release zorgt ervoor dat de [!DNL AppMeasurement] de bibliotheek verzendt correct koekjes voor alle verbindingstypes.

* [!DNL AppMeasurement] blokkeert cookietransmissies tijdens POST. (AN-165538)
* Ondersteuning voor XDomainRequest neerzetten. (AN-165733)
* Verkleinen [!DNL AppMeasurement] standaardlevensduur van cookies van vijf tot twee jaar. (AN-158572)
* De mediamodule verwijderen uit Codebeheer ( [!DNL AppMeasurement]) (AN-166590)

## Versie 2.9.0

Releasedatum: **24 mei 2018**

>[!NOTE]
>
>Voor klanten die de [!DNL Experience Cloud] ID-service. Adobe raadt aan een upgrade uit te voeren naar de nieuwste versie van de Visitor API wanneer gekoppelde codebibliotheken worden bijgewerkt ( [!DNL at.js], [!DNL AppMeasurement.js], enzovoort.)

* Bijgewerkt [!DNL AppMeasurement] om de bijgewerkte interface van de Bezoeker te gebruiken voor het aanvragen van id&#39;s. (AN-151483)
* Probleem verholpen waarbij de functie voor het bijhouden van koppelingen steeds wordt weggeschreven nadat het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Probleem verholpen waarbij `registerPreTrackCallback` en `registerPostTrackCallback` Hiermee wordt de callback-functiehandtekening afgebroken wanneer deze meerdere keren wordt aangeroepen. (AN-158566)

## Versie 2.8.2

Releasedatum: **12 april 2018**

* Bijwerken [!DNL AppMeasurement] gebruiken om de bijgewerkte bezoekersinterface te gebruiken voor het aanvragen van id&#39;s. (AN-151483)
* De functie voor het bijhouden van koppelingen wordt steeds opnieuw geschreven als het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Verkleinen [!DNL AppMeasurement] standaardlevensduur van cookies van vijf tot twee jaar. (AN-158572)

## Versie 2.8.1

Releasedatum: **29 maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

## Versie 2.8.0

Releasedatum: **15 maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

* VAPI v3.1 bundelen met [!DNL AppMeasurement] v2.8. (AN-158353)
* Refactor bouwt het eindpunt van de gegevensverzameling om het delen te vergemakkelijken. (AN-156647)
* De metriek van de verzoekround-trip timing toevoegen aan [!DNL AppMeasurement]. (AN-158343)

## Versie 2.7.0

Releasedatum: **vrijdag 18 januari 2018**

* Ondersteuning voor IE 6 tot en met 9
* Opname van de Bezoeker-API v3.0.0
* Opname van DIL v7.00

## Versie 2.6.0

Releasedatum: **vrijdag 9 november 2017**

Probleem verholpen waarbij [!DNL AppMeasurement] de bibliotheek plaatst niet altijd de correcte rekeningscombinatie wanneer s_gl wordt geroepen. (AN-152153)

## Versie 2.5.0

Releasedatum: **vrijdag 21 september 2017**

* Opname van [!DNL dil.js 6.12] ( [!DNL Audience Manager] module)
* Opname van de Bezoeker-API 2.5.0.

## Versie 2.4.0

Releasedatum: **vrijdag 17 augustus 2017**

* Inclusief dil.js v6.11
* Inclusief bezoeker-API 2.4.0

## Versie 2.3.0

Releasedatum: **vrijdag 20 juli 2017**

* Vaste bug waarbij `s.Util.getQueryParam` vastgelegd `#`
* Toegevoegd v6.10 van `dil.js` (AN-145701)

## Versie 2.2.0

Releasedatum: **vrijdag 8 juni 2017**

* Extra ondersteuning voor meerdere [!DNL AppMeasurement] instantiatievolgorde. (AN-138237)
* Opname van versie 2.2.0 Bezoeker-API. (AN-144042)

## Versie 2.1.0

Releasedatum: **vrijdag 20 april 2017**

* Meest recente versie van `dil.js` (AN-140396)
* Extra ondersteuning voor `adobe_mc_ref` parameter die de paginaverwijzing overschrijft. (AN-131920)
* Opnieuw opgenomen Bezoeker-API 2.1.0. (AN-140873)
* Toegevoegd `mcorgid` parameter. (AN-139586)
* Toegevoegde cp (customerPerspective) parameter. (AN-140897)

## Versie 2.0.0

Releasedatum: **vrijdag 9 maart 2017**

* Verplaatst naar een nieuw bouwstijlproces dat een update van het versieaantal aan 2.0.0 vereist. (AN-137878)
* Verplaatst mboxMCSDID behandeling in de correcte sectieplaats waar de volgende vraag wordt gemaakt. (AN-138483)

## Versie 1.8.0

Releasedatum: **vrijdag 19 januari 2017**

* Include VisitorAPI 2.0.0
* Herhaalde functieaanroepen en controles zodat SDID wordt verbruikt nadat de afbreekcontrole is voltooid. (AN-134364)
* Toegevoegd `s.registerPreTrackCallback` en `s.registerPostTrackCallback` haken. (AN-134567)

## Versie 1.7.0

Bijgewerkt: **zaterdag 11 november 2016**

* Inclusief Bezoeker-API 1.10.1.
* Bijwerken [!DNL Audience Manager] met Demdex Integration Library (DIL) 6.6. (AN-132065)
* Opname van de Bezoeker-API 1.9.0. (AN-132072)
* Bijwerken [!DNL AppMeasurement] [!DNL Audience Manager] Module met DIL 6.5 en Aanvullende Configuraties (AN-129411)
* Opname van Bezoeker API 1.8.0 (AN-129887)

## Versie 1.6.4

Bijgewerkt: **vrijdag 18 augustus 2016**

* Bijgewerkt [!DNL AppMeasurement] voor het lezen en schrijven van AMCV-cookies. (AN-127098)
* Opname van de Bezoeker-API 1.7.0.

>[!NOTE]
>
>Zie ook de volgende releaseopmerkingen voor [!DNL JavaScript] versie 1.6.3, die bijgewerkte vereisten voor de dienst van identiteitskaart van het Experience Cloud omvat.

## Versie 1.6.3

Bijgewerkt: **vrijdag 4 augustus 2016**

* Probleem verholpen waarbij [!DNL AppMeasurement] vroegtijdig beëindigde verzoekverbindingen. (AN-126448)

>[!IMPORTANT]
>
>Versie 1.6.0 van het [!DNL Experience Cloud] ID-service *vereist* [!DNL AppMeasurement] for [!DNL JavaScript] versie 1.6.3 of hoger. Als u aan versie 1.6.0 van de dienst van identiteitskaart van het Experience Cloud wilt bevorderen, zorg ervoor dat u AppMeasurement 1.6.3 of hoger gebruikt.

## Versie 1.6.2

Releasedatum: **21 juli 2016**

* Opname van de Bezoeker-API 1.6.0.
* Probleem verholpen dat [!DNL AppMeasurement] de onjuiste, verduisterde methode in de Bezoeker-API aanroepen. (AN-126006)
* Probleem verholpen waardoor de [!DNL JavaScript] fout: &quot;Kenmerk alleen geldig op v:image&quot;. (AN-124009)

## Versie 1.6.1

Releasedatum: **vrijdag 16 juni 2016**

* Opname van de Bezoeker-API 1.5.7.
* Probleem verholpen met het volgen van koppelingen in Firefox die de gebeurtenis complete niet hebben geactiveerd.

## Versie 1.6

Releasedatum: **21 april 2016**

* De [!DNL AppMeasurement] De module Activity Map is geïntegreerd in het [!DNL AppMeasurement] standaardmodule, zodat u slechts naar één moet verwijzen [!DNL .js] bestand. Bovendien wordt het bijhouden van Activity Mappen standaard geactiveerd. (AN-112689)
* Probleem met afkapping opgelost die optreedt met de volgorde van query-tekenreeksvariabelen in [!DNL AppMeasurement], zodat *`pageURLRest`* is de laatste. (AN-114647)

## Versie 1.5.4

Releasedatum: **17 maart 2016**

* Opname van de Bezoeker-API 1.5.4
* Ondersteuning voor de opt-out voor bezoekers-API 1.5.4+

## Versie 1.5.3

Releasedatum: **21 januari 2016**

* Vaste afhandeling van [!DNL Audience Manager] module wanneer POSTs voor het volgen van vraag wordt gebruikt. (AN-115381)
* Verplaatst de rest van de pagina-URL (&quot;-g&quot;) naar het einde van de queryreeks voor het volgende verzoek. (AN-114647)

## Versie 1.5.2

Releasedatum: **5 november 2015**

* Opname van de Bezoeker-API 1.5.3.
* Vaste detectie van IE11 voor URL Truncation 2047 (AN-114914)

## Versie 1.5.1

Releasedatum: **17 september 2015**

* Opname van de Bezoeker-API 1.5.2
* Bijgewerkt [!DNL Audience Manager] om Adobe Audience Manager DIL 6.2 te gebruiken - getCustomer IDs van VisitorAPI.js en hen in /event vraag door te geven aan Adobe Audience Manager. (AN-104978)

## Versie 1.5

Releasedatum: **18 juni 2015**

* Ondersteuning voor Bezoeker API 1.5, die de *`getCustomerIDs`* methode om Klant IDs en voor authentiek verklaarde staat te verzamelen, en identiteitskaarts binnen met de verzoeken van de gegevensinzameling te verzenden.
* Oplossing voor het maken van een duplicaat van de doeliframe in **[!UICONTROL AudienceManagement]** module (DIL 6.1)
* Oplossing voor het bekende probleem dat in release 1.4.5 werd beschreven.

## Versie 1.4.5

Releasedatum: **21 mei 2015**

* Vanaf iOS SDK versie 4.5 kunt u met een nieuwe iOS-extensie gebruiksgegevens verzamelen van uw Apple Watch-apps, hedendaagse widgets, widgets voor fotobewerking en alle andere iOS-extensie-apps.
* Vanaf Android SDK versie 4.5 kunt u met een nieuwe Android-extensie gegevens verzamelen van uw Android-webtoepassing die kan worden gebruikt.
* Opname van de Bezoeker-API 1.4.
* Bijgewerkte module van het Beheer van het Publiek om DIL versie 6.0 te gebruiken.

>[!NOTE]
>
>**Bekend probleem**: In de API voor bezoekers / [!DNL AppMeasurement] [!DNL Audience Manager] De integratie van de module, zijn er twee die bestemmings het publiceren iFrame verzoeken in IE6-9 worden gemaakt: `//fast.<subdomain>.demdex.net/dest5.html` en  `//fast.<subdomain>.demdex.net/dest4.html`. Het juiste gedrag, zoals in andere browsers wordt getoond, is alleen laden `//fast.<subdomain>.demdex.net/dest5.html`.

## Versie 1.4.4

Releasedatum: **16 april 2015**

* U kunt nu aangepaste contextgegevensvariabelen opnemen met levenscyclusmetriek.
* De `trackBeacon` en `clearCurrentBeacon` De vraag is nu beschikbaar in PhoneGap.
* Een minder belangrijke moeilijke situatie om identiteitskaart van het de vraagprofiel van de lichte server na te ontruimen `trackLight` vraag.

## Versie 1.4.3

Releasedatum: **19 februari 2015**

* Alle behandeling van vertraagde het volgen vraag verenigbaar gemaakt, die kwesties met gesteunde variabelen tijdens de vertraging, zoals het geklikte voorwerp lost.
* Veranderd om automatisch verwijzende volgen na de eerste volgende vraag niet te doen zodat zal de tweede, derde, enz het volgen vraag (gewoonlijk verbinding het volgen) niet de verwijzer tweemaal tellen wanneer *`s.referrer`* handmatig ingesteld vóór de eerste volgende aanroep.
* Het ZIP voor distributie is bijgewerkt en bevat Bezoeker API 1.3.5.

## Versie 1.4.2

Releasedatum: **15 januari 2015**

* Correctie van de afhandeling van de WebKit-prerender om te voorkomen dat vooraf weergegeven pagina&#39;s die niet worden weergegeven, worden bijgehouden.
* Het ZIP voor distributie is bijgewerkt en bevat Bezoeker API 1.3.4 en een bijgewerkte versie **[!UICONTROL AudienceManagement]** die DIL versie 5.5 bevat.

## Versie 1.4.1

Releasedatum: **18 september 2014**

* Toegevoegde `tagContainerMarker` een variabele waarmee de implementatie maximaal 4 tekens kan opgeven die samen met een extra scheidingsteken voor streepjestekens aan de versietekenreeks worden toegevoegd. Dit wordt gebruikt door dynamisch tagbeheer.

  ```js
  // JavaScript
  s.tagContainerMarker = "D1.0";
  
  // Data Collection request
  //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
  ```

  De 4 tekens zijn beperkt tot tekens die zijn toegestaan in URL-bestandspaden, zoals alfanumeriek en punt.

* Op pagina&#39;s met twee labels en H-code heeft u een lus gecorrigeerd die kan optreden tijdens het automatisch bijhouden van koppelingen (downloaden en afsluiten) waarbij geforceerde koppelingen moeten worden bijgehouden (standaard in Webkit-browsers). Daarnaast is er een algemene beveiliging toegevoegd rondom het automatisch bijhouden van koppelingen om vergelijkbare lusbewerkingen te voorkomen. Met deze beveiliging wordt het automatisch bijhouden van koppelingen voor herhaalde klikken beperkt tot de *zelfde* om de 10 seconden. Deze beveiliging is alleen van toepassing op het automatisch bijhouden van koppelingen, zodat oproepen voor het handmatig bijhouden van koppelingen (s.tl) niet beperkt zijn. Klikken op verschillende objecten worden ook niet beïnvloed door deze beveiliging en worden bijgehouden.
* Correctie van afhandeling van geklikt object wanneer een vertraging nodig is.
* Probleem verholpen waarbij een aantal pagina&#39;s werd geteld wanneer s.t werd aangeroepen vanuit een functie klikkoppeling als de bezoeker-API nog niet de vereiste waarden heeft.
* Ondersteuning voor HTTP-POST.

  >[!IMPORTANT]
  >
  >Voor een [!DNL Analytics] aanroep om de methode POST te gebruiken in plaats van de methode GET in [!DNL AppMeasurement] (een oplosmethode [afgekapte URL&#39;s in IE](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html)), moet u de recentste implementatie van de Dienst van identiteitskaart van de Bezoeker voor het Experience Cloud gebruiken.

## Versie 1.4

Releasedatum: **21 augustus 2014**

* Bijhouden van browserplug-ins is verwijderd (`p` queryparameter) als plug-ins wordt niet meer gerapporteerd in versie 15.
* Toevoeging van de **[!UICONTROL AudienceManagement]** Module in het gecomprimeerde bestand.
* Extra ondersteuning voor extra eVars (76 - 250) en evenementen (101-1000).

>[!NOTE]
>
>H-Code biedt geen ondersteuning voor de extra gebeurtenissen en gebeurtenissen.

## Versie 1.3.2

Releasedatum: **19 juni 2014**

* Behandeling van voltooide en wachtende vlaggen voor Bezoeker API-velden zoals de verouderde [!DNL Analytics] Bezoeker-id, die fouten veroorzaakte.
* Ondersteuning voor nieuwe functies in bezoekersidentiteitsservice 1.3.

## Versie 1.3.1

Releasedatum: **22 mei 2014**

* [!DNL AppMeasurement] for [!DNL JavaScript] `s_gi` functie heeft met H-code gemaakte instanties niet correct gevonden `s_gi`. Merk op dat dit probleem slechts invloed had op enkele implementaties van dubbele tags waar [!DNL AppMeasurement] for [!DNL JavaScript] en H-code zich op dezelfde pagina bevond met afzonderlijke exemplaren, en `s_gi` werd gebruikt om instanties door rapportreeks te vinden.

## Versie 1.3

Releasedatum: **17 april 2014**

* Steun voor de [Experience Cloud Visitor ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Versie 1.2.4

Releasedatum: **13 maart 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.3

Releasedatum: **20 februari 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.2

Releasedatum: **6 februari 2014**

* Oplossing voor een compatibiliteitsprobleem met de [!DNL Audience Manager] DIL module. [!DNL Audience Manager] klanten moeten ook bijwerken naar versie 4.8 van de module DIL.

## Versie 1.2.1

Releasedatum: **15 november 2013**

* Gebeurtenissen voor een vaste pagina die worden gebruikt voor het meten van hartslagvideo.

## Versie 1.2

Releasedatum: **14 november 2013**

* Extra ondersteuning voor [Videometing hartslagmaat](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html).
* `VisitorAPI.js` is toegevoegd aan ondersteuning [Bezoekersidentiteitsservice](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Versie 1.1.1

* Er is voorkomen dat een aanroep voor het bijhouden van koppelingen vanuit Opera-browsers wordt verzonden voor koppelingen die beginnen met &quot;opera:&quot; (&quot;opera:&quot; is vergelijkbaar met &quot;about:&quot; en &quot;chrome:&quot; in andere browsers).
* Toegevoegd `alt=""` op alle voorwerpen van het Beeld om aan Toegankelijke Video en Communicatie Wet te voldoen.

## Versie 1.1

Releasedatum: **18 september 2013**

* Vaste ondersteuning voor het plaatsen van de bibliotheek- en paginacode in de `head` -tag.
* Ontbrekende module toegevoegd `onLoad` ondersteuning.

## Versie 1.0.3

Releasedatum: **15 augustus 2013**

* Toegevoegde ondersteuning voor implementatie via tagbeheer voor Adoben.
* Probleem verholpen waardoor hiërarchievariabelen niet konden worden ingesteld op het tabblad [!DNL AppMeasurement] object.

## Versie 1.0.2

Releasedatum: **18 juli 2013**

* De hash/het fragment wordt nu genegeerd door de koppeling automatisch te volgen. Eerder werd automatisch de volgende URL bijgehouden sinds de gehele URL `href` beëindigd in `.pdf`:

  ```js
  <a href="index.htm#anchor.pdf">Test Link</a>
  ```

  De hash/het fragment wordt nu genegeerd, zodat de koppeling alleen wordt bijgehouden wanneer de bestandsnaam eindigt in een extensie die overeenkomt.

## Versie 1.0.1

Releasedatum: **23 mei 2013**

Een nieuwe [!DNL JavaScript] [!DNL AppMeasurement] bibliotheek is nu beschikbaar in Codebeheer. Deze bibliotheek biedt dezelfde basisfunctionaliteit als [!DNL s_code.js], maar is lichter en sneller voor gebruik op zowel mobiele als desktopsites.

* 3-7 keer sneller dan de H.25-code.
* Slechts 21k ongecomprimeerd en 8k gzipped (H.25 code is 33k ongecomprimeerd en 13k gzipped).
* Native ondersteuning voor het ophalen van queryparameters, het lezen en schrijven van cookies en het uitvoeren van geavanceerde koppelingstracering.
* Klein en snel genoeg voor gebruik met mobiele sites en robuust genoeg voor gebruik op het volledige desktopweb, zodat u in alle webomgevingen gebruik kunt maken van één bibliotheek.
