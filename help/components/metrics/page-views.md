---
title: Paginaweergaven
description: Het aantal keren dat een dimensie-item in Adobe Analytics is ingesteld of blijvend is.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# Paginaweergaven

De **[!UICONTROL Page views]** [metrisch](overview.md) toont het aantal tijden een bepaald afmetingspunt (afmetingswaarde) werd bepaald of voortgeduurd (d.w.z. wanneer het verloopt) op een pagina. Het is één van de gemeenschappelijkste en basismetriek in rapporten.

Bijvoorbeeld de [!UICONTROL Days of Week] De dimensie bestaat uit de volgende dimensieitems: zondag, maandag, dinsdag, woensdag, donderdag, vrijdag en zaterdag.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle het volgen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)) in een rapportenpakket. Voor dimensies, omvat het klusjes waar een afmeting punt wordt bepaald of voortgeduurd. Het omvat geen verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) of gegevens uit samenvatting [Gegevensbronnen](/help/import/data-sources/overview.md).

## Vergelijken met vergelijkbare cijfers

* **Paginaweergaven versus [Bezoeken](visits.md)**: Paginaweergaven tellen het aantal keer dat een pagina wordt weergegeven. Bezoekingen tellen het aantal sessies voor bezoekers. Een bezoek kan uit een of meer paginaweergaven bestaan.
* **Paginaweergaven versus [Gebeurtenissen van Page](page-events.md)**: Paginaweergaven tellen het aantal aanroepen voor het bijhouden van paginaweergaven (`t()`), en sluit verbinding het volgen vraag ( uit`tl()`). De gebeurtenissen van de pagina zijn het tegenovergestelde; zij tellen het aantal verbinding het volgen vraag, en sluiten paginamening het volgen vraag uit.
