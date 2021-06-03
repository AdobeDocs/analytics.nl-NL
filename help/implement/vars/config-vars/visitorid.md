---
title: visitorID
description: Gebruik een aangepaste bezoeker-id.
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---

# bezoekerID

Adobe gebruikt verschillende methoden om bezoekers op uw site te identificeren. De variabele `visitorID` negeert alle andere methoden voor bezoekersidentificatie.

>[!IMPORTANT]
>
>Adobe raadt u af deze variabele te gebruiken. Gebruik in plaats hiervan [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Bezoeker-id in Adobe Experience Platform Launch

[!UICONTROL Visitor ID] is een veld onder de  [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Visitor ID] zichtbaar wordt.

Wijs dit veld toe aan het gegevenselement dat uw aangepaste bezoeker-id bevat. Stel dit veld niet in op een statische waarde.

## s.bezoekerID in AppMeasurement en Launch de redacteur van de douanecode

De variabele `s.visitorID` is een tekenreeks die een aangepaste unieke id voor de bezoeker bevat. Geldige waarden zijn alfanumerieke tekens tot 100 bytes. Gebruik geen streepjes, spaties, onderstrepingstekens of symbolen in deze variabele.

>[!WARNING]
>
>Als u de variabele `visitorID` partway door een bezoek plaatst, resultaten de gegevens in twee afzonderlijke unieke bezoekers.

```js
s.visitorID = "abc123";
```

>[!CAUTION]
>
>Een ongeldige implementatie van aangepaste gebruikers-id&#39;s voor bezoekers kan leiden tot onjuiste gegevens en slechte rapportprestaties. Als deze variabele een standaardwaarde bevat (zoals `"0"` of `"NULL"`), behandelt Adobe deze treffers alsof ze dezelfde bezoeker zijn. Deze situatie resulteert in onjuiste gegevens, met lage aantallen bezoekers en bezoekersniveausegmenten niet zoals verwacht. Bij onjuist geïmplementeerde aangepaste gebruikers-id&#39;s wordt ook een zware belasting op de verwerkingsservers veroorzaakt, waardoor de latentie [toeneemt](/help/technotes/latency.md) en de rapportprestaties afnemen.
