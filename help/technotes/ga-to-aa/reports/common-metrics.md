---
title: Algemeen gebruikte metriek op andere platforms vertaalgids
description: Begrijp hoe u metrische gegevens voor veel voorkomende rapporten kunt ophalen met gebruik van terminologie die beter bekend is bij Google Analytics-gebruikers.
translation-type: tm+mt
source-git-commit: ''

---


# Algemeen gebruikte metriek op andere platforms vertaalgids

Op andere platforms, zoals Google Analytics, delen veel rapporten een gemeenschappelijk aantal metriek. Gebruik deze pagina om te begrijpen hoe te om de metriek te ontspannen die in vele rapporten wordt gebruikt.

Als u meerdere metriek wilt toevoegen aan een tabel in vrije vorm voor een werkruimte, sleept u de metrische waarde uit het gebied met componenten naast de metrische koptekst in de werkruimte:

![Extra metrisch](/help/technotes/ga-to-aa/assets/new_metric.png)

## Verwervingsgegevens

**Gebruikers** zijn ongeveer gelijk aan **Unieke bezoekers** in Workspace. Raadpleeg de metrische waarde voor [Unieke bezoekers](/help/components/c-variables/c-metrics/metrics-unique-visitors.md) in de gebruikershandleiding voor componenten voor meer informatie.

**Nieuwe gebruikers** kunnen worden verkregen door:

1. Sleep de metrische waarde van de **unieke bezoekers** naar de werkruimte.
2. Sleep het segment **Eerste bezoeken** boven de metrische koppen van Unieke bezoekers:

   ![Eerste bezoeken](../assets/first_time_visits.png)

**Sessies** zijn ongeveer gelijk aan **bezoeken** in de analysewerkruimte. Raadpleeg de metrische informatie over [bezoeken](/help/components/c-variables/c-metrics/metrics-visit.md) in de gebruikershandleiding van Componenten voor meer informatie.

![Verwervingsgegevens](../assets/acquisition_metrics.png)

## Gedragmetriek

**De Stuitsnelheid** is gemakkelijk beschikbaar in de Werkruimte van de Analyse als metrisch. Zie de metrische [Stuitsnelheid](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) in de gebruikersgids van Componenten voor extra informatie.

**Pagina&#39;s/sessie** is een berekende metrische waarde. Het kan worden verkregen door:

1. Als u deze berekende metrische waarde al hebt gemaakt, zoekt u deze onder Metrisch en sleept u deze naar de werkruimte.
2. Als u deze berekende metrische waarde nog niet hebt gecreeerd, klik het **+** pictogram dichtbij de metrische lijst om de Berekende Metrische Bouwer te openen.
3. Geef deze de titel &#39;Paginaweergaven per bezoek&#39; en desgewenst een beschrijving.
4. Stel de indeling in op Decimaal en stel het aantal decimalen in op 2.
5. Sleep de metrische weergave **van de** paginaweergaven en **Bezoek** -metrisch naar het definitiegebied.
6. Rangschik de definitie zodat de formule **Paginaweergaven gedeeld door Bezoekopdrachten** is.

   ![Paginaweergaven per bezoek](/help/technotes/ga-to-aa/assets/page_views_per_visit.png)

7. Klik op Opslaan om terug te gaan naar uw werkruimte.
8. Sleep de nieuw gedefinieerde berekende metrische waarde naar de werkruimte.

   Meer informatie over [berekende meetgegevens](/help/components/c-variables/c-metrics/calculated-metric.md) vindt u in de gebruikershandleiding voor componenten.

**Gem. De duur** van de zitting is ongeveer gelijk aan **Tijd die per Bezoek (seconden)** wordt uitgegeven. Meer informatie over de metriek van de [Tijd](/help/components/c-variables/c-metrics/metrics-time-spent.md) in de de gebruikersgids van Componenten.

## Omzettingscijfers

**Het Tarief** van de Omzetting van het doel, de Voltooiingen **van het** Doel, en de Waarde **van het** Doel vereisen extra implementatie op beide platforms. Als uw implementatie al ruimte biedt voor de productdimensie en de aankoopgebeurtenis, kunt u de volgende stappen uitvoeren:

1. Sleep metrische **Orden** , de metrische **Opbrengst** , en de metrische **Bezoekingen** op de werkruimte.
1. Maak een berekende metrische waarde voor **bestellingen per bezoek**. Gebruik Ctrl+klikken (Windows) of cmd+klikken (Mac) op beide metrische koppen om deze te markeren. Klik met de rechtermuisknop op een van de kopteksten, selecteer Metrisch **maken van selectie** en klik op **Splitsen**. Deze nieuwe metrische waarde is gelijkaardig aan een Tarief van de Omzetting van het Doel.
1. Als decimalen nodig zijn, bewerkt u de Berekende metrisch. Klik op de knop Info in de metrische kop en vervolgens op het potloodpictogram. Voeg 1 of 2 Decimale Plaatsen in het Berekende Metrische venster van de Bouwer toe, dan klik sparen.

   ![Bestellingen per bezoek](/help/technotes/ga-to-aa/assets/orders_per_visit.png)

Als uw implementatie nog geen gegevens over producten of conversie bevat, raadt Adobe aan samen te werken met een implementatieconsultant om de kwaliteit en integriteit van de gegevens te garanderen.
