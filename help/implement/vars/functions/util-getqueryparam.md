---
title: Util.getQueryParam
description: Retourneert de waarde van een querytekenreeksparameter.
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Util.getQueryParam

Parameters van queryreeksen in een browser-URL bevatten vaak belangrijke gegevens voor Analytics. Gebruik de `Util.getQueryParam` methode om gegevens van het vraagkoord terug te winnen.

## Gegevens over querytekenreeksparameters ophalen in Adobe Experience Platform Launch

U kunt de parametergegevens van het vraagkoord krijgen door waarden in gegevenselementen te plaatsen.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Data Elements] tabblad en klik vervolgens op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op [!UICONTROL Core]en de [!UICONTROL Data Element Type] op [!UICONTROL Query String Parameter].
5. Voer de parameter voor de querytekenreeks in het tekstveld in.

De parameterwaarde van het vraagkoord wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de variabelen van de Analyse toe te wijzen.

## s.Util.getQueryParam() in de aangepaste code-editor van AppMeasurement en Launch

Roep de `s.Util.getQueryParam()` methode aan om een waarde van het vraagkoord van browser URL terug te winnen. Het tekenreeksargument met een querytekenreeksparameter is vereist. Deze methode retourneert een tekenreeks die u kunt toewijzen aan variabelen van Analytics:

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

> [!NOTE] In eerdere versies van AppMeasurement was een insteekmodule met naam `s.getQueryParam` beschikbaar. Deze plug-in is niet meer nodig, omdat deze nu standaard in AppMeasurement is opgenomen.
