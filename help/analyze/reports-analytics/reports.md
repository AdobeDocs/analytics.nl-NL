---
title: Rapporten
description: De afmetingen en metriek die Rapporten & Analytics voor elk rapport gebruiken.
feature: Grondbeginselen van rapporten en analyses
role: User, Admin
exl-id: e3c23d17-fc4b-479e-9c48-6f27ef0de4e3
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '1866'
ht-degree: 0%

---

# Rapporten

Elk rapport in Rapporten &amp; Analytics gebruikt een specifieke afmeting en metrisch gebrek. U kunt metrisch in elk rapport veranderen en onderverdelingen toevoegen indien gewenst. De volgende lijsten verstrekken welke dimensie in elk rapport wordt gebruikt.

>[!NOTE]
>
>Het menu Rapporten kan er anders uitzien, afhankelijk van aanpassingen die een beheerder in uw organisatie heeft aangebracht. Zie [Menu&#39;s aanpassen](/help/admin/admin/customize-menus.md) in de gebruikershandleiding Admin.

## Sitecijfers

Bevat rapporten die typisch het gebruiken van een datumwaaier trenderen. Bevat ook unieke rapporten, zoals Aanbevolen rapporten en Real-time rapporten.

* Mijn aanbevolen rapporten: Hiermee maakt u een dashboard dat meerdere rapporten bevat voor directe inzichten.
* Belangrijkste cijfers: Een rapport dat u toestaat om tot vijf metriek tegelijkertijd te trenderen. Trends [Paginaweergaven](/help/components/metrics/page-views.md), [Visits](/help/components/metrics/visits.md) en [Unieke bezoekers](/help/components/metrics/unique-visitors.md) standaard.
* Paginaweergaven: Trends [Paginaweergaven](/help/components/metrics/page-views.md) metrisch in de loop van de tijd.
* Bezoeken: Trends [Visits](/help/components/metrics/visits.md) metrisch in tijd.
* Bezoekers: Trends diverse [Unieke bezoekers](/help/components/metrics/unique-visitors.md) metriek in tijd.
   * Unieke bezoekers: Telt bezoekers slechts eenmaal voor het volledige geselecteerde datumbereik.
   * Uur unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende uren van het geselecteerde datumbereik.
   * Dagelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende dagen van het geselecteerde datumbereik.
   * Wekelijks unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende weken van het geselecteerde datumbereik.
   * Maandelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende maanden van het geselecteerde datumbereik.
   * Unieke bezoekers op kwartaalbasis: Hiermee telt u bezoekers meerdere keren als ze in verschillende kwartalen van het geselecteerde datumbereik een bezoek brengen. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke jaarlijkse bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende kalenderjaren van het geselecteerde datumbereik.
* Tijd besteed per bezoek: Gebruikt de [Tijd besteed per bezoek - buckette](/help/components/dimensions/time-spent-per-visit.md) dimensie.
* Tijd vóór de gebeurtenis: Gebruikt de [Tijd voorafgaand aan gebeurtenis](/help/components/dimensions/time-prior-to-event.md) dimensie.
* Aankopen: Bevat rapporten over op aankoop-gebaseerde metriek.
   * Conversietrechter aanschaffen: Verslag over [Bezoekingen](/help/components/metrics/visits.md), [Tekstpakketten](/help/components/metrics/carts.md), [Bestellingen](/help/components/metrics/orders.md), [Opbrengst](/help/components/metrics/revenue.md) en [Eenheden](/help/components/metrics/units.md) in een kernenrapport. Een gelijkaardige visualisatie wordt bereikt in Analysis Workspace gebruikend [Fallout visualization](../analysis-workspace/visualizations/fallout/fallout-flow.md).
   * Ontvangsten: Trends de metrische [Inkomsten](/help/components/metrics/revenue.md) in tijd.
   * Bestellingen: Trends metrisch [Orders](/help/components/metrics/orders.md) in tijd.
   * Eenheden: Trends de metrische [Eenheden](/help/components/metrics/units.md) in tijd.
* Winkelwagentje: Bevat rapporten over winkelwagenmaateenheden.
   * Kanaal voor kleuromzetting: Rapporteert [Instanties](/help/components/metrics/instances.md), [Carts](/help/components/metrics/carts.md), [Checkouts](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Revenue](/help/components/metrics/revenue.md) in een trechterrapport.
   * Houtskaarten: Trends de metrische [Kaarten](/help/components/metrics/carts.md) in tijd.
   * Winkelweergaven: Trends de metrische [Cart meningen](/help/components/metrics/cart-views.md) in tijd.
   * Extra winkelwagentjes: Trends de metrische [toevoegingen van de Kunst](/help/components/metrics/cart-additions.md) in tijd.
   * Verhuizingen van winkelwagentjes: Trends de metrische [Cart verwijderingen](/help/components/metrics/cart-removals.md) in tijd.
   * Afbeeldingen: Trends de metrische [Checkouts](/help/components/metrics/checkouts.md) in tijd.
* Aangepaste gebeurtenissen: Bevat alle rapporten rond douane [Gebeurtenissen](/help/components/metrics/custom-events.md) specifiek voor uw implementatie.
* Bots: Hiermee worden beide gerelateerde rapporten weergegeven.
   * Bots: Hiermee geeft u de gebieden weer die uw site het meest frequent gebruiken. Zie [Bot rules](../../admin/admin/bot-removal/bot-rules.md) in de Admin gebruikershandleiding.
   * Beide pagina&#39;s: Hiermee geeft u de pagina&#39;s weer die het meest worden bereikt.
* In real time: Hiermee worden bepaalde afmetingen en meetwaarden weergegeven binnen seconden na de gegevensverzameling. Zie [Real-time rapporten](/help/components/c-real-time-reporting/realtime.md) voor meer informatie.

## Site-inhoud

Bevat rapporten rond afmetingen die typisch plaatsinhoud tonen. U kunt classificaties toepassen op sommige van deze rapporten. Als u classificaties toepast, wordt een rapport een menu dat het bronrapport en de classificatierapporten bevat.

* Pagina&#39;s: Hiermee gebruikt u de [Page](/help/components/dimensions/page.md)-dimensie.
* Sectie Site: Hiermee gebruikt u de [Site-sectie](/help/components/dimensions/site-section.md)-dimensie.
* Servers: Gebruikt de [Server](/help/components/dimensions/server.md) dimensie.
* Koppelingen: Bevat rapporten die verbinding het volgen gebruiken.
   * Koppelingen afsluiten: Hiermee gebruikt u de [Afmeting Afsluiten](/help/components/dimensions/exit-link.md).
   * Bestanden downloaden: Hiermee gebruikt u de [downloadkoppeling](/help/components/dimensions/download-link.md)-dimensie.
   * Aangepaste koppelingen: Hiermee gebruikt u de [Aangepaste koppeling](/help/components/dimensions/custom-link.md)-dimensie.
   * Pagina&#39;s niet gevonden: Hiermee gebruikt u de [Niet-gevonden pagina&#39;s](/help/components/dimensions/pages-not-found.md)-dimensie.

## Mobile

Bevat rapporten over verouderde mobiele rapporten. Deze rapporten baseren hun gegevens op het koord van de gebruikersagent. Ze gebruiken verschillende [mobiele afmetingen](/help/components/dimensions/mobile-dimensions.md) voor hun respectieve rapporten.

* Apparaten: Gebruikt de [Mobiel apparaat](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Type apparaat: Gebruikt de [afmeting van het mobiele apparatentype](/help/components/dimensions/mobile-dimensions.md).
* Fabrikant: Gebruikt de [Mobiele fabrikant](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermgrootte: Hiermee gebruikt u de [afmetingen voor mobiel scherm](/help/components/dimensions/mobile-dimensions.md).
* Schermhoogte: Gebruikt de [Grootte van het mobiele scherm](/help/components/dimensions/mobile-dimensions.md).
* Schermbreedte: Hiermee gebruikt u de [afmetingen voor mobiel scherm](/help/components/dimensions/mobile-dimensions.md).
* Ondersteuning voor cookie: Gebruikt de [Mobiele cookie-ondersteuning](/help/components/dimensions/mobile-dimensions.md)-dimensie.
* Ondersteuning voor afbeeldingen: Gebruikt de [Mobiele beeldsteun](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Kleurdiepte: Hiermee gebruikt u de [Mobiele kleurdiepte](/help/components/dimensions/mobile-dimensions.md)-dimensie.
* Audioondersteuning: Hiermee gebruikt u de [Mobiele audioondersteuning](/help/components/dimensions/mobile-dimensions.md)-dimensie.
* Video-ondersteuning: Gebruikt de [Mobiele videoondersteuning](/help/components/dimensions/mobile-dimensions.md)-dimensie.
* Besturingssysteem (afgekeurd): Hiermee gebruikt u de [afgekeurde afmeting van het mobiele besturingssysteem](/help/components/dimensions/mobile-dimensions.md).

## Paden

Bevat rapporten waarmee u tekengegevens voor bezoekers kunt bekijken.

* Volgende paginastroom: Gebruikt een stroomrapport op het punt van de hoogste paginadimensie. De meningen van de weg zijn gelijkaardig aan [Instanties](/help/components/metrics/instances.md). U kunt de gerapporteerde dimensie-item wijzigen. Een gelijkaardig rapport in Analysis Workspace is beschikbaar gebruikend [Stroom visualization](../analysis-workspace/visualizations/c-flow/flow.md).
* Volgende pagina: Neemt het bovenste pagina dimensie-item en toont u de volgende pagina&#39;s waar bezoekers naartoe zijn gegaan.
* Vorige paginastroom: Gebruikt een stroomrapport op het punt van de hoogste paginadimensie A gelijkaardig rapport in Analysis Workspace is beschikbaar gebruikend [Stroom visualization](../analysis-workspace/visualizations/c-flow/flow.md).
* Vorige pagina: Neemt het bovenste pagina dimensie-item en toont u de vorige pagina&#39;s waar bezoekers vandaan kwamen.
* Uitvallen: Hiermee kunt u pagina-elementen in stappen selecteren en wordt aangegeven hoeveel personen dat pad wel en niet hebben gevolgd. Een gelijkaardig rapport in Analysis Workspace is beschikbaar gebruikend [Fallout visualization](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Volledige paden: Hiermee geeft u afzonderlijke paden weer als dimensie-items. in Analysis Workspace; gebruik in plaats hiervan [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* PathFinder: Verstrekt veelvoudige types van rapporten die u wegen (gepensioneerd in Analysis Workspace) laten analyseren.
* Lengte pad: Hiermee gebruikt u de [Visit depth](/help/components/dimensions/visit-depth.md)-dimensie.
* Paginaanalyse
   * Paginaoverzicht: Neemt het bovenste pagina dimensie-item en toont een trendweergave. Geeft ook ingangspunten, vorige pagina&#39;s, exitpunten en volgende pagina&#39;s voor dat bovenste pagina-afmetingitem weer.
   * Opnieuw laden: Gebruikt de [Pagina](/help/components/dimensions/page.md) afmeting met [herlaadt](/help/components/metrics/reloads.md) metrisch.
   * Tijd besteed aan pagina: Gebruikt de [Tijd die aan pagina wordt doorgebracht - buckette](/help/components/dimensions/time-spent-on-page.md) afmeting.
   * Klik op pagina: Neemt het item voor de bovenste pagina-dimensie en toont het aantal klikken dat nodig was om naar die pagina te gaan tijdens een bepaald bezoek.
* Vermeldingen en uitgangen
   * Invoerpagina&#39;s: Hiermee gebruikt u de [Entry pages](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Oorspronkelijke invoerpagina&#39;s: Gebruikt de [Invoerpagina origineel](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Bezoeken op één pagina: Hiermee gebruikt u de [Pagina](/help/components/dimensions/page.md)-dimensie met het door Adobe verschafte segment &#39;Bezoeken van één pagina&#39; toegepast.
   * Pagina&#39;s afsluiten: Hiermee gebruikt u de [Afmeting Pagina&#39;s afsluiten](/help/components/dimensions/exit-dimensions.md).

>[!NOTE]
>
>Andere rapporten kunnen in deze omslag verschijnen. Het zijn andere dimensies, zoals eigenschappen, waar u [het kleven toegelaten ](../../admin/admin/c-traffic-variables/traffic-var.md) onder de montages van de rapportreeks hebt.

## Verkeersbronnen

Bevat een rapport dat inzicht geeft in waar bezoekers vandaan kwamen voordat ze naar uw site kwamen. Deze rapporten werken niet correct tenzij u correct [Interne filters URL ](../../admin/admin/internal-url-filter-admin.md) onder de montages van de rapportreeks plaatst.

* Trefwoorden zoeken - alle: Gebruikt de [dimensie van het sleutelwoord van het Onderzoek](/help/components/dimensions/search-keyword.md).
* Trefwoorden zoeken - betaald: Gebruikt het [sleutelwoord van het Onderzoek - betaalde](/help/components/dimensions/search-keyword.md) afmeting.
* Trefwoorden zoeken - natuurlijk: Gebruikt het [sleutelwoord van het Onderzoek - natuurlijk](/help/components/dimensions/search-keyword.md) afmeting
* Zoekprogramma&#39;s - allemaal: Hiermee gebruikt u de [Zoekengine](/help/components/dimensions/search-engine.md)-dimensie.
* Zoekprogramma&#39;s - betaald: Hiermee gebruikt u de [Zoekengine - betaalde](/help/components/dimensions/search-engine.md)-dimensie.
* Zoekprogramma&#39;s - natuurlijk: Gebruikt de [Zoekengine - natuurlijke ](/help/components/dimensions/search-engine.md)-dimensie.
* Alle rangschikkingen op zoekpagina&#39;s: Gebruikt de [Alle afmeting van de onderzoekspagina ](/help/components/dimensions/all-search-page-rank.md).
* Verwijzen naar domeinen: Gebruikt de [Refering domain](/help/components/dimensions/referring-domain.md) dimensie
* Oorspronkelijke verwijzende domeinen: Gebruikt de [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md) dimensie
* Referenties: Gebruikt de [Referrer](/help/components/dimensions/referrer.md) dimensie.
* Typen referenties: Gebruikt de [dimensie Referrer type](/help/components/dimensions/referrer-type.md).

## Campagnes

Bevat rapporten hoofdzakelijk rond de [het Volgen code](/help/components/dimensions/tracking-code.md) dimensie.

* Kanaal voor conversie van campagne: Meldt click-through, [Checkouts](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Revenue](/help/components/metrics/revenue.md) in een kanaalrapport. De metrische klikdoorhalingen is gelijkaardig aan [Instanties](/help/components/metrics/instances.md) metrisch in context van [het Volgen code](/help/components/dimensions/tracking-code.md) afmeting. Een gelijkaardige visualisatie wordt bereikt in Analysis Workspace gebruikend [Fallout visualization](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Trackingcode: Hiermee gebruikt u de [dimensie Code bijhouden](/help/components/dimensions/tracking-code.md).

## Producten

Bevat rapporten hoofdzakelijk rond de [dimensie van het Product](/help/components/dimensions/product.md).

* Trechter voor productomzetting: Rapporteert [Productweergaven](/help/components/metrics/product-views.md), [Cart-toevoegingen](/help/components/metrics/cart-additions.md), [Checkouts](/help/components/metrics/checkouts.md), [Bestellingen](/help/components/metrics/orders.md), [Eenheden](/help/components/metrics/units.md) en [Opbrengst](/help/components/metrics/revenue.md) in een kernrapport. Een gelijkaardige visualisatie wordt bereikt in Analysis Workspace gebruikend [Fallout visualization](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Producten: Gebruikt de [Afmeting van Producten](/help/components/dimensions/product.md).
* Cross-sell: Geeft producten weer die gezamenlijk worden verkocht (in Analysis Workspace afgeschreven).
* Categorieën: Hiermee gebruikt u de [afmetingen Categorie](/help/components/dimensions/category.md).

## Bezoekersbewaring

Bevat rapporten rondom bezoekers die terugkeren naar uw site.

* Retourfrequentie: Gebruikt de [Return frequency](/help/components/dimensions/return-frequency.md) dimensie.
* Terugkeerbezoeken: Trends [Visits](/help/components/metrics/visits.md) metrisch in tijd met de Adobe-Geleverde &quot;Bezoekingen van de Terugkeer&quot;toegepast.
* Bezoek nummer: Gebruikt de [Visit number](/help/components/dimensions/visit-number.md) dimensie.
* Verkoopcyclus: Map voor aankoopgerelateerde rapporten.
   * Klantenloyaliteit: Gebruikt de [Klantenloyaliteit](/help/components/dimensions/customer-loyalty.md) dimensie.
   * Dagen vóór eerste aankoop: Gebruikt de [Dagen vóór eerste aankoop](/help/components/dimensions/days-before-first-purchase.md) dimensie.
   * Dagen sinds laatste aankoop: Gebruikt de [Dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md) dimensie.
   * Dagelijkse unieke klanten: Trends [Dagelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop van de tijd met het door Adobe verschafte &#39;kopers&#39;-segment toegepast.
   * Weekse unieke klanten: Trends [Wekelijks unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop van de tijd met het door Adobe verschafte &#39;kopers&#39;-segment toegepast.
   * Unieke klanten per maand: Trends [Maandelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte &#39;kopers&#39;-segment toegepast.
   * Unieke klanten op kwartaalbasis: Trends [Driemaandelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte &#39;kopers&#39;-segment toegepast. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke klanten in het jaar: Trends [Yearly unique bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte &#39;kopers&#39;-segment toegepast.

## Bezoekersprofiel

Bevat rapporten over wie uw plaats bezoekt.

* Geosegmentatie: Rapporten over waar op de wereld hits naar uw site vandaan komen.
   * Landen: Gebruikt de [Country](/help/components/dimensions/countries.md) dimensie.
   * Regio: Hiermee gebruikt u de [Regio](/help/components/dimensions/regions.md)-dimensie.
   * Steden: Gebruikt de [dimensie van Steden](/help/components/dimensions/cities.md).
   * VS-staten: Hiermee gebruikt u de [Amerikaanse dimensie](/help/components/dimensions/us-states.md).
   * US DMA: Gebruikt de [US DMA](/help/components/dimensions/us-dma.md) dimensie.
* Talen: Gebruikt de [Taal](/help/components/dimensions/language.md) dimensie.
* Tijdzones: Gebruikt de dimensie van de tijdzone (gepensioneerd in Analysis Workspace). Dimension-items zijn de GMT-verschuiving van de hit.
* Domein: Hiermee gebruikt u de [Domein](/help/components/dimensions/domain.md)-dimensie.
* Domein op hoofdniveau: Gebruikt de domeindimensie op het hoogste niveau (in Analysis Workspace niet meer beschikbaar). Het groepeert de [domeinen](/help/components/dimensions/domain.md) dimensie in hoger-niveaucategorieën, typisch door land van het domein.
* Technologie: Map met rapporten over wat de bezoeker heeft gebruikt om uw site te openen.
   * Browsers: Gebruikt de [Browsers](/help/components/dimensions/browser.md) dimensie.
   * Browsertype: Gebruikt de [Browsertype](/help/components/dimensions/browser-type.md) dimensie.
   * Breedte browser: Gebruikt de [Browserbreedte - buckette](/help/components/dimensions/browser-width.md) afmeting.
   * Hoogte browser: Hiermee gebruikt u de [browserhoogte - buckette](/help/components/dimensions/browser-height.md)-dimensie.
   * Besturingssysteem: Gebruikt de [Afmeting van besturingssystemen](/help/components/dimensions/operating-systems.md).
   * Type besturingssysteem: Gebruikt de [Afmeting van besturingssystemen](/help/components/dimensions/operating-system-types.md).
   * Kleurdiepte monitor: Hiermee gebruikt u de [kleurdiepte](/help/components/dimensions/color-depth.md)-dimensie.
   * Monitorresolutie: Hiermee gebruikt u de [beeldschermresolutie](/help/components/dimensions/monitor-resolution.md)-dimensie.
   * Java: Gebruikt de [toegelaten Java](/help/components/dimensions/java-enabled.md) dimensie.
   * JavaScript: Gebruikt de voor JavaScript ingeschakelde dimensie (in Analysis Workspace afgebroken). Dimension-items zijn &#39;Ingeschakeld&#39;, &#39;Uitgeschakeld&#39; of &#39;Onbekend&#39;, afhankelijk van het feit of de browser JavaScript heeft ingeschakeld.
   * JavaScript-versie: gebruikt de JavaScript-versie-dimensie (in Analysis Workspace afgebroken). Dimension-items tonen de versie van JavaScript die de browser gebruikt.
   * Cookies: Gebruikt de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md)-dimensie.
   * Verbindingstypen: Gebruikt de [afmeting van het verbindingstype](/help/components/dimensions/connection-type.md).
   * Mobiele drager: Gebruikt de [Mobiele drager](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Status bezoeker: Gebruikt de overheidsdimensie (gepensioneerd in Analysis Workspace). Dimension-items komen voort uit de variabele [`state`](../../implement/vars/page-vars/state.md).
* Postcode bezoeker: Gebruikt de [Zip code](/help/components/dimensions/zip-code.md) dimensie.

## Aangepaste conversie

Bevat specifieke rapporten voor uw implementatie. Aangepaste omzettingsrapporten gebruiken [eVars](/help/components/dimensions/evar.md) als de dimensie.

## Aangepast verkeer

Bevat specifieke rapporten voor uw implementatie. Aangepaste verkeersrapporten gebruiken [props](/help/components/dimensions/prop.md) als dimensie.

## Marketingkanalen

Bevat rapporten met [Marketing kanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Rapport Kanaaloverzicht: Een speciaal aangepast rapport voor rapporten en analyses. Gebruikt marketingkanalen als dimensie-items, met meetwaarden die de eerste of laatste aanraakkenmerk gebruiken.
* Eerste aanraakkanaal: Hiermee gebruikt u de [Eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md)-dimensie.
* Details eerste aanraakkanaal: Hiermee gebruikt u de [Eerste aanraakkanaaldetail](/help/components/dimensions/first-touch-detail.md)-dimensie.
* Laatste aanraakkanaal: Hiermee gebruikt u de [Afmeting Laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md).
* Laatste aanraakkanaaldetails: Hiermee gebruikt u de [Last touch channel detail](/help/components/dimensions/last-touch-detail.md) dimensie.

## Bladwijzers

Bevat rapporten die u met bladwijzer hebt gemarkeerd. Zie [Bladwijzers](bookmarks.md) voor meer informatie.

## Dashboards

Bevat dashboards die u creeerde. Zie [Dashboards](dashboard.md) voor meer informatie.

## Targets

Bevat doelen die u hebt gemaakt. Zie [Doelstellingen](targets.md) voor meer informatie.

>[!NOTE]
>
>Als u uw rapport niet op deze hulppagina kunt vinden, is het mogelijk dat uw beheerder anders genoemd of aangepaste omslagen. Zie [Menu&#39;s aanpassen](/help/admin/admin/customize-menus.md) in de gebruikershandleiding Admin.
