---
title: trackInlineStats
description: Activiteitenoverzicht in uw implementatie in- of uitschakelen.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackInlineStats

Activiteitenoverzicht is een functie in Adobe Analytics die gegevens verzamelt over waar bezoekers klikken en waarop ze klikken. U kunt deze gegevens weergeven in analyserapporten of met een browserextensieoverlay. Schakel deze variabele in als u Activiteitenoverzicht wilt gebruiken.

Wanneer toegelaten, verzamelt AppMeturement informatie over de verbinding en verzendt die gegevens in het volgende beeldverzoek. De informatie van elke klik wordt opgeslagen in een gekookt geëtiketteerd `s_sq`.

## Klikmap inschakelen in Adobe Experience Platform Launch

[!UICONTROL Enable Clickmap] is een selectievakje onder de [!UICONTROL Link Tracking] accordeon wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Link Tracking] accordeon uit, zodat het [!UICONTROL Enable Clickmap] selectievakje zichtbaar wordt.

Klik op het selectievakje om Activiteit maps bijhouden in te schakelen.

## s.trackInlineStats in AppMeasurement en Launch, aangepaste code-editor

Het `s.trackInlineStats` is een Booleaanse waarde die het bijhouden van activiteitenkaarten in- of uitschakelt. De standaardwaarde is `false`. Plaats deze waarde aan `true` als u de gegevensinzameling van de kaart van de Activiteit wilt toelaten.

```js
s.trackInlineStats = true;
```
