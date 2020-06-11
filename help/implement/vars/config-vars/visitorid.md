---
title: bezoekerID
description: Gebruik een aangepaste bezoeker-id.
translation-type: tm+mt
source-git-commit: b9bb7a60398b8c392393a8d16b58292f91ab0ea7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# bezoekerID

Adobe gebruikt verschillende methoden om bezoekers op uw site te identificeren. De `visitorID` variabele negeert alle andere methoden voor bezoekersidentificatie.

>[!IMPORTANT] Adobe raadt u af deze variabele te gebruiken. Gebruik in plaats hiervan de [Adobe Experience Cloud Identity Service](https://docs.adobe.com/content/help/en/id-service/using/home.html) .

## Bezoeker-id in Adobe Experience Platform Launch

[!UICONTROL Visitor ID] is een veld onder de [!UICONTROL Cookies] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Breid de accordeon uit, die het [!UICONTROL Cookies] [!UICONTROL Visitor ID] veld onthult.

Wijs dit veld toe aan het gegevenselement dat uw aangepaste bezoeker-id bevat. Stel dit veld niet in op een statische waarde.

## s.bezoekerID in AppMeasurement en Launch de redacteur van de douanecode

De `s.visitorID` variabele is een tekenreeks die een aangepaste unieke id voor de bezoeker bevat. Geldige waarden zijn alfanumerieke tekens tot 100 bytes. Gebruik geen streepjes, spaties, onderstrepingstekens of symbolen in deze variabele.

>[!WARNING] Als u de variabele `visitorID` partway door een bezoek plaatst, resultaten de gegevens in twee afzonderlijke unieke bezoekers.

```js
s.visitorID = "abc123";
```

>[!CAUTION] Een ongeldige implementatie van aangepaste gebruikers-id&#39;s voor bezoekers kan leiden tot onjuiste gegevens en slechte rapportprestaties. Als deze variabele een standaardwaarde bevat (zoals `"0"` of `"NULL"`), behandelt Adobe deze resultaten alsof ze dezelfde bezoeker zijn. Deze situatie resulteert in onjuiste gegevens, met lage aantallen bezoekers en bezoekersniveausegmenten niet zoals verwacht. De onjuist uitgevoerde identiteitskaart van de douanebezoeker introduceert ook zware lading op verwerkingsservers, verhoogt [latentie](/help/technotes/latency.md) en vermindert rapportprestaties.
