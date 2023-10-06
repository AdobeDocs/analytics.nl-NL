---
title: Rapporten
description: De afmetingen en metriek die Rapporten & Analytics voor elk rapport gebruiken.
feature: Reports & Analytics Basics
role: User, Admin
exl-id: e3c23d17-fc4b-479e-9c48-6f27ef0de4e3
source-git-commit: 246fbe068898ad04db2f324975fc27cb24bc7f58
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 0%

---

# Rapporten

{{ra-eol}}

Elk rapport in Rapporten &amp; Analytics gebruikt een specifieke afmeting en metrisch gebrek. U kunt metrisch in elk rapport veranderen en onderverdelingen toevoegen indien gewenst. De volgende lijsten verstrekken welke dimensie in elk rapport wordt gebruikt.

>[!NOTE]
>
>Het menu Rapporten kan er anders uitzien, afhankelijk van aanpassingen die een beheerder in uw organisatie heeft aangebracht. Zie [Menu&#39;s aanpassen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md) in de handleiding voor Admin-gebruikers.

## Sitecijfers

Bevat rapporten die typisch het gebruiken van een datumwaaier trenderen. Bevat ook unieke rapporten, zoals Aanbevolen rapporten en Real-time rapporten.

* Mijn aanbevolen rapporten: maakt een dashboard dat verschillende rapporten bevat voor directe inzichten.
* Zeer belangrijke metriek: Een rapport dat u toestaat om tot vijf metriek tegelijkertijd te trenderen. Trends [Paginaweergaven](/help/components/metrics/page-views.md), [Bezoeken](/help/components/metrics/visits.md), en [Unieke bezoekers](/help/components/metrics/unique-visitors.md) standaard.
* Paginaweergaven: Hiermee wordt de [Paginaweergaven](/help/components/metrics/page-views.md) metrisch over tijd.
* Bezoeken: Trends the [Bezoeken](/help/components/metrics/visits.md) metrisch over tijd.
* Bezoekers: verschillende trends [Unieke bezoekers](/help/components/metrics/unique-visitors.md) metriek in de loop der tijd.
   * Unieke bezoekers: telt bezoekers slechts één keer voor het volledige geselecteerde datumbereik.
   * Uur unieke bezoekers: telt bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende uren van het geselecteerde datumbereik.
   * Unieke dagelijkse bezoekers: telt bezoekers meerdere keren als ze gedurende verschillende dagen van het geselecteerde datumbereik een bezoek brengen.
   * Wekelijks unieke bezoekers: telt bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende weken van het geselecteerde datumbereik.
   * Unieke maandelijkse bezoekers: telt bezoekers meerdere keren als ze gedurende verschillende maanden van het geselecteerde datumbereik een bezoek brengen.
   * Unieke kwartaalbezoekers: telt bezoekers meerdere keren als ze in verschillende kwartalen van het geselecteerde datumbereik bezoeken. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke jaarlijkse bezoekers: telt bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende kalenderjaren van het geselecteerde datumbereik.
* Tijd besteed per bezoek: gebruikt de [Tijd doorgebracht per bezoek - ingekapseld](/help/components/dimensions/time-spent-per-visit.md) dimensie.
* Tijd vóór gebeurtenis: gebruikt de gebeurtenis [Tijd vóór de gebeurtenis](/help/components/dimensions/time-prior-to-event.md) dimensie.
* Aankopen: bevat rapporten over op aanschaf gebaseerde cijfers.
   * Conversietrechter aanschaffen: rapporteren over [Bezoeken](/help/components/metrics/visits.md), [Houtskaarten](/help/components/metrics/carts.md), [Orders](/help/components/metrics/orders.md), [Ontvangsten](/help/components/metrics/revenue.md), en [Eenheden](/help/components/metrics/units.md) in een trechter-rapport. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
   * Inkomsten: trends van de metrische waarde [Ontvangsten](/help/components/metrics/revenue.md) na verloop van tijd.
   * Orders: Trends the metrisch [Orders](/help/components/metrics/orders.md) na verloop van tijd.
   * Eenheden: Trends de metrische waarde [Eenheden](/help/components/metrics/units.md) na verloop van tijd.
* Winkelwagentje: bevat rapporten over winkelwagentjes.
   * Kanaal voor kleuromzetting: rapporten [Instanties](/help/components/metrics/instances.md), [Houtskaarten](/help/components/metrics/carts.md), [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport.
   * Haartjes: Trends the metrisch [Houtskaarten](/help/components/metrics/carts.md) na verloop van tijd.
   * Illustratieweergaven: hiermee wordt de metrische waarde verhoogd [Winkelweergaven](/help/components/metrics/cart-views.md) na verloop van tijd.
   * Extra winkelwagentjes: hiermee wordt de metrische waarde verhoogd [Extra winkelwagentjes](/help/components/metrics/cart-additions.md) na verloop van tijd.
   * Verhuizingen van winkelwagentjes: trends van de metrische waarde [Winkelwagentjes](/help/components/metrics/cart-removals.md) na verloop van tijd.
   * Checkouts: hiermee wordt de metrische waarde verhoogd [Afbeeldingen](/help/components/metrics/checkouts.md) na verloop van tijd.
* Aangepaste gebeurtenissen: bevat alle rapporten rondom aangepaste gebeurtenissen [Gebeurtenissen](/help/components/metrics/custom-events.md) specifiek voor uw implementatie.
* Bots: geeft beide gerelateerde rapporten weer.
   * Bots: toont de vlekken die uw plaats het meest frequent voorkomen. Zie [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) in de handleiding voor Admin-gebruikers.
   * Beide pagina&#39;s: geeft de pagina&#39;s weer die het meest worden bereikt.
* In real time: toont bepaalde afmetingen en metriek binnen seconden na gegevensinzameling. Zie [Real-time rapporten](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) voor meer informatie .

## Site-inhoud

Bevat rapporten rond afmetingen die typisch plaatsinhoud tonen. U kunt classificaties toepassen op sommige van deze rapporten. Als u classificaties toepast, wordt een rapport een menu dat het bronrapport en de classificatierapporten bevat.

* Pagina&#39;s: gebruikt de [Pagina](/help/components/dimensions/page.md) dimensie.
* Sectie Site: gebruikt de [Sectie Site](/help/components/dimensions/site-section.md) dimensie.
* Servers: gebruikt de [Server](/help/components/dimensions/server.md) dimensie.
* Koppelingen: bevat rapporten waarin het bijhouden van koppelingen wordt gebruikt.
   * Koppelingen afsluiten: gebruikt de [Koppeling afsluiten](/help/components/dimensions/exit-link.md) dimensie.
   * Bestanden downloaden: gebruikt de [Koppeling downloaden](/help/components/dimensions/download-link.md) dimensie.
   * Aangepaste koppelingen: gebruikt de [Aangepaste koppeling](/help/components/dimensions/custom-link.md) dimensie.
   * Pagina&#39;s niet gevonden: gebruikt de [Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) dimensie.

## Mobile

Bevat rapporten over verouderde mobiele rapporten. Deze rapporten baseren hun gegevens op het koord van de gebruikersagent. Ze gebruiken verschillende [mobiele afmetingen](/help/components/dimensions/mobile-dimensions.md) voor hun respectieve verslagen.

* Apparaten: gebruikt de [Mobiel apparaat](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Apparaattype: gebruikt de [Mobiel apparaattype](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Fabrikant: gebruikt de [Mobiele fabrikant](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermgrootte: gebruikt de [Grootte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermhoogte: gebruikt de [Hoogte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermbreedte: gebruikt de [Breedte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Cookie-ondersteuning: gebruikt de [Ondersteuning voor mobiele cookies](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Ondersteuning voor afbeeldingen: gebruikt de [Ondersteuning voor mobiele images](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Kleurdiepte: gebruikt de [Mobiele kleurdiepte](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Audioondersteuning: gebruikt de [Ondersteuning voor mobiele audio](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Video-ondersteuning: gebruikt de [Ondersteuning voor mobiele video](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Besturingssysteem (afgekeurd): gebruikt de [Mobiel besturingssysteem (afgekeurd)](/help/components/dimensions/mobile-dimensions.md) dimensie.

## Paden

Bevat rapporten waarmee u tekengegevens voor bezoekers kunt bekijken.

* Volgende paginastroom: gebruikt een stroomrapport op het bovenste pagina dimensiepunt. Padweergaven lijken op [Instanties](/help/components/metrics/instances.md). U kunt de gerapporteerde dimensie-item wijzigen. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Volgende pagina: neemt het item voor de bovenste pagina-afmetingen en toont u de volgende pagina&#39;s waar bezoekers naartoe zijn gegaan.
* Vorige paginastroom: gebruikt een stroomrapport op de bovenste pagina dimensie-item Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Vorige pagina: neemt het item voor de bovenste pagina-afmetingen en toont u de vorige pagina&#39;s waar bezoekers vandaan kwamen.
* Uitvallen: hiermee kunt u pagina-elementen in stappen selecteren en geeft u het aantal personen weer dat dat pad wel en niet heeft gevolgd. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Volledige paden: afzonderlijke paden worden weergegeven als dimensie-items. Gepensioneerd in Analysis Workspace; gebruik de [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md) in plaats daarvan.
* PathFinder: Verstrekt veelvoudige types van rapporten die u wegen (gepensioneerd in Analysis Workspace) laten analyseren.
* Padlengte: gebruikt de [Diepte bezoeken](/help/components/dimensions/visit-depth.md) dimensie.
* Paginaanalyse
   * Paginaoverzicht: neemt het item voor de bovenste pagina-afmeting en toont een trendweergave. Geeft ook ingangspunten, vorige pagina&#39;s, exitpunten en volgende pagina&#39;s voor dat bovenste pagina-afmetingitem weer.
   * Opnieuw laden: gebruikt de [Pagina](/help/components/dimensions/page.md) dimensie met de [Opnieuw laden](/help/components/metrics/reloads.md) metrisch.
   * Tijd besteed aan pagina: gebruikt de [Tijd doorgebracht op pagina - ingesloten](/help/components/dimensions/time-spent-on-page.md) dimensie.
   * Klik op pagina: neemt het item voor de afmetingen van de bovenste pagina en toont het aantal klikken dat nodig was om naar die pagina te gaan tijdens een bepaald bezoek.
* Invoer en uitgang
   * Invoerpagina&#39;s: gebruikt de [Invoerpagina&#39;s](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Oorspronkelijke invoerpagina&#39;s: gebruikt de [Invoerpagina origineel](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Bezoeken op één pagina: gebruikt de [Pagina](/help/components/dimensions/page.md) dimensie met het door de Adobe verschafte segment &quot;Bezoeken van één pagina&quot; toegepast.
   * Pagina&#39;s afsluiten: gebruikt de [Pagina&#39;s afsluiten](/help/components/dimensions/exit-dimensions.md) dimensie.

>[!NOTE]
>
>Andere rapporten kunnen in deze omslag verschijnen. Het zijn andere afmetingen, zoals profielen, waar u [plakken ingeschakeld](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) onder rapportsuite-instellingen.

## Verkeerbronnen

Bevat een rapport dat inzicht geeft in waar bezoekers vandaan kwamen voordat ze naar uw site kwamen. Deze rapporten werken alleen correct als u ze juist hebt ingesteld [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) onder rapportsuite-instellingen.

* Trefwoorden zoeken - alles: gebruikt de [Trefwoord zoeken](/help/components/dimensions/search-keyword.md) dimensie.
* Trefwoorden zoeken - betaald: gebruikt de [Zoeken op trefwoord - betaald](/help/components/dimensions/search-keyword.md) dimensie.
* Trefwoorden zoeken - natuurlijk: gebruikt de [Zoeken op trefwoord - natuurlijk](/help/components/dimensions/search-keyword.md) dimensie
* Zoekprogramma&#39;s - allemaal: gebruikt de [Zoekmachine](/help/components/dimensions/search-engine.md) dimensie.
* Zoekprogramma&#39;s - betaald: gebruikt de [Zoekmachine - betaald](/help/components/dimensions/search-engine.md) dimensie.
* Zoekprogramma&#39;s - natuurlijk: gebruikt de [Zoekmachine - natuurlijk](/help/components/dimensions/search-engine.md) dimensie.
* Alle rangschikkingen op de zoekpagina: gebruikt de opdracht [Alle zoekpaginanummers](/help/components/dimensions/all-search-page-rank.md) dimensie.
* Verwijzen naar domeinen: gebruikt de [Verwijzen naar domein](/help/components/dimensions/referring-domain.md) dimensie
* Oorspronkelijke verwijzende domeinen: gebruikt de [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md) dimensie
* Referenties: gebruikt de [Referenter](/help/components/dimensions/referrer.md) dimensie.
* Typen referenties: gebruikt de [Type referentie](/help/components/dimensions/referrer-type.md) dimensie.

## Campagnes

Bevat hoofdzakelijk rapporten rond [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie.

* Kanaal voor conversie van campagne: meldt doorklikbewerkingen, [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport. Metrisch klikken-door is gelijkaardig aan [Instanties](/help/components/metrics/instances.md) in de context van de [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Trackingcode: gebruikt de [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie.

## Producten

Bevat hoofdzakelijk rapporten rond [Product](/help/components/dimensions/product.md) dimensie.

* Conversietrechter voor producten: rapporten [Productweergaven](/help/components/metrics/product-views.md), [Extra winkelwagentjes](/help/components/metrics/cart-additions.md), [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), [Eenheden](/help/components/metrics/units.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Producten: gebruikt de [Producten](/help/components/dimensions/product.md) dimensie.
* Crosssell: toont producten die vaak samen worden verkocht (in Analysis Workspace met pensioen).
* Categorieën: gebruikt de [Categorie](/help/components/dimensions/category.md) dimensie.

## Bezoekersbewaring

Bevat rapporten rondom bezoekers die terugkeren naar uw site.

* Retourfrequentie: gebruikt de [Geretourneerde frequentie](/help/components/dimensions/return-frequency.md) dimensie.
* Terugkeerbezoeken: trends van de [Bezoeken](/help/components/metrics/visits.md) metrisch in tijd met Adobe-Geleverde &quot;Bezoekingen van de Terugkeer&quot;toegepast segment.
* Bezoek nummer: gebruikt de [Bezoek nummer](/help/components/dimensions/visit-number.md) dimensie.
* Verkoopcyclus: map voor aan aankoop gerelateerde rapporten.
   * Klantenloyaliteit: gebruikt de [Klantenloyaliteit](/help/components/dimensions/customer-loyalty.md) dimensie.
   * Dagen vóór eerste aankoop: gebruikt de [Dagen vóór eerste aankoop](/help/components/dimensions/days-before-first-purchase.md) dimensie.
   * Dagen sinds laatste aankoop: gebruikt de [Dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md) dimensie.
   * Dagelijkse unieke klanten: trends [Dagelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door de Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Wekelijks unieke klanten: trends [Wekelijks unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door de Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Unieke klanten per maand: trends [Maandelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door de Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Unieke klanten op kwartaalbasis: trends [Unieke bezoekers op kwartaalbasis](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door de Adobe verschafte segment &quot;kopers&quot; van toepassing was. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke klanten in het jaar: trends [Unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door de Adobe verschafte segment &quot;kopers&quot; van toepassing was.

## Bezoekersprofiel

Bevat rapporten over wie uw plaats bezoekt.

* Geosegmentatie: rapporten over waar op de wereld treffers naar uw site vandaan komen.
   * Landen: gebruikt de [Landen](/help/components/dimensions/countries.md) dimensie.
   * Regio: gebruikt de [Regio&#39;s](/help/components/dimensions/regions.md) dimensie.
   * Steden: gebruikt de [Plaatsen](/help/components/dimensions/cities.md) dimensie.
   * VS-staten: gebruikt de [VS-staten](/help/components/dimensions/us-states.md) dimensie.
   * US DMA: gebruikt de [US DMA](/help/components/dimensions/us-dma.md) dimensie.
* Talen: gebruikt de [Taal](/help/components/dimensions/language.md) dimensie.
* Tijdzones: gebruikt de tijdzonedimensie (in Analysis Workspace met pensioen gegaan). Dimension-items zijn de GMT-verschuiving van de hit.
* Domein: gebruikt het [Domein](/help/components/dimensions/domain.md) dimensie.
* Domein op hoofdniveau: gebruikt de domeindimensie op het hoogste niveau (in Analysis Workspace afgebroken). Het groepeert de [domeinen](/help/components/dimensions/domain.md) dimensie in categorieën op hoger niveau, typisch door land van het domein.
* Technologie: map met rapporten over wat de bezoeker heeft gebruikt om toegang te krijgen tot uw site.
   * Browsers: gebruikt de [Browsers](/help/components/dimensions/browser.md) dimensie.
   * Browsertype: gebruikt de [Browsertype](/help/components/dimensions/browser-type.md) dimensie.
   * Browserbreedte: gebruikt de [Browserbreedte - gespaard](/help/components/dimensions/browser-width.md) dimensie.
   * Hoogte browser: gebruikt de [Browserhoogte - ingesloten](/help/components/dimensions/browser-height.md) dimensie.
   * Besturingssysteem: gebruikt het [Besturingssystemen](/help/components/dimensions/operating-systems.md) dimensie.
   * Type besturingssysteem: gebruikt het [Typen besturingssystemen](/help/components/dimensions/operating-system-types.md) dimensie.
   * Kleurdiepte van monitor: gebruikt de [Kleurdiepte](/help/components/dimensions/color-depth.md) dimensie.
   * Monitorresolutie: gebruikt de [Monitorresolutie](/help/components/dimensions/monitor-resolution.md) dimensie.
   * Java: gebruikt de [Java ingeschakeld](/help/components/dimensions/java-enabled.md) dimensie.
   * JavaScript: gebruikt de voor JavaScript ingeschakelde dimensie (in Analysis Workspace afgebroken). Dimension-items zijn &#39;Ingeschakeld&#39;, &#39;Uitgeschakeld&#39; of &#39;Onbekend&#39;, afhankelijk van het feit of de browser JavaScript heeft ingeschakeld.
   * JavaScript-versie: gebruikt de JavaScript-versiedimensie (in Analysis Workspace afgebroken). Dimension-items tonen de JavaScript-versie die de browser gebruikt.
   * Cookies: gebruikt de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) dimensie.
   * Verbindingstypen: gebruikt de [Verbindingstype](/help/components/dimensions/connection-type.md) dimensie.
   * Mobiele drager: gebruikt de [Mobiele drager](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Staat van bezoeker: Gebruikt de overheidsdimensie (gepensioneerd in Analysis Workspace). Dimension-items komen van de [`state`](../../implement/vars/page-vars/state.md) variabele.
* Postcode bezoeker: gebruikt de code [Postcode](/help/components/dimensions/zip-code.md) dimensie.

## Aangepaste conversie

Bevat specifieke rapporten voor uw implementatie. Gebruik aangepaste omzettingsrapporten [eVars](/help/components/dimensions/evar.md) als de dimensie.

## Aangepast verkeer

Bevat specifieke rapporten voor uw implementatie. Het gebruik van aangepaste verkeersrapporten [props](/help/components/dimensions/prop.md) als de dimensie.

## Marketingkanalen

Bevat rapporten waarin [Marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Kanaaloverzichtrapport: een aangepast rapport dat specifiek is voor Rapporten en Analyse. Gebruikt marketingkanalen als dimensie-items, met meetwaarden die de eerste of laatste aanraakkenmerk gebruiken.
* Eerste aanraakkanaal: gebruikt het [Eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md) dimensie.
* Details eerste aanraakkanaal: gebruikt de [Eerste aanraakkanaaldetail](/help/components/dimensions/first-touch-detail.md) dimensie.
* Laatste aanraakkanaal: gebruikt het [Laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md) dimensie.
* Laatste aanraakkanaaldetails: gebruikt de [Laatste aanraakkanaaldetail](/help/components/dimensions/last-touch-detail.md) dimensie.

## Bladwijzers

Bevat rapporten die u met bladwijzer hebt gemarkeerd. Zie [Bladwijzers](bookmarks.md) voor meer informatie .

## Dashboards

Bevat dashboards die u creeerde. Zie [Dashboards](dashboard.md) voor meer informatie .

## Targets

Bevat doelen die u hebt gemaakt. Zie [Doelen](targets.md) voor meer informatie .

>[!NOTE]
>
>Als u uw rapport niet op deze hulppagina kunt vinden, is het mogelijk dat uw beheerder anders genoemd of aangepaste omslagen. Zie [Menu&#39;s aanpassen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md) in de handleiding voor Admin-gebruikers.
