---
title: Rapporten
description: De afmetingen en metriek die Rapporten & Analytics voor elk rapport gebruiken.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 0%

---


# Rapporten

Elk rapport in Rapporten &amp; Analytics gebruikt een specifieke dimensie en standaard metrisch. U kunt metrisch in elk rapport veranderen en onderverdelingen toevoegen indien gewenst. De volgende lijsten verstrekken welke dimensie in elk rapport wordt gebruikt.

>[!NOTE]
>
>Het menu Rapporten kan er anders uitzien, afhankelijk van aanpassingen die een beheerder in uw organisatie heeft aangebracht. Zie [Menu&#39;s aanpassen](/help/admin/admin/customize-menus.md) in de gebruikershandleiding voor Admin.

## Sitecijfers

Bevat rapporten die typisch het gebruiken van een datumwaaier trenderen. Bevat ook unieke rapporten, zoals Aanbevolen rapporten en Real-time rapporten.

* Mijn aanbevolen rapporten: Hiermee maakt u een dashboard dat meerdere rapporten bevat voor directe inzichten.
* Belangrijkste cijfers: Een rapport dat u toestaat om tot vijf metriek tegelijkertijd te trenderen. Trends [Page views](/help/components/metrics/page-views.md), [Visits](/help/components/metrics/visits.md)en [Unique bezoekers](/help/components/metrics/unique-visitors.md) standaard.
* Paginaweergaven: Hiermee wordt de metrische weergave [van de](/help/components/metrics/page-views.md) paginaweergave in de loop der tijd gebogen.
* Bezoeken: Trends metrisch van [Bebezoeken](/help/components/metrics/visits.md) in tijd.
* Bezoekers: Trends various [Unique bezoekers](/help/components/metrics/unique-visitors.md) metrics in time.
   * Unieke bezoekers: Telt bezoekers slechts eenmaal voor het volledige geselecteerde datumbereik.
   * Uur unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende uren van het geselecteerde datumbereik.
   * Dagelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende dagen van het geselecteerde datumbereik.
   * Wekelijks unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende weken van het geselecteerde datumbereik.
   * Maandelijkse unieke bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende maanden van het geselecteerde datumbereik.
   * Unieke bezoekers op kwartaalbasis: Hiermee telt u bezoekers meerdere keren als ze in verschillende kwartalen van het geselecteerde datumbereik een bezoek brengen. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke jaarlijkse bezoekers: Hiermee telt u bezoekers meerdere keren als ze een bezoek brengen tijdens verschillende kalenderjaren van het geselecteerde datumbereik.
* Tijd besteed per bezoek: Gebruikt de [Tijd besteed per bezoek - geketende](/help/components/dimensions/time-spent-per-visit.md) dimensie.
* Tijd vóór de gebeurtenis: Gebruikt de [tijd voorafgaand aan de dimensie van de gebeurtenis](/help/components/dimensions/time-prior-to-event.md) .
* Aankopen: Bevat rapporten over op aankoop-gebaseerde metriek.
   * Conversietrechter aanschaffen: Rapport over [bezoeken](/help/components/metrics/visits.md), [winkelwagentjes](/help/components/metrics/carts.md), [bestellingen](/help/components/metrics/orders.md), [inkomsten](/help/components/metrics/revenue.md)en [eenheden](/help/components/metrics/units.md) in een verslag van de trechter. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Fallout-visualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
   * Ontvangsten: Trends de metrische [Inkomsten](/help/components/metrics/revenue.md) in tijd.
   * Bestellingen: Trends de metrische [Orders](/help/components/metrics/orders.md) in tijd.
   * Eenheden: Trends de metrische [Eenheden](/help/components/metrics/units.md) in tijd.
* Winkelwagentje: Bevat rapporten over winkelwagenmaateenheden.
   * Kanaal voor kleuromzetting: Hiermee rapporteert u [instanties](/help/components/metrics/instances.md), [kaarten](/help/components/metrics/carts.md), [incheckouts](/help/components/metrics/checkouts.md), [bestellingen](/help/components/metrics/orders.md)en [inkomsten](/help/components/metrics/revenue.md) in een kabelrapport.
   * Houtskaarten: Trends de metrische [Houtjes](/help/components/metrics/carts.md) in tijd.
   * Winkelweergaven: Trends de weergaven [van het metrische](/help/components/metrics/cart-views.md) winkelwagentje in de loop van de tijd.
   * Extra winkelwagentjes: Trends de metrische toevoegingen van het [Kart](/help/components/metrics/cart-additions.md) in tijd.
   * Verhuizingen van winkelwagentjes: Trends de metrische verwijderingen van de [Kaart](/help/components/metrics/cart-removals.md) in tijd.
   * Afbeeldingen: Trends de metrische [Checkouts](/help/components/metrics/checkouts.md) in tijd.
* Aangepaste gebeurtenissen: Bevat alle rapporten rond douanegebeurtenissen [](/help/components/metrics/custom-events.md) specifiek voor uw implementatie.
* Bots: Hiermee worden beide gerelateerde rapporten weergegeven.
   * Bots: Hiermee geeft u de gebieden weer die uw site het meest frequent gebruiken. Zie [Bot-regels](../../admin/admin/bot-removal/bot-rules.md) in de gebruikershandleiding voor Admin.
   * Beide pagina&#39;s: Hiermee geeft u de pagina&#39;s weer die het meest worden bereikt.
* In real time: Hiermee worden bepaalde afmetingen en meetwaarden weergegeven binnen seconden na de gegevensverzameling. Zie [Real-time rapporten](/help/components/c-real-time-reporting/realtime.md) voor meer informatie.

## Site-inhoud

Bevat rapporten rond afmetingen die typisch plaatsinhoud tonen. U kunt classificaties toepassen op sommige van deze rapporten. Als u classificaties toepast, wordt een rapport een menu dat het bronrapport en de classificatierapporten bevat.

* Pagina&#39;s: Hiermee gebruikt u de afmeting [Pagina](/help/components/dimensions/page.md) .
* Sectie Site: Hiermee gebruikt u de sectie [](/help/components/dimensions/site-section.md) Site.
* Servers: Gebruikt de dimensie [Server](/help/components/dimensions/server.md) .
* Koppelingen: Bevat rapporten die verbinding het volgen gebruiken.
   * Koppelingen afsluiten: Hiermee gebruikt u de dimensie [Afsluiten](/help/components/dimensions/exit-link.md) .
   * Bestanden downloaden: Gebruikt de dimensie van de verbinding [van de](/help/components/dimensions/download-link.md) Download.
   * Aangepaste koppelingen: Hiermee gebruikt u de dimensie van de [aangepaste koppeling](/help/components/dimensions/custom-link.md) .
   * Pagina&#39;s niet gevonden: Hiermee gebruikt u de [pagina&#39;s die niet zijn gevonden](/help/components/dimensions/pages-not-found.md) .

## Mobile

Bevat rapporten over verouderde mobiele rapporten. Deze rapporten baseren hun gegevens op het koord van de gebruikersagent. Zij gebruiken verschillende [mobiele dimensies](/help/components/dimensions/mobile-dimensions.md) voor hun respectieve rapporten.

* Apparaten: Gebruikt de afmeting [Mobiel apparaat](/help/components/dimensions/mobile-dimensions.md) .
* Type apparaat: Hiermee gebruikt u de afmetingen van het [mobiele](/help/components/dimensions/mobile-dimensions.md) apparaattype.
* Fabrikant: Hiermee gebruikt u de afmetingen van de [mobiele fabrikant](/help/components/dimensions/mobile-dimensions.md) .
* Schermgrootte: Hiermee gebruikt u de afmetingen voor de grootte [van het](/help/components/dimensions/mobile-dimensions.md) mobiele scherm.
* Schermhoogte: Hiermee gebruikt u de hoogte [van het](/help/components/dimensions/mobile-dimensions.md) mobiele scherm.
* Schermbreedte: Hiermee gebruikt u de afmetingen voor de breedte [van het](/help/components/dimensions/mobile-dimensions.md) mobiele scherm.
* Ondersteuning voor cookie: Gebruikt de ondersteuningsdimensie voor [](/help/components/dimensions/mobile-dimensions.md) mobiele cookies.
* Ondersteuning voor afbeeldingen: Hierbij wordt de ondersteuningsdimensie voor [](/help/components/dimensions/mobile-dimensions.md) mobiele afbeeldingen gebruikt.
* Kleurdiepte: Hiermee gebruikt u de [Mobile-kleurdiepte](/help/components/dimensions/mobile-dimensions.md) .
* Audioondersteuning: Gebruikt de dimensie [Mobiele audioondersteuning](/help/components/dimensions/mobile-dimensions.md) .
* Video-ondersteuning: Hiermee gebruikt u de dimensie [Mobiele videoondersteuning](/help/components/dimensions/mobile-dimensions.md) .
* Besturingssysteem (afgekeurd): Gebruikt de (afgekeurde) [afmeting van het](/help/components/dimensions/mobile-dimensions.md) mobiele besturingssysteem.

## Paden

Bevat rapporten waarmee u tekengegevens voor bezoekers kunt bekijken.

* Volgende paginastroom: Gebruikt een stroomrapport op de waarde van de hoogste paginadimensie. De padweergaven zijn vergelijkbaar met die van [instanties](/help/components/metrics/instances.md). U kunt de gerapporteerde waarde van de dimensie wijzigen. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Volgende pagina: Neemt de waarde voor de afmetingen van de bovenste pagina en toont u de volgende pagina&#39;s die bezoekers hebben bezocht.
* Vorige paginastroom: Gebruikt een stroomrapport op de waarde van de hoogste paginadimensie Een gelijkaardig rapport in Analysis Workspace is beschikbaar gebruikend een [Stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md).
* Vorige pagina: Neemt de waarde voor de afmetingen van de bovenste pagina op en toont u de vorige pagina&#39;s waar bezoekers vandaan kwamen.
* Uitvallen: Hiermee kunt u de waarden voor de pagina-afmetingen in stappen selecteren en wordt aangegeven hoeveel personen dat pad wel en niet hebben gevolgd. Een vergelijkbaar rapport in Analysis Workspace is beschikbaar via een [Fallout-visualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Volledige paden: Hiermee geeft u afzonderlijke paden weer als waarden voor afmetingen. in Analysis Workspace; gebruik in plaats hiervan de [stroomvisualisatie](../analysis-workspace/visualizations/c-flow/flow.md) .
* PathFinder: Verstrekt veelvoudige types van rapporten die u wegen (gepensioneerd in Analysis Workspace) laten analyseren.
* Lengte pad: Hiermee gebruikt u de diepte [van](/help/components/dimensions/visit-depth.md) Bezoek.
* Paginaanalyse
   * Paginaoverzicht: Neemt de waarde van de hoogste paginafmeting en toont een trended mening. Hier worden ook de invoerpunten, vorige pagina&#39;s, eindpunten en volgende pagina&#39;s voor de waarde van de afmeting van de bovenste pagina weergegeven.
   * Opnieuw laden: Gebruikt de afmeting van de [Pagina](/help/components/dimensions/page.md) met [herlaadt](/help/components/metrics/reloads.md) metrisch.
   * Tijd besteed aan pagina: Gebruikt de [Tijd die aan pagina wordt doorgebracht - geknipte](/help/components/dimensions/time-spent-on-page.md) afmeting.
   * Klik op pagina: Neemt de waarde van de hoogste paginafmeting en toont het aantal kliks het nam om aan die pagina in een bepaald bezoek te krijgen.
* Vermeldingen en uitgangen
   * Invoerpagina&#39;s: Hiermee gebruikt u de dimensie [Pagina](/help/components/dimensions/entry-dimensions.md) &#39;s invoeren.
   * Oorspronkelijke invoerpagina&#39;s: Hiermee gebruikt u de oorspronkelijke [afmeting van de](/help/components/dimensions/entry-dimensions.md) invoerpagina.
   * Bezoeken op één pagina: Hiermee gebruikt u de [pagina](/help/components/dimensions/page.md) -dimensie met het door Adobe verschafte segment &#39;Bezoeken van één pagina&#39; toegepast.
   * Pagina&#39;s afsluiten: Hiermee gebruikt u de dimensie Pagina [&#39;s](/help/components/dimensions/exit-dimensions.md) afsluiten.

>[!NOTE]
>
>Andere rapporten kunnen in deze omslag verschijnen. Het zijn andere dimensies, zoals steunen, waar u [het kleven hebt toegelaten](../../admin/admin/c-traffic-variables/traffic-var.md) onder de montages van de rapportreeks.

## Verkeersbronnen

Bevat een rapport dat inzicht geeft in waar bezoekers vandaan kwamen voordat ze naar uw site kwamen. Deze rapporten werken alleen correct als u de [interne URL-filters](../../admin/admin/internal-url-filter-admin.md) correct instelt onder de instellingen van de rapportsuite.

* Trefwoorden zoeken - alle: Gebruikt de dimensie van het sleutelwoord [van het](/help/components/dimensions/search-keyword.md) Onderzoek.
* Trefwoorden zoeken - betaald: Gebruikt het sleutelwoord van het [Onderzoek - betaalde](/help/components/dimensions/search-keyword.md) afmeting.
* Trefwoorden zoeken - natuurlijk: Gebruikt het sleutelwoord van het [Onderzoek - natuurlijke](/help/components/dimensions/search-keyword.md) dimensie
* Zoekprogramma&#39;s - allemaal: Hiermee gebruikt u de afmetingen van de [zoekengine](/help/components/dimensions/search-engine.md) .
* Zoekprogramma&#39;s - betaald: Gebruikt de [zoekmachine - betaalde](/help/components/dimensions/search-engine.md) dimensie.
* Zoekprogramma&#39;s - natuurlijk: Gebruikt de motor van het [Onderzoek - natuurlijke](/help/components/dimensions/search-engine.md) afmeting.
* Alle rangschikkingen op zoekpagina&#39;s: Hiermee gebruikt u de [achterwaartse](/help/components/dimensions/all-search-page-rank.md) afmeting van de zoekpagina.
* Verwijzen naar domeinen: Gebruikt de dimensie [Verwijzend domein](/help/components/dimensions/referring-domain.md)
* Oorspronkelijke verwijzende domeinen: Gebruikt de [Originele verwijzende domeindimensie](/help/components/dimensions/original-referring-domain.md)
* Referenties: Hiermee gebruikt u de [dimensie Referrer](/help/components/dimensions/referrer.md) .
* Typen referenties: Hiermee gebruikt u de afmetingen van het type [](/help/components/dimensions/referrer-type.md) Refersor.

## Campagnes

Bevat hoofdzakelijk rapporten rond de [het Volgen codedimensie](/help/components/dimensions/tracking-code.md) .

* Kanaal voor conversie van campagne: Meldt doorklikkingen, [Afhandelingen](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), en [Ontvangsten](/help/components/metrics/revenue.md) in een kanaalrapport. Metrische klikdoorhalingen is gelijkaardig aan metrische [Instanties](/help/components/metrics/instances.md) in context van de [het Volgen codedimensie](/help/components/dimensions/tracking-code.md) . Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Fallout-visualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Trackingcode: Hiermee gebruikt u de dimensie [Code](/help/components/dimensions/tracking-code.md) bijhouden.

## Producten

Bevat hoofdzakelijk rapporten rond de dimensie van het [Product](/help/components/dimensions/product.md) .

* Trechter voor productomzetting: Meldt [de meningen](/help/components/metrics/product-views.md)van het Product, de toevoegingen [van het](/help/components/metrics/cart-additions.md)Kunstwerk, [Checkouts](/help/components/metrics/checkouts.md), [Orders](/help/components/metrics/orders.md), [Eenheden](/help/components/metrics/units.md)[](/help/components/metrics/revenue.md) , en Revenue in een het kanaalrapport. Een vergelijkbare visualisatie wordt bereikt in Analysis Workspace met behulp van de [Fallout-visualisatie](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* Producten: Hiermee gebruikt u de dimensie [Producten](/help/components/dimensions/product.md) .
* Cross-sell: Geeft producten weer die gezamenlijk worden verkocht (in Analysis Workspace afgeschreven).
* Categorieën: Gebruikt de afmeting van de [Categorie](/help/components/dimensions/category.md) .

## Bezoekersbewaring

Bevat rapporten rondom bezoekers die terugkeren naar uw site.

* Retourfrequentie: Gebruikt de de frequentiesafmeting van de [Terugkeer](/help/components/dimensions/return-frequency.md) .
* Terugkeerbezoeken: Trends the [Visits](/help/components/metrics/visits.md) metrisch over tijd met het Adobe-Geleverde segment van &quot;terugkeerbezoeken&quot;toegepast.
* Bezoek nummer: Hiermee gebruikt u de dimensie [Bezoek nummer](/help/components/dimensions/visit-number.md) .
* Verkoopcyclus: Map voor aankoopgerelateerde rapporten.
   * Klantenloyaliteit: Gebruikt de dimensie van de loyaliteit [van de](/help/components/dimensions/customer-loyalty.md) Klant.
   * Dagen vóór eerste aankoop: Gebruikt de [Dagen vóór eerste aankoop](/help/components/dimensions/days-before-first-purchase.md) dimensie.
   * Dagen sinds laatste aankoop: Gebruikt de [dagen sinds laatste aankoop](/help/components/dimensions/days-since-last-purchase.md) dimensie.
   * Dagelijkse unieke klanten: Trends [Daily unique bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte segment &#39;kopers&#39; toegepast.
   * Weekse unieke klanten: Trends [Weekelijks unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte segment &#39;kopers&#39; toegepast.
   * Unieke klanten per maand: Trends [Monthly unique bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte segment &#39;kopers&#39; toegepast.
   * Unieke klanten op kwartaalbasis: Trends [Driemaandelijkse unieke bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte segment &#39;kopers&#39; toegepast. Kwarten zijn januari-maart, april-juni, juli-september, en oktober-december.
   * Unieke klanten in het jaar: Trends [Yearly unique bezoekers](/help/components/metrics/unique-visitors.md) in de loop der tijd met het door Adobe verschafte segment &#39;kopers&#39; toegepast.

## Bezoekersprofiel

Bevat rapporten over wie uw plaats bezoekt.

* Geosegmentatie: Rapporten over waar op de wereld hits naar uw site vandaan komen.
   * Landen: Gebruikt de dimensie [Landen](/help/components/dimensions/countries.md) .
   * Regio: Gebruikt de dimensie [Regio](/help/components/dimensions/regions.md) .
   * Steden: Gebruikt de dimensie [Steden](/help/components/dimensions/cities.md) .
   * VS-staten: Gebruikt de [Amerikaanse](/help/components/dimensions/us-states.md) dimensie.
   * US DMA: Gebruikt de [dimensie DMA](/help/components/dimensions/us-dma.md) van de V.S.
* Talen: Gebruikt de dimensie [Taal](/help/components/dimensions/language.md) .
* Tijdzones: Gebruikt de dimensie van de tijdzone (gepensioneerd in Analysis Workspace). Dimensiewaarden zijn de GMT-verschuiving van de hit.
* Domein: Gebruikt de dimensie van het [Domein](/help/components/dimensions/domain.md) .
* Domein op hoofdniveau: Gebruikt de domeindimensie op het hoogste niveau (in Analysis Workspace niet meer beschikbaar). Het groepeert de [domeinen](/help/components/dimensions/domain.md) dimensie in hoger-niveaucategorieën, typisch door land van het domein.
* Technologie: Map met rapporten over wat de bezoeker heeft gebruikt om uw site te openen.
   * Browsers: Hiermee gebruikt u de dimensie [Browsers](/help/components/dimensions/browser.md) .
   * Browsertype: Hiermee gebruikt u de afmetingen voor het type [](/help/components/dimensions/browser-type.md) browser.
   * Breedte browser: Hiermee gebruikt u de breedte van de [browser, de geknipte](/help/components/dimensions/browser-width.md) afmeting.
   * Hoogte browser: Hiermee gebruikt u de [browserhoogte - geknipte](/help/components/dimensions/browser-height.md) afmeting.
   * Besturingssysteem: Gebruikt de dimensie [Besturingssystemen](/help/components/dimensions/operating-systems.md) .
   * Type besturingssysteem: Gebruikt de dimensie [Besturingssysteem](/help/components/dimensions/operating-system-types.md) .
   * Kleurdiepte monitor: Hierbij wordt de [kleurdiepte](/help/components/dimensions/color-depth.md) gebruikt.
   * Monitorresolutie: Hierbij wordt de resolutieafmeting van de [monitor](/help/components/dimensions/monitor-resolution.md) gebruikt.
   * Java: Gebruikt de dimensie [Java ingeschakeld](/help/components/dimensions/java-enabled.md) .
   * JavaScript: Gebruikt de voor JavaScript ingeschakelde dimensie (in Analysis Workspace afgebroken). Dimensiewaarden worden &#39;Enabled&#39;, &#39;Disabled&#39; of &#39;Unknown&#39; (Onbekend), afhankelijk van het feit of de browser JavaScript heeft ingeschakeld.
   * JavaScript-versie: gebruikt de JavaScript-versie-dimensie (in Analysis Workspace afgebroken). De waarden van de afmeting tonen de versie van JavaScript die browser gebruikt.
   * Cookies: Hiermee gebruikt u de [ondersteuningsdimensie](/help/components/dimensions/cookie-support.md) voor cookies.
   * Verbindingstypen: Gebruikt de het type [afmeting van de](/help/components/dimensions/connection-type.md) Verbinding.
   * Mobiele drager: Gebruikt de afmeting [Mobiele drager](/help/components/dimensions/mobile-dimensions.md) .
* Status bezoeker: Gebruikt de overheidsdimensie (gepensioneerd in Analysis Workspace). Dimensiewaarden komen voort uit de [`state`](../../implement/vars/page-vars/state.md) variabele.
* Postcode bezoeker: Hiermee wordt de [dimensie Postcode](/help/components/dimensions/zip-code.md) gebruikt.

## Aangepaste conversie

Bevat specifieke rapporten voor uw implementatie. Aangepaste omzettingsrapporten gebruiken [eVars](/help/components/dimensions/evar.md) als dimensie.

## Aangepast verkeer

Bevat specifieke rapporten voor uw implementatie. De het verkeersrapporten van de douane gebruiken [steunen](/help/components/dimensions/prop.md) als dimensie.

## Marketingkanalen

Bevat rapporten met betrekking tot [Marketing kanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* Rapport Kanaaloverzicht: Een speciaal aangepast rapport voor Rapporten en Analytics. Gebruikt marketingkanalen als dimensiewaarden, met meetwaarden die de eerste of laatste aanraakkenmerk gebruiken.
* Eerste aanraakkanaal: Hiermee gebruikt u de dimensie van het [eerste aanraakkanaal](/help/components/dimensions/first-touch-channel.md) .
* Details eerste aanraakkanaal: Hiermee gebruikt u de detaildimensie van het [eerste aanraakkanaal](/help/components/dimensions/first-touch-detail.md) .
* Laatste aanraakkanaal: Hiermee gebruikt u de dimensie van het [laatste aanraakkanaal](/help/components/dimensions/last-touch-channel.md) .
* Laatste aanraakkanaaldetails: Hiermee gebruikt u de detaildimensie van het [laatste aanraakkanaal](/help/components/dimensions/last-touch-detail.md) .

## Bladwijzers

Bevat rapporten die u met bladwijzer hebt gemarkeerd. See [Bookmarks](bookmarks.md) for more information.

## Dashboards

Bevat dashboards die u creeerde. See [Dashboards](dashboard.md) for more information.

## Targets

Bevat doelen die u hebt gemaakt. See [Targets](targets.md) for more information.

>[!NOTE]
>
>Als u uw rapport niet op deze hulppagina kunt vinden, is het mogelijk dat uw beheerder anders genoemd of aangepaste omslagen. Zie [Menu&#39;s aanpassen](/help/admin/admin/customize-menus.md) in de gebruikershandleiding voor Admin.
