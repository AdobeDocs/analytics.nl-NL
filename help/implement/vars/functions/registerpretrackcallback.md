---
title: registerPreTrackCallback
description: Maak callback-functies voordat u een hit naar Adobe verzendt.
translation-type: tm+mt
source-git-commit: ''

---


# registerPreTrackCallback

Met de `registerPreTrackCallback` variabele kan uw organisatie een JavaScript-functie koppelen nadat een URL voor een afbeeldingsaanvraag is gecompileerd, maar voordat deze wordt verzonden. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld.

> [!IMPORTANT] Roep geen volgende functies zoals `t` of `tl` binnen de `registerPostTrackCallback` variabele aan. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de `registerPreTrackCallback` variabele aanroept, koppelt u die functie om te worden uitgevoerd telkens wanneer een afbeeldingsaanvraag-URL wordt gecompileerd. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

> [!NOTE] De timing en de volgorde van de functies die tussen `registerPreTrackCallback` en `registerPostTrackCallback` worden uitgevoerd, zijn niet gegarandeerd. Vermijd afhankelijkheden tussen deze twee functies.

## Back-up voor track registreren bij starten van Adobe Experience Platform

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPreTrackCallback in AppMeasurement en Launch, aangepaste code-editor

Het `s.registerPreTrackCallback` is een functie die een functie als het enige argument gebruikt. De geneste functie wordt uitgevoerd vlak voordat een afbeeldingsaanvraag wordt verzonden.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in de code wilt gebruiken, verwijst u naar het `requestUrl` tekenreeksargument in de geneste functie. U kunt de `requestUrl` variabele voor uw gewenste gebruik ontleden; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

De functie kan extra argumenten bevatten, die in de genestelde functie kunnen worden gebruikt: `s.registerPreTrackCallback`

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

> [!NOTE] Het instellen van paginariabelen of het wijzigen van de `requestUrl` tekenreeks binnen deze functie heeft *geen* invloed op de afbeeldingsaanvraag die kort na deze functieaanroep wordt verzonden.
