---
title: trackExternalLinks
description: Automatisch koppelen bijhouden in- of uitschakelen voor afsluitkoppelingen.
feature: Variables
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# trackExternalLinks

Adobe biedt de mogelijkheid om uitgaande koppelingen bij te houden zonder handmatig de [`tl()`](../functions/tl-method.md) methode voor elke exit link. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor afsluitkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt AppMeasurement elke aangeklikte koppeling-URL met waarden in [`linkInternalFilters`](linkinternalfilters.md) en [`linkExternalFilters`](linkexternalfilters.md). Als er een gelijke is, brand automatisch een verbinding van de uitgangsverbinding die vraag volgt.

## Uitgaande koppelingen bijhouden met tags in Adobe Experience Platform

Uitgaande koppelingen bijhouden is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Track outbound links] selectievakje.

Klik op het selectievakje om automatische tracering van afsluitkoppelingen in te schakelen.

## s.trackExternalLinks in AppMeasurement en aangepaste code-editor

De `s.trackExternalLinks` is een Booleaanse waarde die het automatisch bijhouden van afsluitkoppelingen in- of uitschakelt. Als u uitgaande verbindingen niet wilt volgen, of zou verkiezen manueel te roepen `tl()` methode om uitgangsverbindingen te volgen, plaats deze variabele aan `false`.

```js
s.trackExternalLinks = true;
```
