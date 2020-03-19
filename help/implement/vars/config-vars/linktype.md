---
title: linkType
description: Gebruik de variabele linkType om te bepalen tot welke afmeting het verbinden behoort.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkType

Een van de volgende drie dimensies kan worden gevuld door treffers voor het bijhouden van koppelingen:

* Aangepaste koppelingen
* Koppelingen afsluiten
* Koppelingen downloaden

Gebruik de `linkType` variabele om te bepalen welke afmeting u wilt bevolken wanneer het runnen van de volgende [`tl()`](../functions/tl-method.md) functie.

## Koppelingstype in Adobe Experience Platform Launch

Plaats het verbindingstype wanneer het vormen van een regel om een baken te verzenden.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en de knop [!UICONTROL Action Type] To Send Beacon.
6. Klik op het `s.tl()` keuzerondje dat het [!UICONTROL Link Type] vervolgkeuzemenu weergeeft.

U kunt deze vervolgkeuzelijst instellen op [!UICONTROL Custom Link], [!UICONTROL Download Link]of [!UICONTROL Exit Link].

## s.linkType in AppMeasurement en Launch, aangepaste code-editor

De `s.linkType` variabele is een tekenreeks die een van de drie waarden van één teken accepteert: `o`, `d`, of `e`. Als een `tl()` methode zonder een verbindingstype wordt geroepen, blijft het aan de verbinding van de Douane in gebreke.

* `o` - Aangepaste koppelingen
* `d` - Koppelingen downloaden
* `e` - Koppelingen afsluiten

> [!TIP] Deze variabele is de tweede parameter van de `tl()` methode en hoeft gewoonlijk niet als een zelfstandige variabele te worden ingesteld. U kunt de `linkType` variabele echter wel gebruiken als u geen waarden als argumenten in de `tl()` methode wilt instellen.

```js
s.linkType = "e";
```

## Voorbeeld

De volgende twee voorbeeld verbindingen het volgen vraag is functioneel identiek. Het zijn verschillende methoden om dezelfde hit voor het bijhouden van koppelingen te bereiken.

```js
// Set link tracking arguments as individual variables
s.linkType = "d";
s.linkName = "Example download link";
s.tl();

// Set link tracking arguments directly in the tl() function
s.tl(this,"d","Example download link");
```
