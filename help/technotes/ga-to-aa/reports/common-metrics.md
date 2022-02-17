---
title: Algemeen gebruikte metriek op andere platforms vertaalgids
description: Begrijp hoe te om metrische gegevens voor vele gemeenschappelijke rapporten te trekken gebruikend terminologie vertrouwd aan de gebruikers van Google Analytics.
feature: Third-party Integration
exl-id: e95b0530-8099-4a08-9e2b-75174546277d
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Algemeen gebruikte metriek op andere platforms vertaalgids

Op andere platforms zoals Google Analytics, delen vele rapporten een gemeenschappelijk aantal metriek. Gebruik deze pagina om te begrijpen hoe te om de metriek te ontspannen die in vele rapporten wordt gebruikt.

Als u meerdere metriek wilt toevoegen aan een tabel in vrije vorm voor een werkruimte, sleept u de metrische waarde uit het gebied met componenten naast de metrische koptekst in de werkruimte:

![Extra metrisch](/help/technotes/ga-to-aa/assets/new_metric.png)

## Verwervingsgegevens

**Gebruikers** is ongeveer gelijk aan **Unieke bezoekers** in Workspace. Zie de [Unieke bezoekers](/help/components/metrics/unique-visitors.md) In de gebruikershandleiding voor componenten vindt u meer informatie.

**Nieuwe gebruikers** kan worden verkregen door:

1. Sleep de **Unieke bezoekers** metrisch op de werkruimte.
2. Sleep de **Eerste bezoeken** segment boven de metrische koppen van Unieke bezoekers:

   ![Eerste bezoeken](../assets/first_time_visits.png)

**Sessies** is ongeveer gelijk aan **Bezoeken** in Analysis Workspace. Zie de [Bezoeken](/help/components/metrics/visits.md) In de gebruikershandleiding voor componenten vindt u meer informatie.

![Verwervingsgegevens](../assets/acquisition_metrics.png)

## Gedragmetriek

**Stuitsnelheid** gemakkelijk beschikbaar in Analysis Workspace als metrisch. Zie de [Stuitsnelheid](/help/components/metrics/bounce-rate.md) metrisch in de de gebruikersgids van Componenten voor extra informatie.

**Pagina&#39;s/sessie** is een berekende metrische waarde. Het kan worden verkregen door:

1. Als u deze berekende metrische waarde al hebt gemaakt, zoekt u deze onder Metrisch en sleept u deze naar de werkruimte.
2. Als u deze berekende metrisch nog niet hebt gecreeerd, klik **+** pictogram bij de metrische lijst om de Berekende Metrische Bouwer te openen.
3. Geef deze de titel &#39;Paginaweergaven per bezoek&#39; en desgewenst een beschrijving.
4. Stel de indeling in op Decimaal en stel het aantal decimalen in op 2.
5. Sleep de **Paginaweergaven** metrisch en **Bezoeken** in het definitiegebied.
6. De definitie ordenen zodat de formule **Paginaweergaven gedeeld door Bezoekopdrachten**.

   ![Paginaweergaven per bezoek](/help/technotes/ga-to-aa/assets/page_views_per_visit.png)

7. Klik op Opslaan om terug te gaan naar uw werkruimte.
8. Sleep de nieuw gedefinieerde berekende metrische waarde naar de werkruimte.

   Meer informatie over [Berekende cijfers](/help/components/c-calcmetrics/cm-overview.md) in de gebruikershandleiding van Componenten.

**Gem. Sessieduur** is ongeveer gelijk aan **Tijd besteed per bezoek (seconden)**. Meer informatie over [Tijd besteed per bezoek](/help/components/metrics/time-spent-per-visit.md) cijfers in de gebruikershandleiding van Componenten.

## Omzettingscijfers

**Omzetsnelheid doel**, **Goal Completions**, en **Waarde van doel** aanvullende implementatie op beide platforms vereisen. Als uw implementatie al ruimte biedt voor de productdimensie en de aankoopgebeurtenis, kunt u de volgende stappen uitvoeren:

1. Sleep de **Orders** metrisch, **Ontvangsten** metrisch, en **Bezoeken** metrisch op de werkruimte.
1. Een berekende metrische waarde maken van **Bestellingen per bezoek**. Gebruik Ctrl+klikken (Windows) of cmd+klikken (Mac) op beide metrische koppen om deze te markeren. Klik met de rechtermuisknop op een van de kopteksten en selecteer **Metrisch maken van selectie** en klik vervolgens op **Verdelen**. Deze nieuwe metrische waarde is gelijkaardig aan een Tarief van de Omzetting van het Doel.
1. Als decimalen nodig zijn, bewerkt u de Berekende metrisch. Klik op de knop Info in de metrische kop en vervolgens op het potloodpictogram. Voeg 1 of 2 Decimale Plaatsen in het Berekende Metrische venster van de Bouwer toe, dan klik sparen.

   ![Bestellingen per bezoek](/help/technotes/ga-to-aa/assets/orders_per_visit.png)

Als uw implementatie nog geen product- of conversiegegevens bevat, raadt Adobe aan om samen te werken met een implementatieconsultant om de kwaliteit en integriteit van de gegevens te garanderen.
