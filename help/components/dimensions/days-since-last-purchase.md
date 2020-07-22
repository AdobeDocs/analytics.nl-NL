---
title: Dagen sinds laatste aankoop
description: Het aantal dagen tussen de huidige treffer en de laatste aankoop die ze hebben gedaan.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Dagen sinds laatste aankoop

De dimensie &#39;Dagen sinds laatste aankoop&#39; meet de tijd die is verstreken tussen de huidige treffer van de bezoeker en de laatste aankoop op dat moment. Met deze dimensie krijgt u inzicht in het gedrag dat bezoekers maken nadat ze iets op uw site hebben aangeschaft.

Bezoekers die nog nooit iets hebben gekocht, vallen niet onder deze dimensie. Bovendien worden treffers die vóór de eerste aankoop van een bezoeker zijn gemaakt, ook niet opgenomen. Alleen treffers na de eerste aankoop van de bezoeker worden opgenomen.

## Deze dimensie vullen met gegevens

Adobe vult deze dimensie automatisch in op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) gebeurtenis in uw implementatie. Als u de `purchase` gebeurtenis op uw site implementeert, werkt deze dimensie altijd.

## Dimensie-items

Dimensie-items bevatten het aantal dagen tussen de meest recente aankoop van een bezoeker en de huidige treffer. Elk aantal dagen is een apart item met een dimensie, waarbij &quot;Zelfde dag&quot; plaatsvindt waar de meest recente aankoop van een bezoeker en de huidige treffer op dezelfde dag hebben plaatsgevonden.
