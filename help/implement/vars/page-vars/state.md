---
title: Staat
description: Vul het "Bezoekersrapport" in Rapporten en Analytics.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# state

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Gebruik in plaats hiervan de dimensie &#39;US States&#39;, die AppMeasurement automatisch verzamelt op basis van de locatie van de bezoeker.

In eerdere versies van Adobe Analytics werd de `state` variabele gebruikt toen bezoekers verzendgegevens op winkelsites invulden. Deze is functioneel identiek aan een proxy, maar is niet beschikbaar in Analysis Workspace.

## Status in Adobe Experience Platform Launch

U kunt de status instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL State] sectie.

U kunt de status instellen op elke tekenreekswaarde of elk gegevenselement.

## s.state in AppMeasurement en Launch de redacteur van de douanecode

De `s.state` variabele is een tekenreeks die doorgaans de staat of provincie van de bezoeker bevat. Volledige statusnamen of codes met twee letters zijn beide geldig. Het heeft een maximumwaarde van 50 bytes; langere waarden worden afgekapt. De standaardwaarde is een lege tekenreeks.

```js
s.state = "Utah";
```
