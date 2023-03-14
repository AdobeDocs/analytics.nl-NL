---
title: De methode tl() gebruiken met Activity Map
description: U kunt de methode tl() gebruiken om aangepaste elementen bij te houden en om overlayrendering voor dynamische inhoud te configureren.
feature: Activity Map
role: User, Admin
exl-id: e4e32de7-0e46-413a-abc9-9707e273903d
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Gebruik de `tl()` methode met Activity Map

U kunt de `tl()` methode om aangepaste elementen bij te houden en overlayrendering voor dynamische inhoud te configureren.

## Aangepaste elementen bijhouden

Met de [`tl()` methode](/help/implement/vars/functions/tl-method.md) als onderdeel van de Activity Map AppMeturement module kunt u om het even welk voorwerp volgen dat wordt geklikt, zelfs voorwerpen die geen ankermarkeringen of beeldelementen zijn. Gebruiken `tl()`kunt u aangepaste elementen bijhouden die niet resulteren in het laden van een pagina.

In de `tl()` de `linkName` parameter die momenteel wordt gebruikt om de uitgangsverbindingen, douaneverbindingen, enz. te identificeren. wordt nu ook gebruikt om identiteitskaart van de Verbinding voor de variabele van de Activity Map te identificeren.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

Met andere woorden, als u `tl()` om uw douaneelementen te volgen, wordt identiteitskaart getrokken van de waarde die als derde parameter (de naam van de Verbinding) in wordt overgegaan `tl()` methode. Deze wordt niet opgehaald uit het standaardkoppelingsvolgalgoritme dat wordt gebruikt voor [standaardspatiëring](activitymap-link-tracking-methodology.md) in Activity Map.

## Bedekking renderen voor dynamische inhoud

Wanneer de `tl()` Deze methode wordt rechtstreeks aangeroepen vanuit de klikgebeurtenis van het HTML-element. Bij het laden van de webpagina kan de Activity Map een overlay voor dat element weergeven. Voorbeeld:

```html
<a href="javascript:" onclick="s.tl(this,'o','Example custom link');">Example link text</a>
```

Wanneer webpagina-inhoud aan de pagina wordt toegevoegd nadat de eerste pagina is geladen, wordt `tl()` Deze methode wordt indirect aangeroepen en er kunnen alleen overlays voor die nieuwe inhoud worden weergegeven als deze expliciet wordt geactiveerd/geklikt. Dan wordt een nieuw proces van de verbindingsinzameling teweeggebracht van Activity Map.

Wanneer de `tl()` Deze methode wordt niet rechtstreeks aangeroepen vanuit de klikgebeurtenis van het HTML-element. Activity Map kan alleen overlay weergeven als de gebruiker op dat element heeft geklikt. Hier is een voorbeeld van de `tl()` Methode wordt indirect aangeroepen:

```html
<a href="javascript:" onclick="someFn(event);">Example link text</a>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

De beste manier voor Activity Map om dynamische inhoudskoppelingen te bedekken is om een aangepaste `ActivityMap.link` functie die is ingesteld om dezelfde functie aan te roepen waarvan de geretourneerde waarde is doorgegeven aan `tl()`. Bijvoorbeeld:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName)
{
    // if this is a s.tl call, just return string passed
    return linkName ||      
    // this is ActivityMap reporting time
    makeLinkName(element) ||
    // our custom function didn't return anything, so just return the default ActivityMap Link
    originalLinkFunction(element,linkName);
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

Hier hebben we de `ActivityMap.link` functie om één van drie dingen te doen wanneer geroepen:

1. Indien `linkName` is doorgegeven, is dit aangeroepen door `tl()`, dus kom terug op `tl()` doorgegeven als `linkName`.
2. Indien opgeroepen door Activity Map op het rapportagetijdstip, wordt een `linkName` wordt nooit overgegaan, en zo vraag `makeLinkName()` met het koppelingselement. Dit is een cruciale stap in deze richting - de `makeLinkName(element)` de oproep moet hetzelfde zijn als de `tl()` het derde argument van de vraag in `<button>` tag. Dit betekent dat wanneer `tl()` wordt aangeroepen, volgen we de tekenreeks die is geretourneerd door `makeLinkName()`. Wanneer de Activity Map over de verbindingen op de pagina meldt, gebruikt het de zelfde vraag om een verbinding te maken.
3. De definitieve oplossing is enkel de originele terugkeerwaarde van de gebrek ActivityMap verbindingsfunctie terug te keren. Als u deze referentie rond wilt houden om de standaardcase aan te roepen, kunt u alleen aangepaste code voor `makeLinkName()` en niet om met een waarde van de verbindingsterugkeer voor alle verbindingen op de pagina te hoeven komen.
