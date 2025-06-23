---
title: eVar (variabele Verwerking)
description: Aangepaste variabelen die aan afzonderlijke producten zijn gekoppeld.
feature: Appmeasurement Implementation
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# eVar (Merchandising)

*Deze hulppagina beschrijft hoe te om het veranderen eVars uit te voeren. Voor informatie over hoe de handel drijvende eVars als afmeting werkt, zie [ Vars (de afmeting van het Merchandising) ](/help/components/dimensions/evar-merchandising.md) in de de gebruikersgids van Componenten.*

Voor een gedetailleerde bespreking van hoe de handel drijvende eVars werkt, zie [ het Merchandising Vars en product het vinden methodes ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html).

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor dat u eVar aan de gewenste syntaxis in de montages van de rapportreeks vormt. Zie [ variabelen van de Omzetting ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de gids Admin.

>[!WARNING]
>
>Het niet correct configureren van merchandising Vars leidt tot onverwachte waarden of gegevensverlies voor de variabele. Zorg ervoor het correct voor uw implementatie wordt gevormd.

## Implementeren met behulp van productsyntaxis

Wanneer &#39;Productsyntaxis&#39; is ingeschakeld, wordt de categorie Verkoop direct ingevuld in de variabele `products` . Het is dus niet nodig een bindingsgebeurtenis te selecteren en in te stellen. Dit is de aanbevolen methode en moet worden gebruikt, tenzij de waarde niet beschikbaar is om in `products` in te stellen wanneer de gebeurtenis success plaatsvindt.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

De waarde voor `eVar1` wordt toegewezen aan het product. Alle volgende succesgebeurtenissen met betrekking tot dit product worden aan de eVar-waarde gecrediteerd.

### Productsyntaxis met de Web SDK

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), gebruiken de de handelende variabelen van de productsyntaxis de volgende gebieden XDM:

* Productsyntaxisverkoop-eVars worden toegewezen onder `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar1` aan `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar250` .
* Verhandelingsgebeurtenissen voor productsyntaxis worden toegewezen onder `xdm.productListItems[]._experience.analytics.event1to100.event1.value` aan `xdm.productListItems[]._experience.analytics.event901to1000.event1000.value` . [ rangschikking van de Gebeurtenis ](events/event-serialization.md) XDM gebieden worden in kaart gebracht onder `xdm.productListItems[]._experience.analytics.event1to100.event1.id` aan `xdm.productListItems[]._experience.analytics.event901to1000.event1000.id`.

>[!NOTE]
>
>Wanneer u gebeurtenissen instelt onder `productListItems` , hoeft u deze niet in te stellen in de gebeurtenistekenreeks. Wanneer deze op beide plaatsen zijn ingesteld, heeft de waarde in de gebeurtenistekenreeks voorrang.

Het volgende voorbeeld toont één enkel [ product ](products.md) gebruikend veelvoudige handelaarsVars en gebeurtenissen:

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

Het bovenstaande voorbeeldobject wordt als `";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"` naar Adobe Analytics verzonden.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), eVar gebruikt het merchandising `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` na de syntaxis van AppMeasurement.

## Implementeren met syntaxis van conversievariabelen

Conversievariabele Syntax wordt gebruikt wanneer de eVar-waarde niet kan worden ingesteld in de `products` -variabele. Dit scenario betekent doorgaans dat de pagina geen context heeft van het kanaal voor handelsdoeleinden of de zoekmethode. In deze gevallen stelt u de variabele merchandising in voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens de configuratie is geselecteerd, plaatsvindt, wordt de blijvend waarde van de eVar aan het product gekoppeld. Als `prodView` bijvoorbeeld is opgegeven als de bindingsgebeurtenis, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een eVar bijwerken die al aan een product is toegewezen.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

De waarde `"Aviary"` for `eVar1` wordt toegewezen aan het product `"Canary"` . Alle volgende succesgebeurtenissen met betrekking tot dit product worden aan `"Canary"` gecrediteerd. Bovendien is de huidige waarde van de variabele voor handelsdoeleinden aan alle volgende producten gekoppeld totdat aan een van de volgende voorwaarden is voldaan:

* De eVar verloopt (op basis van de instelling &#39;Verlopen na&#39;)
* De eVar voor handelsdoeleinden wordt overschreven door een nieuwe waarde.

### Syntaxis van conversievariabele met gebruik van de Web SDK

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), de syntaxis op dezelfde wijze aan het uitvoeren van andere [ eVars ](evar.md) en [ gebeurtenissen ](events/events-overview.md) werkt. XDM die het voorbeeld hierboven weerspiegelt zou als het volgende kijken:

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

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), zouden de gegevensvoorwerpen die het voorbeeld hierboven weerspiegelen als het volgende kijken:

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
