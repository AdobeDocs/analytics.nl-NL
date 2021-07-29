---
title: trackExternalLinks
description: Automatisch koppelen bijhouden in- of uitschakelen voor afsluitkoppelingen.
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# trackExternalLinks

Adobe biedt de capaciteit aan om uitgaande verbindingen te volgen zonder manueel de [`tl()`](../functions/tl-method.md) methode voor elke uitgangsverbinding te plaatsen. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor afsluitkoppelingen.

Wanneer toegelaten, vergelijkt AppMeasurement om het even welke geklikte verbinding URL met waarden in [`linkInternalFilters`](linkinternalfilters.md) en [`linkExternalFilters`](linkexternalfilters.md). Als er een gelijke is, brand automatisch een verbinding van de uitgangsverbinding die vraag volgt.

## Uitgaande koppelingen bijhouden met tags in Adobe Experience Platform

Uitgaande koppelingen bijhouden is een selectievakje onder de accordeon [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Link Tracking] accordeon uit, die [!UICONTROL Track outbound links] checkbox openbaart.

Klik op het selectievakje om automatische tracering van afsluitkoppelingen in te schakelen.

## s.trackExternalLinks in AppMeasurement en aangepaste code-editor

`s.trackExternalLinks` is een booleaanse waarde die het automatisch bijhouden van afsluitkoppelingen in- of uitschakelt. Als u uitgaande verbindingen niet wilt volgen, of zou verkiezen `tl()` methode manueel te roepen om uitgangsverbindingen te volgen, plaats deze variabele aan `false`.

```js
s.trackExternalLinks = true;
```
