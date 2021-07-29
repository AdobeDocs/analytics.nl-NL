---
title: campaign
description: Vul de dimensie 'Code bijhouden' in.
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# campagne

De variabele `campaign` is gewijd aan het verzamelen van volgcodes op uw plaats. In eerdere versies van Adobe Analytics had het een speciale behandeling, waarbij het kon worden gebruikt als indeling in de meeste dimensies. In de huidige versie van Adobe Analytics werkt deze hetzelfde als een eVar.

Deze variabele vult de dimensie &#39;Tracking Code&#39; in.

## Campagne met tags in Adobe Experience Platform

U kunt campagne of terwijl het vormen van de uitbreiding van Analytics (globale variabelen) of onder regels plaatsen.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Campaign].

U kunt campagne aan een waarde of een parameter van het vraagkoord plaatsen.

## s.campagne in AppMeasurement en de redacteur van de douanecode

De `s.campaign` variabele is een koord dat typisch een het volgen code bevat die in marketing inspanningen wordt gebruikt. De maximale lengte is 255 bytes. waarden die langer zijn dan 255 bytes, worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
