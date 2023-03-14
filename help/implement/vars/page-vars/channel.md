---
title: channel
description: Vul de dimensie 'Sitesecties' in.
feature: Variables
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# channel

De `channel` Met een variabele wordt doorgaans het gedeelte van de site opgeslagen waarop een bepaalde pagina is ingeschakeld. Het is handig om te bepalen welke groepen van uw site het populairst zijn. Deze variabele vult de dimensie &#39;Sitesecties&#39;.

## Kanaal dat de SDK van het Web gebruikt

Kanaal is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.siteSection`.

## Kanaal met Adobe Analytics-extensie

U kunt het kanaal instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Channel] sectie.

U kunt het kanaal instellen op elke tekenreekswaarde of elk gegevenselement.

## s.channel in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.channel` variabele is een tekenreeks die doorgaans de sitesectie van de pagina bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
s.channel = "Example site section";
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.channel = digitalData.page.category.primaryCategory;
```
