---
title: registerPostTrackCallback
description: Creeer callback functies na het verzenden van een klap naar Adobe.
feature: Variables
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# registerPostTrackCallback

De `registerPostTrackCallback` Met deze variabele kan uw organisatie een JavaScript-functie direct koppelen nadat een hit naar Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld, of veranderlijke waarden in enig-paginatoepassingen op te schonen.

>[!WARNING]
>
>Om het even welke het volgen vraag niet zoals te roepen [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen `registerPostTrackCallback` variabele. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de `registerPostTrackCallback` variabele, verbindt u die functie om onmiddellijk te lopen nadat een beeldverzoek met succes wordt verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die worden geactiveerd tussen [`registerPreTrackCallback`](registerpretrackcallback.md) en `registerPostTrackCallback` niet gegarandeerd zijn. Vermijd afhankelijkheden tussen deze twee functies.

## Natrack Callback die de uitbreiding van SDK van het Web gebruikt

Binnenkort verkrijgbaar!

## Natrack Callback die manueel SDK van het Web uitvoert

U kunt een JavaScript-belofte gebruiken wanneer u een gebeurtenis verzendt om een functie te registreren nadat gegevens naar Adobe zijn verzonden.

```js
alloy("sendEvent",{
  "xdm": {}
}).then(function(result) {
  Console.Log("Data was successfully sent.");
});
```

Zie [Reacties van gebeurtenissen afhandelen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#handling-responses-from-events) in de documentatie van SDK van het Web voor meer informatie.

## Navolgende callback registreren met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPostTrackCallback in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.registerPostTrackCallback` is een functie die een functie als het enige argument neemt. De geneste functie wordt direct uitgevoerd nadat een afbeeldingsaanvraag is verzonden.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in de code wilt gebruiken, raadpleegt u de `requestUrl` tekenreeksargument binnen de geneste functie. U kunt de `requestUrl` variabele voor het gewenste gebruik; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

U kunt aanvullende argumenten opnemen in het dialoogvenster `s.registerPostTrackCallback` functie, die in de geneste functie kan worden gebruikt:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Voorbeeld van hoofdletters gebruiken

Registreren van de [`clearVars()`](clearvars.md) functie in de callback post track kan voordelig zijn voor single-page toepassingen. Telkens wanneer u met succes een klap naar Adobe verzendt, `clearVars()` functie wordt uitgevoerd. Uw implementatie kan vervolgens opnieuw variabelen definiëren zonder dat u zich zorgen hoeft te maken over onjuist blijvende waarden.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
