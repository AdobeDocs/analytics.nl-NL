---
title: Gebeurtenissen van Page
description: Het aantal acties voor het bijhouden van koppelingen dat wordt geactiveerd.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Gebeurtenissen van Page

De gebeurtenissen &#39;Page&#39; [metrisch](overview.md) toont het aantal tijden om het even welke verbinding het volgen vraag werd gemaakt. Deze maatstaf is handig wanneer u wilt weten welke pagina&#39;s de meest aantrekkelijke inhoud hebben. De meting voor deze metrische waarde is zeer waardevol wanneer een bezoeker een actie op de pagina kan uitvoeren zonder aan een nieuwe pagina te navigeren.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen allen [Aanroepen voor het bijhouden van koppelingen (`tl()`)](/help/implement/vars/functions/tl-method.md) in een rapportenpakket. Alle typen koppelingen zijn opgenomen (aangepaste koppelingen, downloadkoppelingen en afsluitkoppelingen). Het omvat niet: [Aanroepen voor bijhouden van paginaweergave (`t()`)](/help/implement/vars/functions/t-method.md).

## Vergelijken met vergelijkbare cijfers

* **Pagina-gebeurtenissen vs. [Paginaweergaven](page-views.md)**: Pagina-gebeurtenissen tellen het aantal aanroepen voor het bijhouden van koppelingen (`tl()`) en sluit het bijhouden van aanroepen van paginaweergaven uit (`t()`). Paginaweergaven zijn het tegenovergestelde; het telt het aantal opvolgende aanroepen voor paginaweergave en sluit koppelingen uit.
