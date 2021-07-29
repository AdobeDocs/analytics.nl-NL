---
title: events
description: Stel de gebeurtenisvariabele in, die de meeste meetgegevens op uw site beheert.
exl-id: 6ef99ee5-40c3-4ff2-a75d-c97f2e8ec1f8
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# gebeurtenissen

Dimension en metriek zijn essentiële onderdelen van rapporten. De `events` variabele is verantwoordelijk voor gegevensinzameling van vele metriek op uw plaats. Gebeurtenissen verhogen gewoonlijk [metriek](/help/components/metrics/overview.md) in rapporten.

Alvorens gebeurtenissen uit te voeren, zorg ervoor dat u hen onder [de gebeurtenissen van het Succes](/help/admin/admin/c-success-events/success-event.md) in de montages van de Reeks van het Rapport creeert en vormt. Als u van plan bent om douanegebeurtenissen in verbindingsvolgtreffers te gebruiken, zorg ervoor dat [`linkTrackVars`](../../config-vars/linktrackvars.md) en [`linkTrackEvents`](../../config-vars/linktrackevents.md) correct worden geplaatst.

## Gebeurtenissen met tags in Adobe Experience Platform

U kunt gebeurtenissen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Events].

Er zijn verschillende functies beschikbaar:

* In een vervolgkeuzelijst kunt u de gebeurtenis selecteren die u wilt opnemen
* Een optioneel tekstveld voor serienummering. Zie [gebeurtenisserialisatie](event-serialization.md) voor meer informatie.
* Een optioneel tekstveld voor een gebeurteniswaarde. U kunt een valuta voor valutagebeurtenissen opnemen of een geheel getal voor gebeurtenissen buiten de valuta om deze meerdere keren te verhogen. Als u bijvoorbeeld `event1` selecteert onder de vervolgkeuzelijst en `10` opneemt in dit veld, wordt de rapportage met 10 verhoogd in stappen `event1`.
* Een knop om een andere gebeurtenis toe te voegen. Er geldt geen redelijke limiet voor het aantal gebeurtenissen dat u in een hit kunt opnemen.

## s.events in AppMeasurement en aangepaste code-editor

De variabele `s.events` is een tekenreeks die een door komma&#39;s gescheiden lijst met gebeurtenissen bevat die in de hit moeten worden opgenomen. Er is geen bytelimiet voor deze variabele, zodat de variabele niet wordt afgekapt. Geldige waarden zijn:

* `event1` -  `event1000`: Aangepaste gebeurtenissen instellen op de gewenste manier. Registreer hoe u elke gebeurtenis in [document van het oplossingsontwerp ](../../../prepare/solution-design.md) gebruikt. Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met de accountmanager van uw organisatie als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.
* `purchase`: Verhoogt  [&#39;Orders&#39;](/help/components/metrics/orders.md) metrisch door 1, en neemt waarden die in de  `products` variabele worden geplaatst om  [&#39;Eenheden&#39;](/help/components/metrics/units.md) en  [&#39;Opbrengsten&#39;](/help/components/metrics/revenue.md) te berekenen. Zie [aankoopgebeurtenis](event-purchase.md) voor meer informatie.
* `prodView`: Verhoogt de  [&#39;](/help/components/metrics/product-views.md) metrische weergave van het Product.
* `scOpen`: Hiermee verhoogt u de  [metrische ](/help/components/metrics/carts.md) waarde van de winkelwagen.
* `scAdd`: Verhoogt de  [&#39;Cart Additions&#39;](/help/components/metrics/cart-additions.md) metrisch.
* `scRemove`: Verhoogt de  [&#39;Kar Verwijderingen&#39;](/help/components/metrics/cart-removals.md) metrisch.
* `scView`: Verhoogt de  [metrische ](/help/components/metrics/cart-views.md) waarde voor Kaartweergaven.
* `scCheckout`: Verhoogt de  [&#39;Checkouts&#39;](/help/components/metrics/checkouts.md) metrische waarde.

>[!NOTE]
>
>Deze variabele is hoofdlettergevoelig. Vermijd het gebruik van onjuiste hoofdletters voor gebeurteniswaarden om een nauwkeurige gegevensverzameling te garanderen.

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

>[!NOTE]
>
>Tegengebeurtenissen ondersteunen geen valuta- of decimale waarden. Gebruik valutagebeurtenissen voor valuta, of numerieke gebeurtenissen voor decimale waarden.

### Valutagebeurten gebruiken

U kunt een aangepaste gebeurtenis wijzigen en valuta gebruiken in plaats van gehele getallen. Valutamarkeringen worden automatisch omgezet in de valuta van de rapportsuite als de valuta van de rapportsuite en de variabele `currencyCode` niet overeenkomen. Ze zijn handig voor het berekenen van verzendkosten, kortingen of terugbetalingen. U kunt valutagebeurtenissen instellen in de variabele `products` als u de gebeurtenis alleen aan dat product wilt toewijzen.

Voordat u valutagebeurtenissen implementeert, moet u de gewenste gebeurtenis instellen op &#39;Valuta&#39; onder [Succesgebeurtenissen](/help/admin/admin/c-success-events/success-event.md) in de instellingen van de rapportsuite.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

>[!NOTE]
>
>Als u een valutawaarde instelt in zowel de variabele `events` als de variabele `products`, wordt de valutawaarde in `events` gebruikt. Stel geen valutawaarden in zowel de variabelen `events` als `products` in.

### Numerieke gebeurtenissen gebruiken

U kunt een aangepaste gebeurtenis wijzigen om decimale waarden te accepteren in plaats van gehele getallen. Numerieke gebeurtenissen gedragen zich op dezelfde manier als valutagebeurtenissen, maar gebruiken geen valutaomrekening. U kunt numerieke gebeurtenissen instellen in de variabele `products` als u de gebeurtenis alleen aan dat product wilt toewijzen.

Voordat u numerieke gebeurtenissen implementeert, moet u de gewenste gebeurtenis instellen op &#39;Numeriek&#39; onder [Gebeurtenissen met succes](/help/admin/admin/c-success-events/success-event.md) in de instellingen van de rapportsuite.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE]
>
>Als u een numerieke waarde instelt in zowel de variabele `events` als de variabele `products`, wordt de numerieke waarde in `events` gebruikt. Plaats geen numerieke waarden in zowel de variabelen `events` als `products`.
