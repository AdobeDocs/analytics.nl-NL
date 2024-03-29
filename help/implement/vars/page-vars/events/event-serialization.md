---
title: Serienummering voor gebeurtenissen
description: Help metrische gegevens op uw site te dupliceren.
feature: Variables
exl-id: 54de0fd7-9056-44af-bd59-b8eb55fc816e
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Serienummering voor gebeurtenis-id

De rangschikking van gebeurtenissen is het proces om maatregelen uit te voeren om dubbele gebeurtenissen te verhinderen in Analytics rapportering in te gaan. Het dupliceren van gebeurtenissen is belangrijk in gevallen waarin bezoekers de pagina niet willen laten opblazen door maateenheden.

>[!NOTE]
>
>Gegevensbronnen ondersteunen geen serialisatie van gebeurtenissen of deduplicatie.

## Gebeurtenisserienummering instellen

U moet eerst een gebeurtenis instellen [!UICONTROL Unique Event Recording] tot [!UICONTROL Use Event ID] in rapportsuite-instellingen. Zie [Gebeurtenissen geslaagd](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) in de handleiding voor Admin-gebruikers.

Bij het gebruik van gebeurtenis-id&#39;s gebeurt deduplicatie op de volgende niveaus:

* Elke variabele gebruikt zijn eigen lijst voor deduplicatie. Bijvoorbeeld: `event1:ABC` en `event2:ABC` worden beide meegeteld in de rapportage.
* De-duplicatie gebeurt wereldwijd voor alle bezoekers. Indien bezoeker A verzendt `event1:ABC` vervolgens verzendt bezoeker B ook `event1:ABC`, negeert Adobe de tweede instantie van bezoeker B.
* De-duplicatie verloopt niet. Als een bezoeker `event1:ABC` dan komt terug twee jaar later en verzendt `event1:ABC` ook hier negeert Adobe het tweede exemplaar.

>[!TIP]
>
>Als u de duplicatie van de [`purchase`](event-purchase.md) -gebeurtenis, gebruikt u de [`purchaseID`](../purchaseid.md) in plaats daarvan variabele.

## Gebeurtenis-id&#39;s gebruiken met de Web SDK

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md), gebruikt de gebeurtenisrangschikking het gewenste XDM gebied van de gebeurtenis `id`. Het volledige XDM-pad is afhankelijk van de gebeurtenis die u wilt serialiseren.

Als u bijvoorbeeld de metrische waarde voor toevoeging van winkelwagentjes wilt serialiseren, stelt u `xdm.commerce.productListAdds.id` naar de gewenste serienummeringswaarde. Als u Aangepaste gebeurtenis 20 wilt serialiseren, stelt u `xdm._experience.analytics.event1to100.event20` naar de gewenste serienummeringswaarde.

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md), gebruik van gebeurtenisserialisatie `data.__adobe.analytics.events`, volgens tekenreekssyntaxis van AppMeasurement.

## Gebeurtenis-id&#39;s gebruiken met de Adobe Analytics-extensie

U kunt het veld voor de gebeurtenis-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of als een handeling in een regel.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Events] , waarin elke gebeurtenis een [!UICONTROL Event ID] veld.

Geldige waarden zijn alfanumerieke tekens met een lengte tot 20 bytes. Als u een waarde invoert die langer is dan 20 bytes, wordt de waarde door het systeem ingekort tot de eerste 20 bytes.

## Gebeurtenis-id&#39;s gebruiken in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De rangschikking van gebeurtenissen maakt deel uit van `s.events` variabele. Wijs een id toe aan elke gebeurtenis met een dubbele punt in de tekenreeks.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Als voor een gebeurtenis serialisatie is ingeschakeld maar geen serialisatie-id bevat, wordt de gebeurtenis altijd geteld.
