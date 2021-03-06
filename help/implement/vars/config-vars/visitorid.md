---
title: visitorID
description: Gebruik een aangepaste bezoeker-id.
feature: Variables
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# bezoekerID

Adobe gebruikt verschillende methoden om bezoekers op uw site te identificeren. De `visitorID` variabele heeft voorrang op alle andere methoden voor bezoekersidentificatie.

>[!IMPORTANT]
>
>Adobe raadt u af deze variabele te gebruiken. Gebruik de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) in plaats daarvan.

## Overschrijving bezoekersidentiteitskaart gebruikend de SDK van het Web

Binnenkort verkrijgbaar!

## Bezoeker-id met de Adobe Analytics-extensie

[!UICONTROL Visitor ID] is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Visitor ID] veld.

Wijs dit veld toe aan het gegevenselement dat uw aangepaste bezoeker-id bevat. Stel dit veld niet in op een statische waarde.

## s.bezoekorID in AppMeturement en de de coderedacteur van de de uitbreidingsuitbreiding van de Analyse

De `s.visitorID` variabele is een tekenreeks die een aangepaste unieke id voor de bezoeker bevat. Geldige waarden zijn alfanumerieke tekens tot 100 bytes. Gebruik geen streepjes, spaties, onderstrepingstekens of symbolen in deze variabele.

>[!WARNING]
>
>Als u de `visitorID` variabele partway door een bezoek, resultaten gegevens in twee afzonderlijke unieke bezoekers.

```js
s.visitorID = "abc123";
```

>[!CAUTION]
>
>Een ongeldige implementatie van aangepaste gebruikers-id&#39;s voor bezoekers kan leiden tot onjuiste gegevens en slechte rapportprestaties. Als deze variabele een standaardwaarde bevat (zoals `"0"` of `"NULL"`), behandelt Adobe deze treffers alsof ze dezelfde bezoeker zijn. Deze situatie resulteert in onjuiste gegevens, met lage aantallen bezoekers en bezoekersniveausegmenten niet zoals verwacht. De onjuist ge??mplementeerde aangepaste bezoeker-id&#39;s zorgen ook voor een zware belasting op de verwerkingsservers, waardoor de [latentie](/help/technotes/latency.md) en afnemende rapportprestaties.
