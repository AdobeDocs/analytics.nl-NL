---
description: Ontdek alles wat u met Advertising Analytics kunt doen, inclusief de vereiste machtigingen en de beschikbare afmetingen en metriek.
title: Advertising Analytics
feature: Advertising Analytics
exl-id: bc18b74a-0317-4871-b2e0-ec0977ef1731
source-git-commit: cf0f528f1ccb0346786c017b4d0d48dd5ab6dfc2
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 90%

---

# Advertising Analytics

Met Advertising Analytics kunt u alle data van Google en Bing paid search naast elkaar weergeven in Adobe Analytics. Vroeger moesten alle data van Google AdWords/DFA of Microsoft Bing Ads worden weergegeven in Adobe Advertising Cloud (AMO) of in Google/Bing. U kunt nu de volgende gegevens ophalen in Adobe Analytics: Impressies, klikken, Kostengegevens rechtstreeks vanuit de zoekmachines en een AMO ID-instantie (klik op Instanties).

Door de data van deze zoekprogramma&#39;s samen te brengen in Adobe Analytics, kunt u dezelfde data analyseren met de kracht van Analysis Workspace. Deze analyse wordt mogelijk gemaakt door een nieuwe sjabloon voor [paid search-prestaties](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) in Workspace.

![](assets/aa_aw.png)

Deze integratie is gericht op de volgende doelgroepen:

* De **analist** die prestatierapporten moet verzamelen voor de paid search-marketeer.
* De **paid search-marketeer** die antwoorden op deze vragen wil: Hoeveel verkeer verzend ik naar onze site, en zijn klanten aan het converteren? Welke van mijn advertentiecampagnes zijn rendabel?


## Vereisten {#prerequisites}

* Advertising Analytics is alleen beschikbaar voor Adobe Analytics [Select](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html) en [Ultimate](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html) SKU&#39;s.
* Deze functionaliteit is beschikbaar voor klanten die geen advertenties maken in de cloud of in een andere indeling dan AMO.
* U moet een Adobe Analytics-beheerder zijn om toegang te hebben tot Advertising Analytics. Vervolgens kunt u [toegang verlenen](/help/integrate/c-advertising-analytics/overview.md#permissions) aan niet-beheerders.
* Voor elke rapportsuite waarin u de zoekdata van Google/Bing wilt weergeven, moet u [deze rapportsuite(s) inschakelen voor Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) (**[!UICONTROL Admin]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**).
* U hebt aanmeldingsgegevens nodig voor een gebruiker met bewerkingsmachtiging voor de zoekaccount(s) die u wilt integreren met Adobe Analytics, zoals een account-id en wachtwoord-id van Google.
* In het geval van Bing Ads hebt u ook de Bing-klant-id nodig.

## Advertising Analytics-machtigingen {#permissions}

Analytics heeft twee machtigingen die automatisch worden verleend aan Analytics-beheerders. Beheerders kunnen deze machtigingen vervolgens aan niet-beheerders verlenen.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Machtiging </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Machtiging verlenen in Adobe Analytics </th> 
   <th colname="col4" class="entry"> Machtiging verlenen als u bent aangemeld bij Adobe Experience Cloud </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-beheer </p> </td> 
   <td colname="col2"> <p>Hiermee kunnen gebruikers zoekaccounts voor advertenties instellen/bewerken/weergeven. </p> </td> 
   <td colname="col3"><span class="ignoretag"> <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> All admin </span> &gt; <span class="uicontrol"> Gebruikersbeheer </span> &gt; <span class="uicontrol"> Groepen </span> &gt; <span class="uicontrol"> Edit All Report Access </span> &gt; <span class="uicontrol"> Customize Analytics Tools </span> &gt; <span class="uicontrol"> Advertising Analytics Management </span> </span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Aanmelden bij adminconsole.adobe.com</span> &gt; <span class="uicontrol"> Producten</span> &gt; <span class="uicontrol"> Productprofiel</span> &gt; <span class="uicontrol"> Tabblad Toestemmingen</span> &gt; <span class="uicontrol"> Analytics-tools</span> &gt; <span class="uicontrol"> Advertising Analytics-beheer</span></span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-configuratie </p> </td> 
   <td colname="col2"> <p>Hiermee kunnen gebruikers rapportsuites configureren die moeten worden ingericht voor Advertising Analytics. </p> </td> 
   <td colname="col3"><span class="ignoretag"> <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> All admin </span> &gt; <span class="uicontrol"> Gebruikersbeheer </span> &gt; <span class="uicontrol"> Groepen </span> &gt; <span class="uicontrol"> Edit All Report Access </span> &gt; <span class="uicontrol"> Customize Report Suite Tools </span> &gt; <span class="uicontrol"> Advertising Analytics Configuration </span> </span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Aanmelden bij adminconsole.adobe.com</span> &gt; <span class="uicontrol"> Producten</span> &gt; <span class="uicontrol"> Productprofiel</span> &gt; <span class="uicontrol"> Tabblad Toestemmingen</span> &gt; <span class="uicontrol"> Rapportsuite-tools</span> &gt; <span class="uicontrol"> Advertising Analytics-configuratie</span></span> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics Dimensions en Metrics {#dimensions-metrics}

Advertising Analytics voegt de volgende afmetingen en metriek toe aan Analysis Workspace, Report Builder en de Analytics Reporting API.

### Dimensies

>[!IMPORTANT]
>
>Deze integratie creëert een nieuwe reeks dimensies door classificaties van de AMO-id-variabele. Deze nieuwe dimensies beïnvloeden of wijzigen de bestaande marketingkanalen of de dimensies van variabelen voor campagnetracking niet. De AMO-id is verbonden met het profiel van een bezoeker wanneer een bezoeker op de site terechtkomt via een paid search-advertentie. De AMO-dimensies kunnen dan ook worden gebruikt om zowel de AMO-cijfers die door deze integratie worden verstrekt, als alle data die door de bezoeker downstream worden vastgelegd (bezoeken, bezoekers, paginaweergaven, bouncepercentage, orders, omzet, aangepaste gebeurtenissen, enz.), uit te splitsen. Ze kunnen ook worden uitgesplitst in andere dimensies bij rapportage over andere onsite-cijfers.
>
>De classificaties voor deze cijfers worden dagelijks bijgewerkt. Als u dus wijzigingen aanbrengt in de metadata in een zoekmachine, ziet u deze wijzigingen misschien pas tot de volgende dag, wanneer de classificaties zijn bijgewerkt.

| Naam van classificatie (dimensie) | Definitie |
|--- |--- |
| Trefwoord MatchType (AMO-id) | Het trefwoordmatchtype. Als het type advertentie geen matchtype heeft, zijn de waarden doorgaans breed, per zinsdeel, exact of geen waarde. |
| Advertentieplatform (AMO-id) | De naam van de zoekmachine. Waarden kunnen Google AdWords of Microsoft Bing Ads zijn. |
| Account (AMO-id) | De naam van het zoekmachineaccount dat wordt bijgehouden. |
| Campagne (AMO-id) | De naam van de campagne in uw zoekmachineaccount. |
| Advertentiegroep (AMO-id) | De naam van de advertentiegroep in uw zoekmachinecampagnes. |
| Advertentie (AMO-id) | De titel + beschrijving die bij uw advertentie worden gebruikt. |
| Trefwoord (AMO-id) | De trefwoordwaarde van uw zoekmachineaccount. |
| Matchtype (AMO-id) | Het trefwoordmatchtype dat aan uw trefwoord is toegewezen. Als het type advertentie geen matchtype heeft, zijn de waarden doorgaans breed, per zinsdeel, exact of geen waarde. |
| Advertentietype (AMO-id) | Het type advertentie dat wordt aangeboden, meestal &quot;Tekstadvertentie&quot;. |
| Advertentietitel (AMO-id) | Het titelobject dat in uw advertentie wordt gebruikt. |
| Advertentiebeschrijving (AMO-id) | Het object voor titelbeschrijving dat in uw advertentie wordt gebruikt. |
| URL voor advertentieweergave (AMO-id) | Het URL-object voor advertentieweergave dat in uw advertentie wordt gebruikt. |
| Doel-URL van de advertentie (AMO-id) | URL van de landingspagina of de definitieve URL die aan uw advertentie is toegewezen. |
| Netwerk (AMO-id) | Het netwerk waarop de advertentie wordt aangeboden. Voor Advertising Analytics is deze waarde altijd &quot;Search&quot; (Zoeken). |
| Plaatsing (AMO-id) | De beheerde plaatsingswebsite (voor contentnetwerken). Deze dimensie wordt alleen gebruikt door beheerde plaatsingen. |
| Productdoel (AMO-id) | De naam van het productdoel dat op PLA-advertenties wordt gebruikt (niet het daadwerkelijk gekochte product). |
| Optimalisatie (AMO-id) | Dit wordt niet gebruikt door Advertising Analytics. Het wordt alleen gebruikt door Advertising Cloud-klanten. |
| Apparaat (AMO-id) | Momenteel niet in gebruik. Plaatsaanduiding voor mogelijke toekomstige productverbetering naar aangewezen doelapparaattype (bv. mobiel, desktop) van de advertentie (niet het werkelijke apparaat van de bezoeker). |

### Metrics

>[!IMPORTANT]
>
>De cijfers die worden verstrekt door Advertising Analytics (zie hieronder) zijn data op overzichtsniveau van de zoekmachines. Ze zijn niet verbonden met de Analytics-bezoekersprofielen. Ze zijn alleen verbonden met de AMO-id-variabele en de bijbehorende classificatiedimensies. Ze mogen dus niet worden gerapporteerd door andere dimensies/segmenten dan degene die zijn gebaseerd op de AMO-id-dimensies. Als u dit wel doet, worden in Analytics nullen voor de data weergegeven. U kunt deze in de berekende standaard opnemen met andere cijfers, maar deze berekende standaard mag ook alleen worden uitgesplitst op basis van de dimensies van de AMO-id.
>
>Deze cijfers zijn gebaseerd op dagelijkse data, dus er zijn geen data voor huidige dag. Ook deze moeten niet met een lagere granulariteit dan dagelijks worden gerapporteerd.
>
>Er is een cijfer voor AMO-id-instanties dat wordt ingesteld wanneer de AMO-id is ingesteld op een landingspagina (dus een doorklikpad). Dit cijfer wordt in real time vastgelegd bij een hit voor de landingspagina en is beschikbaar voor uitsplitsingen met andere dimensies die ook zijn ingesteld voor de landingspagina.

| Naam cijfer | Definitie |
|--- |--- |
| AMO-impressies | Het aantal advertentie-impressies dat door het zoekprogramma wordt gerapporteerd. |
| AMO-klikken | Het aantal klikken op advertenties dat door het zoekprogramma wordt gerapporteerd. |
| AMO-kosten | De betaalde kosten voor elk trefwoord/advertentie zoals gemeld door de zoekmachine. |
