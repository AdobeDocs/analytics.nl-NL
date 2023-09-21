---
title: Aanmelden voor toestemmingsbeheer
description: Zie welke privacy-instellingen een bezoeker heeft ingeschakeld.
exl-id: b2768180-b763-41fb-8cba-665fac047e29
feature: Dimensions
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---

# Aanmelden voor toestemmingsbeheer

De optie &#39;Inschakelen voor beheer van toestemming&#39; [dimensie](overview.md) geeft aan welke privacy-instellingen een bezoeker heeft gekozen. U kunt deze dimensie gebruiken om gegevens te filteren op basis van privacy-instellingen, of de meest gebruikelijke redenen voor privacy-aanmelding bekijken.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van het volgende [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['opt.dmp']` wanneer ingesteld op `Y`. Indien `opt.dmp` equals `N`de [Afmelden voor beheer van toestemming](cm-opt-out.md) in plaats daarvan wordt de dimensie gevuld.
* `contextData.['opt.sell']` wanneer ingesteld op `Y`. Indien `opt.sell` equals `N`de [Afmelden voor beheer van toestemming](cm-opt-out.md) in plaats daarvan wordt de dimensie gevuld.

Uw organisatie bepaalt de logica om deze variabelen van contextgegevens uit te voeren. Ze blijven niet behouden na de hit waarop ze zijn ingesteld. U moet dus elke variabele van de contextgegevens op elke pagina instellen.

## Dimension-items

Items van het Dimension bevatten de volgende twee waarden:

* **`DMP`**: De bezoeker heeft ervoor gekozen om gegevens te delen naar gegevenbeheer-platforms. Deze dimensie-item is aanwezig wanneer de variabele van de contextgegevens `opt.dmp` equals `Y`.
* **`SELL`**: De bezoeker heeft ervoor gekozen de gegevens te delen of aan derden te verkopen. Deze dimensie is aanwezig wanneer de variabele contextgegevens `opt.sell` equals `Y`.
