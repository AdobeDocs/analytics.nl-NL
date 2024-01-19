---
description: Beschrijft hoe te om doelvalutacodes voor multi-muntsteun te bepalen om te werken.
title: Ondersteuning voor meerdere valuta's
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: 99156dd9d898ce0abf214561cb0040c647d7e6ab
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Ondersteuning voor meerdere valuta&#39;s

Adobe biedt meerdere conversieniveaus voor valuta, zodat uw organisatie in veel rapporten de gewenste valuta kan behalen. Conversie gebeurt op drie niveaus:

## Paginaniveau

U kunt de [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) variabele om de gewenste valuta op elke pagina in te stellen. Als de valuta op de pagina niet de munt van de reeks van het bestemmingsrapport aanpast, voert de Adobe een muntomzetting in de munt van de rapportreeks uit die op de wisselkoers van de huidige dag wordt gebaseerd. De omgezette valuta wordt geregistreerd.

## Niveau van rapportsuite

Elk rapportpakket bevat een **basisvaluta**. Deze valuta dicteert de context van alle valuta metriek (zoals [Ontvangsten](/help/components/metrics/revenue.md)). Alle opgeslagen valutagegevens bevinden zich in de basisvaluta van de rapportsuite.

