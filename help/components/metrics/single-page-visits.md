---
title: Eén pagina bezoeken
description: Het aantal keren dat het item Pagina-afmeting niet is gewijzigd tijdens een bezoek.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Eén pagina bezoeken

*In deze Help-pagina wordt beschreven hoe &#39;Bezoekingen van één pagina&#39; werken als metrisch. Zie de dimensie[Eén pagina bezoekt](../dimensions/single-page-visits.md)voor meer informatie.*

De metrische waarde &#39;Bezoeken van één pagina&#39; toont het aantal bezoeken waarbij het item [Pagina](../dimensions/page.md) -dimensie slechts één unieke waarde voor het volledige bezoek bevatte. Deze maatstaf is handig in het kader van dimensies waar u korte bezoeken wilt zien, maar die niet zo strenge regels hebben als [Bounces](bounces.md).

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal bezoeken waar het de afmetingspunt van de &quot;Pagina&quot;slechts één enkele unieke waarde voor het volledige bezoek bevatte. Als een bezoeker de pagina opnieuw laadt of koppelingsvolgvraag in brand steekt, telt het nog steeds als één enkel paginabezoek. Zodra de afmetingen van de pagina veranderen in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als een enkele paginabezoek.

Zie [Enige toegang](single-access.md) voor een vergelijking tussen metriek.
