---
title: bezoekerID
description: Gebruik een aangepaste bezoeker-id.
feature: Appmeasurement Implementation
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# bezoekerID

Adobe gebruikt verschillende methoden om bezoekers op uw site te identificeren. De variabele `visitorID` negeert alle andere methoden voor bezoekersidentificatie.

>[!IMPORTANT]
>
>Adobe raadt u af deze variabele te gebruiken. Gebruik in plaats hiervan de [ Dienst van de Identiteit van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Bezoeker-id met de Adobe Analytics-extensie

[!UICONTROL Visitor ID] is een veld onder de accordeon van [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Visitor ID] zichtbaar wordt.

Wijs dit veld toe aan het gegevenselement dat uw aangepaste bezoeker-id bevat. Stel dit veld niet in op een statische waarde.

## s.bezoekerID in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.visitorID` is een tekenreeks die een aangepaste unieke id voor de bezoeker bevat. Geldige waarden zijn alfanumerieke tekens tot 100 bytes. Gebruik geen streepjes, spaties, onderstrepingstekens of symbolen in deze variabele.

>[!WARNING]
>
>Als u de variabele `visitorID` partway door een bezoek plaatst, resultaten de gegevens in twee afzonderlijke unieke bezoekers.

```js
s.visitorID = "abc123";
```

>[!CAUTION]
>
>Een ongeldige implementatie van aangepaste gebruikers-id&#39;s voor bezoekers kan leiden tot onjuiste gegevens en slechte rapportprestaties. Als deze variabele een standaardwaarde bevat (zoals `"0"` of `"NULL"` ), behandelt Adobe deze resultaten alsof ze dezelfde bezoeker zijn. Deze situatie resulteert in onjuiste gegevens, met lage aantallen bezoekers en bezoekersniveausegmenten niet zoals verwacht. Incorrect uitgevoerde identiteitskaart van de douanebezoeker introduceert ook zware lading op verwerkingsservers, die [ latentie ](/help/technotes/latency.md) verhogen en rapportprestaties verminderen.

## Bezoeker-id met de Web SDK

Adobe Experience Platform Edge Network staat u toe om veelvoudige herkenningstekens te verstrekken gebruikend de Kaart van de Identiteit XDM [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/overview.html#using-identitymap). Elke identiteit in een identiteitskaart heeft een verschillende namespace. U kunt specificeren welke namespace voor identiteitskaart van de Bezoeker als deel van [ gegevensstroomconfiguratie ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#analytics) zou moeten worden gebruikt. Zodra dit wordt gevormd, wanneer u een gebeurtenis met een waarde verzendt die voor dit namespace wordt gespecificeerd, zal het automatisch als identiteitskaart van de Bezoeker in Analytics worden gebruikt.
