---
title: server
description: Vul de dimensie 'Servers' in.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# server

De `server` variabele slaat typisch hostname van uw plaats op. Het wordt algemeen gebruikt in rapportreeksen die gegevens van veelvoudige domeinen bevatten. Het is functioneel identiek aan een eigenschap prop.

## Server in Adobe Experience Platform Launch

U kunt de server instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Server] sectie.

U kunt de server instellen op elke tekenreekswaarde of elk gegevenselement.

## s.server in AppMeasurement en Launch de redacteur van de douanecode

De `s.server` variabele is een tekenreeks die doorgaans de hostnaam van uw site bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
