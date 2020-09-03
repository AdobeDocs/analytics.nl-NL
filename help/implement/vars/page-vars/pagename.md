---
title: pageName
description: De naam van de pagina op uw site.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---


# pageName

In de `pageName` variabele wordt doorgaans de naam van een bepaalde pagina opgeslagen. Het is handig om te bepalen welke afzonderlijke pagina&#39;s het populairst zijn. Met deze variabele wordt de dimensie [Pagina](/help/components/dimensions/page.md) gevuld.

Als deze variabele niet op een bepaalde pagina het volgen vraag wordt bepaald, wordt de [`pageURL`](pageurl.md) variabele in plaats daarvan gebruikt.

>[!NOTE]
>
>De servers van de gegevensinzameling van Adobe ontdoen deze afmeting van alle [verbinding die beeldverzoeken volgen](/help/implement/vars/functions/tl-method.md) . Als u deze dimensie wilt weergeven in het bijhouden van koppelingen, kunt u deze dimensie kopiëren naar een [eVar](evar.md).

## Paginanaam in Adobe Experience Platform Launch

U kunt paginanaam instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
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

Als u de `digitalData` gegevenslaag [](../../prepare/data-layer.md)gebruikt:

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
