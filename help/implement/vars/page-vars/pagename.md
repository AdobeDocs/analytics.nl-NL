---
title: pageName
description: De naam van de pagina op uw site.
exl-id: 24ac40a9-f0e7-4534-abf2-2397f5fe16c2
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# pageName

In de variabele `pageName` wordt doorgaans de naam van een bepaalde pagina opgeslagen. Het is handig om te bepalen welke afzonderlijke pagina&#39;s het populairst zijn. Deze variabele vult de [Page](/help/components/dimensions/page.md) dimensie.

Als deze variabele niet op een bepaalde pagina het volgen vraag wordt bepaald, wordt [`pageURL`](pageurl.md) variabele gebruikt in plaats daarvan.

>[!NOTE]
>
>De servers van de gegevensinzameling van Adobe ontdoen deze afmeting van alle [verbinding het volgen](/help/implement/vars/functions/tl-method.md) beeldverzoeken. Als u deze afmeting in verbindingsvolgtreffers wilt verschijnen, denk na kopieerend deze afmeting in [eVar](evar.md).

## Paginanaam met tags in Adobe Experience Platform

U kunt paginanaam instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande handeling [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de sectie [!UICONTROL Page name].

U kunt de paginanaam instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.pageName in AppMeasurement en aangepaste code-editor

De variabele `s.pageName` is een tekenreeks die doorgaans de naam van de pagina bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt. Deze afkapping omvat instanties waar het terug naar `pageURL` valt als deze variabele leeg is.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```

Bij gebruik van de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
