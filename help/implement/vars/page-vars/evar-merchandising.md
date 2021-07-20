---
title: eVar (Merchandising)
description: Aangepaste variabelen die aan afzonderlijke producten zijn gekoppeld.
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
source-git-commit: 2e3f078500b80eefa2ca7c4a67de5bd0e91e764f
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# eVar (Merchandising)

*Deze Help-pagina beschrijft hoe u handelsversies van eVars kunt implementeren. Zie [eVars (Merchandising)](/help/components/dimensions/evar-merchandising.md) in de gebruikershandleiding voor componenten voor informatie over hoe merchandising Vars als een dimensie werkt.*

Zie [Verkoop van variabelen en methoden om producten te vinden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=en) voor een gedetailleerde beschrijving van de werking van eVars.

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor u de eVar aan de gewenste syntaxis in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

>[!IMPORTANT]
>
>Het niet correct configureren van merchandising Vars leidt tot onverwachte waarden of gegevensverlies voor de variabele. Zorg ervoor het correct voor uw implementatie wordt gevormd.

## Implementeren met behulp van productsyntaxis

Wanneer &#39;Productsyntaxis&#39; is ingeschakeld, wordt de categorie Verkoop direct ingevuld in de variabele `products`. Het is dus niet nodig een bindingsgebeurtenis te selecteren en in te stellen. Dit is de aanbevolen methode en moet worden gebruikt, tenzij de waarde niet beschikbaar is om in `products` in te stellen wanneer de gebeurtenis success plaatsvindt.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

De waarde voor `eVar1` wordt toegewezen aan het product. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden aan de waarde van de eVar gecrediteerd.

## Implementeren met syntaxis van conversievariabelen

Conversievariabele Syntax wordt gebruikt wanneer de waarde eVar niet beschikbaar is om in te stellen in de variabele `products`. Dit scenario betekent doorgaans dat de pagina geen context heeft van het kanaal voor handelsdoeleinden of de zoekmethode. In deze gevallen stelt u de variabele merchandising in voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens configuratie wordt geselecteerd voorkomt, wordt de persistente waarde van de eVar gekoppeld aan het product. Als bijvoorbeeld `prodView` is opgegeven als bindingsgebeurtenis, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een eVar bijwerken die al aan een product is toegewezen.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = "Birds;Canary";
```

De waarde `"Aviary"` voor `eVar1` wordt toegewezen aan het product `"Canary"`. Alle volgende succesgebeurtenissen die betrekking hebben op dit product, worden gecrediteerd aan `"Canary"`. Bovendien is de huidige waarde van de variabele koophandel aan alle volgende producten gebonden totdat aan een van de volgende voorwaarden is voldaan:

* De eVar verloopt (op basis van de instelling &#39;Verlopen na&#39;)
* De eVar wordt overschreven door een nieuwe waarde.
