---
description: 'null'
title: Overzicht van Advertising Analytics
uuid: 00e461ff-3e17-4071-818b-93fd1e4b36f1
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Overzicht van Advertising Analytics

Met Advertising Analytics kunt u al uw gegevens van Google en Bing Paid Search naast elkaar weergeven, in Adobe Analytics. Eerder moesten alle gegevens van Google AdWords/DFA of Microsoft Bing Ads worden weergegeven in Adobe Advertising Cloud (AMO) of in Google/Bing. De volgende gegevens worden nu opgehaald in Adobe Analytics: Impressies, klikken, Kosten, Kwaliteitsscore en Gemiddelde positie rechtstreeks vanuit de zoekprogramma&#39;s en via een AMO ID-instantie (klik op Instanties).

> [!NOTE] Yahoo Gemini werd door Microsoft Bing geabsorbeerd op 31 maart 2019. Als gevolg hiervan is de optie Yahoo Gemini-advertentieaccount niet meer beschikbaar.

Door de gegevens van deze zoekprogramma&#39;s samen te brengen in Adobe Analytics, kunt u dezelfde gegevens analyseren met de mogelijkheden van de Analyse Workspace. Deze analyse wordt vergemakkelijkt door een nieuwe sjabloon voor [betaalde zoekprestaties](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) in Workspace.

![](assets/aa_aw.png)

Deze integratie is gericht op het volgende publiek:

* De **analist** die prestatierapporten moet verzamelen voor de Betaalde Zoekmarkering.
* De **Betaalde Zoekmarkt** die antwoorden op deze vragen zoekt: Hoeveel verkeer verzend ik naar onze plaats en klanten converteren? Wat zijn mijn kosteneffectieve advertentiecampagnes?

## Vereisten {#section_C25E0CA3474C4EDEAEAA9A5B8AAC9299}

* Advertising Analytics is alleen beschikbaar voor Adobe Analytics [Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html)en [Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html) SKU&#39;s.

* Deze functionaliteit is beschikbaar voor klanten die geen advertenties maken met de cloud of met een andere indeling dan AMO.
* U moet een Adobe Analytics-beheerder zijn om toegang te hebben tot Advertising Analytics. Vervolgens kunt u toegangsmachtigingen [](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) verlenen aan niet-beheerders.
* Elke analytische rapportsuite waarin u de zoekgegevens van Google/Bing wilt bekijken, moet worden [toegewezen aan uw Experience Cloud-organisatie](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html).
* Voor elke rapportsuite waarin u de zoekgegevens van Google/Bing wilt weergeven, moet u deze rapportsuite(s) [inschakelen voor Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) ( **[!UICONTROL Admin]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**).

* U hebt aanmeldingsgegevens nodig voor een gebruiker met bewerkingsmachtigingen voor de zoekaccount(s) die u wilt integreren met Adobe Analytics, zoals een Google-account-id en wachtwoord.
* In het geval van Bing Ads, hebt u ook de identiteitskaart van de Klant van de Bing nodig.
* Als u Internet Explorer 11 (of eerder) gebruikt, kunt u voor geen van de drie zoekprogramma&#39;s een [advertentieaccount](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md) instellen. Gebruik in plaats hiervan andere webbrowsers.

## Machtigingen voor Advertising Analytics {#section_FCC58EB635954A32990D4E67B52B4369}

Analytics heeft twee machtigingen die automatisch worden toegekend aan Analytics Admins. Beheerders kunnen deze machtigingen vervolgens aan niet-beheerders verlenen.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Machtiging </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Toestemming verlenen in Adobe Analytics </th> 
   <th colname="col4" class="entry"> Toestemming verlenen als u bent aangemeld bij Adobe Experience Cloud </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics Management </p> </td> 
   <td colname="col2"> <p>Hiermee kunnen gebruikers zoekaccounts voor advertenties instellen, bewerken/weergeven. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> User Management</span> &gt; <span class="uicontrol"> groups</span> &gt; <span class="uicontrol"> Edit All Report Access</span> &gt; <span class="uicontrol"> Customize Analytics Tools</span> &gt; <span class="uicontrol"> Advertising Analytics Management</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Meld u aan bij beheerconsole.adobe.com</span> &gt; <span class="uicontrol"> Producten</span> &gt; <span class="uicontrol"> Productprofiel</span> &gt; tabblad <span class="uicontrol"> Machtigingen &gt;</span> Analysehulpmiddelen <span class="uicontrol"> &gt; Analysebeheer voor</span> <span class="uicontrol"> advertenties</span></span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Configuratie Advertising Analytics </p> </td> 
   <td colname="col2"> <p>Hiermee kunnen gebruikers rapportsuites configureren die moeten worden ingericht voor Advertising Analytics. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> User Management</span> &gt; <span class="uicontrol"> groups</span> &gt; <span class="uicontrol"> Edit All Report Access</span> &gt; <span class="uicontrol"> Customize Report Suite Tools</span> &gt; <span class="uicontrol"> Advertising Analytics Configuration</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Meld u aan bij beheerconsole.adobe.com</span> &gt; <span class="uicontrol"> Producten</span> &gt; <span class="uicontrol"> Productprofiel</span> &gt; tabblad <span class="uicontrol"> Machtigingen &gt;</span> Rapportsuite-gereedschappen <span class="uicontrol"> &gt; Configuratie van</span> <span class="uicontrol"> Advertising Analytics</span></span> </td> 
  </tr> 
 </tbody> 
</table>

## Afmetingen en metingen van advertentieanalyse {#section_C0DF4A08EA9E46ADABE9E465AFC11E32}

Advertising Analytics voegt de volgende dimensies en metriek toe aan de Analyse Workspace, Reports &amp; Analytics, Report Builder en de Analytics Reporting API.

**Afmetingen**

>[!IMPORTANT]
>
>Deze integratie leidt tot een nieuwe reeks dimensies door classificaties van de variabele van identiteitskaart van AMO. Deze nieuwe afmetingen hebben geen invloed op of wijzigen de bestaande marketingkanalen of de variabeleafmetingen voor het bijhouden van campagnes. De AMO-id is gekoppeld aan het profiel van een bezoeker wanneer een bezoeker de site aanlandt via een betaalde zoekadvertentie. Als zodanig kunnen de afmetingen van de AMO worden gebruikt om zowel de maatstaven van de AMO die door deze integratie worden verschaft, als alle gegevens die door de bezoeker stroomafwaarts worden vastgelegd (bezoeken, bezoekers, paginaweergaven, stuiterende frequentie, bestellingen, inkomsten, aangepaste gebeurtenissen, enz.), op te splitsen. Ze kunnen ook naar andere dimensies worden uitgesplitst wanneer ze worden gerapporteerd over andere onsite metriek.
>
>De classificaties voor deze metriek worden dagelijks bijgewerkt. Als u daarom wijzigingen aanbrengt in de metagegevens in een zoekprogramma, ziet u deze wijzigingen mogelijk pas tot de volgende dag wanneer de classificaties worden bijgewerkt.

| Naam van classificatie (afmeting) | Definitie |
|--- |--- |
| Trefwoord MatchType (AMO-id) | Het trefwoordmatrixtype. De waarden zijn doorgaans breed, woordelijk, exact of geen waarde als het type Advertentie geen overeenkomend type heeft. |
| Advertentieplatform (AMO-id) | De naam van het zoekprogramma. Waarden kunnen bestaan uit Google AdWords of Microsoft Bing Ads. |
| Account (AMO-id) | De naam van het zoekprogrammaaccount dat wordt bijgehouden. |
| Campagne (AMO-id) | De naam van de campagne in uw account voor zoekprogramma&#39;s. |
| Advertentiegroep (AMO-id) | De naam van de advertentiegroep in uw zoekprogramma&#39;s. |
| Advertentie (AMO-ID) | De beschrijving voor Advertentie en Advertentie die op je advertentie wordt gebruikt. |
| Trefwoord (AMO-id) | De trefwoordwaarde van uw zoekprogrammaaccount |
| Type overeenkomst (AMO-id) | Het type van Gelijke van het Sleutelwoord dat aan uw sleutelwoord wordt toegewezen. De waarden zijn doorgaans breed, woordelijk, exact of geen waarde als het type Advertentie geen overeenkomend type heeft. |
| Advertentietype (AMO-id) | Het type advertentie dat wordt aangeboden. Dit is doorgaans &#39;&#39;Text Ad&#39;&#39;. |
| Advertentitel (AMO-ID) | Het object Title dat in de advertentie wordt gebruikt. |
| Advertentiebeschrijving (AMO-id) | Het object Advertentiebeschrijving dat in de advertentie wordt gebruikt. |
| URL voor advertentieweergave (AMO-id) | Het object URL van advertentieweergave toevoegen dat in de advertentie wordt gebruikt. |
| Doel-URL (AMO-id) toevoegen | De bestemmingspagina-URL of Definitieve URL die aan uw Advertentie wordt toegewezen. |
| Netwerk (AMO-id) | Het netwerk de Advertentie wordt gediend aan. Voor Advertising Analytics is deze waarde altijd &quot;Search&quot; (Zoeken). |
| Plaatsing (AMO-id) | De beheerde plaatsingswebsite (voor inhoudsnetwerken). Deze dimensie wordt alleen gebruikt door beheerde plaatsen. |
| Productdoel (AMO-id) | De naam van het productdoel dat op PLA-advertenties wordt gebruikt (niet het werkelijk gekochte product). |
| Optimalisatie (AMO-id) | Dit wordt niet gebruikt door Advertising Analytics. Het wordt alleen gebruikt door klanten van de Advertising Cloud. |
| Apparaat (AMO-id) | Niet gebruikt vandaag. Plaatsaanduiding voor mogelijke toekomstige productverbetering tot het aangegeven doelapparaattype (bv. mobiel, bureaublad) van advertentie (niet het werkelijke apparaat van de bezoeker). |

**Metrisch**

>[!IMPORTANT]
>
>De meetgegevens die worden verstrekt door Advertising Analytics (zie hieronder) zijn gegevens op overzichtsniveau van de zoekmachines. Ze zijn niet verbonden met de analytische bezoekersprofielen. Ze zijn alleen verbonden met de variabele van de AMO ID en de bijbehorende classificatiedimensies. Als zodanig mogen zij niet worden gerapporteerd door andere dimensies/segmenten dan die welke op de afmetingen van de AMO-id zijn gebaseerd. Als u dit doet, worden er nullen voor de gegevens weergegeven in Analytics. U kunt ze in berekende metriek opnemen met andere metriek, maar deze berekende metrische waarde moet ook alleen worden uitgesplitst op basis van de afmetingen van de AMO-id.
>
>Deze gegevens zijn dagelijks afkomstig van gegevens, zodat zij geen gegevens voor de huidige dag hebben. Zij dienen ook niet te worden gerapporteerd met een korreligheid lager dan dagelijks.
>
>Er is een metrische waarde voor instanties van een AMO-id die wordt ingesteld wanneer de AMO-id op een bestemmingspagina is ingesteld (dus een doorklikpad). Deze metrische waarde wordt in real-time vastgelegd bij een treffer voor de bestemmingspagina en is beschikbaar voor uitsplitsingen met andere afmetingen die ook op de landingspagina zijn ingesteld.

| Metrische naam | Definitie |
|--- |--- |
| AMO-indrukkingen | Het aantal en het aantal indrukken dat door het zoekprogramma wordt gemeld. |
| AMO-klikken | Het aantal klikken op advertenties dat door het zoekprogramma wordt gemeld. |
| AMO-kosten | De kosten die voor elk trefwoord/advertentie zijn betaald, zoals opgegeven door het zoekprogramma. |
| Gem. Pos | Een berekende maateenheid die de gemiddelde positie van de advertenties weerspiegelt zoals die door de zoekmachine wordt gemeld. |
| Gem. Kwaliteitsscore | Een berekende maatstaf die de gemiddelde kwaliteitsscore weerspiegelt zoals die door de zoekmachine wordt gerapporteerd. |
