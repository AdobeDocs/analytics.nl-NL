---
title: producten
description: Gegevens verzenden over het product of de producten die worden weergegeven of in het winkelwagentje.
feature: Appmeasurement Implementation
exl-id: f26e7c93-f0f1-470e-a7e5-0e310ec666c7
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# producten

Met de variabele `products` worden producten en eigenschappen bijgehouden die aan de variabelen zijn gekoppeld. Deze variabele wordt doorgaans ingesteld op afzonderlijke productpagina&#39;s, winkelwagenpagina&#39;s en pagina&#39;s met aankoopbevestiging. Dit is een variabele met meerdere waarden. Dit betekent dat u meerdere producten in hetzelfde resultaat kunt verzenden en dat Adobe de waarde in afzonderlijke dimensie-items parseert.

>[!NOTE]
>
>Als deze variabele in een klap zonder de [`events`](events/events-overview.md) variabele wordt geplaatst, de [&#x200B; Metrische toename van de Meningen van het Product &#x200B;](/help/components/metrics/product-views.md) door 1. Zorg ervoor dat u de juiste gebeurtenissen instelt voor elke hit met de variabele `products` .

## Producten die het Web SDK gebruiken

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), worden de producten in kaart gebracht aan de volgende variabelen:

* Categorie is toegewezen aan `xdm.productListItems[].productCategories[].categoryID` . Het eerste item in de array `productCategories[]` wordt gebruikt. `lineItemId` wordt ook correct toegewezen, maar Adobe raadt `categoryID` aan omdat het standaard-XDM is. Als beide XDM-velden aanwezig zijn, heeft `lineItemId` voorrang.
* Het product wordt toegewezen aan `xdm.productListItems[].SKU` of `xdm.productListItems[].name`. Als beide XDM-velden aanwezig zijn, wordt `xdm.productListItems[].SKU` gebruikt.
* Aantal is toegewezen aan `xdm.productListItems[].quantity`.
* Prijs wordt toegewezen aan `xdm.productListItems[].priceTotal`.
* Merchandising eVars worden toegewezen aan `xdm.productListItems._experience.analytics.customDimensions.eVars.eVar1` to `xdm.productListItems._experience.analytics.customDimensions.eVars.eVar250` , afhankelijk van welke eVar u aan een product wilt binden.
* Merchandising-gebeurtenissen worden toegewezen aan `xdm.productListItems[]._experience.analytics.event1to100.event1.value` aan `xdm.productListItems._experience.analytics.event901to1000.event1000.value` , afhankelijk van de gebeurtenis die u aan een product wilt binden. Als u een gebeurtenis op één van deze gebieden plaatst, is het automatisch inbegrepen in het [&#x200B; gebeurtenis &#x200B;](events/events-overview.md) koord dat naar Adobe Analytics wordt verzonden.

```json
{
  "xdm": {
    "productListItems": [{
      "productCategories": [{
        "categoryID": "Men's"
      }],
      "name": "Hiking boot",
      "quantity": 1,
      "priceTotal": 49.99
    },
    {
      "productCategories": [{
        "categoryID": "Camping"
      }],
      "name": "Hunting blind",
      "quantity": 3,
      "priceTotal": 699.69
    }]
  }
}
```

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruikt de productvariabele `data.__adobe.analytics.products` na de syntaxis van AppMeasurement. Als u dit veld instelt, worden alle producten die in het XDM-object zijn ingesteld, overschreven en niet verzonden naar Adobe Analytics.

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "products": "Archery;Fletched arrow;12;159.99"
      }
    }
  }
}
```

## Producten die de extensie Adobe Analytics gebruiken

Er is geen specifiek veld in de gegevensverzameling van Adobe Experience Platform om deze variabele in te stellen. Er zijn echter meerdere extensies van derden voor hulp.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Extensions] en klik vervolgens op [!UICONTROL Catalog] om alle beschikbare extensies weer te geven.
4. Zoek naar de term &quot;product&quot;, die verscheidene uitbreidingen beschikbaar om te helpen plaatsen deze variabele openbaart.

U kunt een van deze extensies gebruiken, maar u kunt ook de aangepaste code-editor gebruiken die volgt op de syntaxis van AppMeasurement hieronder.

## s.products in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.products` is een tekenreeks die meerdere gescheiden velden per product bevat. Scheid elk gebied met een puntkomma (`;`) in het koord.

* **Categorie** (facultatief): De productcategorie. De maximumlengte voor dit veld is 100 bytes.
* **Naam van het Product** (vereist): De naam van het product. De maximumlengte voor dit veld is 100 bytes.
* **Hoeveelheid** (facultatief): Hoeveel van dit product in de kar is. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Prijs** (facultatief): De totale prijs van het product als decimaal. Indien meer dan één hoeveelheid is, de totale prijs en niet de individuele productprijs. Lijn de valuta van deze waarde uit zodat deze overeenkomt met de variabele [`currencyCode`](../config-vars/currencycode.md) . Plaats het valutasymbool niet in dit veld. Dit veld is alleen van toepassing op hits met de koopgebeurtenis.
* **Gebeurtenissen** (facultatief): Gebeurtenissen verbonden aan het product. Scheidt veelvoudige gebeurtenissen met een pijp (`|`). Zie [&#x200B; gebeurtenissen &#x200B;](events/events-overview.md) voor meer informatie.
* **eVars** (facultatief): het verhandelen van eVars verbonden aan het product. Scheidt veelvoudige handelende steunen met een pijp (`|`). Zie [&#x200B; handelend eVars &#x200B;](evar-merchandising.md) voor meer informatie.

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

Deze variabele ondersteunt meerdere producten in dezelfde hit. Het is waardevol voor winkelwagentjes en aankopen die meerdere producten bevatten. De maximumlengte voor de gehele `products` -tekenreeks is 64 kB. Scheid elk product met een komma (`,`) in het koord.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2;1;5.99";
```

>[!WARNING]
>
>Hiermee kunt u alle puntkomma&#39;s, komma&#39;s en pijpen van productnamen, categorieën en eVar-waarden voor handelsdoeleinden verwijderen. Als een productnaam een komma bevat, wordt deze door AppMeasurement geparseerd als het begin van een nieuw product. Door deze onjuiste parsering wordt de rest van de productreeks verwijderd, waardoor onjuiste gegevens in afmetingen en rapporten ontstaan.

## Voorbeelden

De variabele `products` is flexibel wanneer u velden weglaat en meerdere producten opneemt. Dankzij deze flexibiliteit kunt u gemakkelijk een scheidingsteken missen, waardoor uw implementatie onjuiste gegevens naar Adobe stuurt.

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

Als het gebruiken van de `digitalData` [&#x200B; gegevenslaag &#x200B;](../../prepare/data-layer.md), kunt u door de `digitalData.product` objecten serie herhalen:

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
