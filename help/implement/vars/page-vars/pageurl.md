---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
feature: Variables
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL wilt overschrijven die automatisch wordt verzameld door AppMeasurement, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE]
>
>Deze variabele is geen beschikbare dimensie in Analysis Workspace. Deze optie is alleen beschikbaar in Data Warehouse- en gegevensfeeds. Bovendien verwijderen de servers van de gegevensinzameling van Adobe deze afmeting van allen [koppeling bijhouden](/help/implement/vars/functions/tl-method.md) verzoeken om afbeeldingen. Als u pagina-URL wilt gebruiken als een dimensie in Analysis Workspace of als u deze dimensie wilt gebruiken in het bijhouden van koppelingen, kunt u overwegen de URL door te geven `pageURL` variabele in een [eVar](evar.md) bij elke hit.

## Pagina-URL met tags in Adobe Experience Platform

De UI van de Inzameling van Gegevens bevolkt automatisch pagina URL. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de **[!UICONTROL Rules]** klikt u op de gewenste regel (of maakt u een regel).
4. Onder **[!UICONTROL Actions]** klikt u op een bestaande **[!UICONTROL Adobe Analytics - Set Variables]** of klik op het pictogram &#39;+&#39;.
5. Stel de **[!UICONTROL Extension]** en de **[!UICONTROL Action Type]** tot **[!UICONTROL Set Variables]**.
6. Zoek de **[!UICONTROL Page URL]** sectie.

U kunt de pagina-URL instellen op elke gewenste tekenreekswaarde.

## s.pageURL in AppMeasurement en aangepaste code-editor

De `s.pageURL` variabele is een tekenreeks die de URL van de pagina bevat. AppMeasurement verzamelt deze variabele automatisch, nochtans kunt u zijn waarde indien gewenst met voeten treden.

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
