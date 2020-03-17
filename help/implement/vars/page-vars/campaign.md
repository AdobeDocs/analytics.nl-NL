---
title: campagne
description: Vul de dimensie 'Code bijhouden' in.
translation-type: tm+mt
source-git-commit: c5a60bc9756af2742740dbc6a26a081f55ee3235

---


# campagne

De `campaign` variabele wordt gewijd aan het verzamelen van volgcodes op uw plaats. In eerdere versies van Adobe Analytics was er een speciale behandeling voor de plaats waar deze kon worden gebruikt als indeling in de meeste dimensies. In de huidige versie van Adobe Analytics werkt deze hetzelfde als een eVar.

Deze variabele vult de dimensie &#39;Tracking Code&#39; in.

## Campagne in Adobe Experience Platform Launch

U kunt campagne of terwijl het vormen van de uitbreiding van Analytics (globale variabelen) of onder regels plaatsen.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Campaign] sectie.

U kunt campagne aan een waarde of een parameter van het vraagkoord plaatsen.

## s.campagne in de redacteur van de douanecode van AppMeasurement en van de Lancering

De `s.campaign` variabele is een tekenreeks die doorgaans een trackingcode bevat die wordt gebruikt bij marketingactiviteiten. De maximale lengte is 255 bytes. Als waarden langer zijn dan 100 bytes, worden deze automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
