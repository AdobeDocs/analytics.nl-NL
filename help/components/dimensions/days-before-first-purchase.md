---
title: Dagen vóór eerste aankoop
description: Het aantal dagen tussen het eerste bezoek van een bezoeker en de eerste aankoop.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Dagen vóór eerste aankoop

De dimensie &#39;Dagen voor eerste aankoop&#39; geeft aan hoeveel dagen er verstrijken tussen de eerste keer dat een bezoeker uw site bereikt en het moment waarop hij een aankoop doet. Als een bezoeker bijvoorbeeld één dag na de eerste visite een aankoop doet, behoort een volgend bezoek of evenement tot het dimensie-item &quot;1 dag&quot;.

Nadat een bezoeker zijn eerste aankoop heeft gedaan, behoren ze tot hetzelfde dimensie-item voor de rest van de levensduur van het cookie van de bezoeker.

## Deze dimensie vullen met gegevens

Deze dimensie wordt automatisch door Adobe gevuld op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) -gebeurtenis in uw implementatie. Als u de `purchase` op uw site werkt deze dimensie altijd.

## Dimension-items

Dimension-objecten bevatten het aantal dagen tussen het eerste bezoek van een bezoeker aan uw site en de eerste aankoop. Elk aantal dagen is een apart onderdeel met een eigen dimensie, waarbij &quot;Zelfde dag&quot; plaatsvindt waar het eerste bezoek van een bezoeker en de eerste aankoop op dezelfde dag hebben plaatsgevonden.
