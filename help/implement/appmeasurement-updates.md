---
title: AppMeasurement voor JavaScript-releaseopmerkingen
description: Cumulatieve releaseopmerkingen voor AppMeasurement voor JavaScript.
subtopic: Release notes
exl-id: 80b935f0-3ec5-4ffa-9858-f83ae9a6b763
source-git-commit: 7f27e92b1fc378516423bc971b05e34880897ec9
workflow-type: tm+mt
source-wordcount: '2214'
ht-degree: 3%

---

# AppMeasurement voor JavaScript-releaseopmerkingen

Cumulatieve releaseopmerkingen voor [!DNL AppMeasurement] voor JavaScript.

<!-- https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log -->

U kunt de recentste versie van AppMeasurement in [de Manager van de Code ](/help/admin/admin/code-manager-admin.md) downloaden.

## Versie 2.2.2.3

Releasedatum: **11 oktober 2021**

* Bijgewerkte dossiers die de documentatie van de Hulp van verwijzingen voorzien om aan de huidige plaatsen van de Hulp te richten.

## Versie 2.2.2

Releasedatum: **7 september 2021**

* Deze update zorgt ervoor dat `opt.dmp` en `opt.sell` altijd worden opgenomen bij het bijhouden van koppelingen. Hier volgt een [volledige lijst van toestemmingsvariabelen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html).

## Versie 2.22.1

Releasedatum: **17 augustus 2021**

* Klanten die opt-out gebruiken hebben de server-side het door:sturen opt-out parameters niet kunnen gezien wanneer het volgen van verbindingen. De correcties in deze release zorgen ervoor dat de markeringen voor niet-deelname worden verzonden als deze aanwezig zijn bij het bijhouden van koppelingen.

## Versie 2.2.2.0

Releasedatum: **4 augustus 2020**

* Oplossing voor ontbrekende referentie wanneer de eerste melding niet is verzonden vanwege de gebruikersvoorkeuren.

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

* AppMeturement kan koekjes nu dwingen om het Veilige attribuut te omvatten door de [`writeSecureCookies`](vars/config-vars/writesecurecookies.md) variabele te plaatsen. De vereiste voor deze variabele is dat de gehele clientwebsite veilig wordt aangeboden (HTTPS). (AN-204604)

## Versie 2.17.0

Releasedatum: **23 augustus 2019**

* Toegevoegde ondersteuning voor herschikking van Baidu-queryreeks. (AN-182483)
* Probleem verholpen dat storende bezoekerswaarden veroorzaakte in hits die in de wachtrij stonden terwijl werd gewacht op aanmelden. (AN-184391)

## Versie 2.16.0

Releasedatum: **15 augustus 2019**

* Geïmplementeerde `sendBeacon` steun in [!UICONTROL AppMeasurement] voor uitgangsverbindingen. Als bij een treffer `sendBeacon` wordt gebruikt en de pagina wordt verwijderd, is het verzoek nog steeds voltooid. Dit is zeer nuttig voor uitgangsverbindingen omdat het waarschijnlijker is dat de treffer de servers van de gegevensinzameling bereikt. (AN-175142)
* ECID/fid-waarden worden nu in de cache geplaatst bij de eerste hit, ook al veranderen de instellingen voor OptIn. (AN-175142)
* Bijgewerkte Module van het Beheer van het Publiek aan DIL 9.3. (AN-182704)
* De blootgestelde schakelaar in `s.ActivityMap.trackScrollReach` om rolbereik het volgen of weg te zetten. (AN-182754)
* Bijgewerkte AppMeasurement om de Dienst van bezoeker ID 4.4.0 te gebruiken. (AN-182912)

## Versie 2.15.0

Releasedatum: **15 juli 2019**

* Toegevoegde ActivityMap scroll bereiktracking naar de extensie Activity Map (AN-172949)
* DIL 9.2 toegevoegd aan AppMeasurement (AN-182472)

## Versie 2.14.0

Releasedatum: **21 mei 2019**

* Oplossing voor problemen met het beheer van de status van tracker-parameters wanneer meerdere hits in behandeling zijn. (AN-176931, AN-176629, DTM-12758)
* Bijgewerkte AppMeasurement om Visitor.js 4.3.0 (AN-180049) te omvatten

## Versie 2.13.0

Releasedatum: **10 april 2019**

* Oplossing voor veel gemelde problemen met clearVars. Het probleem doet zich voor wanneer hits worden verzonden voordat de tracker gereed is. Wanneer de tracker gereed is, kan de bibliotheek variabelen instellen die al zijn gewist of gewijzigd. (AN-176931, AN-176629, DTM-12758).

## Versie 2.12.0

Releasedatum: **22 februari 2019**

* Bijgewerkte module van het Beheer van de Publiek aan DIL 9.1. (AN-175255)
* GTM-beveiligingsbeleid staat geen Activity Map-module toe. (AN-174679)
* Verbeterde AppMeasurement om opt-out na te leven wanneer de Identiteitsdienst niet in opt-in wordt goedgekeurd. (AN-175259)

## Versie 2.11.0

Releasedatum: **11 februari 2019**

* Toegevoegde ondersteuning voor de nieuwe functionaliteit voor Adobe Opt-in-services in AppMeasurement. (AN-163546)
* Toegevoegde ondersteuning voor het opslaan van gegevens voor het bijhouden van koppelingen in sessieopslag. (AN-162272)
* Toegevoegde ondersteuning voor het type mediastream voor audioanalyse. (AN-173265)

## Versie 2.10.0

Releasedatum: **20 september 2018**

Deze versie zorgt ervoor dat de [!DNL AppMeasurement] bibliotheek cookies correct voor alle verbindingstypen verzendt.

* [!DNL AppMeasurement] blokkeert cookietransmissies tijdens POST. (AN-165538)
* Ondersteuning voor XDomainRequest neerzetten. (AN-165733)
* Verminder [!DNL AppMeasurement] standaardkooklevensduur van vijf tot twee jaar. (AN-158572)
* Verwijder de Module van Media uit de Manager van de Code ( [!DNL AppMeasurement]) (AN-166590)

## Versie 2.9.0

Releasedatum: **24 mei 2018**

>[!NOTE]
>
>Bezoeker-API 3.0 of hoger is vereist voor klanten die de [!DNL Experience Cloud]-id-service gebruiken. Adobe raadt aan een upgrade uit te voeren naar de nieuwste versie van de Bezoeker-API wanneer gekoppelde codebibliotheken worden bijgewerkt ( [!DNL at.js], [!DNL AppMeasurement.js] enzovoort.)

* Bijgewerkt [!DNL AppMeasurement] om de bijgewerkte interface van de Bezoeker voor het vragen van IDs te gebruiken. (AN-151483)
* Probleem verholpen waarbij de functie voor het bijhouden van koppelingen steeds wordt weggeschreven nadat het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Probleem verholpen waarbij `registerPreTrackCallback` en `registerPostTrackCallback` de handtekening van de callback-functie afbreken wanneer deze meerdere keren wordt aangeroepen. (AN-158566)

## Versie 2.8.2

Releasedatum: **12 april 2018**

* Werk [!DNL AppMeasurement] bij om de bijgewerkte bezoekersinterface te gebruiken voor het vragen van IDs. (AN-151483)
* De functie voor het bijhouden van koppelingen wordt steeds opnieuw geschreven als het bijhouden van koppelingen is uitgeschakeld. (AN-156332)
* Verminder [!DNL AppMeasurement] standaardkooklevensduur van vijf tot twee jaar. (AN-158572)

## Versie 2.8.1

Releasedatum: **29 maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

## Versie 2.8.0

Releasedatum: **15 maart 2018**

Rebundle Visitor API 3.1.0 (AN-159524), die de hotfixes bevat: (CORE-11390, CORE-10634)

* Bundel VAPI v3.1 met [!DNL AppMeasurement] v2.8. (AN-158353)
* Refactor bouwt het eindpunt van de gegevensverzameling om het delen te vergemakkelijken. (AN-156647)
* Voeg de metriek van de verzoekround-trip timing aan [!DNL AppMeasurement] toe. (AN-158343)

## Versie 2.7.0

Releasedatum: **18 januari 2018**

* Ondersteuning voor IE 6 tot en met 9
* Opname van de Bezoeker-API v3.0.0
* Opname van DIL v7.00

## Versie 2.6.0

Releasedatum: **9 november 2017**

Probleem verholpen waarbij [!DNL AppMeasurement] de bibliotheek niet altijd de juiste accountcombinatie instelt wanneer s_gl wordt aangeroepen. (AN-152153)

## Versie 2.5.0

Releasedatum: **21 september 2017**

* Opname van [!DNL dil.js 6.12] ( [!DNL Audience Manager] module)
* Opname van de Bezoeker-API 2.5.0.

## Versie 2.4.0

Releasedatum: **17 augustus 2017**

* Inclusief dil.js v6.11
* Inclusief bezoeker-API 2.4.0

## Versie 2.3.0

Releasedatum: **20 juli 2017**

* Correctie van bug waarbij `s.Util.getQueryParam` `#` heeft vastgelegd
* Toegevoegd v6.10 van `dil.js` (AN-145701)

## Versie 2.2.0

Releasedatum: **8 juni 2017**

* Toegevoegde ondersteuning voor meerdere [!DNL AppMeasurement]-instantiatievolgorde. (AN-138237)
* Opname van versie 2.2.0 Bezoeker-API. (AN-144042)

## Versie 2.1.0

Releasedatum: **20 april 2017**

* Inclusief de meest recente versie van `dil.js` (AN-140396)
* Toegevoegde ondersteuning voor de parameter `adobe_mc_ref` die de paginaverwijzing overschrijft. (AN-131920)
* Opnieuw opgenomen Bezoeker-API 2.1.0. (AN-140873)
* Toegevoegde parameter `mcorgid`. (AN-139586)
* Toegevoegde cp (customerPerspective) parameter. (AN-140897)

## Versie 2.0.0

Releasedatum: **9 maart 2017**

* Verplaatst naar een nieuw bouwstijlproces dat een update van het versieaantal aan 2.0.0 vereist. (AN-137878)
* Verplaatst mboxMCSDID behandeling in de correcte sectieplaats waar de volgende vraag wordt gemaakt. (AN-138483)

## Versie 1.8.0

Releasedatum: **19 januari 2017**

* Include VisitorAPI 2.0.0
* Herhaalde functieaanroepen en controles zodat SDID wordt verbruikt nadat de afbreekcontrole is voltooid. (AN-134364)
* Toegevoegde `s.registerPreTrackCallback` en `s.registerPostTrackCallback` haken. (AN-134567)

## Versie 1.7.0

Bijgewerkt: **11 november 2016**

* Inclusief Bezoeker-API 1.10.1.
* Update [!DNL Audience Manager] module met de Bibliotheek van de Integratie van de Index (DIL) 6.6. (AN-132065)
* Opname van de Bezoeker-API 1.9.0. (AN-132072)
* [!DNL AppMeasurement] [!DNL Audience Manager] Module met DIL 6.5 en Extra Configuraties (AN-129411) bijwerken
* Opname van de Bezoeker-API 1.8.0 (AN-129887)

## Versie 1.6.4

Bijgewerkt: **18 augustus 2016**

* [!DNL AppMeasurement] is bijgewerkt om AMCV-cookies te lezen en te schrijven. (AN-127098)
* Opname van de Bezoeker-API 1.7.0.

>[!NOTE]
>
>Zie ook de volgende releaseopmerkingen voor [!DNL JavaScript] versie 1.6.3, die bijgewerkte vereisten voor de Experience Cloud ID-service bevatten.

## Versie 1.6.3

Bijgewerkt: **4 augustus 2016**

* Probleem verholpen waarbij [!DNL AppMeasurement] vroegtijdig de aanvraagverbindingen beëindigde. (AN-126448)

>[!IMPORTANT]
>
>Versie 1.6.0 van de [!DNL Experience Cloud] ID-service *vereist* [!DNL AppMeasurement] voor [!DNL JavaScript] versie 1.6.3 of hoger. Als u wilt bijwerken naar versie 1.6.0 van de Experience Cloud-id-service, moet u [!DNL AppMeasurement] codecoversie 1.6.3 of hoger gebruiken.

## Versie 1.6.2

Releasedatum: **21 juli 2016**

* Opname van de Bezoeker-API 1.6.0.
* Probleem verholpen waarbij [!DNL AppMeasurement] de onjuiste, verduisterde methode in de Bezoeker-API aanriep. (AN-126006)
* Probleem verholpen die de fout [!DNL JavaScript] veroorzaakte: &quot;Kenmerk alleen geldig op v:image&quot;. (AN-124009)

## Versie 1.6.1

Releasedatum: **16 juni 2016**

* Opname van de Bezoeker-API 1.5.7.
* Probleem verholpen met het volgen van koppelingen in Firefox die de gebeurtenis complete niet hebben geactiveerd.

## Versie 1.6

Releasedatum: **21 april 2016**

* De [!DNL AppMeasurement] module van de Activity Map is geïntegreerd in [!DNL AppMeasurement] standaardmodule, zodat u slechts één [!DNL .js] dossier moet van verwijzingen voorzien. Bovendien wordt het bijhouden van Activity Mappen standaard geactiveerd. (AN-112689)
* Oplossing voor een afbreekprobleem met de volgorde van query-tekenreeksvariabelen in [!DNL AppMeasurement], zodat *`pageURLRest`* het laatst is. (AN-114647)

## Versie 1.5.4

Releasedatum: **17 maart 2016**

* Opname van de Bezoeker-API 1.5.4
* Ondersteuning voor de opt-out voor bezoekers-API 1.5.4+

## Versie 1.5.3

Releasedatum: **21 januari 2016**

* Vaste behandeling van [!DNL Audience Manager] module wanneer POSTs voor het volgen van vraag wordt gebruikt. (AN-115381)
* Verplaatst de rest van de pagina-URL (&quot;-g&quot;) naar het einde van de queryreeks voor het volgende verzoek. (AN-114647)

## Versie 1.5.2

Releasedatum: **5 november 2015**

* Opname van de Bezoeker-API 1.5.3.
* Vaste detectie van IE11 voor URL Truncation 2047 (AN-114914)

## Versie 1.5.1

Releasedatum: **17 september 2015**

* Opname van de Bezoeker-API 1.5.2
* Bijgewerkt [!DNL Audience Manager] module om AAM DIL 6.2 te gebruiken - getCustomer IDs van VisitorAPI.js en hen in /event vraag door te geven aan AAM. (AN-104978)

## Versie 1.5

Releasedatum: **18 juni 2015**

* Ondersteuning voor Bezoeker API 1.5, die de methode *`getCustomerIDs`* gebruikt om id&#39;s van klanten en de geverifieerde status te verzamelen, en de id&#39;s verzendt met verzoeken om gegevensverzameling.
* Oplossing voor het maken van een duplicaat van het doel in de module **[!UICONTROL AudienceManagement]** (DIL 6.1)
* Oplossing voor het bekende probleem dat in release 1.4.5 werd beschreven.

## Versie 1.4.5

Releasedatum: **21 mei 2015**

* Vanaf iOS SDK versie 4.5 kunt u met een nieuwe iOS-extensie gebruiksgegevens verzamelen van uw Apple Watch-apps, hedendaagse widgets, widgets voor fotobewerking en alle andere iOS-extensie-apps. Zie [iOS-extensie-implementatie](https://experienceleague.adobe.com/docs/mobile-services/ios/ios-ext/ios-ext.html) in de gebruikershandleiding voor mobiele services.
* Vanaf Android SDK versie 4.5 kunt u met een nieuwe Android-extensie gegevens verzamelen van uw Android-webtoepassing die kan worden gebruikt. Zie [Android-variabelen](https://experienceleague.adobe.com/docs/mobile-services/android/wearables-android/android-wearable.html) in de gebruikershandleiding voor mobiele services.
* Opname van de Bezoeker-API 1.4.
* Bijgewerkte module van het Beheer van het Publiek om DIL versie 6.0 te gebruiken.

>[!NOTE]
>
>**Bekend probleem**: In de integratie van de API/ [!DNL AppMeasurement] [!DNL Audience Manager] module van de Bezoeker zijn er twee iFrame-aanvragen voor het publiceren van de bestemming gemaakt in IE6-9:  `//fast.<subdomain>.demdex.net/dest5.html` en   `//fast.<subdomain>.demdex.net/dest4.html`. Het correcte gedrag, zoals in andere browsers wordt gezien, is om slechts `//fast.<subdomain>.demdex.net/dest5.html` te laden.

## Versie 1.4.4

Releasedatum: **16 april 2015**

* U kunt nu aangepaste contextgegevensvariabelen opnemen met levenscyclusmetriek.
* De `trackBeacon` en `clearCurrentBeacon` vraag zijn nu beschikbaar in PhoneGap.
* Een kleine oplossing om de lichte identiteitskaart van het de vraagprofiel van de server na `trackLight` vraag te ontruimen.

## Versie 1.4.3

Releasedatum: **19 februari 2015**

* Alle behandeling van vertraagde het volgen vraag verenigbaar gemaakt, die kwesties met gesteunde variabelen tijdens de vertraging, zoals het geklikte voorwerp lost.
* Veranderd om automatisch verwijzend volgen na de eerste volgende vraag niet te doen zodat zal de tweede, derde, enz het volgen vraag (gewoonlijk verbinding het volgen) niet de verwijzer tweemaal tellen wanneer *`s.referrer`* manueel vóór de eerste volgende vraag werd geplaatst.
* Het ZIP voor distributie is bijgewerkt en bevat Bezoeker API 1.3.5.

## Versie 1.4.2

Releasedatum: **15 januari 2015**

* Correctie van de afhandeling van de WebKit-prerender om te voorkomen dat vooraf weergegeven pagina&#39;s die niet worden weergegeven, worden bijgehouden.
* De ZIP voor distributie is bijgewerkt en bevat nu bezoeker API 1.3.4 en een bijgewerkte **[!UICONTROL AudienceManagement]**-module die DIL versie 5.5 bevat.

## Versie 1.4.1

Releasedatum: **18 september 2014**

* Er is een variabele `tagContainerMarker` toegevoegd waarmee de implementatie maximaal 4 tekens kan opgeven die samen met een extra streepjesteken aan de versiereeks worden toegevoegd. Dit wordt gebruikt door dynamisch tagbeheer.

   ```js
   // JavaScript
   s.tagContainerMarker = "D1.0";
   
   // Data Collection request
   //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
   ```

   De 4 tekens zijn beperkt tot tekens die zijn toegestaan in URL-bestandspaden, zoals alfanumeriek en punt.

* Op pagina&#39;s met twee labels en H-code heeft u een lus gecorrigeerd die kan optreden tijdens het automatisch bijhouden van koppelingen (downloaden en afsluiten) waarbij geforceerde koppelingen moeten worden bijgehouden (standaard in Webkit-browsers). Daarnaast is er een algemene beveiliging toegevoegd rondom het automatisch bijhouden van koppelingen om vergelijkbare lusbewerkingen te voorkomen. Deze bescherming beperkt het automatisch volgen van verbindingen van herhaalde kliks aan *same* voorwerp tot eens om de 10 seconden. Deze beveiliging is alleen van toepassing op het automatisch bijhouden van koppelingen, zodat oproepen voor het handmatig bijhouden van koppelingen (s.tl) niet beperkt zijn. Klikken op verschillende objecten worden ook niet beïnvloed door deze beveiliging en worden bijgehouden.
* Correctie van afhandeling van geklikt object wanneer een vertraging nodig is.
* Probleem verholpen waarbij een aantal pagina&#39;s werd geteld wanneer s.t werd aangeroepen vanuit een functie klikkoppeling als de bezoeker-API nog niet de vereiste waarden heeft.
* Ondersteuning voor HTTP-POST.

   >[!IMPORTANT]
   >
   >Voor een [!DNL Analytics] vraag om de methode van de POST in plaats van de methode van de GET in [!DNL AppMeasurement] (een methode om [beknot URLs in IE](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html) op te lossen) te gebruiken, moet u de recentste implementatie van de Dienst van identiteitskaart van de Bezoeker voor de Experience Cloud gebruiken.

## Versie 1.4

Releasedatum: **21 augustus 2014**

* Het verwijderen van het volgen van browser stop-ins (`p` vraagparameter) als stop-ins wordt niet meer gemeld in versie 15.
* Toevoeging van de **[!UICONTROL AudienceManagement]** Module in het gecomprimeerde bestand.
* Extra ondersteuning voor extra eVars (76 - 250) en evenementen (101-1000).

>[!NOTE]
>
>H-Code biedt geen ondersteuning voor de extra gebeurtenissen en gebeurtenissen.

## Versie 1.3.2

Releasedatum: **19 juni 2014**

* Correctie van de afhandeling van voltooide en wachtende vlaggen voor Bezoeker API-velden zoals de verouderde [!DNL Analytics] Bezoeker-id die fouten veroorzaakte.
* Ondersteuning voor nieuwe functies in bezoekersidentiteitsservice 1.3.

## Versie 1.3.1

Releasedatum: **22 mei 2014**

* [!DNL AppMeasurement] voor  [!DNL JavaScript] `s_gi` functie is het niet correct zoeken naar instanties die zijn gemaakt met H-code  `s_gi`. Merk op dat dit probleem slechts invloed had op enkele implementaties van dubbele codering waarbij [!DNL AppMeasurement] voor [!DNL JavaScript] en H-code op dezelfde pagina met afzonderlijke instanties stonden en `s_gi` werd gebruikt om instanties te zoeken op basis van een rapportsuite.

## Versie 1.3

Releasedatum: **17 april 2014**

* Ondersteuning voor de service [Experience Cloud-bezoeker-id](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Versie 1.2.4

Releasedatum: **13 maart 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.3

Releasedatum: **20 februari 2014**

* Bugfixes voor hartslagvideo.

## Versie 1.2.2

Releasedatum: **6 februari 2014**

* Probleem verholpen met compatibiliteit met de module [!DNL Audience Manager] DIL. [!DNL Audience Manager] klanten moeten ook bijwerken naar versie 4.8 van de module DIL.

## Versie 1.2.1

Releasedatum: **15 november 2013**

* Gebeurtenissen voor een vaste pagina die worden gebruikt voor het meten van hartslagvideo.

## Versie 1.2

Releasedatum: **14 november 2013**

* Toegevoegde ondersteuning voor [Videometing hartslag](https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html).
* `VisitorAPI.js` is toegevoegd ter ondersteuning van  [Bezoeker-id-service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Versie 1.1.1

* Er is voorkomen dat een aanroep voor het bijhouden van koppelingen vanuit Opera-browsers wordt verzonden voor koppelingen die beginnen met &quot;opera:&quot; (&quot;opera:&quot; is vergelijkbaar met &quot;about:&quot; en &quot;chrome:&quot; in andere browsers).
* `alt=""` toegevoegd aan alle voorwerpen van het Beeld om aan Toegankelijke Video en Communicatie Wet te voldoen.

## Versie 1.1

Releasedatum: **18 september 2013**

* Correctie van ondersteuning voor het plaatsen van de bibliotheek- en paginacode in de tag `head`.
* Ontbrekende module `onLoad`-ondersteuning toegevoegd.

## Versie 1.0.3

Releasedatum: **15 augustus 2013**

* Extra ondersteuning voor implementatie via tagbeheer van Adobe.
* Probleem verholpen waarbij werd voorkomen dat hiërarchievariabelen op het object [!DNL AppMeasurement] werden ingesteld.

## Versie 1.0.2

Releasedatum: **18 juli 2013**

* De hash/het fragment wordt nu genegeerd door de koppeling automatisch te volgen. Eerder werd de volgende URL automatisch bijgehouden aangezien de volledige `href` in `.pdf` beëindigde:

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   De hash/het fragment wordt nu genegeerd, zodat de koppeling alleen wordt bijgehouden wanneer de bestandsnaam eindigt in een extensie die overeenkomt met de bestandsnaam.

## Versie 1.0.1

Releasedatum: **23 mei 2013**

Er is nu een nieuwe [!DNL JavaScript] [!DNL AppMeasurement]-bibliotheek beschikbaar in Codebeheer. Deze bibliotheek biedt dezelfde basisfunctionaliteit als [!DNL s_code.js], maar is lichter en sneller voor gebruik op zowel mobiele als desktopsites.

* 3-7 keer sneller dan de H.25-code.
* Slechts 21k ongecomprimeerd en 8k gzipped (de code van H.25 is 33k ongecomprimeerd en 13k gzipped).
* Native ondersteuning voor het ophalen van queryparameters, het lezen en schrijven van cookies en het uitvoeren van geavanceerde koppelingstracering.
* Klein en snel genoeg voor gebruik met mobiele sites en robuust genoeg voor gebruik op het volledige desktopweb, zodat u in alle webomgevingen gebruik kunt maken van één bibliotheek.
