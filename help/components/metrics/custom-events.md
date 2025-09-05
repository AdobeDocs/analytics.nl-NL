---
title: Aangepaste gebeurtenissen
description: Het aantal treffers waar een douanegebeurtenis bestaat.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Aangepaste gebeurtenissen

*Deze hulppagina beschrijft hoe de gebeurtenissen van de douane als metrisch werken. Voor informatie over hoe de douanegebeurtenissen als implementatievariabele werken, zie [ Overzicht van Gebeurtenissen ](/help/implement/vars/page-vars/events/events-overview.md) in de de gebruikersgids van het Voer.*

De metriek van de gebeurtenis van de douane [&#128279;](overview.md) toont het aantal treffers waar een bepaalde douanegebeurtenis in een beeldverzoek werd geplaatst. Deze metriek is essentieel voor vele implementaties, aangezien zij insight aan gebeurtenissen verstrekken specifiek voor elke organisatie.

## Hoe deze metrische waarde wordt berekend

Aangepaste gebeurtenissen worden anders berekend, afhankelijk van het type. U kunt het type van een gebeurtenis controleren onder [ gebeurtenissen van het Succes ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) in de reeksinstellingen van het Rapport.

* **gebeurtenissen van de Teller**: De standaardgebeurtenis die. De meeste gebeurtenissen zijn tellergebeurtenissen. Telt het aantal treffers waar de passende douanegebeurtenis `event1` - `event1000` in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele bestaat.
* **Numerieke gebeurtenissen**: vat de numerieke waarde samen die aan de gebeurtenis in de `events` variabele wordt toegewezen.
* **de gebeurtenissen van de Valuta**: Past valutaconversie op de wisselkoers van die dag toe, dan sommen de numerieke waarde die aan elke klap in de `events` variabele wordt toegewezen.

Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met uw Adobe-accountteam als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.

Adobe adviseert sterk dat u registreert hoe u elke gebeurtenis in het document van het de oplossingsontwerp van uw organisatie [&#128279;](/help/implement/prepare/solution-design.md) gebruikt.
