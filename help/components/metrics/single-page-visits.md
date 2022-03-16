---
title: Bezoeken op één pagina (cijfers)
description: Het aantal keren dat het item Pagina-afmeting niet is gewijzigd tijdens een bezoek.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 5%

---

# Eén pagina bezoeken

*In deze Help-pagina wordt beschreven hoe &#39;Bezoekingen van één pagina&#39; werken als metrisch. Zie de [Eén pagina bezoeken](../dimensions/single-page-visits.md) dimensie voor meer informatie.*

De [!UICONTROL Single page visits] metrisch toont het aantal bezoeken waar [Pagina](../dimensions/page.md) dimensie-item bevatte slechts één unieke waarde voor het gehele bezoek. Deze maatstaf is handig in de context van dimensies waar u korte bezoeken wilt zien, maar die niet zo streng van een regel hebben als [[!UICONTROL Bounces]](bounces.md) wel.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal bezoeken waar [!UICONTROL Page] dimensie-item bevatte slechts één unieke waarde voor het gehele bezoek. Als een bezoeker de pagina opnieuw laadt of koppelingsvolgvraag in brand steekt, telt het nog steeds als één enkel paginabezoek. Zodra de pagina-dimensie verandert in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als een enkele pagina-bezoek.

Zie [Enkelvoudige toegang](single-access.md) voor een vergelijking tussen de meetwaarden.

## Aantal herhalingen

Hiermee kunt u aangeven of herhalingsinstanties moeten worden geteld voor de rapportage. Zie voor meer informatie [Aantal herhalingen](/help/components/metrics/count-repeat-instances.md).