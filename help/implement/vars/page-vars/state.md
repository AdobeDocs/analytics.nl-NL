---
title: Staat
description: Vul het "Bezoekersstatusrapport" in Reports and Analytics.
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# state

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Gebruik in plaats hiervan de dimensie &#39;US States&#39;, die AppMeasurement automatisch verzamelt op basis van de locatie van de bezoeker.

In vorige versies van Adobe Analytics werd de variabele `state` gebruikt toen bezoekers verzendgegevens op winkelsites invulden. Deze is functioneel identiek aan een proxy, maar is niet beschikbaar in Analysis Workspace.

## Status met tags in Adobe Experience Platform

U kunt status instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL State].

U kunt de status instellen op elke tekenreekswaarde of elk gegevenselement.

## s.state in AppMeasurement en de redacteur van de douanecode

De variabele `s.state` is een tekenreeks die doorgaans de staat of provincie van de bezoeker bevat. Volledige statusnamen of codes met twee letters zijn beide geldig. Het heeft een maximumwaarde van 50 bytes; langere waarden worden afgekapt. De standaardwaarde is een lege tekenreeks.

```js
s.state = "Utah";
```
