---
title: state
description: (In ruste) Bevolkt het "Bezoekersrapport", dat niet meer beschikbaar is.
feature: Variables
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# state

>[!IMPORTANT]
>
>Deze variabele wordt gepensioneerd en geen beschikbare dimensie in Analysis Workspace. Gebruik de [VS](/help/components/dimensions/us-states.md) in plaats daarvan, welk AppMeasurement automatisch verzamelt gebaseerd op de plaats van de bezoeker.

In eerdere versies van Adobe Analytics `state` de variabele werd gebruikt wanneer bezoekers verzendinformatie op retailsites invulden . Deze is functioneel identiek aan een proxy, maar is niet beschikbaar in Analysis Workspace.

## Status die de extensie Adobe Analytics gebruikt

U kunt de status instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL State] sectie.

U kunt de status instellen op elke tekenreekswaarde of elk gegevenselement.

## s.state in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.state` variabele is een tekenreeks die doorgaans de staat of provincie van de bezoeker bevat. Volledige statusnamen of codes met twee letters zijn beide geldig. De eigenschap heeft een maximumwaarde van 50 bytes. Langere waarden worden afgekapt. De standaardwaarde is een lege tekenreeks.

```js
s.state = "Utah";
```
