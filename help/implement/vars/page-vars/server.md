---
title: server
description: Vul de dimensie 'Servers' in.
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 1%

---

# server

In de variabele `server` wordt doorgaans de hostnaam van uw site opgeslagen. Het wordt algemeen gebruikt in rapportreeksen die gegevens van veelvoudige domeinen bevatten. Het is functioneel identiek aan een eigenschap prop.

## Server met tags in Adobe Experience Platform

U kunt de server instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Server].

U kunt de server instellen op elke tekenreekswaarde of elk gegevenselement.

## s.server in AppMeasurement en de redacteur van de douanecode

De variabele `s.server` is een tekenreeks die doorgaans de hostnaam van uw site bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
