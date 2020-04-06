---
title: linkName
description: Stel de naam in van de aangepaste koppelingshit.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkName

Gebruik de `linkName` variabele om de afmetingswaarde van douaneverbindingen, downloadverbindingen, of uitgangsverbindingen te bepalen wanneer het runnen van de volgende [`tl()`](../functions/tl-method.md) methode.

Als deze variabele leeg is, keert AppMeasurement aan de [`linkURL`](linkurl.md) variabele terug.

## Koppelingsnaam in Adobe Experience Platform Launch

U kunt het gebied van de verbindingsnaam plaatsen wanneer het vormen van een regel om een baken te verzenden.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en de knop [!UICONTROL Action Type] To Send Beacon.
6. Klik op het `s.tl()` keuzerondje dat het [!UICONTROL Link Name] veld weergeeft.

## s.linkName in AppMeasurement en Launch, aangepaste code-editor

De `s.linkName` variabele is een tekenreeks die de waarde van de afmetingen voor aangepaste koppelingen, downloadkoppelingen of afsluitkoppelingen bepaalt (afhankelijk van wat [`s.linkType`](linktype.md) is). Het kan tot 100 bytes bevatten.

>[!TIP] Deze variabele is de derde parameter van de `tl()` methode en hoeft gewoonlijk niet als een zelfstandige variabele te worden ingesteld. U kunt de `linkName` variabele echter wel gebruiken als u geen waarden als argumenten in de `tl()` methode wilt instellen.

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
