---
title: Adobe Analytics- en browsercookies
description: Leer hoe de preventiemaatregelen voor het bijhouden van fouten invloed hebben op cookies van derden en van andere bedrijven die door Adobe Analytics zijn ingesteld.
feature: Data Configuration and Collection
exl-id: c4a4751e-49fc-40c3-aa39-f0f0b20bda1b
role: Admin
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '1908'
ht-degree: 0%

---

# Adobe Analytics- en browsercookies

In dit document wordt uitgelegd wat de invloed is van de traceerpreventiemaatregelen van grote browsers op cookies van derden en van andere bedrijven die door Adobe Analytics zijn ingesteld. Het omvat informatie over het programma van de Preventie van het Intelligente Volgen van Apple (ITP) evenals Chrome beperkingen op derdekoekjes via het attribuut SameSite.

## Hoe hebben browsers het gebruik van cookies beperkt?

>[!NOTE]
>[ Analytics van het Apparaat van de dwars-Apparaat ](/help/components/cda/overview.md#cda) en [ Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html#comparing-cja-to-traditional-adobe-analytics) kan over koekjes vastmaken gebruikend een persoonsidentiteitskaart, zoals gehakt login identiteitskaart, als men beschikbaar is.

### Beperkingen van cookies van andere bedrijven

Cookies die in een context van derden worden gebruikt, worden op grote schaal afgekeurd. Firefox en Safari blokkeren cookies van derden standaard vanaf respectievelijk 2019 en 2020. Chrome heeft plannen aangekondigd om ergens in 2023 een einde te maken aan de ondersteuning van cookies van derden. Als ze dat doen, zijn cookies van andere leveranciers onbruikbaar.

Bovendien staat Chrome momenteel alleen toe dat cookies functioneren in een context van derden als het kenmerk &quot;SameSite&quot; is ingesteld op Geen en als de cookies zijn gelabeld als veilig, wat betekent dat ze alleen kunnen worden gebruikt via HTTPS. Meer informatie is beschikbaar in de sectie &quot;[ wat het het koekjesattribuut SameSite is, en hoe beïnvloedt het Analytics?](#samesite-effect)&quot;

#### Welke Adobe-cookies van derden worden beïnvloed?

De dienst van identiteitskaart van de Bezoeker gebruikt &quot;[ demdex.net ](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)&quot;koekje om een blijvende herkenningsteken voor bezoekers over verschillende klantendomeinen te verstrekken. De dienst van identiteitskaart van de Analyse van de erfenis, &quot;s_vi&quot;koekje, wordt geplaatst als derdekoekje voor implementaties die geen de inzamelingsdomein van de douaneCNAME gebruiken.

In browsers waar cookies van derden worden geblokkeerd, is interdomeintracering niet beschikbaar.

### Beperkingen van cookies van eerste partij {#limitations-first-party-cookies}

Cookies van eerste bedrijven zijn toegestaan in alle grote browsers. Apple beperkt echter de levensduur van cookies van eerste partijen die door Adobe zijn ingesteld via het Intelligent Tracking Program (ITP). Dit is van invloed op Safari en op alle browsers op iOS en iPad OS.

Adobe-cookies van de eerste partij zijn beperkt tot een vervaldatum van 7 dagen of, voor doorklikbewerkingen die volgens Apple uit trackers komen, een vervaldatum van 24 uur. Als een gebruiker bij een vervaldatum van 7 dagen uw site bezoekt en binnen 7 dagen terugkeert, wordt de vervaldatum van de cookie met nog eens 7 dagen verlengd. Als een gebruiker echter uw site bezoekt en binnen acht dagen terugkeert, worden deze tijdens het tweede bezoek behandeld als een nieuwe gebruiker.

Momenteel, is het beleid ITP op alle eerste-partijkoekjes van Adobe van toepassing, of u de dienst van de identiteitskaart van de Bezoeker of de erfenisAnalytics ID (&quot;s_vi&quot;koekje) gebruikt. Op één punt, waren deze beleidsvormen van toepassing slechts op koekjes plaatste cliënt-kant en niet op koekjes plaatste server-kant via een implementatie CNAME. In november 2020, echter, werd ITP bijgewerkt om op implementaties CNAME eveneens van toepassing te zijn.

#### Tijdlijn van belangrijke wijzigingen in ITP-beleid {#ITP-timeline}

* Februari 2019 met [ ITP 2.1 ](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/): De cliënt-zijkoekjes waren beperkt tot een zeven-dag verval
* April 2019 met [ ITP 2.2 ](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/): De cliënt-zijkoekjes waren beperkt tot 24 uren voor en kliks wanneer het verwijzende domein a) betrokken bij het dwars-plaats volgen was en b) definitieve URL bevatte een vraagkoord en/of een fragmentherkenningsteken.
* November 2020 met [ de Campagne van de NAAM die en het Stuiteren die defensie ](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/) volgen: De beperkingen ITP werden uitgebreid tot implementaties CNAME.

Het beleid van ITP evolueert vaak. Voor het recentste beleid, zie Apple [ het Volgen Preventie in Webkit ](https://webkit.org/tracking-prevention).

#### Welke Adobe-cookies van de eerste fabrikant worden beïnvloed?

Alle cookies van de eerste partij die door Adobe zijn ingesteld, en de bijbehorende JavaScript-bibliotheken, worden beïnvloed door het ITP-beleid:

* [ &quot;AMCV&quot;koekjes ](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html) die door de de dienstbibliotheek van de Bezoeker van Adobe Experience Cloud (ECID) worden geplaatst
* De Analytics erfenis [ &quot;s_vi&quot;koekje ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html) wanneer het met de inzameling van de eerste-partijgegevens gebruikend CNAME wordt gevormd
* Het oude cookie [ &quot;s_fid&quot; van Analytics ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html). Dit is het fallback-cookie die wordt gebruikt wanneer &quot;s_vi&quot; niet kan worden ingesteld

#### Wat is de impact van ITP op Safari voor Analytics?

De impact van de ITP-beperkingen kan aanzienlijk variëren, afhankelijk van het gedrag van uw gebruikers. Alleen bezoekers die een browser gebruiken die invloed heeft op ITP (bijvoorbeeld Safari) en die terugkeren na een afwezigheid van zeven dagen, worden hierdoor beïnvloed. Als bezoekers niet binnen zeven dagen een ITP-browser gebruiken of terugkeren, hebben ze geen invloed. Het is belangrijk om uw eigen gegevens in Analytics te herzien om de omvang van de gevolgen van deze beperking te begrijpen. Voor uiteinden op hoe te om het effect aan uw plaatsen te meten, zie &quot;[ hoe ik kan bepalen als de veranderingen van Safari mijn zaken beïnvloeden?](#measure-itp-effect)&quot;

Als deze beperkingen wel van invloed zijn op uw gegevens, ziet u het volgende:

1. Een grotere bezoeker telt mee omdat terugkerende bezoekers worden behandeld als nieuwe bezoekers omdat hun cookies zijn verlopen. Elke metrische waarde op basis van de bezoeker (zoals Verkoop per bezoeker) wordt ook beïnvloed.
2. Wijzigingen in kenmerk. Attributie is afhankelijk van het koppelen van conversiegebeurtenissen aan voorafgaande activiteiten door dezelfde bezoeker. Nadat een cookie is verlopen, worden volgende gebeurtenissen aan een nieuwe bezoeker gekoppeld. De activiteiten van de nieuwe bezoeker kunnen niet worden gekoppeld aan de activiteiten van de vorige bezoeker.

>[!NOTE]
>
>ITP-technologieën zijn momenteel niet van toepassing op ingesloten browsers in mobiele apps.

## Wat is het verschil tussen cookies van derden en cookies van andere leveranciers?

### Cookies van andere bedrijven

Cookies van andere bedrijven worden niet gemaakt door de websites die gebruikers bezoeken.

Hoewel browsers momenteel alle cookies van derden op dezelfde manier behandelen en opslaan, kunnen cookies van andere bedrijven zich op verschillende manieren gedragen. Met de Analytische implementatie van het derdekoekje van een klant, bewaren browsers Adobe [ demdex.net ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) identiteitskaart als derdekoekje, maar de cliënt doet vraag slechts aan Adobe, en niet te onbekende of verdachte derdedomeinen. Deze cookie biedt permanente id&#39;s in verschillende domeinen en maakt beveiligde (HTTPS) inhoud mogelijk. Voor meer informatie, zie [ Cookies en de Dienst van de Identiteit van Experience Platform ](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html).

Binnen de analytische implementaties worden cookies van derden gebruikt voor interdomeintracering en voor het maken van gevallen waarin reclame wordt gebruikt, waaronder het opnieuw aanwijzen van advertenties. De koekjes van de derde staan u toe om bezoekers te identificeren aangezien zij verschillende domeinen bezoeken die u bezit of aangezien zij advertenties op plaatsen worden getoond die u niet bezit.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### Cookies van eerste bedrijven

Cookies van eerste bedrijven zijn domeinspecifiek en worden gemaakt door websites van klanten en opgeslagen in clientbrowsers terwijl gebruikers de websites bezoeken. Alle browsers keuren over het algemeen eerste-partijkoekjes goed, hoewel [ Safari de vervaldatum van sommige soorten eerderangs ](#limitations-first-party-cookies) beperkt.

Binnen de implementaties van Analytics, worden de eerstepartijkoekjes gebruikt om gebruikers te identificeren wanneer zij op uw plaats zijn en daarom al analyse van gebruikersactiviteit steunen. U hebt geen cookies van derden nodig om de activiteiten op de site te begrijpen.

Voor meer informatie, zie [ Ongeveer eerste-partijkoekjes ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html).

![ de vergelijking van het Koekje ](/help/technotes/assets/cookies2.png)

## Wat is het koekjesattribuut SameSite, en hoe beïnvloedt het de koekjes van Analytics? {#samesite-effect}

Met de release van Chrome 80 browser in februari 2020 — en opeenvolgende versies van Firefox- en Edge-browsers — dwingt het SameSite cookie-kenmerk de specificatie af voor drie verschillende waarden die bepalen of cookies in een context van derden kunnen worden gebruikt:

* `None`: met deze instelling is intersite toegang mogelijk en kunnen cookies worden doorgegeven in een context van derden. Als u dit kenmerk wilt opgeven, moet u ook `Secure` opgeven en moeten alle browseraanvragen HTTPS volgen. Wanneer u bijvoorbeeld de cookie instelt, koppelt u de waarden van het kenmerk als volgt: `Set-Cookie: example_session=test12; SameSite=None; Secure` . Als de cookies niet correct zijn gelabeld, kunnen ze niet meer worden gebruikt door de nieuwere browsers en worden ze afgewezen.

* `Lax`: Staat dwars-plaats verzoeken toe om met zelfde-plaats koekjes slechts voor top-level navigatie met *veilig* (read-only, zoals `GET`) methodes van HTTP worden verzonden.

* `Strict`: Dezelfde-site cookie wordt niet verzonden voor externe websiteaanvragen. Het cookie wordt alleen verzonden als de site voor het cookie overeenkomt met de site in de URL-balk.

Het standaardgedrag in deze browserversies is dat cookies zonder het opgegeven kenmerk `SameSite` gelijk worden behandeld als `SameSite=Lax` .

### Hoe beheert Analytics Cookie-kenmerken van SameSite?

Voor klanten die gebruikmaken van de Bezoeker-id-service, hebben cookies standaard de eigenschappen `SameSite=None` en `secure` ingesteld, zodat deze cookies door derden kunnen worden gebruikt.

Voor klanten die oude id&#39;s voor Analytics (`s_vi` en `s_fid` cookies) gebruiken, worden cookies ook ingesteld om gebruik door derden mogelijk te maken met standaardverzamelingsdomeinen: `adobedc.net`, `2o7.net` en `omtrdc.net` . Voor klanten die een CNAME-implementatie gebruiken, stelt Analytics `SameSite=Lax` in.

>[!NOTE]
>
>Als u meerdere domeinen hebt en dezelfde CNAME gebruikt voor gegevensverzameling in al uw domeinen, wordt het cookie op die andere domeinen behandeld als een cookie van een derde. Als u de verouderde analyses-id&#39;s gebruikt, kunt u de instelling bijwerken naar `SameSite=None` zodat deze cookies door uw sites kunnen worden gedeeld. Zie &quot;[ Verandering de waarde SameSite wanneer u één CNAME voor veelvoudige domeinen ](#samesite-one-cname)&quot;in de volgende sectie voor meer informatie gebruikt.

Voor browsers waarvan Google heeft aangegeven dat ze cookies verkeerd verwerken wanneer `SameSite` is ingesteld op `None` , blijft `SameSite` ongezet.

De volgende tabel geeft een overzicht van de SameSite-kenmerken voor Analytics-cookies:

![ lijst van het Koekje ](/help/technotes/assets/cookies1.png)

### Hoe kunnen mijn vereisten van het plaatsadres voor het attribuut SameSite?

#### Geef al uw sitepagina&#39;s met HTTPS

Controleer of in uw JavaScript-configuratie HTTPS wordt gebruikt voor alle aanroepen naar Adobe-services.

Als uw site de Experience Cloud Visitor ID-service gebruikt, stuurt de service HTTP-aanroepen van derden naar het HTTPS-eindpunt, wat de latentie kan verhogen, maar betekent dat u uw configuratie niet hoeft te wijzigen.

#### Wijzig de waarde van SameSite wanneer u één CNAME voor meerdere domeinen gebruikt {#samesite-one-cname}

>[!NOTE]
>
>De volgende informatie heeft alleen betrekking op sites die geen gebruik maken van de service Experience Cloud Visitor ID.

Als u een CNAME-implementatie hebt die in hetzelfde domein als uw website is ingesteld, wordt het cookie gemaakt in een context van de eerste partij en hoeft u geen wijzigingen aan te brengen.

Als u echter meerdere domeinen hebt en dezelfde CNAME gebruikt voor gegevensverzameling in al uw domeinen, wordt het cookie op die andere domeinen behandeld als een cookie van een derde. In Chrome 80 en hoger is de naam niet meer zichtbaar op deze andere domeinen. Om het gedrag in alle browsers meer op elkaar te laten lijken, heeft Analytics de `SameSite` -waarde van dit cookie expliciet ingesteld op `Lax` . Als u deze cookie in een vriendelijke externe context gebruikt, moet u de cookie instellen met de waarde `SameSite=None` . Dit betekent ook dat u altijd HTTPS moet gebruiken. Als u dit nog niet hebt gedaan, neemt u contact op met de klantenservice van Adobe om de SameSite-waarde te wijzigen voor uw beveiligde CNAME&#39;s.

## Hoe kan ik bepalen als de veranderingen Safari mijn zaken beïnvloeden? {#measure-itp-effect}

Adobe raadt klanten aan de impact binnen hun eigen bedrijf te meten voordat ze de gegevensverzameling wijzigen. U kunt Analysis Workspace gebruiken om het effect van de preventie van het volgen van ITP op uw individuele zaken te meten:

* Meet het percentage van uw verkeer van ITP-Beheerde browsers:

   1. Creeer een segment om te zien hoeveel bezoekers een platform ITP gebruiken.

      >[!NOTE]
      >
      >De specifieke browsers die door ITP worden beïnvloed hangen af van of u een implementatie CNAME gebruikte. Zie &quot;[ Chronologie van belangrijke veranderingen in beleid ITP ](#ITP-timeline)&quot;voor meer detail.

      ![ Segment voor bezoekers ITP ](/help/technotes/assets/itp-visitor-segment.png)

   2. Pas het segment op het aantal bezoeken toe om het relatieve gebruik van Safari in uw gebruikersbasis te begrijpen. Hiermee kunt u een tabel als deze maken:

      ![ Percentage bezoeken door bezoekers ITP ](/help/technotes/assets/visits-vs-safari-visits.png)

* Meet het percentage bezoekers dat niet-Safari browsers gebruikt die niet binnen zeven dagen terugkeren. Als uw niet-Safari bezoekers binnen zeven dagen herhaaldelijk terugkeren, kan het zijn dat uw Safari-verkeer hierdoor niet significant wordt beïnvloed.

   1. Creeer een segment als het volgende voor verkeer niet-Safari.

      ![ Segment voor bezoekers die na zeven dagen terugkeren ](/help/technotes/assets/visits-after-seven-days.png)

   2. Pas het segment op het aantal bezoeken toe om het relatieve gebruik van Safari in uw gebruikersbasis te begrijpen. Hiermee kunt u een tabel als deze maken:

      ![ Percentage bezoekers die na zeven dagen terugkeren ](/help/technotes/assets/percent-visits-after-seven-days.png)

### Manieren om uw gegevens tijdens het rapporteren aan te passen

Als uw zaken door ITP het volgen preventie wordt beïnvloed, zou u de volgende maatregelen kunnen overwegen om uw gegevens tijdens het melden aan te passen.

* Creeer een segment om gebruikers uit te filteren ITP.

  ![ Segment voor niet-ITP bezoekers ](/help/technotes/assets/non-itp-visitor-segment.png)

* Maak een berekende maatstaf om de bekende bezoekersinflatie aan te passen.

  ![ Berekende metrisch om voor bezoekersinflatie ](/help/technotes/assets/estimated-itp-visitors-metric.png) aan te passen

>[!MORELIKETHIS]
>
>[ Opties om het effect van browser koekjesbeperkingen te verlichten ](cookieless.md)
>>[De impact van Apple New App Tracking Transparency Framework op Adobe Analytics ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833)
