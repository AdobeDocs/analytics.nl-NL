---
description: De integratie van gegevensconnectors voor DFA gebruikt variabelen van de Analyse om DFA campagneresultaten te volgen.
keywords: DFA
title: Variabelen en gebeurtenissen analyseren
feature: Data Connectors
uuid: 8996cb58-c793-4600-99ef-af3064642b29
exl-id: 8c3df2e8-84cd-4a14-b15b-42233d874c19
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 3%

---

# Variabelen en gebeurtenissen analyseren{#analytics-variables-and-events}

De integratie van gegevensconnectors voor DFA gebruikt variabelen van de Analyse om DFA campagneresultaten te volgen.

Behalve de campagnevariabele, kunt u de Gebeurtenissen van Analytics en de Gebeurtenissen gebruiken die voor u zinvol zijn. Zodra u de gebeurtenis en eVars hebt geïdentificeerd om met deze integratie te gebruiken DFA, gebruik de Admin Console Analytics om hen toe te laten. De integratievariabelen moeten worden toegelaten alvorens de integratie DFA te activeren. In de volgende tabel worden de variabelen voor Analytics beschreven die nodig zijn voor de DFA-integratie.

| Variabele | Vriendschappelijke naam | Populatiemethode | Beschrijving |
|---|---|---|---|
| s.campagne of eVar | Code voor bijhouden van advertentie | Automatisch gevuld door gegevensconnector voor DFA-campagnes. | Volgt klikthrough omzettingen voor alle campagnes. |
| eVar* | Doorkijken | Automatisch ingevuld via VISTA en DFA voor DFA-campagnes. | Tracks view-through gegevens voor DFA IDs. Deze eVar moet dezelfde vervaldatum hebben als de variabele *`s.campaign`*. Moet dezelfde conversievariabele zijn als die in de ID van de Variabele provider wordt geïdentificeerd. Zorg ervoor dat de eVar volledige subrelaties heeft ingeschakeld. De kosten voor het inschakelen van deze functie maken deel uit van de integratiekosten voor gegevensconnectors |
| eVar* | Fouten in DFA-query | (Optioneel) Wordt gevuld met JavaScript-verzamelcode. | Bevat een van de verschillende foutcodes die door DFA worden geretourneerd. |
| gebeurtenis* | Aantal doorkijkers | Automatisch gevuld door gegevensconnector voor DFA-campagnes. | Hiermee legt u vast hoe vaak gebruikers een advertentie hebben bekeken, niet hebben geklikt, maar op uw site zijn aangekomen. |
| gebeurtenis* | Impressies | Automatisch gevuld via een gegevensfeed van DFA. | Tracks the number of time a specific DFA ad was gediend. |
| gebeurtenis* | Klikken | Automatisch gevuld via een gegevensfeed van DFA. | Volgt het aantal keren dat gebruikers op een specifieke DFA-banneradvertentie hebben geklikt. Deze metrische waarde kan verschillende aantallen in vergelijking met de inheemse metrische klikdoorhalingen van Analytics om één van verscheidene redenen veroorzaken. Zie [Metrische discrepanties combineren](/help/import/data-connectors/dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) voor meer informatie. |
| gebeurtenis* | DFA Timeouts | (Optioneel) Wordt gevuld met JavaScript-verzamelcode. | Telt het aantal keren dat DFA niet reageert vóór de *`s.maxDelay`* time-out. Dit kan u helpen bepalen als er een DFA implementatiekwestie is. |
| gebeurtenis* | DFA Media Kosten | Automatisch gevuld via een gegevensfeed van DFA. | Bevat de media kostenmetriek die in de interface DFA zijn ingevoerd. Deze functie moet zijn ingeschakeld aan de DFA-zijde om deze metriek weer te geven. |

*Selecteer een ongebruikte eVar of Aangepaste gebeurtenis.
