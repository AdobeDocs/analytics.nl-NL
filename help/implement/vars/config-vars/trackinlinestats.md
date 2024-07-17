---
title: trackInlineStats
description: (In ruste) Schakel ClickMap in of uit in uw implementatie.
keywords: klikmap uitschakelen
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
role: Admin, Developer
source-git-commit: 1cdcc748e50c7eeffa98897006154aa0953ce7e3
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# trackInlineStats

>[!IMPORTANT]
>
>Deze variabele wordt ingetrokken en wordt niet meer gebruikt.

ClickMap is een gepensioneerde functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. De eigenschap werd vervangen met [ Activity Map ](/help/analyze/activity-map/overview.md).

Wanneer toegelaten, verzamelt het AppMeasurement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een koekje geëtiketteerd `s_sq`.

## ClickMap inschakelen met de Adobe Analytics-extensie

[!UICONTROL Enable ClickMap] is een selectievakje onder de accordeon van [!UICONTROL Link Tracking] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Link Tracking] uit, zodat het selectievakje [!UICONTROL Enable ClickMap] zichtbaar wordt.

>[!NOTE]
>
>Dit selectievakje is anders dan het selectievakje [!UICONTROL Use Activity Map] , dat zich onder de accordeon [!UICONTROL Library management] bevindt.

## s.trackInlineStats in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

`s.trackInlineStats` is een Booleaanse waarde die het bijhouden van ClickMapen in- of uitschakelt. Aangezien de functie is uitgeschakeld, wordt het niet aangeraden deze variabele in te stellen door Adobe. De standaardwaarde is `false` .

```js
s.trackInlineStats = false;
```
