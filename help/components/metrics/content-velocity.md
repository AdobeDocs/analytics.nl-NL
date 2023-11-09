---
title: Contentsnelheid
description: Met Inhoudssnelheid wordt het effect van de inhoud op de downstreaminhoud gemeten.
feature: Metrics
exl-id: 8ba54990-ff7d-4693-92de-7f9d9f916b55
source-git-commit: 26e166e065df90cb327fe1106542e17831069141
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# Contentsnelheid

Met de berekende metrische waarde &#39;Inhoudssnelheid&#39; kunt u meten hoe een dimensie (doorgaans [[!UICONTROL Page]](/help/components/dimensions/page.md)) helpt gebruikers tijd te besteden aan uw website of app.

Dit metrische gebruik [Deelnametoewijzing](/help/analyze/analysis-workspace/attribution/models.md) op de [Paginaweergaven](page-views.md) metrisch als deel van zijn berekening. Met de deelname Bezoek krijgt u, telkens wanneer een pagina wordt geraakt, ook creditering voor alle pagina&#39;s die eerder tijdens hetzelfde bezoek zijn geraakt. Deze formule houdt doorgaans in dat hoe eerder een pagina tijdens een bezoek wordt geraakt, hoe meer creditering wordt ontvangen. (Zie [Paginaweergaven (deelname) | Bezoek) of &quot;Bezoek deelname&quot;](#page-views-participation--visit-or-visit-participation) voor meer informatie .)

## Berekening

&#39;Inhoudssnelheid&#39; is een standaard berekende snelheid [metrisch](overview.md) en wordt de formule gebruikt `Page views (Visit participation)` gedeeld door `Visits`.

![](assets/cont-velo-1.png)

## Algemeen gebruik

[!UICONTROL Content Velocity] wordt vaak gebruikt in inhoudsanalyse naast andere belangrijke meetgegevens zoals [!UICONTROL Page Views], [!UICONTROL Visits], en [!UICONTROL Bounce Rate].

![](assets/cont-velo-3.png)

## Voorbeeld

In het volgende voorbeeld worden de twee delen van Inhoudssnelheid gesplitst: &#39;Paginaweergaven (deelname) | Visit)&quot; en &quot;Visit&quot;.

### Paginaweergaven (deelname) | Bezoek) of &quot;Bezoek deelname&quot;

Bekijk het volgende voorbeeld van de invloed van de deelname aan Visit op de toewijzing:

Op een website bezoekt een gebruiker de volgende pagina&#39;s in deze volgorde:

* Pagina A
* Pagina B
* Pagina C
* Pagina D

In het bovenstaande voorbeeld ontvangt pagina A studiepunten voor 4 treffers, pagina B voor 3 treffers, pagina C voor 2 treffers en pagina D voor 1 treffers.

In het volgende voorbeeld wordt hetzelfde principe geïllustreerd, maar sommige pagina&#39;s worden meerdere keren bezocht.

* Pagina A
* Pagina B
* Pagina C
* Pagina B
* Pagina D
* Pagina A

In het bovenstaande voorbeeld ontvangt pagina A studiepunten voor 7 hits, pagina B voor 8 hits, pagina C voor 4 controles en pagina D voor 2 controles.

### Bezoeken

Nadat de deelname aan het bezoek is berekend, wordt het resultaat gedeeld door het aantal bezoeken.
