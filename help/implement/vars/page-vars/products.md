---
title: products
description: Gegevens verzenden over het product of de producten die worden weergegeven of in het winkelwagentje.
feature: Variables
exl-id: f26e7c93-f0f1-470e-a7e5-0e310ec666c7
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# producten

De `products` met variabele tracks kunt u producten en eigenschappen bijhouden die aan deze producten zijn gekoppeld. Deze variabele wordt doorgaans ingesteld op afzonderlijke productpagina&#39;s, winkelwagenpagina&#39;s en pagina&#39;s met aankoopbevestiging. Dit is een variabele met meerdere waarden. Dit betekent dat u meerdere producten in dezelfde hit kunt verzenden en dat Adobe de waarde parseert in verschillende dimensieitems.

>[!NOTE]
>
>Als deze variabele wordt ingesteld in een hit zonder de opdracht [`events`](events/events-overview.md) variabele, de [Productweergaven](/help/components/metrics/product-views.md) metrische stappen met 1. Zorg ervoor dat u de juiste gebeurtenissen instelt voor elke hit met de knop `products` variabele.

## Producten die SDK van het Web gebruiken

Producten zijn [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder verschillende XDM-velden:

* Categorie is toegewezen aan `productListItems[].name`.
* Product is toegewezen aan `productListItems[]._id`.
* Aantal is toegewezen aan `productListItems[].quantity`.
* Prijs is toegewezen aan `productListItems[].priceTotal`.
* Merchandising eVars worden toegewezen aan `productListItems._experience.analytics.customDimensions.eVars.eVar1` tot `productListItems._experience.analytics.customDimensions.eVars.eVar250`, afhankelijk van welke eVar u aan een product wilt binden.
* Merchandising-gebeurtenissen worden toegewezen aan `productListItems[]._experience.analytics.event1to100.event1.value` tot `productListItems._experience.analytics.event901to1000.event1000.value`, afhankelijk van welke gebeurtenis u aan een product wilt binden.

## Producten die de extensie Adobe Analytics gebruiken

Er is geen specifiek veld in Adobe Experience Platform Data Collection om deze variabele in te stellen; er zijn echter meerdere extensies van derden die u helpen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] tab, en klik vervolgens op [!UICONTROL Catalog] om alle beschikbare extensies weer te geven.
4. Zoek naar de term &quot;product&quot;, die verscheidene uitbreidingen beschikbaar om te helpen plaatsen deze variabele openbaart.

U kunt één van deze uitbreidingen gebruiken, of u kunt de redacteur van de douanecode gebruiken na syntaxis AppMeasurement hieronder.

## s.products in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.products` variabele is een tekenreeks die meerdere gescheiden velden per product bevat. Elk veld scheiden met een puntkomma (`;`) in de tekenreeks.

* **Categorie** (optioneel): De productcategorie. De maximumlengte voor dit veld is 100 bytes.
* **Productnaam** (vereist): De naam van het product. De maximumlengte voor dit veld is 100 bytes.
* **Aantal** (optioneel): Hoeveel van dit product zit in de kar. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Prijs** (optioneel): De totale prijs van het product als decimaal. Indien meer dan één hoeveelheid is, de totale prijs en niet de individuele productprijs. De valuta van deze waarde aanpassen aan de [`currencyCode`](../config-vars/currencycode.md) variabele. Plaats het valutasymbool niet in dit veld. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Gebeurtenissen** (optioneel): Gebeurtenissen die aan het product zijn gekoppeld. Meerdere gebeurtenissen scheiden met een pipe (`|`). Zie [gebeurtenissen](events/events-overview.md) voor meer informatie .
* **eVars** (optioneel): Merchandising eVars gekoppeld aan het product. Meerdere handelsmerken scheiden met een pipe (`|`). Zie [merchandising Vars](evar-merchandising.md) voor meer informatie .

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Deze variabele ondersteunt meerdere producten in dezelfde hit. Het is waardevol voor winkelwagentjes en aankopen die meerdere producten bevatten. De maximumlengte voor de gehele `products` string is 64K. Elk product scheiden met een komma (`,`) in de tekenreeks.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2;1;5.99";
```

>[!WARNING]
>
>Hiermee kunt u alle puntkomma&#39;s, komma&#39;s en eVar uit productnamen, categorieën en waarden voor het wijzigen van handelswaarden verwijderen. Als een productnaam een komma bevat, parseert AppMeasurement deze als het begin van een nieuw product. Door deze onjuiste parsering wordt de rest van de productreeks verwijderd, waardoor onjuiste gegevens in afmetingen en rapporten ontstaan.

## Voorbeelden

De `products` variabele is flexibel wanneer velden worden weggelaten en meerdere producten worden opgenomen. Dankzij deze flexibiliteit kunt u gemakkelijk een scheidingsteken missen, waardoor uw implementatie onjuiste gegevens naar Adobe stuurt.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product 1,;Example product 2";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = ";Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = ";Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = ";Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = ";Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = ";Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md), kunt u door `digitalData.product` objectarray:

```js
for(var i = 0; i < digitalData.product.length; i++) {
    // Add individual product info to the product string
    s.products += digitalData.product[i].category.primaryCategory + ";" + digitalData.product[i].productInfo.productName;
    // If there are more products, add a comma
    if(i != digitalData.product.length - 1) {
        s.products += ",";
    }
}
```
