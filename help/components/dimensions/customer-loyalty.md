---
title: Klantenloyaliteit
description: Categorieën gebaseerd op het aantal eerdere aankopen dat een bezoeker heeft gedaan.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Klantenloyaliteit

De dimensie &#39;Klantenloyaliteit&#39; rapporteert het aantal bezoekers van uw site dat 0 eerdere aankopen, 1 eerdere aankoop, 2 eerdere aankopen of 3+ eerdere aankopen heeft gedaan. Deze dimensie is handig als u wilt begrijpen hoe uw site het aankoopgedrag beïnvloedt. U kunt deze dimensie in een segment ook gebruiken om bezoekers die terugkeren om een aankoop te doen, te concentreren zodat u gelijkaardig gedrag voor nieuwe bezoekers kunt aanmoedigen.

## Deze dimensie vullen met gegevens

Adobe vult deze dimensie automatisch in op basis van de [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) gebeurtenis in uw implementatie. Als u de `purchase` gebeurtenis op uw site implementeert, werkt deze dimensie altijd.

## Dimensie-items

Dimensie-items zijn onder andere:

* **Geen klant**: Op het moment van de treffer heeft de bezoeker nog nooit een aankoop gedaan.
* **Nieuwe klanten**: Op het moment van de treffer heeft de bezoeker één aankoop gedaan.
* **Retourklanten**: Op het moment van de treffer heeft de bezoeker twee aankopen gedaan.
* **Klanten** met goede naam: Op het moment van de treffer heeft de bezoeker drie of meer aankopen gedaan.

Wanneer een bezoeker een aankoop doet (de `purchase` gebeurtenis activeert), worden die hit en alle volgende treffers naar het volgende &quot;emmertje&quot; verplaatst. Als een bezoeker bijvoorbeeld voor het eerst een product van uw site koopt, gaan deze van &quot;Geen klant&quot; naar &quot;Nieuwe klanten&quot;, met de bestelling &quot;Nieuwe klanten&quot;. Aan de dimensie-item &quot;Geen klant&quot; kunnen geen orders worden toegewezen.
