---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL wilt overschrijven die automatisch wordt verzameld door AppMeasurement, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE]
>
>Deze variabele is geen beschikbare dimensie in Analysis Workspace. Deze optie is alleen beschikbaar in Data Warehouse- en gegevensfeeds. Bovendien verwijderen de servers van de gegevensinzameling van Adobe deze afmeting van alle [verbinding het volgen](/help/implement/vars/functions/tl-method.md) beeldverzoeken. Als u pagina URL als afmeting in Analysis Workspace wilt gebruiken of deze afmeting in verbindingsvolgtreffers wilt, denk na overgaand de `pageURL` variabele in [eVar](evar.md) op elke slag.

## Pagina-URL met tags in Adobe Experience Platform

De UI van de Inzameling van Gegevens bevolkt automatisch pagina URL. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het **[!UICONTROL Rules]** lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder **[!UICONTROL Actions]** op een bestaande handeling **[!UICONTROL Adobe Analytics - Set Variables]** of klik op het pictogram &#39;+&#39;.
5. Stel het vervolgkeuzemenu **[!UICONTROL Extension]** in op Adobe Analytics en **[!UICONTROL Action Type]** op **[!UICONTROL Set Variables]**.
6. Zoek de sectie **[!UICONTROL Page URL]**.

U kunt de pagina-URL instellen op elke gewenste tekenreekswaarde.

## s.pageURL in AppMeasurement en aangepaste code-editor

De variabele `s.pageURL` is een tekenreeks die de URL van de pagina bevat. AppMeasurement verzamelt deze variabele automatisch, nochtans kunt u zijn waarde indien gewenst met voeten treden.

```js
s.pageURL = "https://example.com";
```

Als u pagina URL als afmeting in rapporten wilt gebruiken, denk na gebruikend het volgende in uw implementatie:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

Bij gebruik van de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
