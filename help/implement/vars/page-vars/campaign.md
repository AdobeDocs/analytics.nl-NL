---
title: campaign
description: Vul de dimensie 'Code bijhouden' in.
feature: Variables
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# campagne

De `campaign` variabele is gewijd aan het verzamelen van volgcodes op uw plaats. In eerdere versies van Adobe Analytics had het een speciale behandeling, waarbij het kon worden gebruikt als indeling in de meeste dimensies. In de huidige versie van Adobe Analytics werkt deze hetzelfde als een eVar.

Deze variabele vult de dimensie &#39;Tracking Code&#39; in.

## Campagne met tags in Adobe Experience Platform

U kunt campagne of terwijl het vormen van de uitbreiding van Analytics (globale variabelen) of onder regels plaatsen.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Campaign] sectie.

U kunt campagne aan een waarde of een parameter van het vraagkoord plaatsen.

## s.campagne in AppMeasurement en de redacteur van de douanecode

De `s.campaign` variabele is een tekenreeks die doorgaans een trackingcode bevat die wordt gebruikt bij marketingactiviteiten. De maximale lengte is 255 bytes. waarden die langer zijn dan 255 bytes, worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
