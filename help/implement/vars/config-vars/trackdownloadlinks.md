---
title: trackDownloadLinks
description: Schakel het automatisch bijhouden van koppelingen voor downloadkoppelingen in of uit.
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# trackDownLoadLinks

Adobe biedt de capaciteit aan om downloadverbindingen te volgen zonder manueel de [`tl()`](../functions/tl-method.md) methode voor elke downloadverbinding te plaatsen. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor downloadkoppelingen.

Wanneer toegelaten, vergelijkt AppMeasurement om het even welke geklikte verbinding URL met waarden in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Als er een overeenkomst is, wordt automatisch een aanroep voor het bijhouden van de downloadkoppeling geactiveerd.

## Download-koppelingen volgen met tags in Adobe Experience Platform

Downloadkoppelingen bijhouden is een selectievakje onder de accordeon [!UICONTROL Link Tracking] bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Link Tracking] accordeon uit, die [!UICONTROL Track download links] checkbox openbaart.

Klik op het selectievakje om het automatisch bijhouden van downloadkoppelingen in te schakelen.

## s.trackDownloadLinks in AppMeasurement en een aangepaste code-editor

`s.trackDownloadLinks` is een booleaanse waarde die het automatisch bijhouden van downloadkoppelingen in- of uitschakelt. Als u downloadverbindingen niet wilt volgen, of zou verkiezen `tl()` methode manueel te roepen om downloaden te volgen, plaats deze variabele aan `false`.

```js
s.trackDownloadLinks = true;
```
