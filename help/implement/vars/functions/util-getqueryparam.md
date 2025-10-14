---
title: Util.getQueryParam
description: Retourneert de waarde van een querytekenreeksparameter.
feature: Appmeasurement Implementation
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Util.getQueryParam

Parameters van queryreeksen in een browser-URL bevatten vaak belangrijke gegevens voor Analytics. Gebruik de methode `Util.getQueryParam()` om gegevens op te halen uit de queryreeks.

## Gegevens van querytekenreeksparameters ophalen met de extensie Adobe Analytics en Web SDK

U kunt de parametergegevens van het vraagkoord krijgen door waarden in gegevenselementen te plaatsen.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Data Elements] en klik vervolgens op het gewenste gegevenselement (of maak een gegevenselement).
4. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Core]** en de vervolgkeuzelijst op [!UICONTROL Data Element Type] op **[!UICONTROL Query String Parameter]** .
5. Voer de parameter voor de querytekenreeks in het tekstveld in.

De parameterwaarde van het vraagkoord wordt opgeslagen in het gegevenselement. U kunt dan naar het gegevenselement in regels verwijzen om de gewenste variabelen toe te wijzen.

## s.Util.getQueryParam() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `s.Util.getQueryParam()` aan om een waarde van de querytekenreeks op te halen via de URL van de browser. Het tekenreeksargument dat een parameter voor een queryreeks bevat, is vereist. Deze methode retourneert een tekenreeks die u kunt toewijzen aan variabelen van Analytics:

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

Met een derde optioneel argument kunt u het scheidingsteken voor de queryreeks aanpassen. De standaardwaarde is `&` . U kunt deze waarde wijzigen als uw queryreeks een ander scheidingsteken gebruikt.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

>[!TIP]
>
>Er is een vergelijkbare plug-in met de naam [`s.getQueryParam`](../plugins/getqueryparam.md) beschikbaar. Deze plug-in bevat meer geavanceerde functies, maar is ook complexer en wordt standaard niet in AppMeasurement opgenomen.
