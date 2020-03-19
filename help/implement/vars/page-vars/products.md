---
title: producten
description: Gegevens verzenden over het product of de producten die worden weergegeven of in het winkelwagentje.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# producten

De `products` variabele houdt producten en eigenschappen bij die aan hen worden gebonden. Deze variabele wordt doorgaans ingesteld op afzonderlijke productpagina&#39;s, winkelwagenpagina&#39;s en pagina&#39;s met aankoopbevestiging. Dit is een variabele met meerdere waarden. Dit betekent dat u meerdere producten in dezelfde hit kunt verzenden en dat Adobe de waarde parseert in afzonderlijke waarden voor dimensies.

> [!NOTE] Als deze variabele in een hit zonder een winkelwagentgebeurtenis in de [`events`](events/events-overview.md) variabele wordt geplaatst, metrische verhogingen van de &quot;Weergaven van het Product&quot;met 1. Zorg ervoor dat u bij elke treffer de juiste winkelwagentgebeurtenis instelt.

## Producten in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele in te stellen. er zijn echter meerdere extensies van derden die u helpen.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik [!UICONTROL Catalog] om alle beschikbare extensies weer te geven.
4. Zoek naar de term &quot;product&quot;, die verscheidene uitbreidingen beschikbaar om te helpen plaatsen deze variabele openbaart.

U kunt één van deze uitbreidingen gebruiken, of u kunt de redacteur van de douanecode gebruiken na syntaxis AppMeasurement hieronder.

## s.products in AppMeasurement en Launch de redacteur van de douanecode

De `s.products` variabele is een tekenreeks die meerdere gescheiden velden per product bevat. Elk afzonderlijk product kan tot 100 bytes over alle gebieden bevatten. Scheid elk veld met een puntkomma (`;`) in de tekenreeks.

* **Categorie** (optioneel): De overkoepelende productcategorie. Uw organisatie bepaalt hoe producten in categorieën worden gegroepeerd.
* **Productnaam** (verplicht): De naam van het product.
* **Hoeveelheid** (facultatief): Hoeveel van dit product zit in de kar. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Prijs** (optioneel): De totale prijs van het product als decimaal. Indien meer dan één hoeveelheid is, de totale prijs en niet de individuele productprijs. Lijn de valuta van deze waarde uit zodat deze overeenkomt met de [`currencyCode`](../config-vars/currencycode.md) variabele. Plaats het valutasymbool niet in dit veld. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Gebeurtenissen** (optioneel): Gebeurtenissen die aan het product zijn gekoppeld. Maak meerdere gebeurtenissen gescheiden met een pipe (`|`). Zie [gebeurtenissen](events/events-overview.md) voor meer informatie.
* **eVars** (optioneel): Merchandising eVars gekoppeld aan het product. Meerdere merchandising Vars scheiden met een pipe (`|`). Zie [Verkopen Vars](../../../components/c-variables/c-merch-variables/var-merchandising.md) voor meer informatie.

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Deze variabele ondersteunt meerdere producten in dezelfde hit. Het is waardevol voor winkelwagentjes en aankopen die meerdere producten bevatten. Terwijl er een grens 100 byte per product is, is de totale lengte voor de `products` variabele 64K. Scheid elk product met een komma (`,`) in de tekenreeks.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2,1,5.99";
```

> [!IMPORTANT] Strip alle puntkomma&#39;s, komma&#39;s en pijpen van productnamen, categorieën en merchandising eVar-waarden. Als een productnaam een komma bevat, parseert AppMeasurement deze als het begin van een nieuw product. Door deze onjuiste parsering wordt de rest van de productreeks verwijderd, waardoor onjuiste gegevens in afmetingen en rapporten ontstaan.

## Voorbeelden

De `products` variabele is flexibel wanneer velden worden weggelaten en meerdere producten worden opgenomen. Dankzij deze flexibiliteit kunt u gemakkelijk een scheidingsteken missen, waardoor uw implementatie onjuiste gegevens naar Adobe stuurt.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name if you do not want to use product category
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product,;Example product";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = "Example category;Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = "Example category;Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = "Example category 1;Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = "Example category;Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = "Example category;Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```
