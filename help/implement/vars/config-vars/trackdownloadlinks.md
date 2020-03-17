---
title: trackDownloadLinks
description: Schakel het automatisch bijhouden van koppelingen voor downloadkoppelingen in of uit.
translation-type: tm+mt
source-git-commit: 04b97e93a95691132680d4da197dc62eb2b9fdd1

---


# trackDownLoadLinks

Adobe biedt de mogelijkheid downloadkoppelingen bij te houden zonder de functie voor elke downloadkoppeling handmatig in te stellen. `tl()` Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor downloadkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt AppMeasurement elke aangeklikte koppeling-URL met waarden in `downloadLinkFileTypes`. Als er een overeenkomst is, wordt automatisch een aanroep voor het bijhouden van de downloadkoppeling geactiveerd.

## Download-koppelingen bijhouden in Adobe Experience Platform Launch

Downloadkoppelingen bijhouden is een selectievakje onder de [!UICONTROL Link Tracking] accordeon bij het configureren van de extensie Adobe Analytics.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Link Tracking] accordeon uit, zodat het [!UICONTROL Track download links] selectievakje zichtbaar wordt.

Klik op het selectievakje om het automatisch bijhouden van downloadkoppelingen in te schakelen.

## s.trackDownloadLinks in AppMeasurement en Launch, aangepaste code-editor

Het `s.trackDownloadLinks` is een Booleaanse waarde die het automatisch bijhouden van downloadkoppelingen in- of uitschakelt. Als u downloadkoppelingen niet wilt bijhouden of liever handmatig de functie aanroepen om downloads bij te houden, stelt u deze variabele in op `tl()` `false`.

```js
s.trackDownloadLinks = true;
```
