---
title: pageName
description: De naam van de pagina op uw site.
feature: Appmeasurement Implementation
exl-id: 24ac40a9-f0e7-4534-abf2-2397f5fe16c2
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# pageName

In de variabele `pageName` wordt doorgaans de naam van een bepaalde pagina opgeslagen. Het is handig om te bepalen welke afzonderlijke pagina&#39;s het populairst zijn. Deze variabele bevolkt de [&#x200B; dimensie van de Pagina &#x200B;](/help/components/dimensions/page.md).

Als deze variabele niet is gedefinieerd in een bepaalde aanroep om de pagina te volgen, wordt in plaats daarvan de variabele [`pageURL`](pageurl.md) gebruikt.

>[!NOTE]
>
>De servers van de gegevensinzameling van Adobe ontdoen deze afmeting van alle [&#x200B; verbinding die &#x200B;](/help/implement/vars/functions/tl-method.md) beeldverzoeken volgen. Als u deze afmeting in verbindingsvolgende treffers wilt verschijnen, denk na kopieerend deze afmeting in [&#x200B; eVar &#x200B;](evar.md).

## Paginanaam met de Web SDK

De paginanaam wordt toegewezen aan de volgende variabelen:

* [&#x200B; voorwerp XDM &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.name`
* [&#x200B; voorwerp van Gegevens &#x200B;](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageName`

## Paginanaam met de Adobe Analytics-extensie

U kunt paginanaam instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Page name] .

U kunt de paginanaam instellen op elke tekenreekswaarde, inclusief gegevenselementen.

## s.pageName in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.pageName` is een tekenreeks die doorgaans de naam van de pagina bevat. De eigenschap heeft een maximumwaarde van 100 bytes. De langere waarden worden afgebroken. Deze afkapping omvat ook instanties waarbij de waarde terugvalt naar `pageURL` als deze variabele leeg is.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```

Als het gebruiken van de `digitalData` [&#x200B; gegevenslaag &#x200B;](../../prepare/data-layer.md):

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
