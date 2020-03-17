---
title: charSet
description: De charSet-variabele bepaalt welke codering Adobe gebruikt om uw afbeeldingsverzoek te parseren.
translation-type: tm+mt
source-git-commit: f769da139d9890fd736a9b277934b11aa131e166

---


# charSet

De charSet-variabele wordt door Adobe gebruikt om binnenkomende gegevens om te zetten in UTF-8 voor opslag en rapportage door Analytics. Als uw site een andere charSet gebruikt dan UTF-8, zorgt deze variabele ervoor dat uw gegevens correct worden gecodeerd door Adobe. Deze variabele kan per pagina worden ingesteld als uw site verschillende coderingen op verschillende pagina&#39;s gebruikt.

## Tekenset in Adobe Experience Platform Starten

Tekenset is een veld onder de [!UICONTROL General] accordeon tijdens het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL General] [!UICONTROL Character Set] veld onthult.

U kunt een vooraf ingestelde tekenset of een aangepaste tekenset gebruiken. Deze waarde moet overeenkomen met de tekencodering op uw site. De meeste sites gebruiken `UTF-8`.

## s.charSet in AppMeasurement en Launch, aangepaste code-editor

De `charSet` variabele is een tekenreeks. Stel deze variabele in op dezelfde waarde als de `<meta charset="">` HTML-tag op uw site.

```js
s.charSet = "UTF-8";
```
