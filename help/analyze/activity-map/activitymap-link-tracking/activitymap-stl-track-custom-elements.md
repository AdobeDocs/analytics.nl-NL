---
title: De methode tl() gebruiken met Activity Map
description: U kunt de methode tl() gebruiken om aangepaste elementen bij te houden en om overlayrendering voor dynamische inhoud te configureren.
topic: Activiteitenoverzicht
translation-type: tm+mt
source-git-commit: 65cb0a49ef74156f0b8adf4a11c6fec6394d306f
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# De methode `tl()` met Activity Map gebruiken

Met de methode `tl()` kunt u aangepaste elementen bijhouden en overlayrendering configureren voor dynamische inhoud.

## Aangepaste elementen bijhouden

Als u de [`tl()`-methode](/help/implement/vars/functions/tl-method.md) gebruikt als onderdeel van de Activity Map AppMeasurement-module, kunt u elk object volgen waarop wordt geklikt, zelfs objecten die geen ankerlabels of afbeeldingselementen zijn. Met `tl()` kunt u aangepaste elementen bijhouden die niet resulteren in het laden van een pagina.

In de `tl()` methode, de `linkName` parameter die momenteel wordt gebruikt om de uitgangsverbindingen, douaneverbindingen, enz. te identificeren. wordt nu ook gebruikt om identiteitskaart van de Verbinding voor de variabele van de Activity Map te identificeren.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

Met andere woorden, als u `tl()` gebruikt om uw douaneelementen te volgen, wordt identiteitskaart van de verbinding getrokken uit de waarde die als derde parameter (de naam van de Verbinding) in `tl()` methode wordt overgegaan. Het wordt niet getrokken uit het standaardkoppelingsvolgalgoritme dat voor [default tracking](activitymap-link-tracking-methodology.md) in Activity Map wordt gebruikt.

## Bedekking renderen voor dynamische inhoud

Wanneer de methode `tl()` rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan de Activity Map een bedekking voor dat element weergeven wanneer de webpagina wordt geladen. Voorbeeld:

```html
<a href="javascript:" onclick="s.tl(this,'o','Example custom link');">Example link text</a>
```

Wanneer webpagina-inhoud na het laden van de eerste pagina aan de pagina wordt toegevoegd, wordt de methode `tl()` indirect aangeroepen en kunnen er alleen overlays voor die nieuwe inhoud worden weergegeven als deze expliciet is geactiveerd/geklikt. Dan wordt een nieuw proces van de verbindingsinzameling teweeggebracht van Activity Map.

Wanneer de methode `tl()` niet rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan Activity Map alleen bedekking weergeven als de gebruiker op dat element heeft geklikt. Hier volgt een voorbeeld waarin de methode `tl()` indirect wordt aangeroepen:

```html
<a href="javascript:" onclick="someFn(event);">Example link text</a>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

De beste manier voor Activity Map om dynamische inhoudskoppelingen te bedekken is om een aangepaste `ActivityMap.link` functie te hebben opstelling om de zelfde functie te roepen de waarvan terugkeerwaarde tot `tl()` wordt overgegaan. Bijvoorbeeld:

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

Hier, hebben wij de functie `ActivityMap.link` met voeten getreden om één van drie dingen te doen wanneer geroepen:

1. Als `linkName` wordt overgegaan, dan werd dit geroepen door `tl()`, zo enkel wat `tl()` binnen als `linkName` ging.
2. Wanneer geroepen door Activity Map bij het melden van tijd, wordt `linkName` nooit overgegaan, en zo vraag `makeLinkName()` met het verbindingselement. Dit is de cruciale stap hier - de `makeLinkName(element)` vraag zou het zelfde als `tl()` derde argument van de vraag in `<button>` markering moeten zijn. Dit betekent dat wanneer `tl()` wordt geroepen, wij het koord volgen dat door `makeLinkName()` is teruggekeerd. Wanneer de Activity Map over de verbindingen op de pagina meldt, gebruikt het de zelfde vraag om een verbinding te maken.
3. De definitieve oplossing is enkel de originele terugkeerwaarde van de gebrek ActivityMap verbindingsfunctie terug te keren. Als u deze referentie zo houdt dat deze in het standaardgeval wordt aangeroepen, kunt u alleen aangepaste code voor `makeLinkName()` overschrijven of schrijven en hoeft u geen geretourneerde waarde voor alle koppelingen op de pagina op te geven.
