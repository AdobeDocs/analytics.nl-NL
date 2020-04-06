---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL wilt overschrijven die automatisch wordt verzameld door AppMeasurement, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE] Deze variabele is geen beschikbare dimensie in de Werkruimte van de Analyse. Het is alleen beschikbaar in Data Warehouse en Data Feeds. Als u pagina URL als afmeting in de Werkruimte van de Analyse zou willen gebruiken, denk overgaand de `pageURL` variabele in een eVar op elke slag.

Soms zijn URL&#39;s langer dan 255 bytes. AppMeasurement gebruikt de parameter van het `g` vraagkoord voor de eerste 255 bytes van URL in beeldverzoeken. Als een URL langer is dan 255 bytes, wordt de rest van URL opgeslagen in de parameter van het `-g` vraagkoord. Protocol- en querytekenreeksen in de URL worden opgenomen in deze variabele.

## Pagina-URL in Adobe Experience Platform Launch

Met Starten wordt de pagina-URL automatisch ingevuld. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Page URL] sectie.

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
