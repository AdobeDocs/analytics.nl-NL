---
title: useBeacon
description: Met useBeacon kunt u AppMeasurement dwingen de sendBeacon-API van browsers te gebruiken
feature: Appmeasurement Implementation
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# useBeacon

De meeste moderne browsers beschikken over de native methode `navigator.sendBeacon()` . Het verzendt asynchroon een kleine hoeveelheid gegevens over HTTP naar een Webserver. AppMeasurement kan de methode `navigator.sendBeacon()` gebruiken als de variabele `useBeacon` is ingeschakeld. Het is handig om koppelingen af te sluiten en andere situaties te creëren waarin u informatie wilt verzenden voordat de pagina wordt verwijderd.

Als `useBeacon` is ingeschakeld, gebruikt de volgende hit die naar Adobe wordt verzonden de methode `navigator.sendBeacon()` van de browser in plaats van een standaard `GET` -afbeeldingsaanvraag. Deze variabele is van toepassing op afbeeldingsaanvragen [`s.t()`](../functions/t-method.md) en [`s.tl()`](../functions/tl-method.md) . Hiervoor is AppMeasurement 2.17.0 of hoger vereist.

>[!TIP]
>
>AppMeasurement schakelt `useBeacon` automatisch in voor aanvragen voor afsluitingsafbeeldingen.

De variabele `useBeacon` wordt genegeerd wanneer de bezoeker een browser gebruikt die `navigator.sendBeacon()` niet ondersteunt. Voor het gebruik van deze variabele is AppMeasurement 2.16.0 of hoger vereist.

## De sendBeacon-API gebruiken met de Web SDK-extensie

Het selectievakje **[!UICONTROL Document will unload]** in een configuratie van handelingen bepaalt of gegevens die naar Adobe worden verzonden de sendBeacon-API gebruiken.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar het tabblad [!UICONTROL Rules] en klik op de gewenste regel.
1. Klik onder [!UICONTROL Actions] op de gewenste handeling of klik op het pictogram **&#39;+&#39;** om een nieuwe handeling toe te voegen.
1. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Adobe Experience Platform Web SDK]** en op [!UICONTROL Action Type] op **[!UICONTROL Send event]**
1. Klik op het selectievakje **[!UICONTROL Document will unload]** aan de rechterkant.

Als dit vakje wordt gecontroleerd, worden de gegevens verzonden naar Adobe gebruikend sendBeacon API. Deze optie is standaard uitgeschakeld.

## Gebruik sendBeacon API manueel uitvoerend het Web SDK

Stel `documentUnloading` in op `true` wanneer u een gebeurtenis verzendt. Als deze niet is ingesteld, is de standaardwaarde `false` .

```json
alloy("sendEvent", {
  "documentUnloading": true,
  "xdm": {}
});
```

Zie [&#x200B; Gebruikend sendBeacon API &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#using-the-sendbeacon-api) in de documentatie van SDK van het Web voor meer informatie.

## Gebruik baken met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.useBeacon in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.useBeacon` is een Booleaanse waarde die bepaalt of AppMeasurement de methode `navigator.sendBeacon()` van de browser gebruikt. De standaardwaarde is `false` . Stel deze variabele in op `true` voordat u een functie tracking aanroept als u de asynchrone aard van `navigator.sendBeacon()` wilt gebruiken.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nadat een volgende vraag loopt, wordt deze variabele teruggesteld aan `false`. Als uw implementatie meerdere afbeeldingsaanvragen verzendt in dezelfde pagina die wordt geladen (zoals toepassingen van één pagina), stelt u deze variabele in op `true` vóór elke volgende aanroep.
