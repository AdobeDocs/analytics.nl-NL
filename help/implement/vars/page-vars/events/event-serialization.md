---
title: Serienummering voor gebeurtenissen
description: Help metrische gegevens op uw site te dupliceren.
translation-type: tm+mt
source-git-commit: c5a60bc9756af2742740dbc6a26a081f55ee3235

---


# Serienummering voor gebeurtenis-id

De rangschikking van gebeurtenissen is het proces om maatregelen uit te voeren om dubbele gebeurtenissen te verhinderen in Analytics rapportering in te gaan. Het dupliceren van gebeurtenissen is belangrijk in gevallen waarin bezoekers de pagina niet willen laten opblazen door maateenheden.

> [!NOTE] Gegevensbronnen ondersteunen geen serialisatie van gebeurtenissen of deduplicatie.

## Gebeurtenisserienummering instellen

U moet een gebeurtenis eerst instellen [!UICONTROL Unique Event Recording] op [!UICONTROL Use Event ID] de instellingen van de rapportsuite. Zie Gebeurtenissen [geslaagd](../../../../admin/admin/c-success-events/success-event.md) in de gebruikershandleiding voor Admin.

Bij het gebruik van gebeurtenis-id&#39;s gebeurt deduplicatie op de volgende niveaus:

* Elke variabele gebruikt zijn eigen lijst voor deduplicatie. Bijvoorbeeld, `event1:ABC` en `event2:ABC` worden allebei geteld in rapportering.
* De-duplicatie gebeurt wereldwijd voor alle bezoekers. Als bezoeker A `event1:ABC` dan ook bezoeker B verzendt `event1:ABC`, negeert Adobe het tweede exemplaar van bezoeker B.
* De-duplicatie verloopt niet. Als een bezoeker `event1:ABC` dan twee jaar later terugkomt en `event1:ABC` opnieuw verzendt, negeert Adobe het tweede exemplaar.

> [!TIP] Als u de duplicatie van de `purchase` gebeurtenis wilt opheffen, gebruikt u de `purchaseID` variabele.

## Gebeurtenis-id&#39;s gebruiken in Adobe Experience Platform Starten

U kunt het veld voor de gebeurtenis-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of als een handeling in een regel.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] sectie waar elke gebeurtenis een [!UICONTROL Event ID] veld bevat.

Geldige waarden zijn alfanumerieke tekens met een lengte tot 20 bytes.

## Gebeurtenis-id&#39;s gebruiken in de aangepaste code-editor van AppMeasurement en Launch

De rangschikking van de gebeurtenis maakt deel uit van de `s.events` variabele. Wijs een id toe aan elke gebeurtenis met een dubbele punt in de tekenreeks.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Als voor een gebeurtenis serialisatie is ingeschakeld maar geen serialisatie-id bevat, wordt de gebeurtenis altijd geteld.
