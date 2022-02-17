---
title: registerPostTrackCallback
description: Creeer callback functies na het verzenden van een klap naar Adobe.
feature: Variables
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# registerPostTrackCallback

De `registerPostTrackCallback` Met deze variabele kan uw organisatie een JavaScript-functie direct koppelen nadat een hit naar Adobe is verzonden. Als een volgende aanroep mislukt, wordt deze functie niet uitgevoerd. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld, of veranderlijke waarden in enig-paginatoepassingen op te schonen.

>[!IMPORTANT]
>
>Om het even welke het volgen vraag niet zoals te roepen [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen `registerPostTrackCallback` variabele. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de `registerPostTrackCallback` variabele, verbindt u die functie om onmiddellijk te lopen nadat een beeldverzoek met succes wordt verzonden. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die worden geactiveerd tussen [`registerPreTrackCallback`](registerpretrackcallback.md) en `registerPostTrackCallback` niet gegarandeerd zijn. Vermijd afhankelijkheden tussen deze twee functies.

## Bijschrift achteraf registreren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPostTrackCallback in AppMeasurement en aangepaste code-editor

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
