---
description: Ontdek alles wat u met Advertising Analytics kunt doen, inclusief de vereiste machtigingen en de beschikbare afmetingen en metriek.
title: Advertising Analytics
feature: Advertising Analytics
exl-id: bc18b74a-0317-4871-b2e0-ec0977ef1731
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 78%

---

# Advertising Analytics

Met Advertising Analytics kun je al je door Google Ads en Microsoft Advertising betaalde zoekgegevens naast elkaar bekijken in Adobe Analytics. Eerder moesten alle Google Ads- of Microsoft Advertising-gegevens worden weergegeven in Adobe Advertising Cloud (AMO) of in elke respectievelijke advertentiemethode. U kunt nu direct via zoekmachines en via AMO ID-instanties (klik op Instanties) de indruk krijgen, klikken en kostengegevens maken.

Door de data van deze zoekprogramma&#39;s samen te brengen in Adobe Analytics, kunt u dezelfde data analyseren met de kracht van Analysis Workspace. Deze analyse wordt mogelijk gemaakt door een nieuwe sjabloon voor [paid search-prestaties](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) in Workspace.

![](assets/aa_aw.png)

Deze integratie is gericht op de volgende doelgroepen:

* De **analist** die prestatierapporten moet verzamelen voor de paid search-marketeer.
* De **paid search-marketeer** die antwoorden op deze vragen wil: Hoeveel verkeer verzend ik naar onze site, en zijn klanten aan het converteren? Welke van mijn advertentiecampagnes zijn rendabel?


## Vereisten {#prerequisites}

* Advertising Analytics is alleen beschikbaar voor Adobe Analytics [Select](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html) en [Ultimate](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html) SKU&#39;s.
* Deze functionaliteit is beschikbaar voor klanten die geen advertenties maken in de cloud of in een andere indeling dan AMO.
* U moet een Beheerder van Adobe Analytics zijn om toegang tot Advertising Analytics te hebben of tot een productprofiel behoren dat [&#x200B; toegang &#x200B;](/help/integrate/c-advertising-analytics/overview.md#permissions) aan Advertising Analytics is verleend.
* Voor om het even welke rapportreeks waar u de onderzoeksgegevens van Google Ads of van Microsoft Advertising wilt bekijken, moet u [&#x200B; die rapportreeks/s voor Advertising Analytics &#x200B;](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) ( **[!UICONTROL Admin]** toelaten > **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**).
* U hebt aanmeldingsgegevens nodig voor een gebruiker met bewerkingsmachtiging voor de zoekaccount(s) die u wilt integreren met Adobe Analytics, zoals een account-id en wachtwoord-id van Google.
* In het geval van Microsoft Advertising hebt u ook de instructies [[!UICONTROL Account ID] en [!UICONTROL Manager Account ID]](c-adanalytics-workflow/aa-locate-account-id.md) nodig.

## Advertising Analytics-machtigingen {#permissions}

Analytics heeft twee machtigingen die automatisch worden toegekend aan Analytics-beheerders. Beheerders kunnen deze machtigingen vervolgens aan niet-beheerders verlenen.

| Machtiging | Definitie | Machtiging verlenen als u bent aangemeld bij Adobe Experience Cloud |
| --- | --- | --- |
| Advertising Analytics-beheer | Hiermee kunnen gebruikers zoekaccounts voor advertenties instellen/bewerken/weergeven. | Meld u aan bij [&#x200B; adminconsole.adobe.com &#x200B;](https://adminconsole.adobe.com) > [!UICONTROL Products] > [!UICONTROL Adobe Analytics] > [!UICONTROL Product Profile] > [!UICONTROL Permissions] tab > [!UICONTROL Analytics Tools] > [!UICONTROL Advertising Analytics Management] |
| Advertising Analytics-configuratie | Hiermee kunnen gebruikers rapportsuites configureren die moeten worden ingericht voor Advertising Analytics. | Meld u aan bij [&#x200B; adminconsole.adobe.com &#x200B;](https://adminconsole.adobe.com) > [!UICONTROL Products] > [!UICONTROL Adobe Analytics] > [!UICONTROL Product Profile] > [!UICONTROL Permissions] tab > [!UICONTROL Analytics Tools] > [!UICONTROL Advertising Analytics Configuration] |

## Advertising Analytics-afmetingen en -cijfers {#dimensions-metrics}

Advertising Analytics voegt de volgende afmetingen en metriek toe aan Analysis Workspace, Report Builder en de Analytics Reporting API.

### Dimensies

>[!IMPORTANT]
>
>Deze integratie creëert een nieuwe reeks dimensies door classificaties van de AMO-id-variabele. Deze nieuwe dimensies beïnvloeden of wijzigen de bestaande marketingkanalen of de dimensies van variabelen voor campagnetracking niet. De AMO-id is verbonden met het profiel van een bezoeker wanneer een bezoeker op de site terechtkomt via een paid search-advertentie. De AMO-dimensies kunnen dan ook worden gebruikt om zowel de AMO-cijfers die door deze integratie worden verstrekt, als alle data die door de bezoeker downstream worden vastgelegd (bezoeken, bezoekers, paginaweergaven, bouncepercentage, orders, omzet, aangepaste gebeurtenissen, enz.), uit te splitsen. Ze kunnen ook worden uitgesplitst in andere dimensies bij rapportage over andere onsite-cijfers.
>
>De classificaties voor deze cijfers worden dagelijks bijgewerkt. Als u dus wijzigingen aanbrengt in de metadata in een zoekmachine, ziet u deze wijzigingen misschien pas tot de volgende dag, wanneer de classificaties zijn bijgewerkt.

| Naam van de classificatie (afmetingen) | Definitie |
| --- | --- |
| **[!UICONTROL Keyword MatchType (AMO ID)]** | Het trefwoordmatchtype. Als het type advertentie geen matchtype heeft, zijn de waarden doorgaans breed, per zinsdeel, exact of geen waarde. |
| **[!UICONTROL Ad Platform (AMO ID)]** | De naam van de zoekmachine. Waarden kunnen &#39;Google AdWords&#39; of &#39;Microsoft Bing Ads&#39; zijn. |
| **[!UICONTROL Account (AMO ID)]** | De naam van het zoekmachineaccount dat wordt bijgehouden. |
| **[!UICONTROL Campaign (AMO ID)]** | De naam van de campagne in uw zoekmachineaccount. |
| **[!UICONTROL Ad Group (AMO ID)]** | De naam van de advertentiegroep in uw zoekmachinecampagnes. |
| **[!UICONTROL Ad (AMO ID)]** | De titel + beschrijving die bij uw advertentie worden gebruikt. |
| **[!UICONTROL Keyword (AMO ID)]** | De trefwoordwaarde van uw zoekprogrammaaccount. |
| **[!UICONTROL Match Type (AMO ID)]** | Het trefwoordmatchtype dat aan uw trefwoord is toegewezen. Als het type advertentie geen matchtype heeft, zijn de waarden doorgaans breed, per zinsdeel, exact of geen waarde. |
| **[!UICONTROL Ad Type (AMO ID)]** | Het type advertentie dat wordt aangeboden, meestal &quot;Tekstadvertentie&quot;. |
| **[!UICONTROL Ad Title (AMO ID)]** | Het titelobject dat in uw advertentie wordt gebruikt. |
| **[!UICONTROL Ad Description (AMO ID)]** | Het object voor titelbeschrijving dat in uw advertentie wordt gebruikt. |
| **[!UICONTROL Ad Display URL (AMO ID)]** | Het URL-object voor advertentieweergave dat in uw advertentie wordt gebruikt. |
| **[!UICONTROL Ad Destination URL (AMO ID)]** | URL van de landingspagina of de definitieve URL die aan uw advertentie is toegewezen. |
| **[!UICONTROL Network (AMO ID)]** | Het netwerk waarop de advertentie wordt aangeboden. Voor Advertising Analytics is deze waarde altijd &quot;Search&quot; (Zoeken). |
| **[!UICONTROL Placement (AMO ID)]** | De beheerde plaatsingswebsite (voor contentnetwerken). Deze dimensie wordt alleen gebruikt door beheerde plaatsingen. |
| **[!UICONTROL Product Target (AMO ID)]** | De naam van het productdoel dat op PLA-advertenties wordt gebruikt (niet het daadwerkelijk gekochte product). |
| **[!UICONTROL Optimization (AMO ID)]** | Dit wordt niet gebruikt door Advertising Analytics. Het wordt alleen gebruikt door Advertising Cloud-klanten. |
| **[!UICONTROL Device (AMO ID)]** | Momenteel niet in gebruik. Plaatsaanduiding voor mogelijke toekomstige productverbetering naar aangewezen doelapparaattype (bv. mobiel, desktop) van de advertentie (niet het werkelijke apparaat van de bezoeker). |

### Metrics

>[!IMPORTANT]
>
>De cijfers die worden verstrekt door Advertising Analytics (zie hieronder) zijn data op overzichtsniveau van de zoekmachines. Ze zijn niet verbonden met de Analytics-bezoekersprofielen. Ze zijn alleen verbonden met de AMO-id-variabele en de bijbehorende classificatiedimensies. Ze mogen dus niet worden gerapporteerd door andere dimensies/segmenten dan degene die zijn gebaseerd op de AMO-id-dimensies. Als u dit wel doet, worden in Analytics nullen voor de data weergegeven. U kunt deze in de berekende standaard opnemen met andere cijfers, maar deze berekende standaard mag ook alleen worden uitgesplitst op basis van de dimensies van de AMO-id.
>
>Deze cijfers zijn gebaseerd op dagelijkse data, dus er zijn geen data voor huidige dag. Ook deze moeten niet met een lagere granulariteit dan dagelijks worden gerapporteerd.
>
>Er is een cijfer voor AMO-id-instanties dat wordt ingesteld wanneer de AMO-id is ingesteld op een landingspagina (dus een doorklikpad). Dit cijfer wordt in real time vastgelegd bij een hit voor de landingspagina en is beschikbaar voor uitsplitsingen met andere dimensies die ook zijn ingesteld voor de landingspagina.

| Metrische naam | Definitie |
| --- | --- |
| **[!UICONTROL AMO Impressions]** | Het aantal advertentie-impressies dat door het zoekprogramma wordt gerapporteerd. |
| **[!UICONTROL AMO Clicks]** | Het aantal klikken op advertenties dat door het zoekprogramma wordt gerapporteerd. |
| **[!UICONTROL AMO Cost]** | De betaalde kosten voor elk trefwoord/advertentie zoals gemeld door de zoekmachine. |
