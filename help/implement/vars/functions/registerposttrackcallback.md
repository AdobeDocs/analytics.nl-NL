---
title: registerPostTrackCallback
description: Creeer callback functies na het verzenden van een klap aan Adobe.
feature: Variables
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# registerPostTrackCallback

De `registerPostTrackCallback` Met deze variabele kan uw organisatie een JavaScript-functie direct koppelen nadat een treffer naar de Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of in-huis infrastructuur worden verzameld, of veranderlijke waarden in enig-paginatoepassingen op te schonen.

>[!WARNING]
>
>Maak geen volgende vraag zoals [`t()`](t-method.md) of [`tl()`](tl-method.md) in de `registerPostTrackCallback` variabele. Het plaatsen van het volgen vraag in deze variabele veroorzaakt een oneindige lijn van beeldverzoeken!

Elke keer dat u de `registerPostTrackCallback` variabele, verbindt u die functie om onmiddellijk te lopen nadat een beeldverzoek met succes wordt verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die worden geactiveerd tussen [`registerPreTrackCallback`](registerpretrackcallback.md) en `registerPostTrackCallback` niet gegarandeerd zijn. Vermijd afhankelijkheid tussen deze twee functies.

## Natrack Callback die de uitbreiding van SDK van het Web gebruikt

Binnenkort verkrijgbaar!

## Natrack Callback die manueel SDK van het Web uitvoert

U kunt een JavaScript-belofte gebruiken wanneer u een gebeurtenis verzendt om een functie te registreren nadat gegevens naar de Adobe zijn verzonden.

```js
alloy("sendEvent",{
  "xdm": {}
}).then(function(result) {
  Console.Log("Data was successfully sent.");
});
```

Zie [Reacties van gebeurtenissen afhandelen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#handling-responses-from-events) in de documentatie van SDK van het Web voor meer informatie.

## Navolgende callback registreren met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.registerPostTrackCallback in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.registerPostTrackCallback` is een functie die een functie als het enige argument neemt. De geneste functie wordt direct uitgevoerd nadat een afbeeldingsaanvraag is verzonden.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in de code wilt gebruiken, raadpleegt u de `requestUrl` tekenreeksargument binnen de geneste functie. U kunt de `requestUrl` variabele voor het gewenste gebruik. Het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

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

## Hoofdletters gebruiken

Registreren van de [`clearVars()`](clearvars.md) functie in de callback post track kan voordelig zijn voor single-page toepassingen. Telkens wanneer u met succes een klap naar Adobe verzendt, `clearVars()` functie wordt uitgevoerd. Uw implementatie kan vervolgens opnieuw variabelen definiëren zonder dat u zich zorgen hoeft te maken over onjuist blijvende waarden.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
