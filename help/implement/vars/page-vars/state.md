---
title: Staat
description: Vul het "Bezoekersstatusrapport" in Reports and Analytics.
feature: Variables
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# state

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Gebruik in plaats hiervan de dimensie &#39;US States&#39;, die AppMeasurement automatisch verzamelt op basis van de locatie van de bezoeker.

In eerdere versies van Adobe Analytics `state` de variabele werd gebruikt wanneer bezoekers verzendinformatie op retailsites invulden . Deze is functioneel identiek aan een proxy, maar is niet beschikbaar in Analysis Workspace.

## Status met tags in Adobe Experience Platform

U kunt de status instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL State] sectie.

U kunt de status instellen op elke tekenreekswaarde of elk gegevenselement.

## s.state in AppMeasurement en de redacteur van de douanecode

De `s.state` variabele is een tekenreeks die doorgaans de staat of provincie van de bezoeker bevat. Volledige statusnamen of codes met twee letters zijn beide geldig. Het heeft een maximumwaarde van 50 bytes; langere waarden worden afgekapt. De standaardwaarde is een lege tekenreeks.

```js
s.state = "Utah";
```
