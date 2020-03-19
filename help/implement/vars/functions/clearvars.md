---
title: clearVars
description: Wist de volgende waarden van het instantieobject. Deze functie verwijdert de elementen (plaatst hen als "undefined.")
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# clearVars

Sommige implementaties, zoals bij toepassingen van één pagina, vereisen meerdere hits die worden verzonden bij hetzelfde laden van de pagina. Gebruik de `clearVars()` methode om veranderlijke waarden te ontruimen zodat blijven zij aan verdere klappen.

Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel hiervan is het wissen van variabelewaarden uit het instantieobject. Met deze methode worden de volgende elementen ingesteld op `undefined`:

* `prop1` - `prop75`
* `eVar` - `eVar250`
* `hier1` - `hier5`
* `list1` - `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## Variabelen wissen in Adobe Experience Platform Launch

Plaats de Duidelijke actie van Variabelen wanneer het vormen van een regel.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Clear Variables].

## s.clearVars() in de aangepaste code-editor AppMeasurement en Launch

U kunt de `s.clearVars()` methode overal in uw implementatie aanroepen nadat u de instantie van het object Analytics hebt geïnstantieerd.

```js
s.clearVars();
```
