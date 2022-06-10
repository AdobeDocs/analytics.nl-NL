---
title: clearVars
description: Wist de volgende waarden van het instantieobject. Deze functie verwijdert de elementen (plaatst hen als "undefined.")
feature: Variables
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '191'
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

## Variabelen wissen met de SDK van het web

Wanneer u gegevens naar Adobe verzendt gebruikend het Web SDK, worden alle gegevens XDM automatisch ontruimd.

## Variabelen wissen met de Adobe Analytics-extensie

Plaats de Duidelijke actie van Variabelen wanneer het vormen van een regel.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op het pictogram &#39;+&#39;
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Clear Variables].

## s.clearVars() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

U kunt de `s.clearVars()` methode op een willekeurige locatie in de implementatie nadat u de instantie van het object Analytics hebt geïnstantieerd.

```js
s.clearVars();
```
