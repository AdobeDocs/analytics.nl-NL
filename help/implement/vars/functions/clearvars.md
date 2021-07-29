---
title: clearVars
description: Wist de volgende waarden van het instantieobject. Deze functie verwijdert de elementen (plaatst hen als "undefined.")
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---

# clearVars

Sommige implementaties, zoals bij toepassingen van één pagina, vereisen meerdere hits die worden verzonden bij hetzelfde laden van de pagina. Gebruik de methode `clearVars()` om veranderlijke waarden te ontruimen zodat houden zij niet aan verdere klappen voort.

Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel hiervan is het wissen van variabelewaarden uit het instantieobject. Met deze methode worden de volgende elementen ingesteld op `undefined`:

* `prop1` - `prop75`
* `eVar` -  `eVar250`
* `hier1` -  `hier5`
* `list1` -  `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## Variabelen wissen met tags in Adobe Experience Platform

Plaats de Duidelijke actie van Variabelen wanneer het vormen van een regel.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op het pictogram &#39;+&#39;
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Clear Variables].

## s.clearVars() in AppMeasurement en aangepaste code-editor

U kunt de `s.clearVars()` methode overal in uw implementatie roepen nadat u de het objecten van de Analyse instantie concretiseert.

```js
s.clearVars();
```
