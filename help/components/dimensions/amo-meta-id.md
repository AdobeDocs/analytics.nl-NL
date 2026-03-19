---
title: AMO Meta Ads Click ID
description: Adobe Media Optimizer Meta Ads Click ID, die in de integratie van Adobe Advertising wordt gebruikt.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# AMO Meta Ads Click ID

De **[!UICONTROL AMO Meta Ads Click ID]** is een id voor een advertentie-klik die wordt gebruikt in Adobe Advertising-integratie. De afmeting wordt automatisch gecreeerd wanneer het toelaten van [&#x200B; Analytics voor de integratie van Advertising &#x200B;](https://experienceleague.adobe.com/nl/docs/advertising/integrations/analytics/overview). Het is hoofdzakelijk nuttig als ruwe het volgen herkenningsteken eerder dan een leesbare rapporteringsdimensie.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt de waarden ervan op meerdere manieren:

* Voor klik-door verkeer, wordt het gegeven verzameld van de `fbclid` parameter van het vraagkoord in de [&#x200B; Pagina URL &#x200B;](page-url.md), gewoonlijk op de pagina waardoor het ad-gedreven verkeer de plaats ingaat.
* Doorklikken kan ook worden vastgelegd wanneer de URL geen volgcodes bevat, maar de Adobe Advertising JavaScript detecteert een klik in de voorafgaande twee minuten.

## Dimension-objecten

Dimension-items bevatten id&#39;s voor advertenties van Meta (Facebook) die zijn gegenereerd. De lengte van deze gehakte waarden kan variëren, maar is typisch honderden karakters lang. Voorbeelden (afgebroken) van waarden zijn:

```text
IwY2xjawP0bVtleHRuA2FlbQIxMAB[...]AVp_aem_l5TPw-muraFjBGOq8l1w0g
PAb21jcAQB1LNleHRuA2FlbQIxMQB[...]PoFocE1FH44g_aem_FNMJG5EydJ_59aBwKIf4uA
```
