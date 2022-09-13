---
title: events
description: Stel de gebeurtenisvariabele in, die de meeste meetgegevens op uw site beheert.
feature: Variables
exl-id: 6ef99ee5-40c3-4ff2-a75d-c97f2e8ec1f8
source-git-commit: 48f840f3f15702761a453763e7c416a67bcb687b
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# gebeurtenissen

Dimension en metriek zijn essentiële onderdelen van rapporten. De `events` de variabele is verantwoordelijk voor gegevensinzameling van vele metriek op uw plaats. Gebeurtenissen nemen doorgaans toe [cijfers](/help/components/metrics/overview.md) in verslagen.

Alvorens gebeurtenissen uit te voeren, zorg ervoor dat u creeert en hen vormt onder [Gebeurtenissen met succes](/help/admin/admin/c-success-events/success-event.md) in de instellingen van de rapportsuite. Als u aangepaste gebeurtenissen wilt gebruiken bij het bijhouden van koppelingen, controleert u of [`linkTrackVars`](../../config-vars/linktrackvars.md) en [`linkTrackEvents`](../../config-vars/linktrackevents.md) correct zijn ingesteld.

## Gebeurtenissen die de SDK van het Web gebruiken

Aangepaste gebeurtenissen zijn [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder de volgende XDM-velden:

* Aangepaste gebeurtenissen 1-100 worden toegewezen aan `_experience.analytics.event1to100.event1` - `_experience.analytics.event1to100.event100`.
* Aangepaste gebeurtenissen 101-200 worden toegewezen aan `_experience.analytics.event101to200.event100` - `_experience.analytics.event101to200.event200`.
* Dit patroon herhaalt elke 100 gebeurtenissen naar `_experience.analytics.event901to1000.event901` - `_experience.analytics.event901to1000.event1000`. `eventx.value` wordt gebruikt om het te verhogen bedrag te specificeren. `eventx.id` wordt gebruikt voor [serienummering](event-serialization.md).
* Bestellingen worden toegewezen aan `commerce.purchases.value`.
* Eenheden worden toegewezen aan de som van alle eenheden `productListItems[].quantity` velden.
* Opbrengsten worden toegewezen aan de som van alle `productListItems[].priceTotal` velden.
* Productweergaven worden toegewezen aan `commerce.productListViews.value`.
* Karretjes worden toegewezen aan `commerce.productListOpens.value`.
* Extra winkelwagentjes worden toegewezen aan `commerce.productListAdds.value`.
* Winkelwagentjes worden toegewezen aan `commerce.productListRemovals.value`.
* Wisselweergaven worden toegewezen aan `commerce.productListViews.value`.
* Afbeeldingen worden toegewezen aan `commerce.checkouts.value`.

>[!NOTE]
>
>Als een gebeurtenis is ingesteld onder `productListItems` (bijvoorbeeld `productListItems._experience.analytics.event1.value`) en die gebeurtenis zich nog niet in dit veld bevindt, wordt die gebeurtenis automatisch toegevoegd aan dit veld.

## Gebeurtenissen die de extensie Adobe Analytics gebruiken

U kunt gebeurtenissen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] sectie.

Er zijn verschillende functies beschikbaar:

* In een vervolgkeuzelijst kunt u de gebeurtenis selecteren die u wilt opnemen
* Een optioneel tekstveld voor serienummering. Zie [gebeurtenisserienummering](event-serialization.md) voor meer informatie .
* Een optioneel tekstveld voor een gebeurteniswaarde. U kunt een valuta voor valutagebeurtenissen opnemen of een geheel getal voor gebeurtenissen buiten de valuta om deze meerdere keren te verhogen. Als u bijvoorbeeld `event1` onder de vervolgkeuzelijst en inclusief `10` in dit veld, stappen `event1` 10 bij de rapportage.
* Een knop om een andere gebeurtenis toe te voegen. U kunt net zoveel gebeurtenissen toevoegen als u wilt met één regel.

## s.events in AppMeturement en de de coderedacteur van de uitbreiding van de Analyse van de douanecode

De `s.events` variabele is een tekenreeks die een door komma&#39;s gescheiden lijst met gebeurtenissen bevat die in de hit moeten worden opgenomen. Er is geen bytelimiet voor deze variabele, zodat de variabele niet wordt afgekapt. Geldige waarden zijn:

* `event1` - `event1000`: Aangepaste gebeurtenissen instellen op de gewenste manier. Registreer hoe u elke gebeurtenis in uw organisatie gebruikt [document ontwerp oplossing](../../../prepare/solution-design.md). Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met de accountmanager van uw organisatie als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.
* `purchase`: Verhoogt de [&#39;Bestellingen&#39;](/help/components/metrics/orders.md) metrisch bij 1, en neemt waarden die in worden geplaatst `products` variabele die moet worden berekend [&#39;Eenheden&#39;](/help/components/metrics/units.md) en [&quot;Ontvangsten&quot;](/help/components/metrics/revenue.md). Zie [koopgebeurtenis](event-purchase.md) voor meer informatie .
* `prodView`: Verhoogt de [&#39;Productweergaven&#39;](/help/components/metrics/product-views.md) metrisch.
* `scOpen`: Verhoogt de [&quot;Karten&quot;](/help/components/metrics/carts.md) metrisch.
* `scAdd`: Verhoogt de [&#39;Kart Additions&#39;](/help/components/metrics/cart-additions.md) metrisch.
* `scRemove`: Verhoogt de [&#39;Winning van wagentjes&#39;](/help/components/metrics/cart-removals.md) metrisch.
* `scView`: Verhoogt de [&#39;Kleuraweergaven&#39;](/help/components/metrics/cart-views.md) metrisch.
* `scCheckout`: Verhoogt de [&quot;Afhandelingen&quot;](/help/components/metrics/checkouts.md) metrisch.

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

U kunt een aangepaste gebeurtenis wijzigen en valuta gebruiken in plaats van gehele getallen. Valutamarkeringen worden automatisch omgezet in de valuta van de rapportsuite als de rapportsuite valuta bevat en de `currencyCode` variabele komt niet overeen. Ze zijn handig voor het berekenen van verzendkosten, kortingen of terugbetalingen. U kunt valutagebeurtenissen instellen in het dialoogvenster `products` variabele als u de gebeurtenis alleen aan dat product wilt toewijzen.

Voordat u valutagebeurtenissen implementeert, moet u de gewenste gebeurtenis instellen op &#39;Valuta&#39; onder [Gebeurtenissen met succes](/help/admin/admin/c-success-events/success-event.md) in de instellingen van de rapportsuite.

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
>Als u een valutawaarde instelt in beide `events` en de `products` variabele, de valutawaarde in `events` wordt gebruikt. Stel geen valutawaarden in voor beide `events` en `products` variabelen.

### Numerieke gebeurtenissen gebruiken

U kunt een aangepaste gebeurtenis wijzigen om decimale waarden te accepteren in plaats van gehele getallen. Numerieke gebeurtenissen gedragen zich op dezelfde manier als valutagebeurtenissen, maar gebruiken geen valutaomrekening. U kunt numerieke gebeurtenissen instellen in het dialoogvenster `products` variabele als u de gebeurtenis alleen aan dat product wilt toewijzen.

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
>Als u een numerieke waarde instelt in het dialoogvenster `events` en de `products` variabele, de numerieke waarde in `events` wordt gebruikt. Plaats geen numerieke waarden in het dialoogvenster `events` en `products` variabelen.
