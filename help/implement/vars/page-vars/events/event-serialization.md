---
title: Gebeurtenisserialisatie
description: Help metrische gegevens op uw site te dupliceren.
exl-id: 54de0fd7-9056-44af-bd59-b8eb55fc816e
translation-type: tm+mt
source-git-commit: 71581f49eb7ef13577a05c05daee737eeb9e6218
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Serienummering voor gebeurtenis-id

De rangschikking van gebeurtenissen is het proces om maatregelen uit te voeren om dubbele gebeurtenissen te verhinderen in Analytics rapportering in te gaan. Het dupliceren van gebeurtenissen is belangrijk in gevallen waarin bezoekers de pagina niet willen laten opblazen door maateenheden.

>[!NOTE]
>
>Gegevensbronnen ondersteunen geen serialisatie van gebeurtenissen of deduplicatie.

## Gebeurtenisserienummering instellen

U moet eerst de [!UICONTROL Unique Event Recording] van een gebeurtenis aan [!UICONTROL Use Event ID] in de montages van de rapportreeks plaatsen. Zie [Gebeurtenissen met succes](/help/admin/admin/c-success-events/success-event.md) in de gebruikershandleiding voor Admin.

Bij het gebruik van gebeurtenis-id&#39;s gebeurt deduplicatie op de volgende niveaus:

* Elke variabele gebruikt zijn eigen lijst voor deduplicatie. `event1:ABC` en `event2:ABC` worden bijvoorbeeld beide geteld in de rapportage.
* De-duplicatie gebeurt wereldwijd voor alle bezoekers. Als bezoeker A `event1:ABC` verzendt dan verzendt bezoeker B ook `event1:ABC`, negeert Adobe de tweede instantie van bezoeker B.
* De-duplicatie verloopt niet. Als een bezoeker `event1:ABC` dan terugkomt twee jaar later en `event1:ABC` opnieuw verzendt, negeert Adobe de tweede instantie.

>[!TIP]
>
>Als u de gebeurtenis [`purchase`](event-purchase.md) wilt dedupliceren, gebruikt u in plaats daarvan de variabele [`purchaseID`](../purchaseid.md).

## Gebeurtenis-id&#39;s gebruiken in Adobe Experience Platform Launch

U kunt het veld voor de gebeurtenis-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of als een handeling in een regel.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Events], waarin elke gebeurtenis een veld [!UICONTROL Event ID] bevat.

Geldige waarden zijn alfanumerieke tekens met een lengte tot 20 bytes. Als u een waarde invoert die langer is dan 20 bytes, wordt de waarde door het systeem ingekort tot de eerste 20 bytes.

## Gebeurtenis-id&#39;s gebruiken in de aangepaste code-editor van AppMeasurement en Launch

De rangschikking van de gebeurtenis maakt deel uit van `s.events` variabele. Wijs een id toe aan elke gebeurtenis met een dubbele punt in de tekenreeks.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Als voor een gebeurtenis serialisatie is ingeschakeld maar geen serialisatie-id bevat, wordt de gebeurtenis altijd geteld.
