---
title: linkTrackEvents
description: Bepaal welke gebeurtenissen moeten worden opgenomen in aanvragen voor het bijhouden van koppelingen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkTrackEvents

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik de [`linkTrackVars`](linktrackvars.md) en de `linkTrackEvents` variabelen om afmetingen en metriek in [`tl()`](../functions/tl-method.md) vraag selectief te omvatten.

Deze variabele wordt niet gebruikt voor de vraag van de paginamening ([`t()`](../functions/t-method.md) methode).

## Gebeurtenissen in koppelingencontrole voor aanroepen met Adobe Experience Platform Launch

Start detecteert automatisch gebeurtenissen die in de interface zijn gedefinieerd en neemt deze op in resultaten voor het bijhouden van koppelingen.

>[!IMPORTANT] Als u gebeurtenissen in Lancering plaatst gebruikend de redacteur van de douanecode, moet u de gebeurtenis ook omvatten in het `linkTrackEvents` gebruiken van douanecode.

## s.linkTrackEvents in AppMeasurement en Launch, aangepaste code-editor

De `s.linkTrackEvents` variabele is een tekenreeks die een door komma&#39;s gescheiden lijst met gebeurtenissen bevat die u wilt opnemen in aanvragen voor het bijhouden van koppelingen (`tl()` methode). Aan de volgende drie criteria moet worden voldaan om meetgegevens op te nemen in treffers voor het bijhouden van koppelingen:

* Stel de gewenste gebeurtenis in de [`events`](../page-vars/events/events-overview.md) variabele in. Bijvoorbeeld, `s.events = "event1";`.
* Stel de `events` variabele in `linkTrackVars`. Bijvoorbeeld, `s.linkTrackVars = "events";`.
* Stel de gewenste gebeurtenis in de `linkTrackEvents` variabele in. Bijvoorbeeld, `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Als deze variabele niet is gedefinieerd, worden alle gebeurtenissen opgenomen in aanvragen voor het bijhouden van koppelingen. Merk op dat de Lancering automatisch deze variabele bevolkt die op gebeurtenissen in de interface wordt geplaatst, zodat wordt het altijd geplaatst in implementaties gebruikend Lancering.

>[!TIP] Vermijd het gebruik van de object-id (`s.`) voor Analytics wanneer u gebeurtenissen in deze variabele opgeeft. De waarde `s.linkTrackEvents = "event1";` is bijvoorbeeld correct, maar `s.linkTrackEvents = "s.event1";` is onjuist.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `event1` (niet `event2`) de afbeeldingsaanvraag die naar Adobe wordt verzonden:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
