---
title: Klantenloyaliteit
description: Categorieën gebaseerd op het aantal eerdere aankopen dat een bezoeker heeft gedaan.
feature: Dimensions
exl-id: 48ac1fdf-9a32-4bcc-8b23-bf58358a3470
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# Klantenloyaliteit

De dimensie &#39;Klantenloyaliteit&#39; rapporteert het aantal bezoekers van uw site dat 0 eerdere aankopen, 1 eerdere aankoop, 2 eerdere aankopen of 3+ eerdere aankopen heeft gedaan. Deze dimensie is handig als u wilt begrijpen hoe uw site het aankoopgedrag beïnvloedt. U kunt deze dimensie in een segment ook gebruiken om bezoekers die terugkeren om een aankoop te doen, te concentreren zodat u gelijkaardig gedrag voor nieuwe bezoekers kunt aanmoedigen.

## Deze dimensie vullen met gegevens

Deze dimensie wordt automatisch door Adobe gevuld op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) -gebeurtenis in uw implementatie. Als u de `purchase` op uw site werkt deze dimensie altijd.

## Dimension-items

Dimension-items zijn onder andere:

* **Geen klant**: Op het moment van de treffer heeft de bezoeker nog nooit een aankoop gedaan.
* **Nieuwe klanten**: Op het moment van de treffer heeft de bezoeker één aankoop gedaan.
* **Retourklanten**: Op het moment van de treffer heeft de bezoeker twee aankopen gedaan.
* **Kredietklanten**: Op het moment van de treffer heeft de bezoeker drie of meer aankopen gedaan.

Wanneer een bezoeker een aankoop doet (activeert de `purchase` (gebeurtenis), die hit en alle volgende hits gaan naar de volgende &quot;emmertje&quot;. Als een bezoeker bijvoorbeeld voor het eerst een product van uw site koopt, gaan deze van &quot;Geen klant&quot; naar &quot;Nieuwe klanten&quot;, met de bestelling &quot;Nieuwe klanten&quot;. Aan de dimensie-item &quot;Geen klant&quot; kunnen geen orders worden toegewezen.
