---
title: campagne
description: Vul de dimensie 'Code bijhouden' in.
feature: Variables
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# campagne

De `campaign` variabele is gewijd aan het verzamelen van volgcodes op uw plaats. In eerdere versies van Adobe Analytics had het een speciale behandeling, waarbij het kon worden gebruikt als indeling in de meeste dimensies. In de huidige versie van Adobe Analytics werkt het net als een eVar.

Deze variabele vult de [Trackingcode](/help/components/dimensions/tracking-code.md) dimensie. De waarde wordt doorgaans opgehaald uit een queryreeks met behulp van [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) nutsmethode. Uw organisatie bepaalt echter exact hoe deze variabele moet worden ingesteld.

## Campagne die de SDK van het Web gebruikt

Campagne is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `marketing.trackingCode`.

## Campagne met de Adobe Analytics-extensie

U kunt campagne of terwijl het vormen van de uitbreiding van Analytics (globale variabelen) of onder regels plaatsen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Campaign] sectie.

U kunt campagne aan een waarde of een parameter van het vraagkoord plaatsen.

## s.campagne in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.campaign` variabele is een tekenreeks die doorgaans een trackingcode bevat die wordt gebruikt bij marketingactiviteiten. De maximale lengte is 255 bytes. De waarden langer dan 255 bytes worden automatisch afgebroken wanneer ze naar de Adobe worden verzonden.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
