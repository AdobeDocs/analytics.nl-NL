---
title: linkTrackEvents
description: Bepaal welke gebeurtenissen moeten worden opgenomen in aanvragen voor het bijhouden van koppelingen.
feature: Appmeasurement Implementation
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# linkTrackEvents

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik de variabelen [`linkTrackVars`](linktrackvars.md) en `linkTrackEvents` om op selectieve wijze dimensies en metriek op te nemen in [`tl()`](../functions/tl-method.md) -aanroepen.

Deze variabele wordt niet gebruikt voor de vraag van de paginamening ([`t()`](../functions/t-method.md) methode).

## Bepaal welke gebeurtenissen van Analytics om in een gebeurtenis te omvatten XDM gebruikend het Web SDK

Het Web SDK sluit bepaalde gebieden voor verbinding het volgen vraag niet uit. U kunt echter de callback van `onBeforeEventSend` gebruiken om de gewenste velden te wissen of in te stellen voordat gegevens naar Adobe worden verzonden. Zie [ Veranderend gebeurtenissen globaal ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

## Gebeurtenissen in koppelingencontrole voor aanroepen met de Adobe Analytics-extensie

Als u geen aangepaste code gebruikt, worden in Adobe Experience Platform automatisch gedefinieerde gebeurtenissen opgenomen in resultaten voor het bijhouden van koppelingen.

>[!IMPORTANT]
>
>Als u gebeurtenissen instelt in de aangepaste code-editor van de extensie Analytics, moet u de gebeurtenis ook opnemen in `linkTrackEvents` met behulp van aangepaste code.

## s.linkTrackEvents in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkTrackEvents` is een tekenreeks met een door komma&#39;s gescheiden lijst met gebeurtenissen die u wilt opnemen in aanvragen voor het bijhouden van koppelingen (`tl()` -methode). Aan de volgende drie criteria moet worden voldaan om meetgegevens op te nemen in treffers voor het bijhouden van koppelingen:

* Stel de gewenste gebeurtenis in de variabele [`events`](../page-vars/events/events-overview.md) in. Bijvoorbeeld `s.events = "event1";` .
* Stel de variabele `events` in `linkTrackVars` in. Bijvoorbeeld `s.linkTrackVars = "events";` .
* Stel de gewenste gebeurtenis in de variabele `linkTrackEvents` in. Bijvoorbeeld `s.linkTrackEvents = "event1";` .

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Als deze variabele niet is gedefinieerd, worden alle gebeurtenissen opgenomen in aanvragen voor het bijhouden van koppelingen. Merk op dat de Inzameling van Gegevens automatisch deze variabele bevolkt die op gebeurtenissen in de interface wordt geplaatst, zodat wordt het altijd geplaatst voor implementaties die markeringen in Adobe Experience Platform gebruiken.

>[!TIP]
>
>Vermijd het gebruik van de object-id Analytics (`s.`) wanneer u gebeurtenissen in deze variabele opgeeft. `s.linkTrackEvents = "event1";` is bijvoorbeeld correct, terwijl `s.linkTrackEvents = "s.event1";` onjuist is.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `event1` (niet `event2` ) in de afbeeldingsaanvraag die naar Adobe wordt verzonden:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
