---
description: Met de methode s.tl() kunt u aangepaste elementen bijhouden en overlayrendering configureren voor dynamische inhoud.
title: De methode s.tl() gebruiken
topic: Activity map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# De `tl()` methode gebruiken

U kunt de `tl()` methode gebruiken om aangepaste elementen bij te houden en bedekking renderen voor dynamische inhoud te configureren.

## Aangepaste elementen bijhouden {#section_5D6688DFFFC241718249A9A0C632E465}

Met de [`tl()` methode](/help/implement/vars/functions/tl-method.md) als onderdeel van de Activity Map AppMeasurement-module kunt u elk object volgen waarop wordt geklikt, zelfs objecten die geen ankerlabels of afbeeldingselementen zijn. Met s.tl kunt u aangepaste elementen bijhouden die niet resulteren in het laden van een pagina.

In de `tl()` methode, de `linkName` parameter die momenteel wordt gebruikt om de uitgangsverbindingen, douaneverbindingen, enz. te identificeren. wordt nu ook gebruikt om identiteitskaart van de Verbinding voor de variabele van de Kaart van de Activiteit te identificeren.

```js
s.tl(this,linkType,linkName,variableOverrides)
```

Met andere woorden, als u gebruikt `s.tl()` om uw douaneelementen te volgen, wordt identiteitskaart getrokken van de waarde die als derde parameter (linkName) in de `s.tl()` methode wordt overgegaan. Het wordt niet getrokken uit het standaardkoppelingsvolgalgoritme dat voor [gebrek het volgen](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in de Kaart van de Activiteit wordt gebruikt.

## Bedekking renderen voor dynamische inhoud {#section_FD24B61A732149C7B58BA957DD84A5E7}

Wanneer de functie s.tl() rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan Activity Map een bedekking voor dat element weergeven wanneer de webpagina wordt geladen. Voorbeeld:

```html
<div onclick="s.tl(this,'o','Example custom link')">Example link text</a>
```

Wanneer webpagina-inhoud na het laden van de eerste pagina aan de pagina wordt toegevoegd, wordt de `tl()` methode onrechtstreeks aangeroepen en kunnen er alleen overlays voor die nieuwe inhoud worden weergegeven als deze expliciet wordt geactiveerd/geklikt. Dan wordt een nieuw proces van de verbindingsinzameling teweeggebracht van de Kaart van de Activiteit.

Wanneer de `tl()` methode niet rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan de Activiteitenkaart alleen overlay weergeven als de gebruiker op dat element heeft geklikt. Hier volgt een voorbeeld waarin de `tl()` methode indirect wordt aangeroepen:

```html
<div onclick="someFn(event)"></div>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

De beste manier voor Activiteitenkaart om dynamische inhoudskoppelingen te bedekken is om een aangepaste ActivityMap.link functie te hebben die opstelling om de zelfde functie te roepen de waarvan terugkeerwaarde wordt overgegaan tot `s.tl`. Bijvoorbeeld:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName) {
    return linkName ||      // if this is a s.tl call, just return string passed
        makeLinkName(element) || // this is ActivityMap reporting time
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

Hier, hebben wij de functie ActivityMap.link met voeten getreden om één van drie dingen te doen wanneer geroepen:

1. Als linkName wordt overgegaan, wordt dit geroepen door s.tl (), zodat keer enkel wat s.tl binnen als linkName wordt overgegaan.
2. Dit wordt geroepen door de Kaart van de Activiteit bij het melden van tijd, zodat wordt een linkName nooit overgegaan, en zo vraag makeLinkName () met het verbindingselement. Dit is de cruciale stap hier - de vraag &quot;makeLinkName(element)&quot;zou het zelfde bij het derde argument van de vraag s.tl in de `<button>` markering moeten zijn. Dit betekent dat wanneer s.tl wordt geroepen, wij het koord volgen dat door makeLinkName is teruggekeerd. Wanneer de Kaart van de Activiteit over de verbindingen op de pagina meldt, gebruikt de zelfde vraag om een verbinding te maken.
3. De definitieve oplossing is enkel de originele terugkeerwaarde van de gebrek ActivityMap verbindingsfunctie terug te keren. Als u deze referentie rondom houdt om in het standaardgeval aan te roepen, kunt u alleen aangepaste code voor makeLinkName overschrijven of schrijven en niet met een koppelingsgeretourneerde waarde voor alle koppelingen op de pagina hoeven te komen.
