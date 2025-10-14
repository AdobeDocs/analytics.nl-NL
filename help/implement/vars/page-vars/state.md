---
title: state
description: (In ruste) Bevolkt het "Bezoekersrapport", dat niet meer beschikbaar is.
feature: Appmeasurement Implementation
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# state

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Gebruik in plaats hiervan de [&#x200B; dimensie van Staten van de V.S. &#x200B;](/help/components/dimensions/us-states.md), die AppMeasurement automatisch verzamelt die op de plaats van de bezoeker wordt gebaseerd.

In eerdere versies van Adobe Analytics werd de variabele `state` gebruikt toen bezoekers verzendgegevens op winkelsites invulden. Deze is functioneel identiek aan een proxy, maar is niet beschikbaar in Analysis Workspace.

## Status die de extensie Adobe Analytics gebruikt

U kunt de status instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL State] .

U kunt de status instellen op elke tekenreekswaarde of elk gegevenselement.

## s.state in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.state` is een tekenreeks die doorgaans de staat of provincie van de bezoeker bevat. Volledige statusnamen of codes met twee letters zijn beide geldig. De eigenschap heeft een maximumwaarde van 50 bytes. Langere waarden worden afgekapt. De standaardwaarde is een lege tekenreeks.

```js
s.state = "Utah";
```
