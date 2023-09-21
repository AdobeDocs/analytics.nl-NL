---
title: Aangepaste gebeurtenissen
description: Het aantal treffers waar een douanegebeurtenis bestaat.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Aangepaste gebeurtenissen

*Deze Help-pagina beschrijft hoe aangepaste gebeurtenissen werken als metrisch. Zie voor informatie over hoe aangepaste gebeurtenissen werken als een implementatievariabele [Overzicht van gebeurtenissen](/help/implement/vars/page-vars/events/events-overview.md) in de gebruikershandleiding Implementeren.*

Aangepaste gebeurtenis [cijfers](overview.md) toont het aantal treffers waar een bepaalde douanegebeurtenis in een beeldverzoek werd geplaatst. Deze metriek is essentieel voor vele implementaties, aangezien zij inzicht aan gebeurtenissen verstrekken specifiek voor elke organisatie.

## Hoe deze metrische waarde wordt berekend

Aangepaste gebeurtenissen worden anders berekend, afhankelijk van het type. U kunt het gebeurtenistype controleren onder [Gebeurtenissen met succes](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) in de instellingen van de rapportsuite.

* **Gebeurtenissen tellen**: De standaardinstelling voor gebeurtenissen. De meeste gebeurtenissen zijn tellergebeurtenissen. Telt het aantal treffers waar de passende douanegebeurtenis `event1` - `event1000` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele.
* **Numerieke gebeurtenissen**: Hiermee wordt de numerieke waarde samengevat die aan de gebeurtenis is toegewezen in het dialoogvenster `events` variabele.
* **Valutapenheden**: Past valutaomrekening toe op basis van de wisselkoers van die dag en sommen vervolgens de numerieke waarde op die aan elke treffer is toegewezen in het dialoogvenster `events` variabele.

Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met het accountteam van de Adobe als u niet zeker weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.

De Adobe adviseert sterk dat u registreert hoe u elke gebeurtenis in uw organisatie gebruikt [document ontwerp oplossing](/help/implement/prepare/solution-design.md).
