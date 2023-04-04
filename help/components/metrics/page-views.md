---
title: Paginaweergaven
description: Het aantal keren dat een dimensie-item is ingesteld of geduurd in Adobe Analytics.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 1be9a8ceb03f8102a0799f4518db35c1e8cd7b14
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# Paginaweergaven

De metrische weergave &#39;Paginaweergaven&#39; toont het aantal keren dat een bepaald dimensie-item op een pagina is ingesteld of aanwezig is. Het is één van de gemeenschappelijkste en basismetriek in rapporten.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle het volgen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)) in een rapportenpakket. Voor dimensies, omvat het klusjes waar een afmeting punt wordt bepaald of voortgeduurd. Het omvat geen verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) of gegevens uit samenvatting [Gegevensbronnen](/help/import/data-sources/overview.md).

## Vergelijken met vergelijkbare cijfers

* **Paginaweergaven versus [Bezoeken](visits.md)**: Paginaweergaven tellen het aantal keer dat een pagina wordt weergegeven. Bezoekingen tellen het aantal sessies voor bezoekers. Een bezoek bestaat uit een of meer paginaweergaven.
* **Paginaweergaven versus [Gebeurtenissen van Page](page-events.md)**: Paginaweergaven tellen het aantal aanroepen voor het bijhouden van paginaweergaven (`t()`), en sluit verbinding het volgen vraag ( uit`tl()`). Pagina-gebeurtenissen zijn het tegenovergestelde; zij tellen het aantal verbinding het volgen vraag, en sluiten pagina mening het volgen vraag uit.
