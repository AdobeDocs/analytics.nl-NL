---
title: linkTrackVars
description: Geef op welke variabelen u wilt opnemen in aanvragen voor het bijhouden van koppelingen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkTrackVars

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik de `linkTrackVars` en de `linkTrackEvents` variabelen om afmetingen en metriek in `tl()` vraag selectief te omvatten.

Deze variabele wordt niet gebruikt voor paginaweergaveaanroepen (`t()` functie).

## Variabelen in koppelingsreeksopvragen met Adobe Experience Platform Launch

Start vult deze variabele automatisch op de achtergrond in op basis van variabelen die in de interface zijn ingesteld. Deze variabele wordt daarom altijd ingesteld in implementaties die Launch gebruiken.

> [!IMPORTANT] Als u variabelen in Lancering gebruikend de redacteur van de douanecode plaatst, moet u de variabele in het `linkTrackVars` gebruiken van douanecode ook omvatten.

## s.linkTrackVars in AppMeasurement en Launch, aangepaste code-editor

De `s.linkTrackVars` variabele is een tekenreeks met een door komma&#39;s gescheiden lijst met variabelen die u wilt opnemen in aanvragen voor het bijhouden van koppelingen (`tl()` functie). Aan beide volgende criteria moet worden voldaan om afmetingen op te nemen in het volgen van koppelingen:

* Stel de gewenste variabelewaarde in. Bijvoorbeeld, `s.eVar1 = "Example value";`.
* Stel de gewenste variabele in de `linkTrackVars` variabele in. Bijvoorbeeld, `s.linkTrackEvents = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Adobe heeft echter wel AppMeasurement-code opgegeven in Codebeheer, waar deze variabele is ingesteld op `"None"`. Geldige waarden zijn variabelen op paginaniveau die een dimensie vullen.

* Als deze variabele niet is gedefinieerd of op een lege tekenreeks is ingesteld, worden *alle* variabelen opgenomen in aanvragen voor het bijhouden van koppelingen.
* Als deze variabele is ingesteld op `"None"`, worden *geen* variabelen opgenomen in aanvragen voor het bijhouden van koppelingen.

> [!TIP] Vermijd het gebruik van de object-id (`s.`) voor Analytics wanneer u variabelen in deze variabele opgeeft. De waarde `s.linkTrackVars = "eVar1";` is bijvoorbeeld correct, maar `s.linkTrackVars = "s.eVar1";` is onjuist.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `eVar1` (niet `eVar2`) de afbeeldingsaanvraag die naar Adobe wordt verzonden:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
