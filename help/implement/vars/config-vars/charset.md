---
title: charSet
description: De charSet-variabele bepaalt welke codering Adobe gebruikt om uw afbeeldingsverzoek te parseren.
translation-type: tm+mt
source-git-commit: 70410af433f540764b71bd29a81ff9d8210cb95c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# charSet

De charSet-variabele wordt door Adobe gebruikt om binnenkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. De meeste sites hoeven deze variabele niet in te stellen.

Stel deze variabele alleen in als u onjuiste waarden ([mojibake](https://en.wikipedia.org/wiki/Mojibake)) in rapporten ziet. U kunt deze variabele per pagina instellen als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in Adobe Experience Platform starten

Tekenset is een veld onder de [!UICONTROL General] accordeon tijdens het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL General] [!UICONTROL Character Set] veld onthult.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Wijzig de waarde niet van `UTF-8` tenzij u onjuiste waarden in rapporten ziet.

## s.charSet in AppMeasurement en Launch, aangepaste code-editor

De `charSet` variabele is een tekenreeks. Als u in Adobe Analytics onjuiste waarden hebt, stelt u deze variabele in op dezelfde waarde als de `<meta charset="">` HTML-tag op uw site.

```js
s.charSet = "UTF-8";
```
