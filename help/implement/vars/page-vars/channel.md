---
title: kanaal
description: Vul de dimensie 'Secties site' in.
feature: Variables
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# kanaal

De `channel` Met een variabele wordt doorgaans het gedeelte van de site opgeslagen waarop een bepaalde pagina is ingeschakeld. Het is handig om te bepalen welke groepen van uw site het populairst zijn. Deze variabele vult de dimensie &#39;Sitesecties&#39;.

## Kanaal dat de SDK van het Web gebruikt

Kanaal is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.siteSection`.

## Kanaal met Adobe Analytics-extensie

U kunt het kanaal instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Channel] sectie.

U kunt het kanaal instellen op elke tekenreekswaarde of elk gegevenselement.

## s.channel in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.channel` variabele is een tekenreeks die doorgaans de sitesectie van de pagina bevat. De eigenschap heeft een maximumwaarde van 100 bytes. De langere waarden worden afgebroken.

```js
s.channel = "Example site section";
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.channel = digitalData.page.category.primaryCategory;
```
