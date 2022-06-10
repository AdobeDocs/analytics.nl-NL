---
title: trackInlineStats
description: Activiteitenoverzicht in uw implementatie in- of uitschakelen.
keywords: activiteitenoverzicht uitschakelen
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# trackInlineStats

Activiteitenoverzicht is een functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. U kunt deze gegevens weergeven in analyserapporten of met een browserextensieoverlay. Schakel deze variabele in als u Activiteitenoverzicht wilt gebruiken.

Wanneer toegelaten, verzamelt AppMeturement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een gekoeld geëtiketteerd `s_sq`.

## Activity Map die SDK van het Web gebruikt

De SDK van het Web ondersteunt nog niet de gegevensverzameling van de Activity Map.

## Klikmap inschakelen met de Adobe Analytics-extensie

[!UICONTROL Enable Clickmap] is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Enable Clickmap] selectievakje.

Klik op het selectievakje om Activiteit maps bijhouden in te schakelen.

## s.trackInlineStats in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.trackInlineStats` is een Booleaanse waarde die het bijhouden van activiteitenkaarten in- of uitschakelt. De standaardwaarde is `false`. Deze waarde instellen op `true` als u de gegevensinzameling van de kaart van de Activiteit wilt toelaten.

```js
s.trackInlineStats = true;
```
