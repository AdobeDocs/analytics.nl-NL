---
title: Util.getQueryParam
description: Retourneert de waarde van een querytekenreeksparameter.
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Util.getQueryParam

Parameters van queryreeksen in een browser-URL bevatten vaak belangrijke gegevens voor Analytics. Gebruik de methode `Util.getQueryParam()` om gegevens van het vraagkoord terug te winnen.

## Parametergegevens voor queryreeksen ophalen met tags in Adobe Experience Platform

U kunt de parametergegevens van het vraagkoord krijgen door waarden in gegevenselementen te plaatsen.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het tabblad [!UICONTROL Data Elements] en klik op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op [!UICONTROL Core] en [!UICONTROL Data Element Type] op [!UICONTROL Query String Parameter].
5. Voer de parameter voor de querytekenreeks in het tekstveld in.

De parameterwaarde van het vraagkoord wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de variabelen van de Analyse toe te wijzen.

## s.Util.getQueryParam() in AppMeasurement en aangepaste code-editor

Roep de methode `s.Util.getQueryParam()` aan om een waarde van het vraagkoord van browser URL terug te winnen. Het tekenreeksargument met een querytekenreeksparameter is vereist. Deze methode retourneert een tekenreeks die u kunt toewijzen aan variabelen van Analytics:

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
>Er is een vergelijkbare plug-in met de naam [`s.getQueryParam`](../plugins/getqueryparam.md) beschikbaar. Deze plug-in bevat meer geavanceerde functies, maar is ook complexer en wordt standaard niet in AppMeasurement opgenomen.
