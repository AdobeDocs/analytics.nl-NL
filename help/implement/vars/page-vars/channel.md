---
title: channel
description: Vul de dimensie 'Sitesecties' in.
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# kanaal

In de variabele `channel` wordt doorgaans het gedeelte van de site opgeslagen waarop een bepaalde pagina is ingeschakeld. Het is handig om te bepalen welke groepen van uw site het populairst zijn. Deze variabele vult de dimensie &#39;Sitesecties&#39;.

## Kanaal met tags in Adobe Experience Platform

U kunt het kanaal instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Channel].

U kunt het kanaal instellen op elke tekenreekswaarde of elk gegevenselement.

## s.channel in AppMeasurement en aangepaste code-editor

De variabele `s.channel` is een tekenreeks die doorgaans de sitesectie van de pagina bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
s.channel = "Example site section";
```

Bij gebruik van de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.channel = digitalData.page.category.primaryCategory;
```
