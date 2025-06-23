---
title: charSet
description: De charSet-variabele bepaalt welke codering Adobe gebruikt om de afbeeldingsaanvraag te parseren.
feature: Appmeasurement Implementation
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# charSet

De variabele `charSet` wordt door Adobe gebruikt om binnenkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. De meeste sites hoeven deze variabele niet in te stellen.

Plaats deze variabele slechts als u verstoorde waarden ([ mojibake ](https://en.wikipedia.org/wiki/Mojibake)) in rapporten ziet. U kunt deze variabele per pagina instellen als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in de Web SDK

Web SDK steunt momenteel slechts UTF-8, en verstrekt geen opties om het coderen te veranderen.

## Tekenset in de Adobe Analytics-extensie

Tekenset is een veld onder de accordion [!UICONTROL General] wanneer u de Adobe Analytics-extensie configureert in Adobe Experience Platform-gegevensverzameling.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL Character Set] zichtbaar wordt.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Wijzig de waarde niet vanuit `UTF-8` , tenzij er onjuiste waarden in rapporten voorkomen.

## s.charSet in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `charSet` is een tekenreeks. Als u de waarden in Adobe Analytics niet juist hebt ingesteld, stelt u deze variabele in op dezelfde waarde als de HTML-tag `<meta charset="">` op uw site.

```js
s.charSet = "UTF-8";
```
