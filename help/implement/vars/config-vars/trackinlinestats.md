---
title: trackInlineStats
description: Schakel ClickMapen in uw implementatie in of uit.
keywords: klikmap uitschakelen
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 4af73d19afd8844f814aafd45153cc638aa535d6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# trackInlineStats

>[!IMPORTANT]
>
>Deze variabele wordt uitgeschakeld. Zie [Activity Map inschakelen](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md) in plaats daarvan.

ClickMap is een gepensioneerde functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. De functie is vervangen door [Activity Map](/help/analyze/activity-map/activity-map.md).

Wanneer toegelaten, verzamelt het AppMeasurement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een koekje geëtiketteerd `s_sq`.

## ClickMap inschakelen met de Adobe Analytics-extensie

[!UICONTROL Enable ClickMap] is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Enable ClickMap] selectievakje.

>[!NOTE]
>
>Dit selectievakje is anders dan het selectievakje [!UICONTROL Use Activity Map] selectievakje, dat zich onder de [!UICONTROL Library management] accordeon.

## s.trackInlineStats in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.trackInlineStats` is een booleaanse waarde die het bijhouden van ClickMapen in- of uitschakelt. Aangezien de functie is uitgeschakeld, wordt het niet aangeraden deze variabele in te stellen door Adobe. De standaardwaarde is `false`.

```js
s.trackInlineStats = false;
```
