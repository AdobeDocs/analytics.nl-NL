---
title: trackExternalLinks
description: Automatisch koppelen bijhouden in- of uitschakelen voor afsluitkoppelingen.
feature: Appmeasurement Implementation
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# trackExternalLinks

Adobe biedt de mogelijkheid om uitgaande koppelingen bij te houden zonder handmatig de methode [`tl()`](../functions/tl-method.md) voor elke afsluitkoppeling in te stellen. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor afsluitkoppelingen.

Als deze optie is ingeschakeld, vergelijkt AppMeasurement de URL van geklikte koppelingen met de waarden in [`linkInternalFilters`](linkinternalfilters.md) en [`linkExternalFilters`](linkexternalfilters.md) . Als er een gelijke is, brand automatisch een verbinding van de uitgangsverbinding die vraag volgt.

## Klikverzameling inschakelen of uitschakelen met de extensie Web SDK

Schakel het selectievakje [!UICONTROL Enable click data collection] in wanneer u de Web SDK configureert. Met dit selectievakje worden zowel afsluitings- als downloadkoppelingen afgehandeld.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Klik onder [!UICONTROL Data Collection] op het selectievakje **[!UICONTROL Enable click data collection]** .

## Schakel de klikverzameling handmatig implementeren van de Web SDK in of uit

Vorm SDK gebruikend [`clickCollectionEnabled` ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL#clickCollectionEnabled). Het veld is een Booleaanse waarde die bepaalt of gegevens die aan koppelingsklikken zijn gekoppeld, automatisch worden verzameld. De standaardwaarde is `true` . Stel deze waarde in op `false` als u het automatisch bijhouden van koppelingen wilt uitschakelen. Met deze instelling wordt het automatisch bijhouden van koppelingen verwerkt voor zowel download- als afsluitkoppelingen.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Uitgaande koppelingen bijhouden met de Adobe Analytics-extensie

Uitgaande koppelingen bijhouden is een selectievakje onder de accordeon [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het selectievakje [!UICONTROL Track outbound links] zichtbaar wordt.

Klik op het selectievakje om automatische tracering van afsluitkoppelingen in te schakelen.

## s.trackExternalLinks in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.trackExternalLinks` is een Booleaanse waarde die het automatisch bijhouden van afsluitkoppelingen in- of uitschakelt. Als u uitgaande koppelingen niet wilt bijhouden of liever handmatig de methode `tl()` aanroept om afsluitkoppelingen bij te houden, stelt u deze variabele in op `false` .

```js
s.trackExternalLinks = true;
```
