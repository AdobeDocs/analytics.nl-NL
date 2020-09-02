---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL wilt overschrijven die automatisch wordt verzameld door AppMeasurement, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE]
>
>Deze variabele is geen beschikbare dimensie in Analysis Workspace. Deze optie is alleen beschikbaar in Data Warehouse- en gegevensfeeds. Bovendien verwijderen de servers van de gegevensinzameling van Adobe deze afmeting van alle [verbinding die beeldverzoeken volgen](/help/implement/vars/functions/tl-method.md) . Als u pagina-URL als een dimensie wilt gebruiken in Analysis Workspace of als u deze dimensie wilt gebruiken in het bijhouden van koppelingen, kunt u overwegen de `pageURL` variabele in een [eVar](evar.md) door te geven bij elke treffer.

## Pagina-URL in Adobe Experience Platform Launch

Met Starten wordt de pagina-URL automatisch ingevuld. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het **[!UICONTROL Rules]** lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder **[!UICONTROL Actions]** op een bestaande **[!UICONTROL Adobe Analytics - Set Variables]** handeling of klik op het pictogram ‘+’.
5. Stel het **[!UICONTROL Extension]** vervolgkeuzemenu in op Adobe Analytics en **[!UICONTROL Action Type]** op **[!UICONTROL Set Variables]**.
6. Zoek de **[!UICONTROL Page URL]** sectie.

U kunt de pagina-URL instellen op elke gewenste tekenreekswaarde.

## s.pageURL in de aangepaste code-editor van AppMeasurement en Launch

De `s.pageURL` variabele is een tekenreeks die de URL van de pagina bevat. AppMeasurement verzamelt deze variabele automatisch, nochtans kunt u zijn waarde indien gewenst met voeten treden.

```js
s.pageURL = "https://example.com";
```

Als u pagina URL als afmeting in rapporten wilt gebruiken, denk na gebruikend het volgende in uw implementatie:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

Als u de `digitalData` gegevenslaag [](../../prepare/data-layer.md)gebruikt:

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
