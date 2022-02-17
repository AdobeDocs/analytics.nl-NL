---
title: Dagen sinds laatste aankoop
description: Het aantal dagen tussen de huidige treffer en de laatste aankoop die ze hebben gedaan.
feature: Dimensions
exl-id: 6f0d9d79-cf40-4de3-9d9f-9b1bc57f97b6
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Dagen sinds laatste aankoop

De dimensie &#39;Dagen sinds laatste aankoop&#39; meet de tijd die is verstreken tussen de huidige treffer van de bezoeker en de laatste aankoop op dat moment. Met deze dimensie krijgt u inzicht in het gedrag dat bezoekers maken nadat ze iets op uw site hebben aangeschaft.

Bezoekers die nog nooit iets hebben gekocht, vallen niet onder deze dimensie. Bovendien worden treffers die vóór de eerste aankoop van een bezoeker zijn gemaakt, ook niet opgenomen. Alleen treffers na de eerste aankoop van de bezoeker worden opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie wordt automatisch door Adobe gevuld op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) -gebeurtenis in uw implementatie. Als u de `purchase` op uw site werkt deze dimensie altijd.

## Dimension-items

Dimension-objecten bevatten het aantal dagen tussen de meest recente aankoop van een bezoeker en de huidige treffer. Elk aantal dagen is een apart item met een dimensie, waarbij &quot;Zelfde dag&quot; plaatsvindt waar de meest recente aankoop van een bezoeker en de huidige treffer op dezelfde dag hebben plaatsgevonden.
