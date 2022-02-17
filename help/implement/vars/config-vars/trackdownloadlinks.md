---
title: trackDownloadLinks
description: Schakel het automatisch bijhouden van koppelingen voor downloadkoppelingen in of uit.
feature: Variables
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# trackDownLoadLinks

Adobe biedt de mogelijkheid downloadkoppelingen te volgen zonder handmatig de [`tl()`](../functions/tl-method.md) methode voor elke downloadkoppeling. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor downloadkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt AppMeasurement elke aangeklikte koppeling-URL met waarden in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Als er een overeenkomst is, wordt automatisch een aanroep voor het bijhouden van de downloadkoppeling geactiveerd.

## Download-koppelingen volgen met tags in Adobe Experience Platform

Downloadkoppelingen bijhouden is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Track download links] selectievakje.

Klik op het selectievakje om het automatisch bijhouden van downloadkoppelingen in te schakelen.

## s.trackDownloadLinks in AppMeasurement en een aangepaste code-editor

De `s.trackDownloadLinks` is een Booleaanse waarde die het automatisch bijhouden van downloadkoppelingen in- of uitschakelt. Als u downloadkoppelingen niet wilt bijhouden of liever handmatig `tl()` methode om downloads te volgen, plaats deze variabele aan `false`.

```js
s.trackDownloadLinks = true;
```
