---
title: Gebeurtenissen van Page
description: Het aantal acties voor het bijhouden van koppelingen dat wordt geactiveerd.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Gebeurtenissen van Page

De metrische waarde &#39;Pagina-gebeurtenissen&#39; geeft het aantal keren weer dat een koppelingentraceringsaanroep is gemaakt. Deze maatstaf is handig wanneer u wilt weten welke pagina&#39;s de meest aantrekkelijke inhoud hebben. De meting voor deze metrische waarde is zeer waardevol wanneer een bezoeker een actie op de pagina kan uitvoeren zonder aan een nieuwe pagina te navigeren.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen alle verbinding volgende vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) in een rapportenpakket. Alle typen koppelingen zijn opgenomen (aangepaste koppelingen, downloadkoppelingen en afsluitkoppelingen). Het omvat geen vraag het volgen van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergelijken met vergelijkbare cijfers

* **Pagina-gebeurtenissen versus [Paginaweergaven](page-views.md)**: Pagina-gebeurtenissen tellen het aantal aanroepen voor het bijhouden van koppelingen (`tl()`) en sluit het bijhouden van aanroepen van paginaweergaven uit (`t()`). Paginaweergaven hebben het tegenovergestelde effect; het telt het aantal pagina mening het volgen vraag, en sluit verbindingen uit.
