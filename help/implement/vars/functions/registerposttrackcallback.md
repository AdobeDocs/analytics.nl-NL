---
title: registerPostTrackCallback
description: Maak callback-functies nadat een hit naar Adobe is verzonden.
feature: Appmeasurement Implementation
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# registerPostTrackCallback

Met de variabele `registerPostTrackCallback` kan uw organisatie een JavaScript-functie direct koppelen nadat een hit naar Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement worden verzameld naar een partner of interne infrastructuur, of veranderlijke waarden in single-page toepassingen op te schonen.

>[!WARNING]
>
>Maak geen volgende aanroepen zoals [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen de variabele `registerPostTrackCallback` . Het plaatsen van het volgen vraag in deze variabele veroorzaakt een oneindige lijn van beeldverzoeken!

Telkens wanneer u de variabele `registerPostTrackCallback` aanroept, koppelt u die functie aan uitvoering direct nadat een afbeeldingsaanvraag is verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die tussen [`registerPreTrackCallback`](registerpretrackcallback.md) en `registerPostTrackCallback` worden geactiveerd, zijn niet gegarandeerd. Vermijd afhankelijkheid tussen deze twee functies.

## Natrack Callback die de uitbreiding van SDK van het Web gebruikt

Binnenkort verkrijgbaar!

## Navolgende Callback die manueel het Web SDK implementeert

U kunt een JavaScript Promise gebruiken wanneer u een gebeurtenis verzendt om een functie te registreren nadat gegevens naar Adobe zijn verzonden.

```js
alloy("sendEvent",{
  "xdm": {}
}).then(function(result) {
  Console.Log("Data was successfully sent.");
});
```

Zie [ Behandelende reacties van gebeurtenissen ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#handling-responses-from-events) in de documentatie van SDK van het Web voor meer informatie.

## Navolgende callback registreren met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.registerPostTrackCallback in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

`s.registerPostTrackCallback` is een functie die een functie als het enige argument neemt. De geneste functie wordt direct uitgevoerd nadat een afbeeldingsaanvraag is verzonden.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in uw code wilt gebruiken, verwijst u naar het tekenreeksargument `requestUrl` in de geneste functie. U kunt de variabele `requestUrl` parseren voor het gewenste gebruik. Het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Aanvullende argumenten kunnen worden opgenomen in de functie `s.registerPostTrackCallback` , die in de geneste functie kan worden gebruikt:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Hoofdletters gebruiken

Het registreren van de functie [`clearVars()`](clearvars.md) in de callback na track kan nuttig zijn voor toepassingen van één pagina. Telkens wanneer u een hit naar Adobe verzendt, wordt de functie `clearVars()` uitgevoerd. Uw implementatie kan vervolgens opnieuw variabelen definiëren zonder dat u zich zorgen hoeft te maken over onjuist blijvende waarden.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
