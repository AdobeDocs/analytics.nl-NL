---
title: Util.getQueryParam
description: Retourneert de waarde van een querytekenreeksparameter.
feature: Variables
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Util.getQueryParam

Parameters van queryreeksen in een browser-URL bevatten vaak belangrijke gegevens voor Analytics. Gebruik de `Util.getQueryParam()` methode om gegevens van het vraagkoord terug te winnen.

## Krijg de parametergegevens van het vraagkoord gebruikend de uitbreiding van Adobe Analytics en de uitbreiding van SDK van het Web

U kunt de parametergegevens van het vraagkoord krijgen door waarden in gegevenselementen te plaatsen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Data Elements] klikt u op het gewenste gegevenselement (of maakt u een gegevenselement).
4. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar **[!UICONTROL Core]** en de [!UICONTROL Data Element Type] tot **[!UICONTROL Query String Parameter]**.
5. Voer de parameter voor de querytekenreeks in het tekstveld in.

De parameterwaarde van het vraagkoord wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de gewenste variabelen toe te wijzen.

## s.Util.getQueryParam() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de `s.Util.getQueryParam()` methode om een waarde van het vraagkoord van browser URL terug te winnen. Het tekenreeksargument met een querytekenreeksparameter is vereist. Deze methode retourneert een tekenreeks die u kunt toewijzen aan variabelen van Analytics:

```js
s.eVar1 = s.Util.getQueryParam("cid");
```

Een tweede facultatief argument staat u toe om het koord te specificeren om voor de parameters van het vraagkoord te controleren. Standaard zoekt het hulpprogramma naar de URL van de browser.

```js
// Search a custom string for query string parameter
var customString = "https://example.com?q=search";

// eVar1 is set to "search"
s.eVar1 = s.Util.getQueryParam("q",customString);
```

Met een derde optioneel argument kunt u het scheidingsteken voor de queryreeks aanpassen. De standaardwaarde is `&`. U kunt deze waarde wijzigen als uw queryreeks een ander scheidingsteken gebruikt.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

>[!TIP]
>
>Een soortgelijke plug-in met de naam [`s.getQueryParam`](../plugins/getqueryparam.md) is beschikbaar. Deze plug-in bevat meer geavanceerde functies, maar is ook complexer en wordt standaard niet in AppMeasurement opgenomen.
