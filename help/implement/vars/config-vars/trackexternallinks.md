---
title: trackExternalLinks
description: Automatisch koppelen bijhouden in- of uitschakelen voor afsluitkoppelingen.
feature: Variables
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# trackExternalLinks

Adobe biedt de mogelijkheid om uitgaande koppelingen bij te houden zonder handmatig de [`tl()`](../functions/tl-method.md) methode voor elke exit link. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor afsluitkoppelingen.

Wanneer deze optie is ingeschakeld, vergelijkt het AppMeasurement de URL van geklikte koppelingen met de waarden in [`linkInternalFilters`](linkinternalfilters.md) en [`linkExternalFilters`](linkexternalfilters.md). Als er een gelijke is, brand automatisch een verbinding van de uitgangsverbinding die vraag volgt.

## Klikverzameling inschakelen of uitschakelen met de extensie Web SDK

Gebruik de [!UICONTROL Enable click data collection] checkbox wanneer het vormen van de Web SDK. Met dit selectievakje worden zowel afsluitings- als downloadkoppelingen afgehandeld.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Enable click data collection]** selectievakje.

## Laat of maak klikinzameling toe onbruikbaar manueel uitvoerend de SDK van het Web

De SDK configureren met [`clickCollectionEnabled`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL#clickCollectionEnabled). Het veld is een Booleaanse waarde die bepaalt of gegevens die aan koppelingsklikken zijn gekoppeld, automatisch worden verzameld. De standaardwaarde is `true`. Deze waarde instellen op `false` als u automatische koppeling bijhouden wilt uitschakelen. Met deze instelling wordt het automatisch bijhouden van koppelingen verwerkt voor zowel download- als afsluitkoppelingen.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Uitgaande koppelingen bijhouden met de Adobe Analytics-extensie

Uitgaande koppelingen bijhouden is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Track outbound links] selectievakje.

Klik op het selectievakje om automatische tracering van afsluitkoppelingen in te schakelen.

## s.trackExternalLinks in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.trackExternalLinks` is een Booleaanse waarde die het automatisch bijhouden van afsluitkoppelingen in- of uitschakelt. Als u uitgaande verbindingen niet wilt volgen, of zou verkiezen manueel te roepen `tl()` methode om uitgangsverbindingen te volgen, plaats deze variabele aan `false`.

```js
s.trackExternalLinks = true;
```
