---
title: trackInlineStats
description: Activiteitenoverzicht in uw implementatie in- of uitschakelen.
keywords: activiteitenoverzicht uitschakelen
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# trackInlineStats

Activiteitenoverzicht is een functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. U kunt deze gegevens weergeven in analyserapporten of met een browserextensieoverlay. Schakel deze variabele in als u Activiteitenoverzicht wilt gebruiken.

Wanneer toegelaten, verzamelt AppMeturement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een gekookt geëtiketteerd `s_sq`.

## Klikmap inschakelen met tags in Adobe Experience Platform

[!UICONTROL Enable Clickmap] is een selectievakje onder de  [!UICONTROL Link Tracking] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Breid [!UICONTROL Link Tracking] accordeon uit, die [!UICONTROL Enable Clickmap] checkbox openbaart.

Klik op het selectievakje om Activiteit maps bijhouden in te schakelen.

## s.trackInlineStats in AppMeasurement en aangepaste code-editor

De `s.trackInlineStats` is een Booleaanse waarde die het bijhouden van activiteitenkaarten in- of uitschakelt. De standaardwaarde is `false`. Stel deze waarde in op `true` als u gegevensverzameling van activiteitstoewijzingen wilt inschakelen.

```js
s.trackInlineStats = true;
```
