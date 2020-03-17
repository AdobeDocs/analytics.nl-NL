---
title: Verwerking en architectuurverschillen tussen analytische platforms
description: Leer hoe sommige gegevens worden verzameld en op verschillende platforms worden weergegeven, zoals Adobe Analytics en Google Analytics.
translation-type: tm+mt
source-git-commit: 757cea821bae49fabe819a65b921797070d328fc

---


# Verwerking en architectuurverschillen tussen analytische platforms

Hoewel Adobe Analytics en Google Analytics beide hulpprogramma&#39;s voor Analytics zijn, is de manier waarop gegevens worden verzameld en verwerkt tussen platforms zeer verschillend. Op deze pagina ziet u enkele belangrijke verschillen in de manier waarop bepaalde dimensies en metriek worden verzameld en waarom er verschillende getallen kunnen worden weergegeven in vergelijkbare rapporten.

## Stuitsnelheid

Bounce Rate is een veelgebruikte PKI die wordt gebruikt om de doeltreffendheid en de relevantie van landingspagina&#39;s in de meeste analysehulpmiddelen te meten. Dit wordt meestal gedefinieerd als bezoeken die de website binnenkomen maar geen klik naar een andere pagina bevatten.

* In Adobe Analytics wordt de Bounce Rate berekend aan de hand van de formule **Bounces gedeeld door Enter**.
* In Google Analytics wordt Bounce Rate berekend met de formule Sessions **voor één** pagina gedeeld door Sessies.

Op beide platforms geldt dat als meerdere hits tijdens hetzelfde bezoek of tijdens dezelfde sessie worden verzonden, dit niet als een stuit wordt beschouwd. In Adobe Analytics zijn aangepaste koppelingen beschikbaar en vaak voorkomende koppelingen, waardoor een bezoek niet als een stuit kan worden beschouwd. Google Analytics verzendt doorgaans niet meer dan één gegevensaanvraag op dezelfde pagina.

Voor een betere pariteit tussen de rapportagegereedschappen gebruikt u de maateenheid Bezoek één pagina in Adobe Analytics in plaats van Bounces als onderdeel van een berekende maatstaf. De meting Eén pagina bezoekt bevat het totale aantal bezoeken dat slechts een paginaweergave bevatte, of bezoeken die de website binnenkomen maar geen klik naar een andere pagina bevatten.

Zie de metrische [Stuitsnelheid](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) in de gebruikersgids van Componenten voor meer informatie.

## Bezoeken en sessies

Bezoeken (sessies in Google Analytics genoemd) zijn een groep paginaweergaven die in een korte tijd door dezelfde gebruiker worden gemaakt. Bezoeken op beide platforms verlopen doorgaans na 30 minuten inactiviteit. Beide platforms staan aanpassing toe wanneer een bezoek verloopt. Er zijn verscheidene scenario&#39;s die verschillen op elk platform kunnen veroorzaken.

* **Einde van de dag:** Alle sessies in Google Analytics verlopen na 23:59 uur op een bepaalde dag. Als de gebruiker na 12.00 uur nog steeds actief is op uw site, wordt een nieuwe sessie gemaakt. Adobe Analytics gaat de volgende dag door met een bezoek.
* **Verschillende campagnes:** Een nieuwe sessie in Google Analytics wordt gestart als de campagnebron van een gebruiker verandert. Als er een nieuwe waarde voor Trackingcode wordt weergegeven in Adobe Analytics, wordt deze waarde beschouwd als onderdeel van hetzelfde bezoek.
* **Handmatige sessieoverschrijving:** Een nieuwe sessie in Google Analytics wordt gestart als u een sessie handmatig start of beëindigt. `sessionControl` Bezoeken kunnen niet handmatig worden beëindigd in Adobe Analytics.
* **Detectie van eerdere bezoeken in Adobe Analytics:** Een nieuw bezoek aan Adobe Analytics wordt automatisch gestart als een gebruiker 12 uur aan ononderbroken activiteit bereikt, 2500 hits of 100 hits binnen 100 seconden. Elk van deze detectiecriteria wordt doorgaans geactiveerd door beide activiteiten.

Zie metrisch [Bezoekt](/help/components/c-variables/c-metrics/metrics-visit.md) in de de gebruikersgids van Componenten voor meer informatie.
