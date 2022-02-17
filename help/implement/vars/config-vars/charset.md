---
title: charSet
description: De charSet-variabele bepaalt welke codering Adobe gebruikt om uw afbeeldingsverzoek te parseren.
feature: Variables
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# charSet

De charSet-variabele wordt door Adobe gebruikt om inkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. De meeste sites hoeven deze variabele niet in te stellen.

Stel deze variabele alleen in als u onjuiste waarden ziet ([mojibake](https://en.wikipedia.org/wiki/Mojibake)) in verslagen. U kunt deze variabele per pagina instellen als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in Adobe Experience Platform

Tekenset is een veld onder de [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Character Set] veld.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Wijzig de waarde niet vanuit `UTF-8` tenzij u onjuiste waarden in rapporten ziet.

## s.charSet in AppMeasurement en aangepaste code-editor

De `charSet` variable is a string. Als u in Adobe Analytics onjuiste waarden hebt ingevoerd, stelt u deze variabele in op dezelfde waarde als de `<meta charset="">` HTML-tag op uw site.

```js
s.charSet = "UTF-8";
```
