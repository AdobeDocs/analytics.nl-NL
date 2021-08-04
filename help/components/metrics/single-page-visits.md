---
title: Eén pagina bezoeken
description: Het aantal keren dat het item Pagina-afmeting niet is gewijzigd tijdens een bezoek.
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 98463103e6e2ba19d11629d40dacc0c02f5b33c9
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# Eén pagina bezoeken

*In deze Help-pagina wordt beschreven hoe &#39;Bezoekingen van één pagina&#39; werken als metrisch. Zie de [Single page visit](../dimensions/single-page-visits.md) dimensie voor meer informatie.*

De [!UICONTROL Single page visits] metrisch toont het aantal bezoeken waar [Pagina](../dimensions/page.md) afmetingspunt slechts één enkele unieke waarde voor het volledige bezoek bevatte. Deze metrische waarde is handig in de context van afmetingen waarin u korte bezoeken wilt zien, maar niet zo streng van een regel als [[!UICONTROL Bounces]](bounces.md).

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt het aantal bezoeken waar het [!UICONTROL Page] afmetingspunt slechts één enkele unieke waarde voor het volledige bezoek bevatte. Als een bezoeker de pagina opnieuw laadt of koppelingsvolgvraag in brand steekt, telt het nog steeds als één enkel paginabezoek. Zodra de pagina-dimensie verandert in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als een enkele pagina-bezoek.

Zie [Enkelvoudige toegang](single-access.md) voor een vergelijking tussen metriek.

## Aantal herhalingen

Hiermee kunt u aangeven of herhalingsinstanties moeten worden geteld voor de rapportage. Zie [Herhalingsinstanties tellen](/help/components/metrics/count-repeat-instances.md) voor meer informatie.