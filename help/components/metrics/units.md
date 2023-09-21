---
title: Eenheden
description: Het totale aantal producten dat binnen alle bestellingen is aangeschaft.
feature: Metrics
exl-id: c7293445-0760-4237-83ae-812224ca6f4b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# Eenheden

De &#39;Eenheden&#39; [metrisch](overview.md) toont het totale aantal producten dat binnen alle bestellingen is aangeschaft. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze maatstaf combineren met elke gewenste dimensie om te zien welke maatitems hebben bijgedragen aan het aantal producten dat is aangeschaft. U kunt bijvoorbeeld de bovenste campagnes zien (met de [Code bijhouden](../dimensions/tracking-code.md) dimensie of hoogste interne zoektermen (met een [eVar](../dimensions/evar.md)) die heeft bijgedragen aan de aangekochte producten.

## Hoe deze metrische waarde wordt berekend

Voor elke hit waar `purchase` bestaat in de [`events`](/help/implement/vars/page-vars/events/events-overview.md) variabele, som van het veld &#39;Quantity&#39; in het veld [`products`](/help/implement/vars/page-vars/products.md) variabele.

## Bestellingen en eenheden vergelijken

De [Orders](orders.md) Met metrisch wordt alleen het aantal aankoopgebeurtenissen vastgelegd. De maatstaf &#39;Eenheden&#39; is doorgaans hoger dan &#39;Bestellingen&#39;, omdat klanten meerdere producten kunnen aanschaffen. In deze gevallen bestaat er één volgorde met meerdere eenheden.

Als u bestellingen hebt die hoger zijn dan eenheden, raadt de Adobe aan de integriteit van uw implementatie te controleren. Het is waarschijnlijk dat uw `products` De variabele wordt niet correct ingesteld bij aankopen, wat doorgaans ongewenst gedrag is.
