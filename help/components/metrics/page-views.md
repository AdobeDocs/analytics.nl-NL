---
title: Paginaweergaven
description: Het aantal keer dat een pagina is weergegeven.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Paginaweergaven

De metrische weergave &#39;Paginaweergaven&#39; toont het aantal keren dat een bepaald dimensie-item op een pagina is ingesteld of aanwezig is. Het is één van de gemeenschappelijkste en basismetriek in rapporten.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen alle het volgen vraag van de paginamening ([`t()`](/help/implement/vars/functions/t-method.md)) in een rapportreeks. Voor dimensies omvat dit ook treffers waarbij een dimensie-item wordt gedefinieerd of blijvend wordt gemaakt. Het omvat geen verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Vergelijken met vergelijkbare cijfers

* **Paginaweergaven versus[bezoeken](visits.md)**: In de paginaweergaven wordt het aantal keer geteld dat een pagina wordt weergegeven. Bezoekingen tellen het aantal sessies voor bezoekers. Een bezoek bestaat uit een of meer pagina&#39;s.
* **Paginaweergaven versus[Pagina-gebeurtenissen](page-events.md)**: De meningen van de pagina tellen het aantal pagina mening het volgen vraag (`t()`), en sluit verbinding het volgen vraag (`tl()`) uit. Pagina-gebeurtenissen zijn het tegenovergestelde; het telt het aantal verbinding het volgen vraag, en sluit paginameningen uit.