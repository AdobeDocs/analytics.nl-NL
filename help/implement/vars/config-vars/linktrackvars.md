---
title: linkTrackVars
description: Geef op welke variabelen u wilt opnemen in aanvragen voor het bijhouden van koppelingen.
feature: Variables
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---

# linkTrackVars

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik de `linkTrackVars` en [`linkTrackEvents`](linktrackevents.md) te selecteren variabelen om afmetingen en metriek op te nemen in [`tl()`](../functions/tl-method.md) oproepen.

Deze variabele wordt niet gebruikt voor paginaweergaveaanroepen ([`t()`](../functions/t-method.md) methode).

## Bepaal welke variabelen om in een gebeurtenis te omvatten XDM gebruikend het Web SDK

De SDK van het Web sluit bepaalde gebieden voor verbinding het volgen vraag niet uit. U kunt echter de opdracht `onBeforeEventSend` callback om gewenste gebieden te ontruimen of te plaatsen alvorens de gegevens naar Adobe worden verzonden. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

## Variabelen in koppelingsvolgaanroepen met de Adobe Analytics-extensie

Deze variabele wordt automatisch ingevuld op de achtergrond op basis van variabelen die in de interface zijn ingesteld. De variabele wordt dus altijd ingesteld in implementaties met de Adobe Analytics-extensie.

>[!IMPORTANT]
>
>Als u variabelen instelt met de aangepaste code-editor, moet u de variabelen opnemen in `linkTrackVars` ook aangepaste code gebruiken.

## s.linkTrackVars in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.linkTrackVars` variabele is een tekenreeks met een door komma&#39;s gescheiden lijst met variabelen die u wilt opnemen in aanvragen voor het bijhouden van koppelingen (`tl()` methode). Aan beide volgende criteria moet worden voldaan om afmetingen op te nemen in het volgen van koppelingen:

* Stel de gewenste variabelewaarde in. Bijvoorbeeld, `s.eVar1 = "Example value";`.
* Stel de gewenste variabele in het dialoogvenster `linkTrackVars` variabele. Bijvoorbeeld, `s.linkTrackVars = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Nochtans, verstrekte Adobe code AppMeasurement in de Manager van de Code waar deze variabele aan wordt geplaatst `"None"`. Geldige waarden zijn variabelen op paginaniveau die een dimensie vullen.

* Als deze variabele niet is gedefinieerd of op een lege tekenreeks is ingesteld, *alles* variabelen zijn opgenomen in aanvragen voor afbeeldingen voor het bijhouden van koppelingen.
* Als deze variabele is ingesteld op `"None"`, *nee* variabelen zijn opgenomen in aanvragen voor afbeeldingen voor het bijhouden van koppelingen.

>[!TIP]
>
>Gebruik de id van het object Analytics (`s.`) wanneer u variabelen in deze variabele opgeeft. Bijvoorbeeld: `s.linkTrackVars = "eVar1";` is correct, terwijl `s.linkTrackVars = "s.eVar1";` is onjuist.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `eVar1` (niet `eVar2`) in de afbeeldingsaanvraag die naar Adobe wordt verzonden:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
