---
title: trackInlineStats
description: Activiteitenoverzicht in uw implementatie in- of uitschakelen.
keywords: activiteitenoverzicht uitschakelen
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# trackInlineStats

Activiteitenoverzicht is een functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. U kunt deze gegevens weergeven in analyserapporten of met een browserextensieoverlay. Schakel deze variabele in als u Activiteitenoverzicht wilt gebruiken.

Wanneer toegelaten, verzamelt AppMeturement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een gekoeld geëtiketteerd `s_sq`.

## Klikmap inschakelen met tags in Adobe Experience Platform

[!UICONTROL Enable Clickmap] is een selectievakje onder [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder Adobe Analytics.
4. Breid uit [!UICONTROL Link Tracking] accordion, die de [!UICONTROL Enable Clickmap] selectievakje.

Klik op het selectievakje om Activiteit maps bijhouden in te schakelen.

## s.trackInlineStats in AppMeasurement en aangepaste code-editor

De `s.trackInlineStats` is een Booleaanse waarde die het bijhouden van activiteitenkaarten in- of uitschakelt. De standaardwaarde is `false`. Deze waarde instellen op `true` als u de gegevensinzameling van de kaart van de Activiteit wilt toelaten.

```js
s.trackInlineStats = true;
```
