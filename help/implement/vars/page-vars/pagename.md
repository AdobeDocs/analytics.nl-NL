---
title: pageName
description: De naam van de pagina op uw site.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# pageName

In de `pageName` variabele wordt doorgaans de naam van een bepaalde pagina opgeslagen. Het is handig om te bepalen welke afzonderlijke pagina&#39;s het populairst zijn. Deze variabele vult de dimensie &#39;Paginanaam&#39;.

> [!NOTE] Deze dimensie wordt altijd gestript van verbinding het volgen vraag. Als u de paginanaam wilt zien waar een verbinding werd gevolgd, overweeg het kopiëren van deze variabele in een eVar.

Als deze variabele niet op een bepaalde pagina het volgen vraag wordt bepaald, wordt de [`pageURL`](pageurl.md) variabele in plaats daarvan gebruikt.

## Paginanaam in Adobe Experience Platform Launch

U kunt paginanaam instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Page name] sectie.

U kunt de paginanaam instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.pageName in AppMeasurement en Launch, aangepaste code-editor

De `s.pageName` variabele is een tekenreeks die doorgaans de naam van de pagina bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt. Deze afkapping omvat ook instanties waar het terug naar valt `pageURL` als deze variabele leeg is.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
