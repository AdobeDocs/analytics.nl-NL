---
title: charSet
description: De charSet-variabele bepaalt welke codering Adobe gebruikt om uw afbeeldingsverzoek te parseren.
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# charSet

De charSet-variabele wordt door Adobe gebruikt om inkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. De meeste sites hoeven deze variabele niet in te stellen.

Stel deze variabele alleen in als u onjuiste waarden ([mojibake](https://en.wikipedia.org/wiki/Mojibake)) ziet in rapporten. U kunt deze variabele per pagina instellen als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in Adobe Experience Platform

Tekenset is een veld onder de accordeon [!UICONTROL General] wanneer u de Adobe Analytics-extensie configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL General] uit, zodat het veld [!UICONTROL Character Set] zichtbaar wordt.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Wijzig de waarde niet vanaf `UTF-8`, tenzij er onjuiste waarden in rapporten staan.

## s.charSet in AppMeasurement en aangepaste code-editor

De variabele `charSet` is een tekenreeks. Als u in Adobe Analytics onjuiste waarden hebt, stelt u deze variabele in op dezelfde waarde als de HTML-tag `<meta charset="">` op uw site.

```js
s.charSet = "UTF-8";
```
