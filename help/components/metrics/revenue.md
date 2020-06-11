---
title: Ontvangsten
description: Het monetaire bedrag van de producten die binnen alle orders worden aangekocht.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Ontvangsten

De maatstaf &quot;Opbrengsten&quot; toont de monetaire hoeveelheid producten die binnen alle orders worden aangekocht. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingswaarden aan opbrengst droegen. U kunt bijvoorbeeld de bovenste campagnes (met de dimensie [Code](../dimensions/tracking-code.md) bijhouden) of de hoogste interne zoektermen (met een [eVar](../dimensions/evar.md)) zien.

## Hoe deze metrische waarde wordt berekend

Voor elke hit waar `purchase` de [`events`](/help/implement/vars/page-vars/events/event-purchase.md) variabele voorkomt, som het veld Prijs binnen de [`products`](/help/implement/vars/page-vars/products.md) variabele.

Deze maatstaf is afhankelijk van de [currencyCode](/help/implement/vars/config-vars/currencycode.md) -variabele als de valuta op de pagina anders is dan de native valuta van de rapportsuite.
