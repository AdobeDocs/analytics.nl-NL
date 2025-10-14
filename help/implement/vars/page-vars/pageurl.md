---
title: pageURL
description: Hef de automatisch verzamelde pagina-URL op uw site op.
feature: Appmeasurement Implementation
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# pageURL

AppMeasurement verzamelt automatisch de pagina-URL in elke hit. Als u de pagina-URL die automatisch door AppMeasurement wordt verzameld, wilt overschrijven, kunt u deze variabele gebruiken. In de meeste gevallen hoeft u deze variabele niet in te stellen.

>[!NOTE]
>
>Deze variabele is geen beschikbare dimensie in Analysis Workspace. Deze optie is alleen beschikbaar in Data Warehouse en Data Feeds. Bovendien, ontdoen de servers van de gegevensinzameling van Adobe deze afmeting van alle [&#x200B; verbinding het volgen &#x200B;](/help/implement/vars/functions/tl-method.md) beeldverzoeken. Als u pagina URL als afmeting in Analysis Workspace wilt gebruiken of deze afmeting in verbindingsvolgende treffers wilt, overweeg het overgaan van de `pageURL` variabele in een [&#x200B; eVar &#x200B;](evar.md) op elke klap.

## Pagina-URL met de Web SDK

Pagina-URL wordt toegewezen aan de volgende variabelen:

* [&#x200B; voorwerp XDM &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.URL`
* [&#x200B; voorwerp van Gegevens &#x200B;](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageURL` of `data.__adobe.analytics.g`

## Pagina-URL met de Adobe Analytics-extensie

De extensie Analytics in Adobe Experience Platform Data Collection vult automatisch pagina-URL in. U kunt echter de URL van de pagina overschrijven tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad **[!UICONTROL Rules]** en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder **[!UICONTROL Actions]** op een bestaande **[!UICONTROL Adobe Analytics - Set Variables]** -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst **[!UICONTROL Extension]** in op Adobe Analytics en op **[!UICONTROL Action Type]** op **[!UICONTROL Set Variables]** .
6. Zoek de sectie **[!UICONTROL Page URL]** .

U kunt de pagina-URL instellen op elke gewenste tekenreekswaarde.

## s.pageURL in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.pageURL` is een tekenreeks die de URL van de pagina bevat. AppMeasurement verzamelt deze variabele automatisch, maar u kunt desgewenst de waarde ervan overschrijven.

```js
s.pageURL = "https://example.com";
```

Als u pagina URL als afmeting in rapporten wilt gebruiken, denk na gebruikend het volgende in uw implementatie:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

Als het gebruiken van de `digitalData` [&#x200B; gegevenslaag &#x200B;](../../prepare/data-layer.md):

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
