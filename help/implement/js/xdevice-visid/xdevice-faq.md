---
title: Veelgestelde vragen over de identificatie van bezoekers tussen apparaten
description: Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten
feature: Implementation Basics
exl-id: da972fee-fe6e-45b2-af01-50674989c375
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Veelgestelde vragen over de identificatie van bezoekers tussen apparaten

Veelgestelde vragen voor identificatie van bezoekers op verschillende apparaten.

**Wat is het verschil tussen de identificatie van de bezoeker van het apparaat en de Analytics van het Apparaat?**

De identificatie van bezoekers van verschillende apparaten gebruikt de `visitorID` variabele om apparaten aan elkaar te koppelen, met verscheidene belangrijke beperkingen. Een van de grootste beperkingen van deze identificatiemethode is dat niet-geverifieerde treffers worden geïsoleerd, tenzij het apparaat al is herkend. Deze ongeautoriseerde treffers kunnen het aantal unieke bezoekers doen toenemen.

Apparaatanalyse is de meest recente identificatiemethode voor bezoekers over het Adobe. De Experience Cloud ID-service en apparaatgrafiek worden gebruikt om bezoeken van verschillende apparaten met terugwerkende kracht aan elkaar te hechten. CDA vereist het gebruik van de `setCustomerIDs` om te bepalen welke apparaten door dezelfde bezoeker worden gebruikt.

**Hoe worden segmenten van de identificatiehandgrepen van de bezoeker van het apparaat gebruikt?**

De identificatie van bezoekers van verschillende apparaten behandelt segmenten gelijkaardig aan andere mogelijkheden. Het kijkt naar elke individuele treffer om te zien of past het de segmentcriteria aan, en omvat die klappen in uw gegevens als het aanpast. Segmenten die gebruikmaken van een bezoek en op bezoekers gebaseerde containers, bekijken nog steeds de bezoeker-id. Zorg ervoor dat uw implementatie de `visitorID` variabele waar mogelijk om unieke bezoekers consequent te identificeren voor segmentatie.
