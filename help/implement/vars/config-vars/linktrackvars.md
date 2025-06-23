---
title: linkTrackVars
description: Geef op welke variabelen u wilt opnemen in aanvragen voor het bijhouden van koppelingen.
feature: Appmeasurement Implementation
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# linkTrackVars

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik de variabelen `linkTrackVars` en [`linkTrackEvents`](linktrackevents.md) om op selectieve wijze dimensies en metriek op te nemen in [`tl()`](../functions/tl-method.md) -aanroepen.

Deze variabele wordt niet gebruikt voor de vraag van de paginamening ([`t()`](../functions/t-method.md) methode).

## Bepaal welke variabelen in een XDM-gebeurtenis moeten worden opgenomen gebruikend de Web SDK

Het Web SDK sluit bepaalde gebieden voor verbinding het volgen vraag niet uit. U kunt echter de callback van `onBeforeEventSend` gebruiken om de gewenste velden te wissen of in te stellen voordat gegevens naar Adobe worden verzonden. Zie [ Veranderend gebeurtenissen globaal ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

## Variabelen in koppelingsvolgaanroepen met de Adobe Analytics-extensie

Deze variabele wordt automatisch ingevuld op de achtergrond op basis van variabelen die zijn ingesteld in de interface. De variabele wordt dus altijd ingesteld in implementaties met de Adobe Analytics-extensie.

>[!IMPORTANT]
>
>Als u variabelen instelt met de aangepaste code-editor, moet u ook de variabelen in `linkTrackVars` opnemen met behulp van aangepaste code.

## s.linkTrackVars in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.linkTrackVars` variabele is een tekenreeks met een door komma&#39;s gescheiden lijst met variabelen die u wilt opnemen in aanvragen voor het bijhouden van koppelingen (`tl()` methode). Aan beide volgende criteria moet worden voldaan om afmetingen op te nemen in het volgen van koppelingen:

* Stel de gewenste variabelewaarde in. Bijvoorbeeld `s.eVar1 = "Example value";` .
* Stel de gewenste variabele in de variabele `linkTrackVars` in. Bijvoorbeeld `s.linkTrackVars = "eVar1";` .

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Adobe heeft echter AppMeasurement-code opgegeven in Codebeheer waar deze variabele is ingesteld op `"None"` . Geldige waarden zijn variabelen op paginaniveau die een dimensie vullen.

* Als deze variabele niet wordt bepaald of aan een leeg koord wordt geplaatst, *alle* variabelen zijn inbegrepen in verbinding het volgen beeldverzoeken.
* Als deze variabele aan `"None"` wordt geplaatst, *geen* variabelen zijn inbegrepen in verbinding volgende beeldverzoeken.

>[!TIP]
>
>Gebruik niet de object-id Analytics (`s.`) wanneer u variabelen in deze variabele opgeeft. `s.linkTrackVars = "eVar1";` is bijvoorbeeld correct, terwijl `s.linkTrackVars = "s.eVar1";` onjuist is.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `eVar1` (niet `eVar2` ) in de afbeeldingsaanvraag die naar Adobe wordt verzonden:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
