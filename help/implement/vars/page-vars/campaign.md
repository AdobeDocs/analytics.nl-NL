---
title: campagne
description: Vul de dimensie 'Code bijhouden' in.
feature: Appmeasurement Implementation
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# campagne

De variabele `campaign` is bedoeld voor het verzamelen van trackingcodes op uw site. In eerdere versies van Adobe Analytics had het een speciale behandeling, waarbij het kon worden gebruikt als indeling in de meeste dimensies. In de huidige versie van Adobe Analytics werkt het net als een eVar.

Deze variabele bevolkt de [ het Volgen dimensie van de Code ](/help/components/dimensions/tracking-code.md). De waarde wordt doorgaans opgehaald uit een queryreeks met behulp van de hulpprogrammamethode [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) . Uw organisatie bepaalt echter exact hoe deze variabele moet worden ingesteld.

## Campagne met de Web SDK

De campagne wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `marketing.trackingCode`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.campaign` of `data.__adobe.analytics.v0`

## Campagne met de Adobe Analytics-extensie

U kunt campagne of terwijl het vormen van de uitbreiding van Analytics (globale variabelen) of onder regels plaatsen.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Campaign] .

U kunt campagne aan een waarde of een parameter van het vraagkoord plaatsen.

## s.campagne in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.campaign` is een tekenreeks die doorgaans een trackingcode bevat die wordt gebruikt bij marketingactiviteiten. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgebroken wanneer ze naar Adobe worden verzonden.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
