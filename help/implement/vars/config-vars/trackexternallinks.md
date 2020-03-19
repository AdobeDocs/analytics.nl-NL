---
title: trackExternalLinks
description: Automatisch koppelen bijhouden in- of uitschakelen voor afsluitkoppelingen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackExternalLinks

Adobe biedt de mogelijkheid om uitgaande koppelingen bij te houden zonder handmatig de [`tl()`](../functions/tl-method.md) methode voor elke afsluitkoppeling in te stellen. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor afsluitkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt AppMeasurement elke aangeklikte koppeling-URL met waarden in [`linkInternalFilters`](linkinternalfilters.md) en [`linkExternalFilters`](linkexternalfilters.md). Als er een gelijke is, brand automatisch een verbinding van de uitgangsverbinding die vraag volgt.

## Uitgaande koppelingen bijhouden in Adobe Experience Platform Launch

Uitgaande koppelingen bijhouden is een selectievakje onder de [!UICONTROL Link Tracking] accordeon bij het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Link Tracking] accordeon uit, zodat het [!UICONTROL Track outbound links] selectievakje zichtbaar wordt.

Klik op het selectievakje om automatische tracering van afsluitkoppelingen in te schakelen.

## s.trackExternalLinks in AppMeasurement en Launch, aangepaste code-editor

Het `s.trackExternalLinks` is een Booleaanse waarde die het automatisch bijhouden van afsluitkoppelingen in- of uitschakelt. Als u uitgaande verbindingen niet wilt volgen, of zou verkiezen de `tl()` methode manueel te roepen om uitgangsverbindingen te volgen, plaats deze variabele aan `false`.

```js
s.trackDownloadLinks = true;
```
