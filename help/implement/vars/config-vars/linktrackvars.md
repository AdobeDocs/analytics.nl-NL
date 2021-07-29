---
title: linkTrackVars
description: Geef op welke variabelen u wilt opnemen in aanvragen voor het bijhouden van koppelingen.
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# linkTrackVars

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik `linkTrackVars` en [`linkTrackEvents`](linktrackevents.md) variabelen om afmetingen en metriek in [`tl()`](../functions/tl-method.md) vraag selectief te omvatten.

Deze variabele wordt niet gebruikt voor de vraag van de paginamening ([`t()`](../functions/t-method.md) methode).

## Variabelen in koppelingsvolgaanroepen met tags in Adobe Experience Platform

Adobe Experience Platform vult deze variabele automatisch op de achtergrond in op basis van variabelen die in de interface zijn ingesteld. Deze variabele wordt daarom altijd ingesteld in implementaties met tags in Adobe Experience Platform.

>[!IMPORTANT]
>
>Als u variabelen plaatst gebruikend de redacteur van de douanecode, moet u de variabele in `linkTrackVars` ook gebruikend douanecode omvatten.

## s.linkTrackVars in AppMeasurement en aangepaste code-editor

De `s.linkTrackVars` variabele is een koord dat een komma-afgebakende lijst van variabelen bevat die u in verbinding het volgen beeldverzoeken (`tl()` methode) wilt omvatten. Aan beide volgende criteria moet worden voldaan om afmetingen op te nemen in het volgen van koppelingen:

* Stel de gewenste variabelewaarde in. Bijvoorbeeld, `s.eVar1 = "Example value";`.
* Stel de gewenste variabele in de variabele `linkTrackVars` in. Bijvoorbeeld, `s.linkTrackVars = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Nochtans, verstrekte Adobe code AppMeasurement in de Manager van de Code waar deze variabele aan `"None"` wordt geplaatst. Geldige waarden zijn variabelen op paginaniveau die een dimensie vullen.

* Als deze variabele niet is gedefinieerd of op een lege tekenreeks is ingesteld, worden *alle*-variabelen opgenomen in aanvragen voor het bijhouden van koppelingen.
* Als deze variabele op `"None"` wordt geplaatst, *no* worden de variabelen omvat in verbinding het volgen beeldverzoeken.

>[!TIP]
>
>Vermijd het gebruik van de object-id Analytics (`s.`) bij het opgeven van variabelen in deze variabele. `s.linkTrackVars = "eVar1";` is bijvoorbeeld juist, terwijl `s.linkTrackVars = "s.eVar1";` onjuist is.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `eVar1` (niet `eVar2`) in het afbeeldingsverzoek dat naar Adobe wordt verzonden:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
