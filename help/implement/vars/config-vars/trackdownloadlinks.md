---
title: trackDownloadLinks
description: Schakel het automatisch bijhouden van koppelingen voor downloadkoppelingen in of uit.
feature: Appmeasurement Implementation
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
role: Admin, Developer
source-git-commit: 7176e068dd05c5589d741f3194d2ad5d795e017d
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# trackDownloadLinks

Adobe biedt de mogelijkheid downloadkoppelingen bij te houden zonder handmatig de methode [`tl()`](../functions/tl-method.md) voor elke downloadkoppeling in te stellen. Schakel deze variabele in als u koppelingen automatisch wilt bijhouden voor downloadkoppelingen.

Als deze optie is ingeschakeld, vergelijkt AppMeasurement de URL van geklikte koppelingen met de waarden in [`linkDownloadFileTypes`](linkdownloadfiletypes.md) . Als er een overeenkomst is, wordt automatisch een aanroep voor het bijhouden van de downloadkoppeling geactiveerd.

## Klikverzameling inschakelen of uitschakelen met de extensie Web SDK

Schakel het selectievakje [!UICONTROL Enable click data collection] in wanneer u de Web SDK configureert. Met dit selectievakje worden zowel afsluitings- als downloadkoppelingen afgehandeld.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Klik onder [!UICONTROL Data Collection] op het selectievakje **[!UICONTROL Enable click data collection]** .

## Schakel de klikverzameling handmatig implementeren van de Web SDK in of uit

Vorm SDK gebruikend [`clickCollectionEnabled` ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html#clickCollectionEnabled). Het veld is een Booleaanse waarde die bepaalt of gegevens die aan koppelingsklikken zijn gekoppeld, automatisch worden verzameld. De standaardwaarde is `true` . Stel deze waarde in op `false` als u het automatisch bijhouden van koppelingen wilt uitschakelen. Met deze instelling wordt het automatisch bijhouden van koppelingen verwerkt voor zowel download- als afsluitkoppelingen.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Download-koppelingen volgen met de Adobe Analytics-extensie

Download-koppelingen bijhouden is een selectievakje onder de accordeon [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het selectievakje [!UICONTROL Track download links] zichtbaar wordt.

Klik op het selectievakje om het automatisch bijhouden van downloadkoppelingen in te schakelen.

## s.trackDownloadLinks in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

`s.trackDownloadLinks` is een Booleaanse waarde die het automatisch bijhouden van downloadkoppelingen in- of uitschakelt. Als u downloadkoppelingen niet wilt bijhouden of liever handmatig de methode `tl()` aanroepen om downloads bij te houden, stelt u deze variabele in op `false` . De veranderlijke [ linkDownloadFileTypes ](linkdownloadfiletypes.md) moet ook voor het automatische volgen van de downloadverbinding worden geplaatst om te werken.

```js
s.trackDownloadLinks = true;
```
