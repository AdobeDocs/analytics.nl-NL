---
title: gebeurtenissen
description: Stel de gebeurtenisvariabele in, die de meeste meetgegevens op uw site beheert.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# gebeurtenissen

Dimensies en metriek zijn essentiële componenten voor rapporten. De `events` variabele is verantwoordelijk voor gegevensinzameling van vele metriek op uw plaats.

## Gebeurtenissen in Adobe Experience Platform Launch

U kunt gebeurtenissen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] sectie.

Er zijn verschillende functies beschikbaar:

* In een vervolgkeuzelijst kunt u de gebeurtenis selecteren die u wilt opnemen
* Een optioneel tekstveld voor serienummering. Zie [gebeurtenisserialisatie](event-serialization.md) voor meer informatie.
* Een optioneel tekstveld voor een gebeurteniswaarde. U kunt een valuta voor valutagebeurtenissen opnemen of een geheel getal voor gebeurtenissen buiten de valuta om deze meerdere keren te verhogen. Als u bijvoorbeeld `event1` onder de vervolgkeuzelijst selecteert en `10` `event1` in dit veld invoegt, wordt de rapportage met 10 verhoogd.
* Een knop om een andere gebeurtenis toe te voegen. Er geldt geen redelijke limiet voor het aantal gebeurtenissen dat u in een hit kunt opnemen.

## s.events in AppMeasurement en Launch de redacteur van de douanecode

De `s.events` variabele is een tekenreeks die een door komma&#39;s gescheiden lijst met gebeurtenissen bevat die in de hit moeten worden opgenomen. Er is geen bytelimiet voor deze variabele, zodat de variabele niet wordt afgekapt. Geldige waarden zijn:

* `event1` - `event1000`: Aangepaste gebeurtenissen instellen op de gewenste manier. Registreer hoe u elke gebeurtenis in het document [van het de](../../../prepare/solution-design.md)oplossingsontwerp van uw organisatie gebruikt. Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met de accountmanager van uw organisatie als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.
* `purchase`: Verhoogt de metrische waarde &#39;Orders&#39; met 1 en neemt waarden die zijn ingesteld in de `products` variabele om &#39;Units&#39; en &#39;Revenue&#39; te berekenen. Zie [Aankoopgebeurtenis](event-purchase.md) voor meer informatie.
* `prodView`: Verhoogt metrisch de &quot;Weergaven van het Product&quot;.
* `scOpen`: Hiermee verhoogt u de metrische waarde &#39;Carts&#39;.
* `scAdd`: Verhoogt de metrische waarde &#39;Cart Additions&#39;.
* `scRemove`: Verhoogt de metrische waarde &#39;Winkels verwijderen&#39;.
* `scView`: Verhoogt metrisch met de optie Wisselende weergaven.
* `scCheckout`: Verhoogt metrisch &quot;Checkouts&quot;.

> [!TIP] Deze variabele is hoofdlettergevoelig. Vermijd het gebruik van onjuiste hoofdletters voor gebeurteniswaarden om een nauwkeurige gegevensverzameling te garanderen.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### Hoektelgebeurtenissen meerdere keren

Desgewenst kunt u aangepaste gebeurtenissen meerdere keren tellen. Wijs een geheel getal toe aan de gewenste gebeurtenis binnen de tekenreeks. Gebeurtenissen die in de instellingen van de rapportsuite worden gemaakt, zijn standaard tegengebeurtenissen.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

> [!NOTE] Tegengebeurtenissen ondersteunen geen valuta- of decimale waarden. Gebruik valutagebeurtenissen voor valuta, of numerieke gebeurtenissen voor decimale waarden.

### Valutagebeurten gebruiken

U kunt een aangepaste gebeurtenis wijzigen en valuta gebruiken in plaats van gehele getallen. Valutamarkeringen worden automatisch omgezet in de valuta van de rapportsuite als de valuta van de rapportsuite en de `currencyCode` variabele niet overeenkomen. Ze zijn handig voor het berekenen van verzendkosten, kortingen of terugbetalingen. U kunt valutagebeurten instellen in de `products` variabele als u de gebeurtenis alleen aan dat product wilt toewijzen.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

> [!NOTE] Als u een valutawaarde instelt in zowel de `events` variabele als de `products` variabele, wordt de valutawaarde in `events` gebruikt. Stel geen valutawaarden in zowel de `events` variabelen als de `products` variabelen in.

### Numerieke gebeurtenissen gebruiken

U kunt een aangepaste gebeurtenis wijzigen om decimale waarden te accepteren in plaats van gehele getallen. Numerieke gebeurtenissen gedragen zich op dezelfde manier als valutagebeurtenissen, maar gebruiken geen valutaomrekening. U kunt numerieke gebeurtenissen in de `products` variabele instellen als u de gebeurtenis alleen aan dat product wilt toewijzen.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

> [!NOTE] Als u een numerieke waarde instelt in zowel de `events` variabele als de `products` variabele, wordt de numerieke waarde in `events` gebruikt. Stel geen numerieke waarden in zowel de `events` variabelen als de `products` variabelen in.
