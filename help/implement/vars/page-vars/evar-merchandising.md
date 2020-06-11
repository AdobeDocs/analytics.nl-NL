---
title: eVar (Merchandising)
description: Aangepaste variabelen die aan afzonderlijke producten zijn gekoppeld.
translation-type: tm+mt
source-git-commit: 52e00470df0f0c6bff84b26c1548e64ff5114fb8
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---


# eVar (Merchandising)

*Deze Help-pagina beschrijft hoe u handelsversies van eVars kunt implementeren. Voor informatie over hoe de handel in eVars als afmeting werkt, zie[Vars (Merchandising)](/help/components/dimensions/evar-merchandising.md)in de de gebruikersgids van Componenten.*

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor u eVar aan de gewenste syntaxis in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

>[!IMPORTANT] Het niet correct configureren van merchandising Vars leidt tot onverwachte waarden of gegevensverlies voor de variabele. Zorg ervoor het correct voor uw implementatie wordt gevormd.

## Implementeren met behulp van productsyntaxis

Wanneer &#39;Productsyntaxis&#39; is ingeschakeld, wordt de categorie Verkoop direct in de `products` variabele ingevuld. Het is dus niet nodig een bindingsgebeurtenis te selecteren en in te stellen. Dit is de aanbevolen methode en moet worden gebruikt, tenzij de waarde niet beschikbaar is om in te stellen wanneer de succesgebeurtenis plaatsvindt. `products`

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

De waarde voor `eVar1` wordt toegewezen aan het product. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden aan de waarde eVar gecrediteerd.

## Implementeren met syntaxis van conversievariabelen

Conversievariabele Syntax wordt gebruikt wanneer de eVar waarde niet beschikbaar is om in de `products` variabele te plaatsen. Dit scenario betekent doorgaans dat de pagina geen context heeft van het kanaal voor handelsdoeleinden of de zoekmethode. In deze gevallen stelt u de variabele merchandising in voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens de configuratie wordt geselecteerd voorkomt, wordt de persistente waarde van eVar geassocieerd met het product. Als de bindingsgebeurtenis bijvoorbeeld `prodView` is opgegeven, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een handelsversie bijwerken die al aan een product is toegewezen.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = "Birds;Canary";
```

De waarde `"Aviary"` voor `eVar1` wordt toegewezen aan het product `"Canary"`. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden gecrediteerd aan `"Canary"`. Bovendien is de huidige waarde van de variabele koophandel aan alle volgende producten gebonden totdat aan een van de volgende voorwaarden is voldaan:

* De eVar verloopt (gebaseerd op de instelling &#39;Verlopen na&#39;)
* De handelsversie van Var wordt overschreven met een nieuwe waarde.
