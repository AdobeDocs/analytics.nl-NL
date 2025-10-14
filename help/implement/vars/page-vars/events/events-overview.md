---
title: gebeurtenissen
description: Stel de gebeurtenisvariabele in, die de meeste meetgegevens op uw site beheert.
feature: Appmeasurement Implementation
exl-id: 6ef99ee5-40c3-4ff2-a75d-c97f2e8ec1f8
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# gebeurtenissen

Dimensies en metriek zijn essentiële componenten voor rapporten. De variabele `events` is verantwoordelijk voor gegevensverzameling van vele metriek op uw plaats. De gebeurtenissen verhogen typisch [&#x200B; metriek &#x200B;](/help/components/metrics/overview.md) in rapporten.

Alvorens gebeurtenissen uit te voeren, zorg ervoor dat u hen onder [&#x200B; gebeurtenissen van het Succes &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) in de reeksinstellingen van het Rapport creeert en vormt. Als u aangepaste gebeurtenissen wilt gebruiken bij het bijhouden van koppelingen, moet u ervoor zorgen dat [`linkTrackVars`](../../config-vars/linktrackvars.md) en [`linkTrackEvents`](../../config-vars/linktrackevents.md) correct zijn ingesteld.

## Gebeurtenissen die de Web SDK gebruiken

Als het gebruiken van het [&#x200B; voorwerp XDM &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md), gebruiken de douanegebeurtenissen de volgende gebieden XDM:

* Aangepaste gebeurtenissen 1-100 worden toegewezen aan `xdm._experience.analytics.event1to100.event1` - `xdm._experience.analytics.event1to100.event100` .
* Aangepaste gebeurtenissen 101-200 worden toegewezen aan `xdm._experience.analytics.event101to200.event100` - `xdm._experience.analytics.event101to200.event200` .
* Dit patroon herhaalt elke 100 gebeurtenissen tot `xdm._experience.analytics.event901to1000.event901` - `xdm._experience.analytics.event901to1000.event1000`. `eventx.value` wordt gebruikt om de hoeveelheid op te geven die moet worden verhoogd. `eventx.id` wordt gebruikt voor [&#x200B; rangschikking &#x200B;](event-serialization.md).
* Orders worden toegewezen aan `xdm.commerce.purchases.value` .
* Eenheden worden toegewezen aan de som van alle `productListItems[].quantity` -velden.
* Opbrengsten worden toegewezen aan de som van alle `productListItems[].priceTotal` -velden.
* Productweergaven worden toegewezen aan `xdm.commerce.productViews.value` .
* Karten worden toegewezen aan `xdm.commerce.productListOpens.value`.
* Extra winkelwagentjes worden toegewezen aan `xdm.commerce.productListAdds.value` .
* Verwijderingen van winkelwagentjes worden toegewezen aan `xdm.commerce.productListRemovals.value` .
* Tekstweergaven worden toegewezen aan `xdm.commerce.productListViews.value` .
* Uitchecken worden toegewezen aan `xdm.commerce.checkouts.value` .

>[!NOTE]
>
>Als een gebeurtenis wordt ingesteld onder `productListItems` (bijvoorbeeld `productListItems._experience.analytics.event1.value` ) en die gebeurtenis zich nog niet in dit veld bevindt, wordt die gebeurtenis automatisch toegevoegd aan dit veld.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruiken alle gebeurtenissen `data.__adobe.analytics.events`, na het koordsyntaxis van AppMeasurement. Als u dit veld instelt, worden gebeurtenissen die in het XDM-object zijn ingesteld, overschreven en niet naar Adobe Analytics verzonden.

## Gebeurtenissen die de extensie Adobe Analytics gebruiken

U kunt gebeurtenissen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Events] .

Er zijn verschillende functies beschikbaar:

* Een vervolgkeuzelijst waarmee u de gebeurtenis kunt selecteren die u wilt opnemen
* Een optioneel tekstveld voor serialisatie. Zie [&#x200B; gebeurtenisrangschikking &#x200B;](event-serialization.md) voor meer informatie.
* Een optioneel tekstveld voor een gebeurteniswaarde. U kunt een valuta voor valutagebeurtenissen opnemen of een geheel getal voor gebeurtenissen buiten de valuta om deze meerdere keren te verhogen. Als u bijvoorbeeld `event1` selecteert onder de vervolgkeuzelijst en `10` in dit veld instelt `event1` , wordt de rapportage verhoogd met 10.
* Een knop om een andere gebeurtenis toe te voegen. U kunt net zoveel gebeurtenissen toevoegen als u wilt met één regel.

## s.events in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.events` is een tekenreeks die een door komma&#39;s gescheiden lijst met gebeurtenissen bevat die in de hit moeten worden opgenomen. De variabele staat tot 64k bytes toe, in feite toelatend zo vele gebeurtenissen aangezien een slag vereist. Geldige waarden zijn:

* `event1` - `event1000`: Aangepaste gebeurtenissen instellen op de gewenste manier. Verslag hoe u elke gebeurtenis in het document van het de oplossingsontwerp van uw organisatie [&#128279;](../../../prepare/solution-design.md) gebruikt. Het aantal beschikbare gebeurtenissen is afhankelijk van het contract Analytics van uw organisatie. De meeste organisaties op niet verouderde contracten hebben 1000 beschikbare douanefouten. Neem contact op met uw Adobe-accountteam als u niet weet hoeveel aangepaste gebeurtenissen voor u beschikbaar zijn.
* `purchase`: Verhoogt metrisch [&#x200B; &quot;Orders&#39; &#x200B;](/help/components/metrics/orders.md) door 1, en neemt waarden die in de `products` variabele worden geplaatst om [&#x200B; &quot;Units&quot; &#x200B;](/help/components/metrics/units.md) en [&#x200B; &quot;Inkomsten&quot; &#x200B;](/help/components/metrics/revenue.md) te berekenen. Zie [&#x200B; aankoopgebeurtenis &#x200B;](event-purchase.md) voor meer informatie.
* `prodView`: Verhoogt metrisch [&#x200B; &quot;van de Mening van het Product&quot;](/help/components/metrics/product-views.md).
* `scOpen`: Verhoogt metrisch [&#x200B; &quot;Havens&#39; &#x200B;](/help/components/metrics/carts.md).
* `scAdd`: Verhoogt metrisch [&#x200B; &quot;Cart Additions&quot; &#x200B;](/help/components/metrics/cart-additions.md).
* `scRemove`: Verhoogt metrisch [&#x200B; &quot;Cart Removals&#39; &#x200B;](/help/components/metrics/cart-removals.md).
* `scView`: Verhoogt metrisch [&#x200B; &quot;Kar Views&#39; &#x200B;](/help/components/metrics/cart-views.md).
* `scCheckout`: Verhoogt metrisch [&#x200B; &quot;Checkouts&quot;](/help/components/metrics/checkouts.md).

>[!NOTE]
>
>Deze variabele is hoofdlettergevoelig. Vermijd het gebruik van onjuiste hoofdletters voor gebeurteniswaarden om een nauwkeurige gegevensverzameling te garanderen.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### Teller-gebeurtenissen van de verhoging meerdere keren

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

U kunt een aangepaste gebeurtenis wijzigen en valuta gebruiken in plaats van gehele getallen. Valutamarkeringen worden automatisch geconverteerd naar de valuta van de rapportsuite als de valuta van de rapportsuite en de variabele `currencyCode` niet overeenkomen. Ze zijn handig voor het berekenen van verzendkosten, kortingen of terugbetalingen. U kunt valutagebeurtenissen instellen in de variabele `products` als u de gebeurtenis alleen aan dat product wilt toewijzen.

Alvorens muntgebeurtenissen uit te voeren, zorg ervoor dat u de gewenste gebeurtenis aan &quot;Valuta&quot;onder [&#x200B; gebeurtenissen van het Succes &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) in de reeksinstellingen van het Rapport plaatst.

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
>Als u een valutawaarde instelt in zowel de `events` -variabele als de `products` -variabele, wordt de valutawaarde in `events` gebruikt. Stel geen valutawaarden in zowel de variabelen `events` als `products` in.

### numerieke gebeurtenissen gebruiken

U kunt een aangepaste gebeurtenis wijzigen om decimale waarden te accepteren in plaats van gehele getallen. Numerieke gebeurtenissen gedragen zich op dezelfde manier als valutagebeurtenissen, maar gebruiken geen valutaomrekening. U kunt numerieke gebeurtenissen instellen in de variabele `products` als u de gebeurtenis alleen aan dat product wilt toewijzen.

Alvorens numerieke gebeurtenissen uit te voeren, zorg ervoor dat u de gewenste gebeurtenis aan &quot;Numeriek&quot;onder [&#x200B; gebeurtenissen van het Succes &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) in de reeksinstellingen van het Rapport plaatst.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE]
>
>Wanneer u een numerieke waarde instelt in zowel de variabele `events` als de variabele `products` , wordt de numerieke waarde in `events` gebruikt. Stel geen numerieke waarden in in de variabelen `events` en `products` .
