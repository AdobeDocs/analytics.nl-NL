---
title: Paginaweergaven
description: Het aantal keren dat een dimensie-item in Adobe Analytics is ingesteld of blijvend is.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---

# Paginaweergaven

De **[!UICONTROL Page views]** [metrisch](overview.md) toont het aantal tijden dat een bepaald afmetingspunt werd geplaatst of op een pagina voortgeduurd. Het is één van de gemeenschappelijkste en basismetriek in rapporten.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle het volgen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)) in een rapportenpakket. Voor dimensies omvat het treffers waar een afmetingspunt wordt geplaatst of voortgeduurd. Het omvat geen verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) of gegevens van [Gegevensbronnen](/help/import/data-sources/overview.md).

## Vergelijken met vergelijkbare cijfers

* **Paginaweergaven versus [Bezoeken](visits.md)**: Paginaweergaven tellen het aantal keren dat een pagina wordt weergegeven. Bezoekingen tellen het aantal sessies voor bezoekers. Een bezoek bestaat uit een of meer paginaweergaven.
* **Paginaweergaven versus [Gebeurtenissen van Page](page-events.md)**: Paginaweergaven tellen het aantal aanroepen voor het bijhouden van paginaweergaven (`t()`), en sluit verbinding het volgen vraag ( uit`tl()`). De gebeurtenissen van de pagina zijn het tegenovergestelde; zij tellen het aantal verbinding het volgen vraag, en sluiten paginamening het volgen vraag uit.
