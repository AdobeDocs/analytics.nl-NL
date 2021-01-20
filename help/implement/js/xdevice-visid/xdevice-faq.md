---
title: Veelgestelde vragen over de identificatie van bezoekers tussen apparaten
description: Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# Veelgestelde vragen over de identificatie van bezoekers tussen apparaten

Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten.

**Wat is het verschil tussen de identificatie van de bezoeker van het apparaat en de Analytics van het Apparaat?**

De identificatie van bezoekers tussen apparaten gebruikt de `visitorID` variabele om apparaten samen te binden, met verscheidene belangrijke beperkingen. Een van de grootste beperkingen van deze identificatiemethode is dat niet-geverifieerde treffers worden geïsoleerd, tenzij het apparaat al is herkend. Deze ongeautoriseerde treffers kunnen het aantal unieke bezoekers doen toenemen.

Apparaatanalyse is de meest recente identificatiemethode voor bezoekers over het Adobe. De Experience Cloud ID-service en apparaatgrafiek worden gebruikt om bezoeken van verschillende apparaten met terugwerkende kracht aan elkaar te hechten. CDA vereist het gebruik van de functie `setCustomerIDs` om te bepalen welke apparaten door de zelfde bezoeker worden gebruikt.

**Hoe worden segmenten van de identificatiehandgrepen van de bezoeker van het apparaat gebruikt?**

De identificatie van bezoekers van verschillende apparaten behandelt segmenten gelijkaardig aan andere mogelijkheden. Het kijkt naar elke individuele treffer om te zien of past het de segmentcriteria aan, en omvat die klappen in uw gegevens als het aanpast. Segmenten die gebruikmaken van een bezoek en op bezoekers gebaseerde containers, bekijken nog steeds de bezoeker-id. Zorg ervoor uw implementatie `visitorID` variabele waar mogelijk gebruikt om unieke bezoekers voor segmentatie constant te identificeren.
