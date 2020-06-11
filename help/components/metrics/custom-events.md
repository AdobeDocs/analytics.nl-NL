---
title: Aangepaste gebeurtenissen
description: Het aantal treffers waar een douanegebeurtenis bestaat.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Aangepaste gebeurtenissen

*Deze Help-pagina beschrijft hoe aangepaste gebeurtenissen werken als metrisch. Voor informatie over hoe de douanegebeurtenissen als implementatievariabele werken, zie het overzicht[van](/help/implement/vars/page-vars/events/events-overview.md)Gebeurtenissen in de de gebruikersgids van het Uitvoeren.*

Metrische gegevens van aangepaste gebeurtenissen geven het aantal resultaten weer waarop een bepaalde aangepaste gebeurtenis in een afbeeldingsaanvraag is ingesteld. Deze metriek is essentieel voor vele implementaties, aangezien zij inzicht aan gebeurtenissen verstrekken specifiek voor elke organisatie.

## Hoe deze metrische waarde wordt berekend

Aangepaste gebeurtenissen worden anders berekend, afhankelijk van het type. U kunt het type van een gebeurtenis controleren onder [Gebeurtenissen](../../admin/admin/c-success-events/success-event.md) van het Succes in de montages van de Reeks van het Rapport.

* **Gebeurtenissen** tellen: De standaardinstelling voor gebeurtenissen. De meeste gebeurtenissen zijn tellergebeurtenissen. Telt het aantal treffers waar de passende douanegebeurtenis `event1` - in de `event1000` [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele bestaat.
* **Numerieke gebeurtenissen**: Hiermee wordt de numerieke waarde samengevat die aan de gebeurtenis in de `events` variabele is toegewezen.
* **Valutagebeurten**: Past valutaomrekening toe op de wisselkoers van die dag, dan sommen de numerieke waarde die aan elke treffer in de `events` variabele wordt toegewezen.

Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met de accountmanager van uw organisatie als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.

Adobe raadt u ten zeerste aan om in het [oplossingsontwerpdocument](/help/implement/prepare/solution-design.md)van uw organisatie op te nemen hoe u elke gebeurtenis gebruikt.
