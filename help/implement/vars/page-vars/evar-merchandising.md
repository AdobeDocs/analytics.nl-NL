---
title: Variabelen eVar (Merchandising)
description: Aangepaste variabelen die aan afzonderlijke producten zijn gekoppeld.
feature: Variables
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
source-git-commit: 9a94e910d4e837bb9808b5662beebe6214ed4174
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# eVar (Merchandising)

*Deze Help-pagina beschrijft hoe u handelsversies van eVars kunt implementeren. Voor informatie over hoe het verhandelen van eVars als dimensie werkt, zie [eVars (Merchandising)](/help/components/dimensions/evar-merchandising.md) in de gebruikershandleiding van Componenten.*

Zie voor een gedetailleerde discussie over de werking van eVars op handelsgebied [Verkoop- en productzoekmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=en).

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor u de eVar aan de gewenste syntaxis in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

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

De waarde voor `eVar1` wordt toegewezen aan het product. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden aan de waarde van de eVar gecrediteerd.

### XDM gebruiken voor Edge Collection

Elk veld in de variabele &#39;products&#39; wordt gevuld door een corresponderend XDM-veld. U kunt een lijst van alle afbeeldingen van XDM aan de parameters van Analytics zien [hier](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en). Hieronder ziet u een voorbeeld van hoe de XDM-velden productListItems worden gecombineerd om een productvariabele te maken.

XDM-structuur:

```js
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

Resulterende &#39;products&#39;-parameter doorgegeven aan Analytics:

```js
pl = ”;Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large”
```

## Implementeren met syntaxis van conversievariabelen

Conversievariabele Syntaxis wordt gebruikt wanneer de waarde van de eVar niet beschikbaar is om in te stellen in het dialoogvenster `products` variabele. Dit scenario betekent doorgaans dat de pagina geen context heeft van het kanaal voor handelsdoeleinden of de zoekmethode. In deze gevallen stelt u de variabele merchandising in voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens configuratie wordt geselecteerd voorkomt, wordt de persistente waarde van de eVar gekoppeld aan het product. Als `prodView` wordt opgegeven als de bindingsgebeurtenis, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een eVar bijwerken die al aan een product is toegewezen.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

De waarde `"Aviary"` for `eVar1` is toegewezen aan het product `"Canary"`. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden gecrediteerd aan `"Canary"`. Bovendien is de huidige waarde van de variabele koophandel aan alle volgende producten gebonden totdat aan een van de volgende voorwaarden is voldaan:

* De eVar verloopt (op basis van de instelling &#39;Verlopen na&#39;)
* De eVar wordt overschreven door een nieuwe waarde.

### XDM gebruiken voor Edge Collection

U kunt dezelfde informatie opgeven met XDM-velden die zijn toegewezen aan Analytics-velden. U kunt een lijst van alle afbeeldingen van XDM aan de parameters van Analytics zien [hier](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en). XDM die het voorbeeld hierboven weerspiegelt zou als het volgende kijken:

Stel de eVar in op dezelfde of vorige gebeurtenisaanroep:

```js
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

```js
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
