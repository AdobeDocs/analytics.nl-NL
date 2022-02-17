---
title: 'Metrische uitleg van paginaweergaven | Adobe Analytics '
description: Leer hoe de pagina metrisch weergeeft in Adobe Analytics en begrijp ook het verschil tussen paginaweergaven en bezoeken.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Meer informatie over paginaweergaven met Adobe Analytics

De metrische weergave &#39;Paginaweergaven&#39; toont het aantal keren dat een bepaald dimensie-item op een pagina is ingesteld of aanwezig is. Het is één van de gemeenschappelijkste en basismetriek in rapporten.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle het volgen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)) in een rapportenpakket. Voor dimensies omvat dit ook treffers waarbij een dimensie-item wordt gedefinieerd of blijvend wordt gemaakt. Het omvat geen verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Vergelijken met vergelijkbare cijfers

* **Paginaweergaven versus [Bezoeken](visits.md)**: In de paginaweergaven wordt het aantal keer geteld dat een pagina wordt weergegeven. Bezoekingen tellen het aantal sessies voor bezoekers. Een bezoek bestaat uit een of meer pagina&#39;s.
* **Paginaweergaven versus [Gebeurtenissen van Page](page-events.md)**: Paginaweergaven tellen het aantal aanroepen voor het bijhouden van paginaweergaven (`t()`), en sluit verbinding het volgen vraag ( uit`tl()`). Pagina-gebeurtenissen zijn het tegenovergestelde; het telt het aantal verbinding het volgen vraag, en sluit paginameningen uit.
