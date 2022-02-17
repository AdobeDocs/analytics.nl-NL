---
title: Omzet
description: Het monetaire bedrag van de producten die binnen alle orders worden aangekocht.
feature: Metrics
exl-id: a70e4d93-704b-46ac-9cec-31ea20d3dcb5
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# Omzet

De maatstaf &quot;Opbrengsten&quot; toont de monetaire hoeveelheid producten die binnen alle orders worden aangekocht. Deze maatstaf is van essentieel belang voor eCommerce-sites bij het meten van de conversie. U kunt deze metrisch met om het even welke afmeting combineren om te zien welke afmetingspunten aan opbrengst droegen. U kunt bijvoorbeeld de bovenste campagnes zien (met de [Code bijhouden](../dimensions/tracking-code.md) dimensie of hoogste interne zoektermen (met een [eVar](../dimensions/evar.md)).

## Hoe deze metrische waarde wordt berekend

Voor elke hit waar `purchase` bestaat in de [`events`](/help/implement/vars/page-vars/events/event-purchase.md) variabele, som het veld Prijs in het veld [`products`](/help/implement/vars/page-vars/products.md) variabele.

Deze metrische waarde is afhankelijk van de [currencyCode](/help/implement/vars/config-vars/currencycode.md) variabele als de valuta op de pagina anders is dan de native valuta van de rapportsuite.
