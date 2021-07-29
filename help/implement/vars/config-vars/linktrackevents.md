---
title: linkTrackEvents
description: Bepaal welke gebeurtenissen moeten worden opgenomen in aanvragen voor het bijhouden van koppelingen.
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 3%

---

# linkTrackEvents

Sommige implementaties willen niet alle variabelen in alle verbinding het volgen beeldverzoeken omvatten. Gebruik [`linkTrackVars`](linktrackvars.md) en `linkTrackEvents` variabelen om afmetingen en metriek in [`tl()`](../functions/tl-method.md) vraag selectief te omvatten.

Deze variabele wordt niet gebruikt voor de vraag van de paginamening ([`t()`](../functions/t-method.md) methode).

## Gebeurtenissen in koppelingsvolgaanroepen met tags in Adobe Experience Platform

Als u geen aangepaste code gebruikt, worden in Adobe Experience Platform automatisch gedefinieerde gebeurtenissen opgenomen in resultaten voor het bijhouden van koppelingen.

>[!IMPORTANT]
>
>Als u gebeurtenissen in de UI van de Inzameling van Gegevens gebruikend de redacteur van de douanecode plaatst, moet u de gebeurtenis in `linkTrackEvents` ook gebruikend douanecode omvatten.

## s.linkTrackEvents in AppMeasurement en aangepaste code-editor

De `s.linkTrackEvents` variabele is een koord dat een komma-afgebakende lijst van gebeurtenissen bevat die u in verbinding het volgen beeldverzoeken (`tl()` methode) wilt omvatten. Aan de volgende drie criteria moet worden voldaan om meetgegevens op te nemen in treffers voor het bijhouden van koppelingen:

* Stel de gewenste gebeurtenis in de variabele [`events`](../page-vars/events/events-overview.md) in. Bijvoorbeeld, `s.events = "event1";`.
* Stel de variabele `events` in `linkTrackVars` in. Bijvoorbeeld, `s.linkTrackVars = "events";`.
* Stel de gewenste gebeurtenis in de variabele `linkTrackEvents` in. Bijvoorbeeld, `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

De standaardwaarde voor deze variabele is een lege tekenreeks. Als deze variabele niet is gedefinieerd, worden alle gebeurtenissen opgenomen in aanvragen voor het bijhouden van koppelingen. Merk op dat de Inzameling van Gegevens automatisch deze variabele bevolkt die op gebeurtenissen in de interface wordt geplaatst, zodat wordt het altijd geplaatst voor implementaties die markeringen in Adobe Experience Platform gebruiken.

>[!TIP]
>
>Vermijd het gebruik van de object-id Analytics (`s.`) bij het opgeven van gebeurtenissen in deze variabele. `s.linkTrackEvents = "event1";` is bijvoorbeeld juist, terwijl `s.linkTrackEvents = "s.event1";` onjuist is.

## Voorbeeld

De volgende functie voor het bijhouden van koppelingen bevat alleen `event1` (niet `event2`) in het afbeeldingsverzoek dat naar Adobe wordt verzonden:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
