---
title: kanaal
description: Vul de dimensie 'Sitesecties' in.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# kanaal

In de `channel` variabele wordt doorgaans het gedeelte van de site opgeslagen waarop een bepaalde pagina is ingeschakeld. Het is handig om te bepalen welke groepen van uw site het populairst zijn. Deze variabele vult de dimensie &#39;Sitesecties&#39;.

## Kanaal in Adobe Experience Platform Starten

U kunt het kanaal instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Channel] sectie.

U kunt het kanaal instellen op elke tekenreekswaarde of elk gegevenselement.

## s.channel in de aangepaste code-editor AppMeturement en Launch

De `s.channel` variabele is een tekenreeks die doorgaans de sitesectie van de pagina bevat. Het heeft een maximumwaarde van 100 bytes; langere waarden worden afgekapt.

```js
s.channel = "Example site section";
```
