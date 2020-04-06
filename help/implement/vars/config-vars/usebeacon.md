---
title: useBeacon
description: Met useBeacon kunt u AppMeasurement forceren om de sendBeacon-API voor browsers te gebruiken
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# useBeacon

De meeste moderne browsers beschikken over de native methode `navigator.sendBeacon()`. Het verzendt asynchroon een kleine hoeveelheid gegevens over HTTP naar een Webserver. AppMeasurement kan de `navigator.sendBeacon()` methode gebruiken als de `useBeacon` variabele wordt toegelaten. Het is handig om koppelingen af te sluiten en andere situaties te creëren waarin u informatie wilt verzenden voordat de pagina wordt verwijderd.

Als `useBeacon` deze optie is ingeschakeld, gebruikt de volgende hit die naar Adobe wordt verzonden de `navigator.sendBeacon()` methode van de browser in plaats van een standaard `GET` afbeeldingsaanvraag. Deze variabele is van toepassing op zowel [`s.t()`](../functions/t-method.md) afbeeldingsaanvragen als [`s.tl()`](../functions/tl-method.md) afbeeldingsaanvragen. Hiervoor is AppMeasurement 2.17.0 of hoger vereist.

>[!TIP] AppMeasurement schakelt automatisch `useBeacon` voor het afsluiten van afbeeldingsaanvragen voor koppelingen in.

De `useBeacon` variabele wordt genegeerd wanneer de bezoeker een browser gebruikt die geen ondersteuning biedt `navigator.sendBeacon()`. Het gebruik van deze variabele vereist AppMeasurement 2.16.0 of hoger.

## Beacon gebruiken in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useBeacon in de redacteur van de douanecode van AppMeasurement en van de Lancering

De `s.useBeacon` variabele is een Booleaanse waarde die bepaalt of AppMeturement de `navigator.sendBeacon()` methode van de browser gebruikt. De standaardwaarde is `false`. Stel deze variabele in op `true` voordat u een functie tracking aanroept als u de asynchrone aard van `navigator.sendBeacon()`de variabele wilt gebruiken.

```js
s.useBeacon = true;
```

>[!NOTE] Nadat een volgende vraag loopt, wordt deze variabele teruggesteld aan `false`. Als uw implementatie meerdere verzoeken om afbeeldingen verzendt in dezelfde pagina die wordt geladen (zoals toepassingen van één pagina), stelt u deze variabele in op `true` vóór elke volgende aanroep.
