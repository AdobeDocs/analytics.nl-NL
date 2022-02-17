---
title: clearVars
description: Wist de volgende waarden van het instantieobject. Deze functie verwijdert de elementen (plaatst hen als "undefined.")
feature: Variables
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---

# clearVars

Sommige implementaties, zoals bij toepassingen van één pagina, vereisen meerdere hits die worden verzonden bij hetzelfde laden van de pagina. Gebruik de `clearVars()` methode om veranderlijke waarden te ontruimen zodat blijven zij niet aan verdere klappen.

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

## Variabelen wissen met tags in Adobe Experience Platform

Plaats de Duidelijke actie van Variabelen wanneer het vormen van een regel.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op het pictogram &#39;+&#39;
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Clear Variables].

## s.clearVars() in AppMeasurement en aangepaste code-editor

U kunt de `s.clearVars()` methode op een willekeurige locatie in de implementatie nadat u de instantie van het object Analytics hebt geïnstantieerd.

```js
s.clearVars();
```
