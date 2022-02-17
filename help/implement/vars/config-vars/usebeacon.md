---
title: useBeacon
description: Met useBeacon kunt u AppMeasurement forceren om de sendBeacon-API voor browsers te gebruiken
feature: Variables
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# useBeacon

De meeste moderne browsers beschikken over de native methode `navigator.sendBeacon()`. Het verzendt asynchroon een kleine hoeveelheid gegevens over HTTP naar een Webserver. AppMeasurement kan de `navigator.sendBeacon()` als de `useBeacon` variable is enabled. Het is handig om koppelingen af te sluiten en andere situaties te creëren waarin u informatie wilt verzenden voordat de pagina wordt verwijderd.

Indien `useBeacon` is ingeschakeld, gebruikt de volgende hit die naar Adobe wordt verzonden de browser `navigator.sendBeacon()` in plaats van een standaard `GET` afbeeldingsverzoek. Deze variabele is van toepassing op beide [`s.t()`](../functions/t-method.md) en [`s.tl()`](../functions/tl-method.md) verzoeken om afbeeldingen. Hiervoor is AppMeasurement 2.17.0 of hoger vereist.

>[!TIP]
>
>AppMeasurement schakelt automatisch `useBeacon` voor verzoeken om verbindingsafbeeldingen af te sluiten.

De `useBeacon` variabele wordt genegeerd wanneer de bezoeker een browser gebruikt die geen ondersteuning biedt `navigator.sendBeacon()`. Het gebruik van deze variabele vereist AppMeasurement 2.16.0 of hoger.

## Baken gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useBeacon in AppMeasurement en aangepaste code-editor

De `s.useBeacon` De variabele is een Booleaanse waarde die bepaalt of AppMeasurement de browser gebruikt `navigator.sendBeacon()` methode. De standaardwaarde is `false`. Deze variabele instellen op `true` voordat u een functie tracking aanroept als u de asynchrone aard van `navigator.sendBeacon()`.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nadat een volgende vraag loopt, wordt deze variabele teruggesteld aan `false`. Als uw implementatie meerdere afbeeldingsaanvragen verzendt in dezelfde pagina die wordt geladen (zoals toepassingen van één pagina), stelt u deze variabele in op `true` vóór elke volgende vraag.
