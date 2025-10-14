---
title: Eenheden
description: Het totale aantal producten dat binnen alle bestellingen is aangeschaft.
feature: Metrics
exl-id: c7293445-0760-4237-83ae-812224ca6f4b
source-git-commit: a1fbd3f483d3a236fe5dc3246f5e90c1b3f51ba9
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Eenheden

De metrische &quot;Eenheden&quot; [&#128279;](overview.md) toont het totale aantal producten die binnen alle orden worden gekocht. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingspunten aan hoeveel producten bijdroegen werden gekocht. Bijvoorbeeld, kon u de hoogste campagnes zien (gebruikend de [&#x200B; het Volgen code &#x200B;](../dimensions/tracking-code.md) afmeting) of hoogste interne onderzoekstermijnen (gebruikend een [&#x200B; eVar &#x200B;](../dimensions/evar.md)) die tot gekochte producten bijdroeg.

## Hoe deze metrische waarde wordt berekend

Voor elke hit waar `purchase` voorkomt in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele, som het veld &#39;Quantity&#39; in de [`products`](/help/implement/vars/page-vars/products.md) variabele.

## Bestellingen en eenheden vergelijken

[&#x200B; orden &#x200B;](orders.md) metrisch registreert slechts het aantal aankoopgebeurtenissen. De maatstaf &#39;Eenheden&#39; is doorgaans hoger dan &#39;Bestellingen&#39;, omdat klanten meerdere producten kunnen aanschaffen. In deze gevallen bestaat er één volgorde met meerdere eenheden.

Als u bestellingen hebt die hoger zijn dan eenheden, raadt de Adobe aan de integriteit van uw implementatie te controleren. Het is waarschijnlijk dat de variabele `products` niet correct is ingesteld bij aankopen, wat doorgaans ongewenst is.
