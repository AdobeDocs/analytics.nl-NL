---
title: Aangepaste gebeurtenissen
description: Het aantal treffers waar een douanegebeurtenis bestaat.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Aangepaste gebeurtenissen

*Deze Help-pagina beschrijft hoe aangepaste gebeurtenissen werken als metrisch. Voor informatie over hoe de gebeurtenissen van de douane als implementatievariabele werken, zie [Overzicht van gebeurtenissen](/help/implement/vars/page-vars/events/events-overview.md) in de gebruikershandleiding Implementeren.*

Metrische gegevens van aangepaste gebeurtenissen geven het aantal resultaten weer waarop een bepaalde aangepaste gebeurtenis in een afbeeldingsaanvraag is ingesteld. Deze metriek is essentieel voor vele implementaties, aangezien zij inzicht aan gebeurtenissen verstrekken specifiek voor elke organisatie.

## Hoe deze metrische waarde wordt berekend

Aangepaste gebeurtenissen worden anders berekend, afhankelijk van het type. U kunt het gebeurtenistype controleren onder [Gebeurtenissen met succes](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) in de instellingen van de rapportsuite.

* **Gebeurtenissen tellen**: De standaardinstelling voor gebeurtenissen. De meeste gebeurtenissen zijn tellergebeurtenissen. Telt het aantal treffers waar de passende douanegebeurtenis `event1` - `event1000` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele.
* **Numerieke gebeurtenissen**: Hiermee wordt de numerieke waarde samengevat die aan de gebeurtenis is toegewezen in het dialoogvenster `events` variabele.
* **Valutapenheden**: Past valutaomrekening toe op de wisselkoers van die dag, dan sommen de numerieke waarde die aan elke treffer in `events` variabele.

Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met het accountteam van Adobe als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.

Adobe raadt u ten zeerste aan om op te nemen hoe u elke gebeurtenis in de [document ontwerp oplossing](/help/implement/prepare/solution-design.md).
