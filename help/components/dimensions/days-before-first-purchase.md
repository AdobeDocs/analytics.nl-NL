---
title: Dagen vóór eerste aankoop
description: Het aantal dagen tussen het eerste bezoek van een bezoeker en de eerste aankoop.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Dagen vóór eerste aankoop

De dimensie &#39;Dagen voor eerste aankoop&#39; geeft aan hoeveel dagen er verstrijken tussen de eerste keer dat een bezoeker uw site bereikt en het moment waarop hij een aankoop doet. Als een bezoeker bijvoorbeeld één dag na de eerste visite een aankoop doet, behoort een volgend bezoek of evenement tot het dimensie-item &quot;1 dag&quot;.

Nadat een bezoeker zijn eerste aankoop heeft gedaan, behoren ze tot hetzelfde dimensie-item voor de rest van de levensduur van het cookie van de bezoeker.

## Deze dimensie vullen met gegevens

Adobe vult deze dimensie automatisch in op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) gebeurtenis in uw implementatie. Als u de `purchase` gebeurtenis op uw site implementeert, werkt deze dimensie altijd.

## Dimensie-items

Dimension-items bevatten het aantal dagen tussen het eerste bezoek van een bezoeker aan uw site en de eerste aankoop. Elk aantal dagen is een apart onderdeel met een eigen dimensie, waarbij &quot;Zelfde dag&quot; plaatsvindt waar het eerste bezoek van een bezoeker en de eerste aankoop op dezelfde dag hebben plaatsgevonden.
