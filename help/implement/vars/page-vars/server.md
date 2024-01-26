---
title: server
description: Vul de dimensie 'Servers' in.
feature: Variables
exl-id: 7904c3c2-9a91-497e-89d0-9eed9ae7a902
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# server

De `server` de variabele slaat typisch hostname van uw plaats op. Het wordt algemeen gebruikt in rapportreeksen die gegevens van veelvoudige domeinen bevatten. Het is functioneel identiek aan een eigenschap prop.

## Server die de SDK van het Web gebruikt

Server is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.server`.

## Server met Adobe Analytics-extensie

U kunt de server instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Server] sectie.

U kunt de server instellen op elke tekenreekswaarde of elk gegevenselement.

## s.server in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.server` variabele is een tekenreeks die doorgaans de hostnaam van uw site bevat. De eigenschap heeft een maximumwaarde van 100 bytes. De langere waarden worden afgebroken.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
