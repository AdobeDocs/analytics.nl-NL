---
title: Gebeurtenissen van Page
description: Het aantal acties voor het bijhouden van koppelingen dat wordt geactiveerd.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 205d86b13046bd17e321734904bf57435ef6e106
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Gebeurtenissen van Page

De gebeurtenissen &#39;Page&#39; [metrisch](overview.md) toont het aantal tijden om het even welke verbinding het volgen vraag werd gemaakt. Deze maatstaf is handig wanneer u wilt weten welke pagina&#39;s de meest aantrekkelijke inhoud hebben. De meting voor deze metrische waarde is zeer waardevol wanneer een bezoeker een actie op de pagina kan uitvoeren zonder aan een nieuwe pagina te navigeren.

In een doorsnee reis van een eCommerce-site kan een bezoeker bijvoorbeeld verschillende interacties uitvoeren op één pagina. Een typische implementatie Analytics heeft deze interactie gevormd als verbinding het volgen ([`tl()`](/help/implement/vars/functions/tl-method.md)) aanroepen, terwijl een paginaweergave ([`t()`](/help/implement/vars/functions/t-method.md)) is gereserveerd voor het eerste laden van de pagina. Deze implementatiemethode biedt verrijkte gebeurtenistracering die inzicht biedt in welke interacties plaatsvinden voordat een bezoeker zijn reis voortzet.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen alle verbinding volgende vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) in een rapportenpakket. Alle verbindingstypes zijn inbegrepen in dit metrisch, specifiek [Aangepaste koppelingen](../dimensions/custom-link.md), [Koppelingen downloaden](../dimensions/download-link.md), en [Koppelingen afsluiten](../dimensions/exit-link.md). Het omvat geen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergelijken met vergelijkbare cijfers

* **Pagina-gebeurtenissen vs. [Paginaweergaven](page-views.md)**: Pagina-gebeurtenissen tellen het aantal aanroepen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)) en sluit het bijhouden van aanroepen van paginaweergaven uit ([`t()`](/help/implement/vars/functions/t-method.md)). Paginaweergaven zijn het tegenovergestelde; het telt het aantal opvolgende aanroepen voor paginaweergave en sluit koppelingen uit.
