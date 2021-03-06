---
title: Adobe Analytics- en browsercookies
description: Leer hoe de preventiemaatregelen voor het bijhouden van fouten invloed hebben op cookies van derden en van andere bedrijven die door Adobe Analytics zijn ingesteld.
feature: Data Configuration and Collection
exl-id: c4a4751e-49fc-40c3-aa39-f0f0b20bda1b
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '1985'
ht-degree: 0%

---

# Adobe Analytics- en browsercookies

In dit document wordt uitgelegd wat de invloed is van de traceerpreventiemaatregelen van grote browsers op cookies van derden en van andere bedrijven die door Adobe Analytics zijn ingesteld. Het omvat informatie over het programma van de Preventie van het Intelligente Volgen van Apple (ITP) evenals de beperkingen van Chrome op derdekoekjes via het attribuut SameSite.

## Hoe hebben browsers het gebruik van cookies beperkt?

>[!NOTE]
>[Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=en#cda) en [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#comparing-cja-to-traditional-adobe-analytics) kan met een persoon-id, zoals een hashed-aanmeldings-id, overschakelen op cookies als deze beschikbaar is.

### Beperkingen van cookies van andere bedrijven

Cookies die in een context van derden worden gebruikt, worden op grote schaal afgekeurd. Firefox en Safari blokkeren cookies van derden standaard vanaf respectievelijk 2019 en 2020. Chrome heeft plannen aangekondigd om ergens in 2023 de ondersteuning van cookies van derden stop te zetten. Als ze dat doen, zijn cookies van andere leveranciers onbruikbaar.

Bovendien staat Chrome momenteel alleen toe dat cookies functioneren in een context van derden als hun kenmerk &quot;SameSite&quot; is ingesteld op Geen en de cookies zijn gemarkeerd als veilig, wat betekent dat ze alleen kunnen worden gebruikt via HTTPS. Meer informatie is beschikbaar in de sectie &quot;[Wat is het koekjesattribuut SameSite, en hoe be??nvloedt het Analytics?](#samesite-effect)&quot;

#### Welke Adobe-cookies van derden worden be??nvloed?

De bezoekersidentiteitsdienst gebruikt &quot;[demdex.net](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)&quot; cookie om bezoekers een permanente id in verschillende klantdomeinen te geven. De dienst van identiteitskaart van de Analyse van de erfenis, &quot;s_vi&quot;koekje, wordt geplaatst als derdekoekje voor implementaties die geen de inzamelingsdomein van de douaneCNAME gebruiken.

In browsers waar cookies van derden worden geblokkeerd, is interdomeintracering niet beschikbaar.

### Beperkingen van cookies van eerste partij {#limitations-first-party-cookies}

Cookies van eerste bedrijven zijn toegestaan in alle grote browsers. Apple beperkt echter de levensduur van cookies van eerste bedrijven die door Adobe via het Intelligent Tracking Program (ITP) zijn ingesteld. Dit is van invloed op Safari en op alle browsers op iOS en iPad OS.

Adobe van eerste partijen zijn beperkt tot een vervaldatum van 7 dagen, want doorklikken die Apple bepaalt komt van trackers, een vervaldatum van 24 uur. Als een gebruiker bij een vervaldatum van 7 dagen uw site bezoekt en binnen 7 dagen terugkeert, wordt de vervaldatum van de cookie met nog eens 7 dagen verlengd. Als een gebruiker echter uw site bezoekt en binnen acht dagen terugkeert, worden deze tijdens het tweede bezoek behandeld als een nieuwe gebruiker.

Momenteel, is het beleid ITP op alle eerste-partijkoekjes van toepassing die door Adobe worden geplaatst, of u de dienst van identiteitskaart van de Bezoeker of de erfenisAnalytics ID (&quot;s_vi&quot;koekje) gebruikt. Op ????n punt, waren deze beleidsvormen van toepassing slechts op koekjes plaatste cli??nt-kant en niet op koekjes plaatste server-kant via een implementatie CNAME. In november 2020, echter, werd ITP bijgewerkt om op implementaties CNAME eveneens van toepassing te zijn.

#### Tijdlijn van belangrijke wijzigingen in ITP-beleid {#ITP-timeline}

* februari 2019 met [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/): Cookies op de client waren beperkt tot zeven dagen.
* april 2019 met [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/): Cookies aan de clientzijde waren beperkt tot 24 uur voor advertenties waarbij het verwijzende domein a) betrokken was bij intersite tracering en b) de uiteindelijke URL een queryreeks en/of een fragment-id bevatte.
* november 2020 met [CNAME Camoufleren en Bounce Tracking Defense](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/): ITP-beperkingen zijn uitgebreid naar CNAME-implementaties.

Het beleid van ITP evolueert vaak. Zie Apple voor het meest recente beleid [Trackingpreventie in Webkit](https://webkit.org/tracking-prevention).

#### Welke Adobe first-party koekjes worden be??nvloed?

Alle cookies van de eerste partij die zijn ingesteld door Adobe en de bijbehorende JavaScript-bibliotheken, worden be??nvloed door het ITP-beleid:

* [&quot;AMCV&quot;-cookies](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html) ingesteld door de Adobe Experience Cloud Visitor ID (ECID)-servicebibliotheek
* De nalatenschap Analytics [cookie &quot;s_vi&quot;](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) wanneer het met de inzameling van de eerste partijgegevens gebruikend een CNAME wordt gevormd
* De nalatenschap Analytics [cookie &quot;s_fid&quot;](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html), dit is de fallback-cookie die wordt gebruikt wanneer &quot;s_vi&quot; niet kan worden ingesteld

#### Wat is de impact van ITP op Safari voor Analytics?

De impact van de ITP-beperkingen kan aanzienlijk vari??ren, afhankelijk van het gedrag van uw gebruikers. Alleen bezoekers die een browser gebruiken die invloed heeft op ITP (bijvoorbeeld Safari) en die terugkeren na een afwezigheid van zeven dagen, worden hierdoor be??nvloed. Als bezoekers niet binnen zeven dagen een ITP-browser gebruiken of terugkeren, hebben ze geen invloed. Het is belangrijk om uw eigen gegevens in Analytics te herzien om de omvang van de gevolgen van deze beperking te begrijpen. Zie voor tips over het meten van de impact op uw sites &quot;[Hoe kan ik bepalen als de veranderingen Safari mijn zaken be??nvloeden?](#measure-itp-effect)&quot;

Als deze beperkingen wel van invloed zijn op uw gegevens, ziet u het volgende:

1. Een grotere bezoeker telt mee omdat terugkerende bezoekers worden behandeld als nieuwe bezoekers omdat hun cookies zijn verlopen. Elke metrische waarde op basis van de bezoeker (zoals Verkoop per bezoeker) wordt ook be??nvloed.
2. Wijzigingen in kenmerk. Attributie is afhankelijk van het koppelen van conversiegebeurtenissen aan voorafgaande activiteiten door dezelfde bezoeker. Nadat een cookie is verlopen, worden volgende gebeurtenissen aan een nieuwe bezoeker gekoppeld. De activiteiten van de nieuwe bezoeker kunnen niet worden gekoppeld aan de activiteiten van de vorige bezoeker.

>[!NOTE]
>
>ITP-technologie??n zijn momenteel niet van toepassing op ingesloten browsers in mobiele apps.

## Wat is het verschil tussen cookies van derden en cookies van andere leveranciers?

### Cookies van andere bedrijven

Cookies van andere bedrijven worden niet gemaakt door de websites die gebruikers bezoeken.

Hoewel browsers momenteel alle cookies van derden op dezelfde manier behandelen en opslaan, kunnen cookies van andere bedrijven zich op verschillende manieren gedragen. Met de Analytics-implementatie van een klant van andere leveranciers slaat de browser de Adobe op [demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) ID als derdekoekje, maar de cli??nt doet vraag slechts aan Adobe, en niet te onbekende of verdachte derdedomeinen. Deze cookie biedt permanente id&#39;s in verschillende domeinen en maakt beveiligde (HTTPS) inhoud mogelijk. Zie voor meer informatie [Cookies en de identiteitsservice van Experience Platforms](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html).

Binnen de analytische implementaties worden cookies van derden gebruikt voor interdomeintracering en voor het maken van gevallen waarin reclame wordt gebruikt, waaronder het opnieuw aanwijzen van advertenties. Met cookies van derden kunt u bezoekers identificeren wanneer ze verschillende domeinen bezoeken die u bezit of waarop advertenties worden weergegeven op sites die u niet hebt.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### Cookies van eerste bedrijven

Cookies van eerste bedrijven zijn domeinspecifiek en worden gemaakt door websites van klanten en opgeslagen in clientbrowsers terwijl gebruikers de websites bezoeken. Alle browsers accepteren cookies van de eerste partij, hoewel [Safari beperkt de vervaldatum van bepaalde soorten cookies van de fabrikant](#limitations-first-party-cookies).

Binnen de implementaties van Analytics, worden de eerstepartijkoekjes gebruikt om gebruikers te identificeren wanneer zij op uw plaats zijn en daarom al analyse van gebruikersactiviteit steunen. U hebt geen cookies van derden nodig om de activiteiten op de site te begrijpen.

Zie voor meer informatie [Cookies van eerste bedrijven](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html).

![Cookie-vergelijking](/help/technotes/assets/cookies2.png)

## Wat is het koekjesattribuut SameSite, en hoe be??nvloedt het de koekjes van Analytics? {#samesite-effect}

Met de release van Chrome 80 browser in februari 2020 ??? en opeenvolgende versies van Firefox- en Edge-browsers ??? dwingt het SameSite cookie-kenmerk de specificatie af voor drie verschillende waarden die bepalen of cookies in een context van derden kunnen worden gebruikt:

* `None`: Met deze instelling hebt u toegang tot andere sites en kunnen cookies worden doorgegeven in een context van derden. Als u dit kenmerk wilt opgeven, moet u ook `Secure` en alle browseraanvragen moeten HTTPS volgen. Wanneer u bijvoorbeeld de cookie instelt, koppelt u de waarden van het kenmerk als volgt: `Set-Cookie: example_session=test12; SameSite=None; Secure`. Als de cookies niet correct zijn gelabeld, kunnen ze niet meer worden gebruikt door de nieuwere browsers en worden ze afgewezen.

* `Lax`: Hiermee kunnen aanvragen voor meerdere sites alleen worden verzonden met cookies op dezelfde site voor navigatie op hoofdniveau met *veilig* (alleen-lezen, zoals `GET`) HTTP-methoden.

* `Strict`: Dezelfde-site cookie wordt niet verzonden voor externe websiteaanvragen. Het cookie wordt alleen verzonden als de site voor het cookie overeenkomt met de site in de URL-balk.

Het standaardgedrag in deze browserversies is dat cookies worden behandeld die niet zijn opgegeven `SameSite` kenmerk gelijk aan `SameSite=Lax`.

### Hoe beheert Analytics Cookie-kenmerken van SameSite?

Voor klanten die de Dienst van identiteitskaart van de Bezoeker gebruiken, hebben de koekjes de eigenschappen `SameSite=None` en `secure` standaard ingesteld, zodat deze cookies door andere gebruikers kunnen worden gebruikt.

Voor klanten die Analytics erfenisherkenningstekens (&quot;s_vi&quot;en &quot;s_fid&quot;koekjes gebruiken), worden de koekjes ook geplaatst om derdegebruiksgevallen met standaard inzamelingsdomeinen toe te laten: adobedc.net, 2o7.net, en omtr dc.net. Voor klanten die een implementatie CNAME gebruiken, de reeksen van Analytics `SameSite=Lax`.

>[!NOTE]
>
>Als u meerdere domeinen hebt en dezelfde CNAME gebruikt voor gegevensverzameling in al uw domeinen, wordt het cookie op die andere domeinen behandeld als een cookie van een derde. Als u de verouderde analytische id&#39;s gebruikt, kunt u de instelling bijwerken naar `SameSite=None` zodat deze cookies door uw sites kunnen worden gedeeld. Zie &quot;[Wijzig de waarde van SameSite wanneer u ????n CNAME voor meerdere domeinen gebruikt](#samesite-one-cname)&quot; in de volgende sectie voor meer informatie.

Voor browsers waarvan Google heeft vastgesteld dat ze cookies verkeerd verwerken wanneer `SameSite` is ingesteld op `None`, `SameSite` wordt in plaats daarvan niet ingesteld.

De volgende tabel geeft een overzicht van de SameSite-kenmerken voor Analytics-cookies:

![Cookie-tabel](/help/technotes/assets/cookies1.png)

### Hoe kunnen mijn vereisten van het plaatsadres voor het attribuut SameSite?

#### Geef al uw sitepagina&#39;s met HTTPS

Controleer of in uw JavaScript-configuratie HTTPS wordt gebruikt voor alle aanroepen naar Adobe-services.

Als uw plaats de dienst van identiteitskaart van de Bezoeker van Experience Cloud gebruikt, richt de dienst derdeHTTP- vraag aan zijn eindpunt HTTPS opnieuw, dat latentie kan verhogen maar betekent dat u niet wordt vereist om uw configuratie te veranderen.

#### Wijzig de waarde van SameSite wanneer u ????n CNAME voor meerdere domeinen gebruikt {#samesite-one-cname}

>[!NOTE]
>
>De volgende informatie heeft alleen betrekking op sites die geen gebruik maken van de service Experience Cloud Visitor ID.

Als u een CNAME-implementatie hebt die in hetzelfde domein als uw website is ingesteld, wordt het cookie gemaakt in een context van de eerste partij en hoeft u geen wijzigingen aan te brengen.

Als u echter meerdere domeinen hebt en dezelfde CNAME gebruikt voor gegevensverzameling in al uw domeinen, wordt het cookie op die andere domeinen behandeld als een cookie van een derde. Met Chrome 80 en hoger is deze niet meer zichtbaar op deze andere domeinen. Als u het gedrag in alle browsers meer op elkaar wilt laten lijken, heeft Analytics expliciet de instelling `SameSite` waarde van deze cookie naar `Lax`. Als u deze cookie in een vriendelijke externe context gebruikt, moet u de cookie met de `SameSite=None` waarde, wat ook betekent dat u altijd HTTPS moet gebruiken. Als u dit nog niet hebt gedaan, neemt u contact op met de klantenservice van Adobe om de SameSite-waarde te wijzigen voor uw beveiligde CNAME&#39;s.

## Hoe kan ik bepalen als de veranderingen Safari mijn zaken be??nvloeden? {#measure-itp-effect}

Adobe raadt klanten aan de impact binnen hun eigen bedrijf te meten voordat ze de gegevensverzameling wijzigen. U kunt Analysis Workspace gebruiken om het effect van de preventie van het volgen van ITP op uw individuele zaken te meten:

* Meet het percentage van uw verkeer van ITP-Beheerde browsers:

   1. Creeer een segment om te zien hoeveel bezoekers een platform ITP gebruiken.

      >[!NOTE]
      >
      >De specifieke browsers die door ITP worden be??nvloed hangen af van of u een implementatie CNAME gebruikte. Zie &quot;[Tijdlijn van belangrijke wijzigingen in ITP-beleid](#ITP-timeline)&quot; voor meer details .

      ![Segment voor ITP-bezoekers](/help/technotes/assets/itp-visitor-segment.png)

   2. Pas het segment op het aantal bezoeken toe om het relatieve gebruik van Safari in uw gebruikersbasis te begrijpen. Hiermee kunt u een tabel als deze maken:

      ![Percentage bezoeken van ITP-bezoekers](/help/technotes/assets/visits-vs-safari-visits.png)

* Meet het percentage bezoekers dat niet-Safari browsers gebruikt die niet binnen zeven dagen terugkeren. Als uw niet-Safari bezoekers binnen zeven dagen herhaaldelijk terugkeren, kan het zijn dat uw Safari-verkeer hierdoor niet significant wordt be??nvloed.

   1. Creeer een segment als het volgende voor verkeer niet-Safari.

      ![Segment voor bezoekers die na zeven dagen terugkeren](/help/technotes/assets/visits-after-seven-days.png)

   2. Pas het segment op het aantal bezoeken toe om het relatieve gebruik van Safari in uw gebruikersbasis te begrijpen. Hiermee kunt u een tabel als deze maken:

      ![Percentage bezoekers die na zeven dagen terugkeren](/help/technotes/assets/percent-visits-after-seven-days.png)

### Manieren om uw gegevens tijdens het rapporteren aan te passen

Als uw zaken door ITP het volgen preventie wordt be??nvloed, zou u de volgende maatregelen kunnen overwegen om uw gegevens tijdens het melden aan te passen.

* Creeer een segment om gebruikers uit te filteren ITP.

   ![Segment voor niet-ITP-bezoekers](/help/technotes/assets/non-itp-visitor-segment.png)

* Maak een berekende maatstaf om de bekende bezoekersinflatie aan te passen.

   ![Berekende maateenheid om bezoekersinflatie aan te passen](/help/technotes/assets/estimated-itp-visitors-metric.png)

>[!MORELIKETHIS]
>
>[Opties om het effect van browsercookiebeperkingen te beperken](cookieless.md)
>[De impact van Apple New App Tracking Transparency Framework op Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833)
