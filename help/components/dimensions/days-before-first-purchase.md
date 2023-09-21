---
title: Dagen vóór eerste aankoop
description: Het aantal dagen tussen het eerste bezoek van een bezoeker en de eerste aankoop.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Dagen vóór eerste aankoop

De &#39;Dagen voor eerste aankoop&#39; [dimensie](overview.md) meldt het aantal dagen dat verstrijkt tussen de eerste keer dat een bezoeker uw site bereikt en het moment dat hij of zij een aankoop doet. Als een bezoeker bijvoorbeeld één dag na de eerste visite een aankoop doet, behoort een volgend bezoek of evenement tot het dimensie-item &quot;1 dag&quot;.

Nadat een bezoeker zijn eerste aankoop heeft gedaan, behoren ze tot hetzelfde dimensie-item voor de rest van de levensduur van het cookie van de bezoeker.

## Deze dimensie vullen met gegevens

Deze Adobe wordt automatisch aangepast op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) -gebeurtenis in uw implementatie. Als u de `purchase` op uw site werkt deze dimensie altijd.

## Dimension-items

Dimensionen bevatten het aantal dagen tussen het eerste bezoek van een bezoeker aan uw site en de eerste aankoop. Elk aantal dagen is een apart onderdeel met een eigen dimensie, waarbij &quot;Zelfde dag&quot; plaatsvindt waar het eerste bezoek van een bezoeker en de eerste aankoop op dezelfde dag hebben plaatsgevonden.
