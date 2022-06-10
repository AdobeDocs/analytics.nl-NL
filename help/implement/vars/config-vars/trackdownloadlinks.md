---
title: trackDownloadLinks
description: Schakel het automatisch bijhouden van koppelingen voor downloadkoppelingen in of uit.
feature: Variables
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# trackDownLoadLinks

Adobe biedt de mogelijkheid downloadkoppelingen te volgen zonder handmatig de [`tl()`](../functions/tl-method.md) methode voor elke downloadkoppeling. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor downloadkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt AppMeasurement elke aangeklikte koppeling-URL met waarden in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Als er een overeenkomst is, wordt automatisch een aanroep voor het bijhouden van de downloadkoppeling geactiveerd.

## Klikverzameling inschakelen of uitschakelen met de extensie Web SDK

Gebruik de [!UICONTROL Enable click data collection] checkbox wanneer het vormen van de Web SDK. Met dit selectievakje worden zowel afsluitings- als downloadkoppelingen afgehandeld.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Enable click data collection]** selectievakje.

## Laat of maak klikinzameling toe onbruikbaar manueel uitvoerend de SDK van het Web

De SDK configureren met [`clickCollectionEnabled`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html#clickCollectionEnabled). Het veld is een Booleaanse waarde die bepaalt of gegevens die aan koppelingsklikken zijn gekoppeld, automatisch worden verzameld. De standaardwaarde is `true`. Deze waarde instellen op `false` als u het automatisch bijhouden van koppelingen wilt uitschakelen. Met deze instelling wordt het automatisch bijhouden van koppelingen verwerkt voor zowel download- als afsluitkoppelingen.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Download-koppelingen volgen met de Adobe Analytics-extensie

Downloadkoppelingen bijhouden is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Track download links] selectievakje.

Klik op het selectievakje om het automatisch bijhouden van downloadkoppelingen in te schakelen.

## s.trackDownloadLinks in AppMeturement en de de coderedacteur van de de uitbreidingsuitbreiding van de Analyse

De `s.trackDownloadLinks` is een Booleaanse waarde die het automatisch bijhouden van downloadkoppelingen in- of uitschakelt. Als u downloadkoppelingen niet wilt bijhouden of liever handmatig `tl()` methode om downloads te volgen, plaats deze variabele aan `false`.

```js
s.trackDownloadLinks = true;
```
