---
title: Serienummering voor gebeurtenissen
description: Help metrische gegevens op uw site te dupliceren.
feature: Appmeasurement Implementation
exl-id: 54de0fd7-9056-44af-bd59-b8eb55fc816e
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
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

U moet eerst de gebeurtenis [!UICONTROL Unique Event Recording] instellen op [!UICONTROL Use Event ID] in de instellingen van de rapportsuite. Zie [ Gebeurtenissen van het Succes ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) in de Admin gebruikersgids.

Bij het gebruik van gebeurtenis-id&#39;s gebeurt deduplicatie op de volgende niveaus:

* Elke variabele gebruikt zijn eigen lijst voor deduplicatie. `event1:ABC` en `event2:ABC` worden bijvoorbeeld allebei geteld in rapportage.
* De-duplicatie gebeurt wereldwijd voor alle bezoekers. Als bezoeker A `event1:ABC` verzendt, verzendt bezoeker B ook `event1:ABC` , negeert Adobe de tweede instantie van bezoeker B.
* De-duplicatie verloopt niet. Als een bezoeker `event1:ABC` verzendt, dan twee jaar later terugkomt en `event1:ABC` opnieuw verzendt, negeert Adobe de tweede instantie.

>[!TIP]
>
>Als u de gebeurtenis [`purchase`](event-purchase.md) wilt dedupliceren, gebruikt u in plaats daarvan de variabele [`purchaseID`](../purchaseid.md) .

## Gebeurtenis-id&#39;s gebruiken met de Web SDK

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), gebruikt de gebeurtenisrangschikking het gewenste gebied van XDM van de gebeurtenis `id`. Het volledige XDM-pad is afhankelijk van de gebeurtenis die u wilt serialiseren.

Stel `xdm.commerce.productListAdds.id` in op de gewenste serienummeringswaarde als u bijvoorbeeld de metrische waarde van Kart-toevoegingen wilt serialiseren. Als u Custom-gebeurtenis 20 wilt serialiseren, stelt u `xdm._experience.analytics.event1to100.event20` in op de gewenste serienummeringswaarde.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruikt de gebeurtenisrangschikking `data.__adobe.analytics.events`, na het koordsyntaxis van AppMeasurement.

## Gebeurtenis-id&#39;s gebruiken met de Adobe Analytics-extensie

U kunt het veld voor de gebeurtenis-id instellen tijdens het configureren van de extensie Analytics (globale variabelen) of als een handeling in een regel.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Events] , waarin elke gebeurtenis een veld [!UICONTROL Event ID] bevat.

Geldige waarden zijn alfanumerieke tekens met een lengte tot 20 bytes. Als u een waarde invoert die langer is dan 20 bytes, wordt de waarde door het systeem ingekort tot de eerste 20 bytes.

## Gebeurtenis-id&#39;s gebruiken in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Serienummering voor gebeurtenissen maakt deel uit van de variabele `s.events` . Wijs een id toe aan elke gebeurtenis met een dubbele punt in de tekenreeks.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Als voor een gebeurtenis serialisatie is ingeschakeld maar geen serialisatie-id bevat, wordt de gebeurtenis altijd geteld.
