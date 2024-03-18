---
title: eVar (variabele Verkoop)
description: Aangepaste variabelen die aan afzonderlijke producten zijn gekoppeld.
feature: Variables
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# eVar (merchandising)

*Deze Help-pagina beschrijft hoe u handelsversies van eVars kunt implementeren. Voor informatie over hoe het verhandelen van eVars als dimensie werkt, zie [eVars (Merchandising-dimensie)](/help/components/dimensions/evar-merchandising.md) in de gebruikershandleiding van Componenten.*

Zie voor een gedetailleerde discussie over de werking van eVars op handelsgebied [Verkoop- en productzoekmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html).

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor dat u de eVar aan de gewenste syntaxis in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

>[!WARNING]
>
>Het niet correct configureren van merchandising Vars leidt tot onverwachte waarden of gegevensverlies voor de variabele. Zorg ervoor het correct voor uw implementatie wordt gevormd.

## Implementeren met behulp van productsyntaxis

Wanneer &#39;Productsyntaxis&#39; is ingeschakeld, wordt de categorie Verkoop direct in het dialoogvenster `products` variabele, dus het is niet nodig een bindingsgebeurtenis te selecteren en in te stellen. Dit is de aanbevolen methode en moet worden gebruikt, tenzij de waarde niet beschikbaar is om in te stellen in `products` wanneer de succesgebeurtenis plaatsvindt.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

De waarde voor `eVar1` wordt toegewezen aan het product. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden aan de waarde eVar gecrediteerd.

### Productsyntaxis met de Web SDK

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md) Handelsvariabelen voor productsyntaxis gebruiken de volgende XDM-velden:

* ProductsyntaxisbewerkingseVars worden toegewezen onder `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar1` tot `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar250`.
* Handelsgerelateerde gebeurtenissen in de productsyntaxis worden toegewezen onder `xdm.productListItems[]._experience.analytics.event1to100.event1.value` tot `xdm.productListItems[]._experience.analytics.event901to1000.event1000.value`. [Serienummering voor gebeurtenissen](events/event-serialization.md) XDM-velden worden toegewezen onder `xdm.productListItems[]._experience.analytics.event1to100.event1.id` tot `xdm.productListItems[]._experience.analytics.event901to1000.event1000.id`.

>[!NOTE]
>
>Wanneer u gebeurtenissen instelt onder `productListItems`, hoeft u deze niet in te stellen in de gebeurtenistekenreeks. Wanneer deze op beide plaatsen zijn ingesteld, heeft de waarde in de gebeurtenistekenreeks voorrang.

In het volgende voorbeeld wordt één [product](products.md) het gebruik van meerdere handelsstromen en gebeurtenissen:

```json
"productListItems": [
  {
    "name": "Bahama Shirt",
    "priceTotal": "12.99",
    "quantity": 3,
    "_experience": {
      "analytics": {
        "customDimensions" : {
          "eVars" : {
            "eVar10" : "green",
            "eVar33" : "large"
          }
        },
        "event1to100" : {
          "event4" : {
            "value" : 1
          },
          "event10" : {
            "value" : 2,
            "id" : "abcd"
          }
        }
      }
    }
  }
]
```

Het bovenstaande voorbeeldobject wordt naar Adobe Analytics verzonden als `";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"`.

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md), gebruik van eVar `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` volgende AppMeasurement syntaxis.

## Implementeren met syntaxis van conversievariabelen

De Syntaxis van de Veranderlijke van de Omzetting wordt gebruikt wanneer de waarde van de eVar niet beschikbaar aan reeks in `products` variabele. Dit scenario betekent doorgaans dat de pagina geen context heeft van het kanaal voor handelsdoeleinden of de zoekmethode. In deze gevallen stelt u de variabele merchandising in voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens configuratie wordt geselecteerd voorkomt, wordt de persisted waarde van de eVar geassocieerd met het product. Als `prodView` wordt opgegeven als de bindingsgebeurtenis, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een eVar bijwerken die al aan een product is toegewezen.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

De waarde `"Aviary"` for `eVar1` is toegewezen aan het product `"Canary"`. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden gecrediteerd aan `"Canary"`. Bovendien is de huidige waarde van de variabele voor handelsdoeleinden aan alle volgende producten gekoppeld totdat aan een van de volgende voorwaarden is voldaan:

* De eVar verloopt (op basis van de instelling &#39;Verlopen na&#39;)
* De eVar voor handelswaar wordt overschreven door een nieuwe waarde.

### De veranderlijke syntaxis van de omzetting gebruikend Web SDK

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md), werkt de syntaxis op dezelfde manier als bij het implementeren van andere [eVars](evar.md) en [gebeurtenissen](events/events-overview.md). XDM die het voorbeeld hierboven weerspiegelt zou als het volgende kijken:

Stel de eVar in op dezelfde of vorige gebeurtenisaanroep:

```json
"_experience": {
  "analytics": {
    "customDimensions": {
      "eVars": {
        "eVar1" : "Aviary"
      }
    }
  }
}
```

Stel de bindingsgebeurtenis en -waarden voor de productreeks in:

```json
"commerce": {
  "productViews" : {
    "value" : 1
  }
},
"productListItems": [
  {
    "name": "Canary"
  }
]
```

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md) De gegevensobjecten die het bovenstaande voorbeeld weerspiegelen, zien er als volgt uit:

Stel de eVar in op dezelfde of vorige gebeurtenisaanroep:

```json
"data": {
  "__adobe": {
    "analytics": {
      "eVar1": "Aviary"
    }
  }
}
```

Stel de bindingsgebeurtenis en -waarden voor de productreeks in:

```json
"data": {
  "__adobe": {
    "analytics": {
      "events": "prodView",
      "products": ";Canary"
    }
  }
}
```
