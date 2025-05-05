---
title: useBeacon
description: useBeacon laat u AppMeasurement dwingen om browsers te gebruiken sendBeacon API
feature: Variables
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# useBeacon

De meeste moderne browsers beschikken over de native methode `navigator.sendBeacon()`. Het verzendt asynchroon een kleine hoeveelheid gegevens over HTTP naar een Webserver. AppMeasurement kan de `navigator.sendBeacon()` als de `useBeacon` variable is enabled. Het is handig om koppelingen af te sluiten en andere situaties te creëren waarin u informatie wilt verzenden voordat de pagina wordt verwijderd.

Indien `useBeacon` is ingeschakeld, gebruikt de volgende hit die naar de Adobe wordt verzonden de browser `navigator.sendBeacon()` in plaats van een standaard `GET` afbeeldingsverzoek. Deze variabele is van toepassing op beide [`s.t()`](../functions/t-method.md) en [`s.tl()`](../functions/tl-method.md) verzoeken om afbeeldingen. Hiervoor is AppMeasurement 2.17.0 of hoger vereist.

>[!TIP]
>
>AppMeasurement schakelt automatisch `useBeacon` voor verzoeken om verbindingsafbeeldingen af te sluiten.

De `useBeacon` variabele wordt genegeerd wanneer de bezoeker een browser gebruikt die geen ondersteuning biedt `navigator.sendBeacon()`. Voor het gebruik van deze variabele is AppMeasurement 2.16.0 of hoger vereist.

## Gebruik sendBeacon API gebruikend de uitbreiding van SDK van het Web

De **[!UICONTROL Document will unload]** checkbox binnen een Configuratie van de Actie bepaalt als de gegevens die naar Adobe worden verzonden sendBeacon API gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Rules] en klikt u op de gewenste regel.
1. Onder [!UICONTROL Actions], klikt u op de gewenste handeling of klikt u op de knop **&#39;+&#39;** pictogram om een nieuwe handeling toe te voegen.
1. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar **[!UICONTROL Adobe Experience Platform Web SDK]** en de [!UICONTROL Action Type] tot **[!UICONTROL Send event]**
1. Klik op het selectievakje **[!UICONTROL Document will unload]** rechts.

Als dit vakje wordt gecontroleerd, worden de gegevens verzonden naar Adobe gebruikend sendBeacon API. Deze optie is standaard uitgeschakeld.

## Gebruik sendBeacon API manueel uitvoerend de SDK van het Web

Set `documentUnloading` tot `true` wanneer u een gebeurtenis verzendt. Indien niet ingesteld, is de standaardwaarde ervan `false`.

```json
alloy("sendEvent", {
  "documentUnloading": true,
  "xdm": {}
});
```

Zie [De sendBeacon-API gebruiken](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#using-the-sendbeacon-api) in de documentatie van SDK van het Web voor meer informatie.

## Gebruik baken met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.useBeacon in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.useBeacon` variabele is een Booleaanse waarde die bepaalt of het AppMeasurement de browser gebruikt `navigator.sendBeacon()` methode. De standaardwaarde is `false`. Deze variabele instellen op `true` voordat u een functie tracking aanroept als u de asynchrone aard van `navigator.sendBeacon()`.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nadat een volgende vraag loopt, wordt deze variabele teruggesteld aan `false`. Als uw implementatie meerdere afbeeldingsaanvragen verzendt in dezelfde pagina die wordt geladen (zoals toepassingen van één pagina), stelt u deze variabele in op `true` vóór elke volgende vraag.
