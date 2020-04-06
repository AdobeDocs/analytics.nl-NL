---
title: AppMeasurement voor JavaScript-releaseopmerkingen
description: Cumulatieve releaseopmerkingen voor AppMeasurement voor JavaScript.
subtopic: Release notes
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# AppMeasurement voor JavaScript-releaseopmerkingen

Cumulatieve releaseopmerkingen voor [!DNL AppMeasurement] JavaScript.

<!-- https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log -->

U kunt de nieuwste versie van AppMeasurement downloaden in [Codebeheer](/help/admin/admin/code-manager-admin.md).

## Versie 2.20.0

Releasedatum: 5 **maart 2020**

* Probleem met betrekking tot beveiliging is opgelost door de Internet Explorer-detectie bij te werken om de JSLint-waarschuwing te onderdrukken.

## Versie 2.19.0

Releasedatum: 21 **februari 2020**

* Bijgewerkte module Audience Management naar DIL 9.4. (AN-209341)

## Versie 2.18.0

Releasedatum: 13 **februari 2020**

* AppMeasurement kan cookies nu dwingen het kenmerk Secure op te nemen door de [`writeSecureCookies`](vars/config-vars/writesecurecookies.md) variabele in te stellen. De vereiste voor deze variabele is dat de gehele clientwebsite veilig wordt aangeboden (HTTPS). (AN-2046/04)

## Versie 2.17.0

Releasedatum: 23 **augustus 2019**

* Toegevoegde ondersteuning voor herschikking van Baidu-queryreeks. (AN-182483)
* Probleem verholpen dat storende bezoekerswaarden veroorzaakte in hits die in de wachtrij stonden terwijl werd gewacht op aanmelden. (AN-184391)

## Versie 2.16.0

Releasedatum: 15 **augustus 2019**

* Geïmplementeerde `sendBeacon` ondersteuning in [!UICONTROL AppMeasurement] voor afsluitkoppelingen. Als een hit wordt gebruikt `sendBeacon` en de pagina wordt verwijderd, is de aanvraag nog steeds voltooid. Dit is zeer nuttig voor uitgangsverbindingen omdat het waarschijnlijker is dat de treffer de servers van de gegevensinzameling bereikt. (AN-175142)
* ECID/fid-waarden worden nu in de cache geplaatst bij de eerste hit, ook al veranderen de instellingen voor OptIn. (AN-175142)
* Bijgewerkte Audience Management Module naar DIL 9.3. (AN-182704)
* De blootgestelde schakelaar binnen `s.ActivityMap.trackScrollReach` om rolbereik het volgen of weg te zetten. (AN-182754)
* Bijgewerkte AppMeasurement om de Dienst van bezoeker ID 4.4.0 te gebruiken. (AN-182912)

## Versie 2.15.0

Releasedatum: 15 **juli 2019**

* Toegevoegde ActivityMap scroll bereiktracking naar de Activity Map-extensie (AN-172949)
* DIL 9.2 is toegevoegd aan AppMeasurement (AN-182472)

## Versie 2.14.0

Releasedatum: 21 **mei 2019**

* Oplossing voor problemen met het beheer van de status van tracker-parameters wanneer meerdere hits in behandeling zijn. (AN-176931, AN-176629, DTM-12758)
* Bijgewerkte AppMeasurement om Visitor.js 4.3.0 (AN-180049) te omvatten

## Versie 2.13.0

Releasedatum: 10 **april 2019**

* Oplossing voor veel gemelde problemen met clearVars. Het probleem doet zich voor wanneer hits worden verzonden voordat de tracker gereed is. Wanneer de tracker gereed is, kan de bibliotheek variabelen instellen die al zijn gewist of gewijzigd. (AN-176931, AN-176629, DTM-12758).

## Versie 2.12.0

Releasedatum: 22 **februari 2019**

* Bijgewerkte module Audience Management naar DIL 9.1. (AN-175255)
* Het GTM-beveiligingsbeleid staat geen Activity Map Module toe. (AN-174679)
* Verbeterde AppMeasurement om opt-out na te leven wanneer de Identiteitsdienst niet in opt-in wordt goedgekeurd. (AN-175259)

## Versie 2.11.0

Releasedatum: 11 **februari 2019**

* Extra ondersteuning voor de nieuwe functionaliteit voor Adobe Opt-in-services in AppMeasurement. (AN-163546)
* Toegevoegde ondersteuning voor het opslaan van gegevens voor het bijhouden van koppelingen in sessieopslag. (AN-162272)
* Toegevoegde ondersteuning voor het type mediastream voor audioanalyse. (AN-173265)

## Versie 2.10.0

Releasedatum: 20 **september 2018**

Deze versie zorgt ervoor dat de [!DNL AppMeasurement] bibliotheek cookies correct verzendt voor alle verbindingstypen.

* [!DNL AppMeasurement] blokkeert cookietransmissies tijdens POST. (AN-165538)
* Ondersteuning voor XDomainRequest neerzetten. (AN-165733)
* Verlaag de [!DNL AppMeasurement] standaardlevensduur van cookies van vijf tot twee jaar. (AN-158572)
* Verwijder de Module van Media uit de Manager van de Code ( [!DNL AppMeasurement]) (AN-166590)

## Versie 2.9.0

Releasedatum: 24 **mei 2018**

>[!NOTE] Bezoeker-API 3.0 of hoger is vereist voor klanten die de [!DNL Experience Cloud] id-service gebruiken. Adobe raadt u aan een upgrade uit te voeren naar de nieuwste versie van de Visitor API wanneer gekoppelde codebibliotheken worden bijgewerkt ( [!DNL at.js], [!DNL AppMeasurement.js]enzovoort).

* Bijgewerkt om de bijgewerkte interface van de Bezoeker te gebruiken voor het aanvragen van id&#39;s. [!DNL AppMeasurement] (AN-151483)
* Probleem verholpen waarbij de functie voor het bijhouden van koppelingen steeds wordt weggeschreven nadat het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Probleem verholpen waarbij `registerPreTrackCallback` en `registerPostTrackCallback` afgebroken callback functie-handtekening werden aangeroepen wanneer deze meerdere keren werd aangeroepen. (AN-158566)

## Versie 2.8.2

Releasedatum: 12 **april 2018**

* Bijwerken [!DNL AppMeasurement] om de bijgewerkte bezoekersinterface te gebruiken voor het aanvragen van id&#39;s. (AN-151483)
* De functie voor het bijhouden van koppelingen wordt steeds opnieuw geschreven als het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Verlaag de [!DNL AppMeasurement] standaardlevensduur van cookies van vijf tot twee jaar. (AN-158572)

## Versie 2.8.1

Releasedatum: 29 **maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

## Versie 2.8.0

Releasedatum: 15 **maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

* Bundel VAPI v3.1 met [!DNL AppMeasurement] v2.8. (AN-158353)
* Refactor bouwt het eindpunt van de gegevensverzameling om het delen te vergemakkelijken. (AN-156647)
* Voeg de metriek van de verzoekround-trip timing aan [!DNL AppMeasurement]. (AN-158343)

## Versie 2.7.0

Releasedatum: 18 **januari 2018**

* Ondersteuning voor IE 6 tot en met 9
* Opname van de Bezoeker-API v3.0.0
* Opname van DIL v7.00

## Versie 2.6.0

Releasedatum: 9 **november 2017**

Probleem verholpen waarbij de [!DNL AppMeasurement] bibliotheek niet altijd de juiste accountcombinatie instelt wanneer s_gl wordt aangeroepen. (AN-152153)

## Versie 2.5.0

Releasedatum: 21 **september 2017**

* Opname van [!DNL dil.js 6.12] ( [!DNL Audience Manager] module)
* Opname van de Bezoeker-API 2.5.0.

## Versie 2.4.0

Releasedatum: 17 **augustus 2017**

* Inclusief dil.js v6.11
* Inclusief bezoeker-API 2.4.0

## Versie 2.3.0

Releasedatum: 20 **juli 2017**

* Correctie van bug waarbij `s.Util.getQueryParam` beelden werden vastgelegd `#`
* Toegevoegd v6.10 van `dil.js` (AN-145701)

## Versie 2.2.0

Releasedatum: 8 **juni 2017**

* Toegevoegde ondersteuning voor meerdere [!DNL AppMeasurement] instantiatievolgorde. (AN-138237)
* Opname van versie 2.2.0 Bezoeker-API. (AN-144042)

## Versie 2.1.0

Releasedatum: 20 **april 2017**

* Inclusief meest recente versie van `dil.js` (AN-140396)
* Toegevoegde ondersteuning voor `adobe_mc_ref` parameter die de paginaverwijzing overschrijft. (AN-131920)
* Opnieuw opgenomen Bezoeker-API 2.1.0. (AN-140873)
* Toegevoegde `mcorgid` parameter. (AN-139586)
* Toegevoegde cp (customerPerspective) parameter. (AN-140897)

## Versie 2.0.0

Releasedatum: 9 **maart 2017**

* Verplaatst naar een nieuw bouwstijlproces dat een update van het versieaantal aan 2.0.0 vereist. (AN-137878)
* Verplaatst mboxMCSDID behandeling in de correcte sectieplaats waar de volgende vraag wordt gemaakt. (AN-138483)

## Versie 1.8.0

Releasedatum: 19 **januari 2017**

* Include VisitorAPI 2.0.0
* Herhaalde functieaanroepen en controles zodat SDID wordt verbruikt nadat de afbreekcontrole is voltooid. (AN-134364)
* Toegevoegde `s.registerPreTrackCallback` en `s.registerPostTrackCallback` haken. (AN-134567)

## Versie 1.7.0

Bijgewerkt: 11 **november 2016**

* Inclusief Bezoeker-API 1.10.1.
* Werk [!DNL Audience Manager] de module bij met de Integratiebibliotheek van de Index (DIL) 6.6. (AN-132065)
* Opname van de Bezoeker-API 1.9.0. (AN-132072)
* Update [!DNL AppMeasurement] [!DNL Audience Manager] Module met DIL 6.5 en Extra Configuraties (AN-129411)
* Opname van de Bezoeker-API 1.8.0 (AN-129887)

## Versie 1.6.4

Bijgewerkt: 18 **augustus 2016**

* Bijgewerkt [!DNL AppMeasurement] voor het lezen en schrijven van AMCV-cookies. (AN-127098)
* Opname van de Bezoeker-API 1.7.0.

>[!NOTE] Zie ook de volgende releaseopmerkingen voor [!DNL JavaScript] versie 1.6.3, die bijgewerkte vereisten voor de service Experience Cloud ID bevat.

## Versie 1.6.3

Bijgewerkt: 4 **augustus 2016**

* Probleem verholpen waarbij [!DNL AppMeasurement] vroegtijdig beëindigde aanvraagverbindingen. (AN-126448)

>[!IMPORTANT] Versie 1.6.0 van de [!DNL Experience Cloud] ID-service *vereist* [!DNL AppMeasurement] voor [!DNL JavaScript] versie 1.6.3 of hoger. Als u wilt upgraden naar versie 1.6.0 van de Experience Cloud ID-service, moet u [!DNL AppMeasurement] code versie 1.6.3 of hoger gebruiken.

## Versie 1.6.2

Releasedatum: 21 **juli 2016**

* Opname van de Bezoeker-API 1.6.0.
* Probleem verholpen waarbij de onjuiste, verduisterde methode in de Bezoeker-API [!DNL AppMeasurement] werd aangeroepen. (AN-126006)
* Probleem verholpen dat de [!DNL JavaScript] fout veroorzaakte: &quot;Kenmerk alleen geldig op v:image&quot;. (AN-124009)

## Versie 1.6.1

Releasedatum: 16 **juni 2016**

* Opname van de Bezoeker-API 1.5.7.
* Probleem verholpen met het volgen van koppelingen in Firefox die de gebeurtenis complete niet hebben geactiveerd.

## Versie 1.6

Releasedatum: 21 **april 2016**

* De module [!DNL AppMeasurement] Activiteitenkaart is geïntegreerd in de [!DNL AppMeasurement] standaardmodule, zodat u slechts naar één [!DNL .js] bestand hoeft te verwijzen. Bovendien wordt het volgen van de Kaart van de Activiteit geactiveerd door gebrek. (AN-112689)
* Oplossing voor een afbreekprobleem met de volgorde van query-tekenreeksvariabelen in [!DNL AppMeasurement], zodat dat het laatst *`pageURLRest`* is. (AN-114647)

## Versie 1.5.4

Releasedatum: 17 **maart 2016**

* Opname van de Bezoeker-API 1.5.4
* Ondersteuning voor de opt-out voor bezoekers-API 1.5.4+

## Versie 1.5.3

Releasedatum: 21 **januari 2016**

* Vaste behandeling van [!DNL Audience Manager] module wanneer POSTs voor het volgen van vraag wordt gebruikt. (AN-115381)
* Verplaatst de rest van de pagina-URL (&quot;-g&quot;) naar het einde van de queryreeks voor het volgende verzoek. (AN-114647)

## Versie 1.5.2

Releasedatum: 5 **november 2015**

* Opname van de Bezoeker-API 1.5.3.
* Vaste detectie van IE11 voor URL Truncation 2047 (AN-114914)

## Versie 1.5.1

Releasedatum: 17 **september 2015**

* Opname van de Bezoeker-API 1.5.2
* Bijgewerkte module om AAM DIL 6.2 te gebruiken - getCustomer IDs van VisitorAPI.js en hen in /event vraag door te geven aan AAM. [!DNL Audience Manager] (AN-104978)

## Versie 1.5

Releasedatum: 18 **juni 2015**

* Ondersteuning voor Bezoeker API 1.5, die de *`getCustomerIDs`* methode gebruikt om id&#39;s van klanten en geverifieerde status te verzamelen, en de id&#39;s verzendt met verzoeken om gegevensverzameling.
* Oplossing voor het maken van een duplicaat van het doeliframe in de **[!UICONTROL AudienceManagement]** module (DIL 6.1)
* Oplossing voor het bekende probleem dat in release 1.4.5 werd beschreven.

## Versie 1.4.5

Releasedatum: 21 **mei 2015**

* Vanaf iOS SDK versie 4.5 kunt u met een nieuwe iOS-extensie gebruiksgegevens verzamelen van uw Apple Watch-apps, Today-widgets, widgets voor fotobewerking en alle andere iOS-extensies. Zie de implementatie [van](https://docs.adobe.com/content/help/en/mobile-services/ios/ios-ext/ios-ext.html) iOS-extensies in de gebruikershandleiding voor mobiele services.
* Vanaf Android SDK versie 4.5 kunt u met een nieuwe Android-extensie gegevens verzamelen van uw Android-webtoepassing die kan worden gebruikt. Zie [Android-variabelen](https://docs.adobe.com/content/help/en/mobile-services/android/wearables-android/android-wearable.html) in de gebruikershandleiding voor mobiele services.
* Opname van de Bezoeker-API 1.4.
* Bijgewerkte module PubliekManagement voor het gebruik van DIL versie 6.0.

>[!NOTE] **Bekend probleem**: In de integratie van de API/ [!DNL AppMeasurement] [!DNL Audience Manager] Module van de Bezoeker zijn er twee iFrame-aanvragen voor het publiceren van de bestemming gemaakt in IE6-9: `//fast.<subdomain>.demdex.net/dest5.html` en `//fast.<subdomain>.demdex.net/dest4.html`. Het juiste gedrag, zoals in andere browsers, is alleen laden `//fast.<subdomain>.demdex.net/dest5.html`.

## Versie 1.4.4

Releasedatum: 16 **april 2015**

* U kunt nu aangepaste contextgegevensvariabelen opnemen met levenscyclusmetriek.
* De `trackBeacon` en de `clearCurrentBeacon` vraag zijn nu beschikbaar in PhoneGap.
* Een minder belangrijke moeilijke situatie om identiteitskaart van het de vraagprofiel van de lichte server na de `trackLight` vraag te ontruimen.

## Versie 1.4.3

Releasedatum: 19 **februari 2015**

* Alle behandeling van vertraagde het volgen vraag verenigbaar gemaakt, die kwesties met gesteunde variabelen tijdens de vertraging, zoals het geklikte voorwerp lost.
* Veranderd om automatisch verwijzend volgen na de eerste volgende vraag niet te doen zodat zal de tweede, derde, enz het volgen vraag (gewoonlijk verbinding het volgen) niet de verwijzer tweemaal tellen wanneer manueel vóór de eerste volgende vraag *`s.referrer`* werd geplaatst.
* Het ZIP voor distributie is bijgewerkt en bevat Bezoeker API 1.3.5.

## Versie 1.4.2

Releasedatum: 15 **januari 2015**

* Correctie van de afhandeling van de WebKit-prerender om te voorkomen dat vooraf weergegeven pagina&#39;s die niet worden weergegeven, worden bijgehouden.
* Het ZIP voor distributie is bijgewerkt en bevat nu Bezoeker API 1.3.4 en een bijgewerkte **[!UICONTROL AudienceManagement]** module met DIL versie 5.5.

## Versie 1.4.1

Releasedatum: 18 **september 2014**

* Er is een `tagContainerMarker` variabele toegevoegd waarmee de implementatie maximaal 4 tekens kan opgeven die samen met een extra streepjesscheidingsteken aan de versietekenreeks worden toegevoegd. Dit wordt gebruikt door dynamisch tagbeheer.

   ```js
   // JavaScript
   s.tagContainerMarker = "D1.0";
   
   // Data Collection request
   //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
   ```

   De 4 tekens zijn beperkt tot tekens die zijn toegestaan in URL-bestandspaden, zoals alfanumeriek en punt.

* Op pagina&#39;s met twee labels en H-code heeft u een lus gecorrigeerd die kan optreden tijdens het automatisch bijhouden van koppelingen (downloaden en afsluiten) waarbij geforceerde koppelingen moeten worden bijgehouden (standaard in Webkit-browsers). Daarnaast is er een algemene beveiliging toegevoegd rondom het automatisch bijhouden van koppelingen om vergelijkbare lusbewerkingen te voorkomen. Met deze beveiliging beperkt u het automatisch bijhouden van koppelingen bij herhaalde klikken tot *hetzelfde* object en dit tot één keer per 10 seconden. Deze beveiliging is alleen van toepassing op het automatisch bijhouden van koppelingen, zodat oproepen voor het handmatig bijhouden van koppelingen (s.tl) niet beperkt zijn. Klikken op verschillende objecten worden ook niet beïnvloed door deze beveiliging en worden bijgehouden.
* Correctie van afhandeling van geklikt object wanneer een vertraging nodig is.
* Probleem verholpen waarbij een aantal pagina&#39;s werd geteld wanneer s.t werd aangeroepen vanuit een functie klikkoppeling als de bezoeker-API nog niet de vereiste waarden heeft.
* Ondersteuning voor HTTP POST.

   > [!IMPORTANT] Voor een [!DNL Analytics] vraag om de POST methode in plaats van de GET methode in te gebruiken [!DNL AppMeasurement] (een methode om afgekapte URLs in IE [](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html)op te lossen), moet u de recentste implementatie van de Dienst van identiteitskaart van de Bezoeker voor de Wolk van de Ervaring gebruiken.

## Versie 1.4

Releasedatum: 21 **augustus 2014**

* Het bijhouden van browserplug-ins (`p` queryparameter) als plug-ins wordt niet meer gerapporteerd in versie 15.
* Toevoeging van de **[!UICONTROL AudienceManagement]** Module in het gecomprimeerde bestand.
* Extra ondersteuning voor extra eVars (76 - 250) en evenementen (101-1000).

>[!NOTE] H-Code biedt geen ondersteuning voor de extra gebeurtenissen en gebeurtenissen.

## Versie 1.3.2

Releasedatum: 19 **juni 2014**

* Correctie van de afhandeling van voltooide en wachtende vlaggen voor Bezoeker API-velden, zoals de oudere [!DNL Analytics] Bezoeker-id, die fouten veroorzaakten.
* Ondersteuning voor nieuwe functies in bezoekersidentiteitsservice 1.3.

## Versie 1.3.1

Releasedatum: 22 **mei 2014**

* [!DNL AppMeasurement] voor [!DNL JavaScript]`s_gi` functie is het niet correct zoeken naar instanties die zijn gemaakt met H-code `s_gi`. Merk op dat deze kwestie slechts enkele dubbele het etiketteren implementaties beïnvloedde waar [!DNL AppMeasurement] for [!DNL JavaScript] en de code van H op de zelfde pagina met afzonderlijke instanties waren, en `s_gi` werd gebruikt om instanties door rapportreeks te vinden.

## Versie 1.3

Releasedatum: 17 **april 2014**

* Ondersteuning voor de [Experience Cloud Visitor ID-service](https://docs.adobe.com/content/help/en/id-service/using/home.html).

## Versie 1.2.4

Releasedatum: 13 **maart 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.3

Releasedatum: 20 **februari 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.2

Releasedatum: 6 **februari 2014**

* Probleem verholpen met compatibiliteit met de [!DNL Audience Manager] DIL-module. [!DNL Audience Manager] klanten moeten ook een update uitvoeren naar versie 4.8 van de DIL-module.

## Versie 1.2.1

Releasedatum: 15 **november 2013**

* Gebeurtenissen voor een vaste pagina die worden gebruikt voor het meten van hartslagvideo.

## Versie 1.2

Releasedatum: 14 **november 2013**

* Extra ondersteuning voor [hartslagvideometing](https://docs.adobe.com/content/help/en/media-analytics/using/media-overview.html).
* `VisitorAPI.js` is toegevoegd ter ondersteuning van [Bezoeker-id-service](https://docs.adobe.com/content/help/en/id-service/using/home.html).

## Versie 1.1.1

* Er is voorkomen dat een aanroep voor het bijhouden van koppelingen vanuit Opera-browsers wordt verzonden voor koppelingen die beginnen met &quot;opera:&quot; (&quot;opera:&quot; is vergelijkbaar met &quot;about:&quot; en &quot;chrome:&quot; in andere browsers).
* Toegevoegd `alt=""` aan alle voorwerpen van het Beeld om aan Toegankelijke Video en Communicatie Wet te voldoen.

## Versie 1.1

Releasedatum: 18 **september 2013**

* Correctie van de ondersteuning voor het plaatsen van de bibliotheek- en paginacode in de `head` tag.
* Ondersteuning voor ontbrekende module toegevoegd. `onLoad`

## Versie 1.0.3

Releasedatum: 15 **augustus 2013**

* Extra ondersteuning voor implementatie via Adobe-tagbeheer.
* Probleem verholpen waarbij het instellen van hiërarchievariabelen voor het [!DNL AppMeasurement] object werd voorkomen.

## Versie 1.0.2

Releasedatum: 18 **juli 2013**

* De hash/het fragment wordt nu genegeerd door de koppeling automatisch te volgen. Eerder werd automatisch de volgende URL bijgehouden sinds het volledige `href` eindigde in `.pdf`:

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   De hash/het fragment wordt nu genegeerd, zodat de koppeling alleen wordt bijgehouden wanneer de bestandsnaam eindigt in een extensie die overeenkomt met de bestandsnaam.

## Versie 1.0.1

Releasedatum: 23 **mei 2013**

Er is nu een nieuwe [!DNL JavaScript] [!DNL AppMeasurement] bibliotheek beschikbaar in Codebeheer. Deze bibliotheek biedt dezelfde basisfunctionaliteit, maar is lichter en sneller voor gebruik op zowel mobiele als desktopsites. [!DNL s_code.js]

* 3-7 keer sneller dan de H.25-code.
* Slechts 21k ongecomprimeerd en 8k gzipped (de code van H.25 is 33k ongecomprimeerd en 13k gzipped).
* Native ondersteuning voor het ophalen van queryparameters, het lezen en schrijven van cookies en het uitvoeren van geavanceerde koppelingstracering.
* Klein en snel genoeg voor gebruik met mobiele sites en robuust genoeg voor gebruik op het volledige desktopweb, zodat u in alle webomgevingen gebruik kunt maken van één bibliotheek.
