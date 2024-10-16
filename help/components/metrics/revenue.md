---
title: Ontvangsten
description: Het monetaire bedrag van de producten die binnen alle orders worden aangekocht.
feature: Metrics
exl-id: a70e4d93-704b-46ac-9cec-31ea20d3dcb5
source-git-commit: a1fbd3f483d3a236fe5dc3246f5e90c1b3f51ba9
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Ontvangsten

De metrische &quot;Inkomsten&quot;[ ](overview.md) toont de monetaire hoeveelheid producten die binnen alle orden worden gekocht. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingspunten tot opbrengst droegen. Bijvoorbeeld, kon u de hoogste campagnes zien (gebruikend de [ het Volgen code ](../dimensions/tracking-code.md) dimensie) of hoogste interne onderzoekstermijnen (gebruikend een [ eVar ](../dimensions/evar.md)).

## Hoe deze metrische waarde wordt berekend

Voor elke hit waar `purchase` voorkomt in de [`events`](/help/implement/vars/page-vars/events/event-purchase.md) variabele, som het veld Prijs in de [`products`](/help/implement/vars/page-vars/products.md) variabele.

Deze metrisch baseert zich op de [ currencyCode ](/help/implement/vars/config-vars/currencycode.md) variabele als de munt op de pagina verschillend is dan de inheemse munt van de rapportreeks.
