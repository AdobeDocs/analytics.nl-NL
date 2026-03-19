---
title: Bezoeken op één pagina (cijfers)
description: Het aantal keren dat het item Pagina-afmeting niet is gewijzigd tijdens een bezoek.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 6d2c278c5525c89b73c39bbfcedbe644806bf989
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Eén pagina bezoeken

*Deze hulppagina beschrijft hoe de &quot;Enige paginabezoeken&quot;als metrisch werken. Zie [ Enige paginabezoeken ](../dimensions/single-page-visits.md) afmeting voor meer informatie.*

**[!UICONTROL Single page visits]** [ metrisch ](overview.md) toont het aantal bezoeken waar het [ pagina ](../dimensions/page.md) afmetingspunt slechts één enkele waarde voor het volledige bezoek bevatte. Deze maatstaf is handig in de context van afmetingen waarin u korte bezoeken wilt zien, maar die niet zo streng zijn als [[!UICONTROL Bounces]](bounces.md) .

## Hoe deze metrische waarde wordt berekend

De definitie van deze metrische waarde is afhankelijk van de projectinstelling [[!UICONTROL Count repeat instances]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings) :

* **[!UICONTROL Count repeat instances]enabled**: Telt het aantal bezoeken waar de [!UICONTROL Page] dimensie één enkele waarde voor het bezoek bevatte. Als een bezoeker de pagina opnieuw laadt, wordt deze als een enkele pagina van het bezoek uitgesloten.
* **[!UICONTROL Count repeat instances]disabled**: Telt het aantal bezoeken waar de [!UICONTROL Page] -dimensie één unieke waarde voor het volledige bezoek bevatte.

Ongeacht het &quot;[!UICONTROL Count repeat instances]&quot;project het plaatsen, volgt dit metrisch aan de volgende regels:

* Een bezoek komt nog steeds in aanmerking als een bezoeker één pagina bezoekt wanneer een bezoeker aanroepen voor het bijhouden van koppelingen activeert (de [!UICONTROL Page] -dimensie wordt verwijderd van alle aanroepen voor het bijhouden van koppelingen).
* Zodra de [!UICONTROL Page] -dimensie verandert in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als een enkele pagina.

Zie [ Enige toegang ](single-access.md) voor een vergelijking tussen metriek.
