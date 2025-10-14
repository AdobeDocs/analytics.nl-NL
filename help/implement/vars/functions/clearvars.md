---
title: clearVars
description: Wis waarden van het instantievoorwerp.
feature: Appmeasurement Implementation
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# clearVars

Sommige implementaties, zoals bij toepassingen van één pagina, vereisen meerdere hits die worden verzonden bij hetzelfde laden van de pagina. Gebruik de methode `clearVars()` om variabelewaarden te wissen zodat deze niet tot volgende treffers blijven bestaan.

Deze methode heeft geen argumenten en retourneert geen waarde. Het enige doel hiervan is het wissen van variabelewaarden uit het instantieobject. Met deze methode worden de volgende elementen ingesteld op `undefined` :

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

## Variabelen wissen met de Web SDK

Wanneer u gegevens naar Adobe verzendt via de Web SDK, worden alle XDM-gegevens automatisch gewist.

## Variabelen wissen met de Adobe Analytics-extensie

Plaats de Duidelijke actie van Variabelen wanneer het vormen van een regel.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op het pictogram &#39;+&#39;
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Clear Variables] .

## s.clearVars() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

U kunt de methode `s.clearVars()` overal in uw implementatie aanroepen nadat u de instantie van het object Analytics hebt geïnstantieerd.

```js
s.clearVars();
```
