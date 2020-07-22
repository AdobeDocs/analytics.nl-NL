---
title: Eenheden
description: Het totale aantal producten dat binnen alle bestellingen is aangeschaft.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Eenheden

De maatstaf &#39;Eenheden&#39; toont het totale aantal producten dat binnen alle bestellingen is aangeschaft. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze maatstaf combineren met elke gewenste dimensie om te zien welke maatitems hebben bijgedragen aan het aantal producten dat is aangeschaft. U kunt bijvoorbeeld de beste campagnes (met de dimensie [Code](../dimensions/tracking-code.md) bijhouden) of de belangrijkste interne zoektermen (met een [eVar](../dimensions/evar.md)) zien die een bijdrage leveren aan de aangeschafte producten.

## Hoe deze metrische waarde wordt berekend

Voor elke treffer waar `purchase` in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele bestaat, som het gebied van de &quot;Hoeveelheid&quot;binnen de [`products`](/help/implement/vars/page-vars/products.md) variabele.

## Bestellingen en eenheden vergelijken

Met de metrische [ordergegevens](orders.md) wordt alleen het aantal aankoopgebeurtenissen vastgelegd. De maatstaf &#39;Eenheden&#39; is doorgaans hoger dan &#39;Bestellingen&#39;, omdat klanten meerdere producten kunnen aanschaffen. In deze gevallen bestaat er één volgorde met meerdere eenheden.

Als u bestellingen hebt die hoger zijn dan eenheden, raadt Adobe aan de integriteit van uw implementatie te controleren. Het is waarschijnlijk dat de `products` variabele niet correct is ingesteld bij aankopen, wat normaal ongewenst gedrag is.
