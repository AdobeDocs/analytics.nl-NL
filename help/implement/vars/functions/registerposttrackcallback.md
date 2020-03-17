---
title: registerPostTrackCallback
description: Maak callback-functies nadat u een hit naar Adobe hebt verzonden.
translation-type: tm+mt
source-git-commit: acfcb1f27650649581875680e7897e5c9813765a

---


# registerPostTrackCallback

Met de `registerPostTrackCallback` variabele kan uw organisatie een JavaScript-functie direct koppelen nadat een hit naar Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld, of veranderlijke waarden in enig-paginatoepassingen op te schonen.

> [!IMPORTANT] Roep geen volgende functies zoals `t` of `tl` binnen de `registerPostTrackCallback` variabele aan. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Telkens wanneer u de `registerPostTrackCallback` variabele aanroept, koppelt u die functie om onmiddellijk te lopen nadat een beeldverzoek met succes wordt verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

> [!NOTE] De timing en de volgorde van de functies die tussen `registerPreTrackCallback` en `registerPostTrackCallback` worden uitgevoerd, zijn niet gegarandeerd. Vermijd afhankelijkheden tussen deze twee functies.

## Callback achteraf registreren bij starten van Adobe Experience Platform

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPostTrackCallback in AppMeasurement en Launch, aangepaste code-editor

Het `s.registerPostTrackCallback` is een functie die een functie als het enige argument gebruikt. De geneste functie wordt uitgevoerd vlak voordat een afbeeldingsaanvraag wordt verzonden.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in de code wilt gebruiken, verwijst u naar het `requestUrl` tekenreeksargument in de geneste functie. U kunt de `requestUrl` variabele voor uw gewenste gebruik ontleden; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

De functie kan extra argumenten bevatten, die in de genestelde functie kunnen worden gebruikt: `s.registerPostTrackCallback`

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Voorbeeld van hoofdletters gebruiken

Registreren van de `clearVars()` functie in de callback achteraf kan nuttig zijn voor toepassingen van één pagina. Telkens wanneer u een hit naar Adobe verzendt, wordt de `clearVars()` functie uitgevoerd. Uw implementatie kan vervolgens opnieuw variabelen definiëren zonder dat u zich zorgen hoeft te maken over onjuist blijvende waarden.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
