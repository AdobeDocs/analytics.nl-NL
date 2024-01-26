---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
feature: Variables
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL die automatisch door het AppMeasurement wordt verzameld, wilt overschrijven, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE]
>
>Deze variabele is geen beschikbare dimensie in Analysis Workspace. Deze optie is alleen beschikbaar in Data Warehouse- en gegevensfeeds. Bovendien verwijderen de servers van de gegevensinzameling van de Adobe deze afmeting van allen [koppeling bijhouden](/help/implement/vars/functions/tl-method.md) verzoeken om afbeeldingen. Als u pagina-URL wilt gebruiken als een dimensie in Analysis Workspace of als u deze dimensie wilt gebruiken in het bijhouden van koppelingen, kunt u overwegen de URL door te geven `pageURL` variabele in een [eVar](evar.md) bij elke hit.

## Pagina-URL met de Web SDK

Pagina-URL is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webPageDetails.URL`.

## Pagina-URL met de Adobe Analytics-extensie

De extensie Analytics in Adobe Experience Platform Data Collection vult automatisch pagina-URL in. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de **[!UICONTROL Rules]** klikt u op de gewenste regel (of maakt u een regel).
4. Onder **[!UICONTROL Actions]**, klikt u op een bestaande **[!UICONTROL Adobe Analytics - Set Variables]** of klik op het pictogram &#39;+&#39;.
5. Stel de **[!UICONTROL Extension]** vervolgkeuzelijst naar Adobe Analytics en de **[!UICONTROL Action Type]** tot **[!UICONTROL Set Variables]**.
6. Zoek de **[!UICONTROL Page URL]** sectie.

U kunt de pagina-URL instellen op elke gewenste tekenreekswaarde.

## s.pageURL in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.pageURL` variabele is een tekenreeks die de URL van de pagina bevat. AppMeasurement verzamelt deze variabele automatisch, maar u kunt desgewenst de waarde ervan overschrijven.

```js
s.pageURL = "https://example.com";
```

Als u pagina URL als afmeting in rapporten wilt gebruiken, denk na gebruikend het volgende in uw implementatie:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
