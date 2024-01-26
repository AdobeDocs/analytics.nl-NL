---
title: pageName
description: De naam van de pagina op uw site.
feature: Variables
exl-id: 24ac40a9-f0e7-4534-abf2-2397f5fe16c2
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# pageName

De `pageName` In een variabele wordt doorgaans de naam van een bepaalde pagina opgeslagen. Het is handig om te bepalen welke afzonderlijke pagina&#39;s het populairst zijn. Deze variabele vult de [Pagina](/help/components/dimensions/page.md) dimensie.

Als deze variabele niet op een bepaalde pagina volgende vraag wordt bepaald, [`pageURL`](pageurl.md) in plaats daarvan wordt een variabele gebruikt.

>[!NOTE]
>
>De servers van de gegevensinzameling van de Adobe verwijderen deze afmeting van allen [koppeling bijhouden](/help/implement/vars/functions/tl-method.md) verzoeken om afbeeldingen. Als u deze dimensie wilt weergeven in het bijhouden van koppelingen, kunt u deze dimensie kopiëren naar een [eVar](evar.md).

## Paginanaam met de Web SDK

Pagina is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.name`.

## Paginanaam met de Adobe Analytics-extensie

U kunt paginanaam instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions], klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Page name] sectie.

U kunt de paginanaam instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.pageName in AppMeasurement en de de coderedacteur van de de uitbreidingsuitbreiding van de Analyse

De `s.pageName` variabele is een tekenreeks die doorgaans de naam van de pagina bevat. De eigenschap heeft een maximumwaarde van 100 bytes. De langere waarden worden afgebroken. Deze afkapping omvat ook gevallen waarin de waarde terugvalt `pageURL` als deze variabele leeg is.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
