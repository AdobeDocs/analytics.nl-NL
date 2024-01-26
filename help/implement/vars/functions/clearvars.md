---
title: clearVars
description: Wis waarden van het instantievoorwerp.
feature: Variables
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

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
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Clear Variables].

## s.clearVars() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

U kunt de `s.clearVars()` methode op een willekeurige locatie in de implementatie nadat u de instantie van het object Analytics hebt geïnstantieerd.

```js
s.clearVars();
```
