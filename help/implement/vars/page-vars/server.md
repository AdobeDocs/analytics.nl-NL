---
title: server
description: Vul de dimensie 'Servers' in.
feature: Variables
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 1%

---

# server

De `server` de variabele slaat typisch hostname van uw plaats op. Het wordt algemeen gebruikt in rapportreeksen die gegevens van veelvoudige domeinen bevatten. Het is functioneel identiek aan een eigenschap prop.

## Server met tags in Adobe Experience Platform

U kunt de server instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Server] sectie.

U kunt de server instellen op elke tekenreekswaarde of elk gegevenselement.

## s.server in AppMeasurement en de redacteur van de douanecode

De `s.server` variabele is een tekenreeks die doorgaans de hostnaam van uw site bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
