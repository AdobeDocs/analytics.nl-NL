---
title: Rapporten
description: De afmetingen en metriek die Rapporten & Analytics voor elk rapport gebruiken.
feature: Reports & Analytics Basics
role: User, Admin
exl-id: e3c23d17-fc4b-479e-9c48-6f27ef0de4e3
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '1950'
ht-degree: 0%

---

# Rapporten

{{ra-eol}}

Elk rapport in Rapporten &amp; Analytics gebruikt een specifieke afmeting en metrisch gebrek. U kunt metrisch in elk rapport veranderen en onderverdelingen toevoegen indien gewenst. De volgende lijsten verstrekken welke dimensie in elk rapport wordt gebruikt.

>[!NOTE]
>
>Het menu Rapporten kan er anders uitzien, afhankelijk van aanpassingen die een beheerder in uw organisatie heeft aangebracht. Zie [Menu aanpassen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md) in de handleiding voor Admin-gebruikers.

>[!IMPORTANT]
>Effectief **31 december 2023**, is Adobe voornemens de rapporten en analyses en de bijbehorende rapporten en functies te beëindigen. Op dat moment werken de rapporten en analyses en alle bijbehorende rapporten en programma&#39;s niet meer. De rapporten, visualisaties en onderliggende technologie die de macht meldt &amp; Analytics niet meer aan de normen van de Adobe voldoet. De meeste functies voor rapporten en analyses zijn beschikbaar in Analysis Workspace. Sinds de release van Analysis Workspace in 2015 zijn de functionaliteit en mogelijkheden van Rapporten en Analytics verplaatst naar Analysis Workspace en is een drempel voor pariteit van de workflow bereikt. Deze kennisgeving legt het einde van de levensduur uit.

## Sitecijfers

Bevat rapporten die typisch het gebruiken van een datumwaaier trenderen. Bevat ook unieke rapporten, zoals Aanbevolen rapporten en Real-time rapporten.

* Mijn aanbevolen rapporten: Hiermee maakt u een dashboard dat meerdere rapporten bevat voor directe inzichten.
* Belangrijkste cijfers: Een rapport dat u toestaat om tot vijf metriek tegelijkertijd te trenderen. Trends [Paginaweergaven](/help/components/metrics/page-views.md), [Bezoeken](/help/components/metrics/visits.md), en [Unieke bezoekers](/help/components/metrics/unique-visitors.md) standaard.
* Paginaweergaven: Trends the [Paginaweergaven](/help/components/metrics/page-views.md) metrisch over tijd.
* Bezoeken: Trends the [Bezoeken](/help/components/metrics/visits.md) metrisch over tijd.
* Bezoekers: Verschillende trends [Unieke bezoekers](/help/components/metrics/unique-visitors.md) metriek in de loop der tijd.
   * Unieke bezoekers: Telt bezoekers slechts eenmaal voor het volledige geselecteerde datumbereik.
   * Uur unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende uren van het geselecteerde datumbereik.
   * Dagelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende dagen van het geselecteerde datumbereik.
   * Wekelijks unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende weken van het geselecteerde datumbereik.
   * Maandelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende maanden van het geselecteerde datumbereik.
   * Unieke bezoekers op kwartaalbasis: Hiermee telt u bezoekers meerdere keren als ze in verschillende kwartalen van het geselecteerde datumbereik een bezoek brengen. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke jaarlijkse bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende kalenderjaren van het geselecteerde datumbereik.
* Tijd besteed per bezoek: Gebruikt de [Tijd doorgebracht per bezoek - ingekapseld](/help/components/dimensions/time-spent-per-visit.md) dimensie.
* Tijd vóór de gebeurtenis: Gebruikt de [Tijd vóór de gebeurtenis](/help/components/dimensions/time-prior-to-event.md) dimensie.
* Aankopen: Bevat rapporten over op aankoop-gebaseerde metriek.
   * Conversietrechter aanschaffen: Rapport over [Bezoeken](/help/components/metrics/visits.md), [Houtskaarten](/help/components/metrics/carts.md), [Orders](/help/components/metrics/orders.md), [Ontvangsten](/help/components/metrics/revenue.md), en [Eenheden](/help/components/metrics/units.md) in een trechter-rapport. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
   * Ontvangsten: Hiermee wordt de metrische waarde verhoogd [Ontvangsten](/help/components/metrics/revenue.md) na verloop van tijd.
   * Bestellingen: Hiermee wordt de metrische waarde verhoogd [Orders](/help/components/metrics/orders.md) na verloop van tijd.
   * Eenheden: Hiermee wordt de metrische waarde verhoogd [Eenheden](/help/components/metrics/units.md) na verloop van tijd.
* Winkelwagentje: Bevat rapporten over winkelwagenmaateenheden.
   * Kanaal voor kleuromzetting: Rapporten [Instanties](/help/components/metrics/instances.md), [Houtskaarten](/help/components/metrics/carts.md), [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport.
   * Houtskaarten: Hiermee wordt de metrische waarde verhoogd [Houtskaarten](/help/components/metrics/carts.md) na verloop van tijd.
   * Winkelweergaven: Hiermee wordt de metrische waarde verhoogd [Winkelweergaven](/help/components/metrics/cart-views.md) na verloop van tijd.
   * Extra winkelwagentjes: Hiermee wordt de metrische waarde verhoogd [Extra winkelwagentjes](/help/components/metrics/cart-additions.md) na verloop van tijd.
   * Verhuizingen van winkelwagentjes: Hiermee wordt de metrische waarde verhoogd [Winkelwagentjes](/help/components/metrics/cart-removals.md) na verloop van tijd.
   * Afbeeldingen: Hiermee wordt de metrische waarde verhoogd [Afbeeldingen](/help/components/metrics/checkouts.md) na verloop van tijd.
* Aangepaste gebeurtenissen: Bevat alle rapporten rond douane [Gebeurtenissen](/help/components/metrics/custom-events.md) specifiek voor uw implementatie.
* Bots: Hiermee worden beide gerelateerde rapporten weergegeven.
   * Bots: Hiermee geeft u de gebieden weer die uw site het meest frequent gebruiken. Zie [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) in de handleiding voor Admin-gebruikers.
   * Beide pagina&#39;s: Hiermee geeft u de pagina&#39;s weer die het meest worden bereikt.
* In real time: Hiermee worden bepaalde afmetingen en meetwaarden weergegeven binnen seconden na de gegevensverzameling. Zie [Real-time rapporten](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md) voor meer informatie .

## Site-inhoud

Bevat rapporten rond afmetingen die typisch plaatsinhoud tonen. U kunt classificaties toepassen op sommige van deze rapporten. Als u classificaties toepast, wordt een rapport een menu dat het bronrapport en de classificatierapporten bevat.

* Pagina&#39;s: Gebruikt de [Pagina](/help/components/dimensions/page.md) dimensie.
* Sectie Site: Gebruikt de [Sectie Site](/help/components/dimensions/site-section.md) dimensie.
* Servers: Gebruikt de [Server](/help/components/dimensions/server.md) dimensie.
* Koppelingen: Bevat rapporten die verbinding het volgen gebruiken.
   * Koppelingen afsluiten: Gebruikt de [Koppeling afsluiten](/help/components/dimensions/exit-link.md) dimensie.
   * Bestanden downloaden: Gebruikt de [Koppeling downloaden](/help/components/dimensions/download-link.md) dimensie.
   * Aangepaste koppelingen: Gebruikt de [Aangepaste koppeling](/help/components/dimensions/custom-link.md) dimensie.
   * Pagina&#39;s niet gevonden: Gebruikt de [Pagina&#39;s niet gevonden](/help/components/dimensions/pages-not-found.md) dimensie.

## Mobile

Bevat rapporten over verouderde mobiele rapporten. Deze rapporten baseren hun gegevens op het koord van de gebruikersagent. Ze gebruiken verschillende [mobiele afmetingen](/help/components/dimensions/mobile-dimensions.md) voor hun respectieve verslagen.

* Apparaten: Gebruikt de [Mobiel apparaat](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Type apparaat: Gebruikt de [Mobiel apparaattype](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Fabrikant: Gebruikt de [Mobiele fabrikant](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermgrootte: Gebruikt de [Grootte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermhoogte: Gebruikt de [Hoogte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Schermbreedte: Gebruikt de [Breedte van mobiel scherm](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Ondersteuning voor cookie: Gebruikt de [Ondersteuning voor mobiele cookies](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Ondersteuning voor afbeeldingen: Gebruikt de [Ondersteuning voor mobiele images](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Kleurdiepte: Gebruikt de [Mobiele kleurdiepte](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Audioondersteuning: Gebruikt de [Ondersteuning voor mobiele audio](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Video-ondersteuning: Gebruikt de [Ondersteuning voor mobiele video](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Besturingssysteem (afgekeurd): Gebruikt de [Mobiel besturingssysteem (afgekeurd)](/help/components/dimensions/mobile-dimensions.md) dimensie.

## Paden

Bevat rapporten waarmee u tekengegevens voor bezoekers kunt bekijken.

* Volgende paginastroom: Gebruikt een stroomrapport op het punt van de hoogste paginadimensie. Padweergaven lijken op [Instanties](/help/components/metrics/instances.md). U kunt de gerapporteerde dimensie-item wijzigen. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Volgende pagina: Neemt het bovenste pagina dimensie-item en toont u de volgende pagina&#39;s waar bezoekers naartoe zijn gegaan.
* Vorige paginastroom: Gebruikt een stroomrapport op het punt van de hoogste paginadimensie A gelijkaardig rapport in Analysis Workspace is beschikbaar gebruikend een [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Vorige pagina: Neemt het bovenste pagina dimensie-item en toont u de vorige pagina&#39;s waar bezoekers vandaan kwamen.
* Uitvallen: Hiermee kunt u pagina-elementen in stappen selecteren en wordt aangegeven hoeveel personen dat pad wel en niet hebben gevolgd. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Volledige paden: Hiermee geeft u afzonderlijke paden weer als dimensie-items. in Analysis Workspace; gebruiken [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md) in plaats daarvan.
* PathFinder: Verstrekt veelvoudige types van rapporten die u wegen (gepensioneerd in Analysis Workspace) laten analyseren.
* Lengte pad: Gebruikt de [Diepte bezoeken](/help/components/dimensions/visit-depth.md) dimensie.
* Paginaanalyse
   * Paginaoverzicht: Neemt het bovenste pagina dimensie-item en toont een trendweergave. Geeft ook ingangspunten, vorige pagina&#39;s, exitpunten en volgende pagina&#39;s voor dat bovenste pagina-afmetingitem weer.
   * Opnieuw laden: Gebruikt de [Pagina](/help/components/dimensions/page.md) met de [Opnieuw laden](/help/components/metrics/reloads.md) metrisch.
   * Tijd besteed aan pagina: Gebruikt de [Tijd doorgebracht op pagina - ingesloten](/help/components/dimensions/time-spent-on-page.md) dimensie.
   * Klik op pagina: Neemt het item voor de bovenste pagina-dimensie en toont het aantal klikken dat nodig was om naar die pagina te gaan tijdens een bepaald bezoek.
* Vermeldingen en uitgangen
   * Invoerpagina&#39;s: Gebruikt de [Invoerpagina&#39;s](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Oorspronkelijke invoerpagina&#39;s: Gebruikt de [Invoerpagina origineel](/help/components/dimensions/entry-dimensions.md) dimensie.
   * Bezoeken op één pagina: Gebruikt de [Pagina](/help/components/dimensions/page.md) dimensie met het door Adobe verschafte segment &quot;Bezoeken van één pagina&quot; toegepast.
   * Pagina&#39;s afsluiten: Gebruikt de [Pagina&#39;s afsluiten](/help/components/dimensions/exit-dimensions.md) dimensie.

>[!NOTE]
>
>Andere rapporten kunnen in deze omslag verschijnen. Het zijn andere dimensies, zoals kronkels, waar u [plakken ingeschakeld](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) onder rapportsuite-instellingen.

## Verkeersbronnen

Bevat een rapport dat inzicht geeft in waar bezoekers vandaan kwamen voordat ze naar uw site kwamen. Deze rapporten werken alleen correct als u ze juist hebt ingesteld [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) onder rapportsuite-instellingen.

* Trefwoorden zoeken - alle: Gebruikt de [Trefwoord zoeken](/help/components/dimensions/search-keyword.md) dimensie.
* Trefwoorden zoeken - betaald: Gebruikt de [Zoeken op trefwoord - betaald](/help/components/dimensions/search-keyword.md) dimensie.
* Trefwoorden zoeken - natuurlijk: Gebruikt de [Zoeken op trefwoord - natuurlijk](/help/components/dimensions/search-keyword.md) dimensie
* Zoekprogramma&#39;s - allemaal: Gebruikt de [Zoekmachine](/help/components/dimensions/search-engine.md) dimensie.
* Zoekprogramma&#39;s - betaald: Gebruikt de [Zoekmachine - betaald](/help/components/dimensions/search-engine.md) dimensie.
* Zoekprogramma&#39;s - natuurlijk: Gebruikt de [Zoekmachine - natuurlijk](/help/components/dimensions/search-engine.md) dimensie.
* Alle rangschikkingen op zoekpagina&#39;s: Gebruikt de [Alle zoekpaginanummers](/help/components/dimensions/all-search-page-rank.md) dimensie.
* Verwijzen naar domeinen: Gebruikt de [Verwijzen naar domein](/help/components/dimensions/referring-domain.md) dimensie
* Oorspronkelijke verwijzende domeinen: Gebruikt de [Origineel verwijzend domein](/help/components/dimensions/original-referring-domain.md) dimensie
* Referenties: Gebruikt de [Referenter](/help/components/dimensions/referrer.md) dimensie.
* Typen referenties: Gebruikt de [Type referentie](/help/components/dimensions/referrer-type.md) dimensie.

## Campagnes

Bevat hoofdzakelijk rapporten rond [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie.

* Kanaal voor conversie van campagne: Meldt klikcontroles, [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport. Metrische klikdoorhalingen is gelijkaardig aan [Instanties](/help/components/metrics/instances.md) in de context van de [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Trackingcode: Gebruikt de [Code bijhouden](/help/components/dimensions/tracking-code.md) dimensie.

## Producten

Bevat hoofdzakelijk rapporten rond [Product](/help/components/dimensions/product.md) dimensie.

* Trechter voor productomzetting: Rapporten [Productweergaven](/help/components/metrics/product-views.md), [Extra winkelwagentjes](/help/components/metrics/cart-additions.md), [Afbeeldingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), [Eenheden](/help/components/metrics/units.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een trechter-rapport. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Uitvalvisualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Producten: Gebruikt de [Producten](/help/components/dimensions/product.md) dimensie.
* Cross-sell: Geeft producten weer die gezamenlijk worden verkocht (in Analysis Workspace afgeschreven).
* Categorieën: Gebruikt de [Categorie](/help/components/dimensions/category.md) dimensie.

## Bezoekersbewaring

Bevat rapporten rondom bezoekers die terugkeren naar uw site.

* Retourfrequentie: Gebruikt de [Retourfrequentie](/help/components/dimensions/return-frequency.md) dimensie.
* Terugkeerbezoeken: Trends the [Bezoeken](/help/components/metrics/visits.md) metrisch in tijd met Adobe-Geleverde &quot;Bezoekingen van de Terugkeer&quot;toegepast segment.
* Bezoek nummer: Gebruikt de [Bezoek nummer](/help/components/dimensions/visit-number.md) dimensie.
* Verkoopcyclus: Map voor aankoopgerelateerde rapporten.
   * Klantenloyaliteit: Gebruikt de [Klantenloyaliteit](/help/components/dimensions/customer-loyalty.md) dimensie.
   * Dagen vóór eerste aankoop: Gebruikt de [Dagen vóór eerste aankoop](/help/components/dimensions/days-before-first-purchase.md) dimensie.
   * Dagen sinds laatste aankoop: Gebruikt de [Dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md) dimensie.
   * Dagelijkse unieke klanten: Trends [Dagelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Weekse unieke klanten: Trends [Wekelijks unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Unieke klanten per maand: Trends [Maandelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door Adobe verschafte segment &quot;kopers&quot; van toepassing was.
   * Unieke klanten op kwartaalbasis: Trends [Unieke bezoekers op kwartaalbasis](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door Adobe verschafte segment &quot;kopers&quot; van toepassing was. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke klanten in het jaar: Trends [Unieke bezoekers](/help/components/metrics/unique-visitors.md) na verloop van tijd waarop het door Adobe verschafte segment &quot;kopers&quot; van toepassing was.

## Bezoekersprofiel

Bevat rapporten over wie uw plaats bezoekt.

* Geosegmentatie: Rapporten over waar op de wereld hits naar uw site vandaan komen.
   * Landen: Gebruikt de [Landen](/help/components/dimensions/countries.md) dimensie.
   * Regio: Gebruikt de [Regio&#39;s](/help/components/dimensions/regions.md) dimensie.
   * Steden: Gebruikt de [Plaatsen](/help/components/dimensions/cities.md) dimensie.
   * VS-staten: Gebruikt de [VS-staten](/help/components/dimensions/us-states.md) dimensie.
   * US DMA: Gebruikt de [US DMA](/help/components/dimensions/us-dma.md) dimensie.
* Talen: Gebruikt de [Taal](/help/components/dimensions/language.md) dimensie.
* Tijdzones: Gebruikt de dimensie van de tijdzone (gepensioneerd in Analysis Workspace). Dimension-items zijn de GMT-verschuiving van de hit.
* Domein: Gebruikt de [Domein](/help/components/dimensions/domain.md) dimensie.
* Domein op hoofdniveau: Gebruikt de domeindimensie op het hoogste niveau (in Analysis Workspace niet meer beschikbaar). Het groepeert de [domeinen](/help/components/dimensions/domain.md) dimensie in categorieën op hoger niveau, typisch door land van het domein.
* Technologie: Map met rapporten over wat de bezoeker heeft gebruikt om uw site te openen.
   * Browsers: Gebruikt de [Browsers](/help/components/dimensions/browser.md) dimensie.
   * Browsertype: Gebruikt de [Browsertype](/help/components/dimensions/browser-type.md) dimensie.
   * Breedte browser: Gebruikt de [Browserbreedte - gespaard](/help/components/dimensions/browser-width.md) dimensie.
   * Hoogte browser: Gebruikt de [Browserhoogte - ingesloten](/help/components/dimensions/browser-height.md) dimensie.
   * Besturingssysteem: Gebruikt de [Besturingssystemen](/help/components/dimensions/operating-systems.md) dimensie.
   * Type besturingssysteem: Gebruikt de [Typen besturingssystemen](/help/components/dimensions/operating-system-types.md) dimensie.
   * Kleurdiepte monitor: Gebruikt de [Kleurdiepte](/help/components/dimensions/color-depth.md) dimensie.
   * Monitorresolutie: Gebruikt de [Monitorresolutie](/help/components/dimensions/monitor-resolution.md) dimensie.
   * Java: Gebruikt de [Java ingeschakeld](/help/components/dimensions/java-enabled.md) dimensie.
   * JavaScript: Gebruikt de voor JavaScript ingeschakelde dimensie (in Analysis Workspace afgebroken). Dimension-items zijn &#39;Ingeschakeld&#39;, &#39;Uitgeschakeld&#39; of &#39;Onbekend&#39;, afhankelijk van het feit of de browser JavaScript heeft ingeschakeld.
   * JavaScript-versie: gebruikt de JavaScript-versie-dimensie (in Analysis Workspace afgebroken). Dimension-items tonen de versie van JavaScript die de browser gebruikt.
   * Cookies: Gebruikt de [Cookie-ondersteuning](/help/components/dimensions/cookie-support.md) dimensie.
   * Verbindingstypen: Gebruikt de [Verbindingstype](/help/components/dimensions/connection-type.md) dimensie.
   * Mobiele drager: Gebruikt de [Mobiele drager](/help/components/dimensions/mobile-dimensions.md) dimensie.
* Status bezoeker: Gebruikt de overheidsdimensie (gepensioneerd in Analysis Workspace). Dimension-items komen van de [`state`](../../implement/vars/page-vars/state.md) variabele.
* Postcode bezoeker: Gebruikt de [Postcode](/help/components/dimensions/zip-code.md) dimensie.

## Aangepaste conversie

Bevat specifieke rapporten voor uw implementatie. Gebruik aangepaste omzettingsrapporten [eVars](/help/components/dimensions/evar.md) als de dimensie.

## Aangepast verkeer

Bevat specifieke rapporten voor uw implementatie. Het gebruik van aangepaste verkeersrapporten [props](/help/components/dimensions/prop.md) als de dimensie.

## Marketingkanalen

Bevat rapporten waarin [Marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Rapport Kanaaloverzicht: Een speciaal aangepast rapport voor rapporten en analyses. Gebruikt marketingkanalen als dimensie-items, met meetwaarden die de eerste of laatste aanraakkenmerk gebruiken.
* Eerste aanraakkanaal: Gebruikt de [Eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md) dimensie.
* Details eerste aanraakkanaal: Gebruikt de [Eerste aanraakkanaaldetail](/help/components/dimensions/first-touch-detail.md) dimensie.
* Laatste aanraakkanaal: Gebruikt de [Laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md) dimensie.
* Laatste aanraakkanaaldetails: Gebruikt de [Laatste aanraakkanaaldetail](/help/components/dimensions/last-touch-detail.md) dimensie.

## Bladwijzers

Bevat rapporten die u met bladwijzer hebt gemarkeerd. Zie [Bladwijzers](bookmarks.md) voor meer informatie .

## Dashboards

Bevat dashboards die u creeerde. Zie [Dashboards](dashboard.md) voor meer informatie .

## Targets

Bevat doelen die u hebt gemaakt. Zie [Doelen](targets.md) voor meer informatie .

>[!NOTE]
>
>Als u uw rapport niet op deze hulppagina kunt vinden, is het mogelijk dat uw beheerder anders genoemd of aangepaste omslagen. Zie [Menu aanpassen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/customize-menus.md) in de handleiding voor Admin-gebruikers.
