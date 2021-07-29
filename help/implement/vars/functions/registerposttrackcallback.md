---
title: registerPostTrackCallback
description: Creeer callback functies na het verzenden van een klap naar Adobe.
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# registerPostTrackCallback

Met de variabele `registerPostTrackCallback` kan uw organisatie een JavaScript-functie direct koppelen nadat een hit naar Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld, of veranderlijke waarden in enig-paginatoepassingen op te schonen.

>[!IMPORTANT]
>
>Roep geen volgende vraag zoals [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen de `registerPostTrackCallback` variabele. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de variabele `registerPostTrackCallback` aanroept, koppelt u die functie om onmiddellijk te worden uitgevoerd nadat een afbeeldingsverzoek is verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die tussen [`registerPreTrackCallback`](registerpretrackcallback.md) en `registerPostTrackCallback` worden geactiveerd, zijn niet gegarandeerd. Vermijd afhankelijkheden tussen deze twee functies.

## Bijschrift achteraf registreren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPostTrackCallback in AppMeasurement en aangepaste code-editor

`s.registerPostTrackCallback` is een functie die een functie als zijn enige argument neemt. De geneste functie wordt direct uitgevoerd nadat een afbeeldingsaanvraag is verzonden.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in uw code wilt gebruiken, verwijst u naar het tekenreeksargument `requestUrl` in de geneste functie. U kunt de `requestUrl` variabele voor uw gewenst gebruik ontleden; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Aanvullende argumenten kunnen worden opgenomen in de functie `s.registerPostTrackCallback`, die in de geneste functie kan worden gebruikt:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Voorbeeld van hoofdletters gebruiken

Registreren van de functie [`clearVars()`](clearvars.md) in de callback na track kan nuttig zijn voor toepassingen van één pagina. Telkens wanneer u een hit naar Adobe verzendt, wordt de functie `clearVars()` uitgevoerd. Uw implementatie kan vervolgens opnieuw variabelen definiëren zonder dat u zich zorgen hoeft te maken over onjuist blijvende waarden.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
