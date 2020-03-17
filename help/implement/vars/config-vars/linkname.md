---
title: linkName
description: Stel de naam in van de aangepaste koppelingshit.
translation-type: tm+mt
source-git-commit: e500332fe16887fa004858b07b59644837e183aa

---


# linkName

Gebruik de `linkName` variabele om de waarde van de afmeting van douaneverbindingen te bepalen, downloadverbindingen, of uitgangsverbindingen wanneer het runnen van de volgende `tl()` functie.

Als deze variabele leeg is, keert AppMeasurement aan de `linkURL` variabele terug.

## Koppelingsnaam in Adobe Experience Platform Launch

U kunt het gebied van de verbindingsnaam plaatsen wanneer het vormen van een regel om een baken te verzenden.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en de knop [!UICONTROL Action Type] To Send Beacon.
6. Klik op het `s.tl()` keuzerondje dat het [!UICONTROL Link Name] veld weergeeft.

## s.linkName in AppMeasurement en Launch, aangepaste code-editor

De `s.linkName` variabele is een tekenreeks die de waarde van de afmetingen voor aangepaste koppelingen, downloadkoppelingen of afsluitkoppelingen bepaalt (afhankelijk van wat `s.linkType` is). Het kan tot 100 bytes bevatten.

> [!TIP] Deze variabele is de derde parameter van de `tl()` functie en hoeft gewoonlijk niet als een standalone variabele te worden ingesteld. U kunt de `linkName` variabele echter wel gebruiken als u geen waarden als argumenten in de `tl()` functie wilt instellen.

```js
s.linkName = "Example custom link";
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
