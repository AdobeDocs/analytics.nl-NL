---
title: Veelgestelde vragen over de identificatie van bezoekers tussen apparaten
description: Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Veelgestelde vragen over de identificatie van bezoekers tussen apparaten

Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten.

**Wat is het verschil tussen de identificatie van de bezoeker van de overkoepelende apparaten en de Analytics van de overkoepelende apparaten?**

De identificatie van bezoekers tussen apparaten gebruikt de `visitorID` variabele om apparaten aan elkaar te koppelen, met verschillende belangrijke beperkingen. Een van de grootste beperkingen van deze identificatiemethode is dat niet-geverifieerde treffers worden geïsoleerd, tenzij het apparaat al is herkend. Deze ongeautoriseerde treffers kunnen het aantal unieke bezoekers doen toenemen.

Apparaatanalyse is de nieuwste identificatiemethode voor bezoekers op verschillende apparaten van Adobe. De Experience Cloud ID-service en apparaatgrafiek worden gebruikt om bezoeken van verschillende apparaten retroactief aan elkaar te koppelen. CDA vereist het gebruik van de `setCustomerIDs` functie om te bepalen welke apparaten door dezelfde bezoeker worden gebruikt.

**Hoe worden segmenten van de identificatiehandgrepen van de bezoeker van het apparaat gebruikt?**

De identificatie van bezoekers van verschillende apparaten behandelt segmenten gelijkaardig aan andere mogelijkheden. Het kijkt naar elke individuele treffer om te zien of past het de segmentcriteria aan, en omvat die klappen in uw gegevens als het aanpast. Segmenten die gebruikmaken van een bezoek en op bezoekers gebaseerde containers, bekijken nog steeds de bezoeker-id. Zorg ervoor dat uw implementatie waar mogelijk de `visitorID` variabele gebruikt om unieke bezoekers voor segmentatie consistent te identificeren.
