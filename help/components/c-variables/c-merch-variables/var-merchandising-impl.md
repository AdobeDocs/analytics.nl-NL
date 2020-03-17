---
description: Beschrijft hoe te om een koopvaardijvariabele toe te laten en uit te voeren.
keywords: Analytics Implementation;merchandising;variable;product syntax;Conversion Variable Syntax;s.products
title: Een variabele voor handelsdoeleinden implementeren
topic: Developer and implementation
translation-type: tm+mt
source-git-commit: ''

---


# Een variabele voor handelsdoeleinden implementeren

Beschrijft hoe te om een koopvaardijvariabele toe te laten en uit te voeren.

## Een variabele voor het wijzigen van tekst inschakelen

Merchandising kan worden ingeschakeld voor elke aangepaste eVar onder **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Conversion Variables]**.

![](assets/merch-enable.png)

| Instelling | Beschrijving |
|--- |--- |
| Verlopen na | Hiermee bepaalt u hoe lang handelswaarden moeten blijven bestaan. |
| Merchandising | **Productsyntaxis:** De waarde wordt ingesteld binnen `s.products`.<br>**Syntaxis conversievariabele:**De waarde wordt ingesteld in de opgegeven merchandising-variabele. |
| Merchandising Binding Event (alleen syntaxis voor conversievariabele) | Hiermee geeft u aan wanneer een product moet worden gekoppeld aan de huidige handelscategorie. U kunt meerdere gebeurtenissen selecteren door Ctrl ingedrukt te houden en op meerdere items in de lijst te klikken. U kunt alleen een gebeurtenis selecteren wanneer de syntaxis van de conversievariabele is geselecteerd. |

## Implementeren met productsyntaxis

Wanneer de Syntaxis van het Product wordt toegelaten, wordt de handelscategorie bevolkt direct binnen de productvariabele, zodat wordt het selecteren van en het plaatsen van een bindende gebeurtenis niet vereist. Dit is de aanbevolen methode en moet worden gebruikt, tenzij de waarde niet beschikbaar is om in te stellen wanneer de succesgebeurtenis plaatsvindt. `s.products`

### Syntaxis

```js
s.products="category;product;quantity;price;event_incrementer;eVarN=merch_category|eVarM=merch_category2";
```

### Voorbeeld

```js
s.events="prodView";
s.products=";Snow Goggles;;;;eVar1=goggles";
```

De waarde &#39;goggles&#39; voor eVar1 wordt toegewezen aan het product &#39;Snow Goggles&#39;. Alle volgende succesgebeurtenissen (product voegt toe, kassa&#39;s, aankopen, enzovoort) die betrekking hebben op dit product, worden gecrediteerd aan &#39;goggles&#39;.

## Implementeren met gebruik van conversievariabele syntaxis

Conversievariabele Syntax moet worden gebruikt wanneer de eVar-waarde niet kan worden ingesteld in `s.products`. Dit betekent doorgaans dat de pagina geen context heeft van het verkoopkanaal of de zoekmethode. In deze gevallen moet u de variabele koopwaar instellen voordat u de productpagina bereikt. De waarde blijft bestaan totdat de gebeurtenis binding plaatsvindt.

Wanneer de bindingsgebeurtenis die tijdens de configuratie wordt geselecteerd voorkomt, wordt de persistente waarde van eVar geassocieerd met het product. Als prodView bijvoorbeeld is opgegeven als de bindingsgebeurtenis, is de categorie Verkoop alleen gekoppeld aan de huidige productlijst op het moment dat de gebeurtenis plaatsvindt. Alleen volgende bindingsgebeurtenissen kunnen een handelsversie bijwerken die al aan een product is toegewezen.

### Syntaxis

Plaats op dezelfde of vorige pagina vóór de bindingsgebeurtenis:

```js
s.eVar1="merchandising_category";
```

Plaats op de pagina waar de gebeurtenis binding plaatsvindt:

```js
s.events="prodView";
s.products="category;product";
```

### Voorbeeld

Op bladzijde 1 van het bezoek:

```js
s.eVar1="Outdoors"
```

Op bladzijde 2 van het bezoek:

```js
s.events="prodView";
s.products=";Snow Goggles";
```

De waarde &quot;Buiten&quot; voor eVar1 wordt toegewezen aan het product &quot;Snow Goggles&quot;. Alle volgende succesgebeurtenissen (product voegt toe, kassa&#39;s, aankopen, enzovoort) die betrekking hebben op dit product, worden aan &quot;Snow Goggles&quot; gecrediteerd. Bovendien is de huidige waarde van de variabele koophandel aan alle volgende producten gebonden totdat aan een van de volgende voorwaarden is voldaan:

* Var verloopt (op basis van de instelling &quot;Verlopen na&quot;)
* De handelsversie van Var wordt overschreven met een nieuwe waarde.

## Externe aanvullende informatie

[Geavanceerde syntaxisverwerking](https://analyticsdemystified.com/adobe-analytics/advanced-conversion-syntax-merchandising/) inschakelen [!DNL analyticsdemystified.com]
