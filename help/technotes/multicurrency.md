---
description: Beschrijft hoe te om doelvalutacodes voor multi-muntsteun te bepalen om te werken.
title: Ondersteuning voor meerdere valuta's
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: f659d1bde361550928528c7f2a70531e3ac88047
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# Ondersteuning voor meerdere valuta&#39;s

Adobe biedt meerdere conversieniveaus voor valuta, zodat uw organisatie in veel rapporten de gewenste valuta kan behalen. Conversie gebeurt op drie niveaus:

## Paginaniveau

U kunt de [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) variabele om de gewenste valuta op elke pagina in te stellen. Als de valuta op de pagina niet overeenkomt met de valuta van de doelrapportsuite, voert Adobe op basis van de wisselkoers van de huidige dag een valutaomrekening uit naar de valuta van de rapportsuite. De omgezette valuta wordt geregistreerd.

## Niveau van rapportsuite

Elk rapportpakket bevat een **basisvaluta**. Deze valuta dicteert de context van alle valuta metriek (zoals [Ontvangsten](/help/components/metrics/revenue.md)). Alle opgeslagen valutagegevens bevinden zich in de basisvaluta van de rapportsuite.

## Gebruikersniveau

Voor Rapporten &amp; Analytics, kunnen de gebruikers een verschillende valuta plaatsen dan de basisvaluta van de rapportreeks onder [Rapportinstellingen](/help/analyze/reports-analytics/report-settings.md). Deze instelling is niet-destructief, wat betekent dat de onderliggende gegevens niet worden gewijzigd. In plaats daarvan past zij de basisvalutaomrekening toe op alle verslagen die worden bekeken op basis van de huidige wisselkoers. Als u hetzelfde rapport op verschillende dagen weergeeft, kunnen de getallen veranderen als gevolg van verschillende dagelijkse wisselkoersen.

Analysis Workspace biedt momenteel geen valutaconversie op gebruikersniveau.
