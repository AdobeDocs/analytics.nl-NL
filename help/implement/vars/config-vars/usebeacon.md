---
title: useBeacon
description: Met useBeacon kunt u AppMeasurement forceren om de sendBeacon-API voor browsers te gebruiken
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# useBeacon

De meeste moderne browsers hebben de native methode `navigator.sendBeacon()`. Het verzendt asynchroon een kleine hoeveelheid gegevens over HTTP naar een Webserver. AppMeasurement kan de `navigator.sendBeacon()` methode gebruiken als `useBeacon` variabele wordt toegelaten. Het is handig om koppelingen af te sluiten en andere situaties te creëren waarin u informatie wilt verzenden voordat de pagina wordt verwijderd.

Wanneer `useBeacon` is ingeschakeld, gebruikt de volgende hit die naar Adobe wordt verzonden de methode `navigator.sendBeacon()` van de browser in plaats van een standaardafbeeldingsaanvraag `GET`. Deze variabele is van toepassing op afbeeldingsaanvragen [`s.t()`](../functions/t-method.md) en [`s.tl()`](../functions/tl-method.md). Hiervoor is AppMeasurement 2.17.0 of hoger vereist.

>[!TIP]
>
>AppMeasurement schakelt automatisch `useBeacon` in voor verzoeken om verbindingsafbeeldingen.

De variabele `useBeacon` wordt genegeerd wanneer de bezoeker een browser gebruikt die `navigator.sendBeacon()` niet ondersteunt. Het gebruik van deze variabele vereist AppMeasurement 2.16.0 of hoger.

## Baken gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useBeacon in AppMeasurement en aangepaste code-editor

De `s.useBeacon` variabele is een booleaanse waarde die bepaalt of AppMeturement de browser `navigator.sendBeacon()` methode gebruikt. De standaardwaarde is `false`. Stel deze variabele in op `true` voordat u een functie tracking aanroept als u de asynchrone aard van `navigator.sendBeacon()` wilt gebruiken.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Na een volgende vraaglooppas, wordt deze variabele teruggesteld aan `false`. Als uw implementatie meerdere afbeeldingsaanvragen verzendt in dezelfde paginalading (zoals toepassingen van één pagina), stelt u deze variabele in op `true` vóór elke volgende aanroep.
