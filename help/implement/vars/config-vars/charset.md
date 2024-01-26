---
title: charSet
description: De variabele charSet bepaalt welke coderingsAdobe gebruikt om uw afbeeldingsverzoek te parseren.
feature: Variables
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# charSet

De `charSet` Adobe gebruikt variabele om inkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. De meeste sites hoeven deze variabele niet in te stellen.

Stel deze variabele alleen in als u onjuiste waarden ziet ([mojibake](https://en.wikipedia.org/wiki/Mojibake)) in verslagen. U kunt deze variabele per pagina instellen als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in de SDK van het web

De SDK van het Web steunt momenteel slechts UTF-8, en verstrekt geen opties om het coderen te veranderen.

## Tekenset in de Adobe Analytics-extensie

Tekenset is een veld onder de [!UICONTROL General] accordeon bij het configureren van de Adobe Analytics-extensie in Adobe Experience Platform Data Collection.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL General] accordion, die de [!UICONTROL Character Set] veld.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Wijzig de waarde niet vanuit `UTF-8` tenzij u onjuiste waarden in rapporten ziet.

## s.charSet in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `charSet` variable is a string. Als u waarden in Adobe Analytics niet juist hebt ingesteld, stelt u deze variabele in op dezelfde waarde als de `<meta charset="">` HTML-tag op uw site.

```js
s.charSet = "UTF-8";
```
