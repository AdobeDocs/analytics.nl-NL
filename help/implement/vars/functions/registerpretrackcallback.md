---
title: registerPreTrackCallback
description: Creeer callback functies alvorens een klap naar Adobe te verzenden.
feature: Variables
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
source-git-commit: 3f4d8df911c076a5ea41e7295038c0625a4d7c85
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# registerPreTrackCallback

De `registerPreTrackCallback` Met een variabele kan uw organisatie een JavaScript-functie koppelen nadat een URL voor een afbeeldingsaanvraag is gecompileerd, maar voordat deze wordt verzonden. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld.

>[!WARNING]
>
>Om het even welke het volgen vraag niet zoals te roepen [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen [`registerPostTrackCallback`](registerposttrackcallback.md) variabele. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de `registerPreTrackCallback` variabele, verbindt u die functie om te lopen telkens als een beeldverzoek URL wordt gecompileerd. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die worden geactiveerd tussen `registerPreTrackCallback` en `registerPostTrackCallback` niet gegarandeerd zijn. Vermijd afhankelijkheden tussen deze twee functies.

## Pre-track callback registreren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPreTrackCallback in AppMeasurement en aangepaste code-editor

De `s.registerPreTrackCallback` is een functie die een functie als het enige argument neemt. De geneste functie wordt uitgevoerd vlak voordat een afbeeldingsaanvraag wordt verzonden.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in de code wilt gebruiken, raadpleegt u de `requestUrl` tekenreeksargument binnen de geneste functie. U kunt de `requestUrl` variabele voor het gewenste gebruik; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

U kunt aanvullende argumenten opnemen in het dialoogvenster `s.registerPreTrackCallback` functie, die in de geneste functie kan worden gebruikt:

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

>[!NOTE]
>
>Paginariabelen instellen of het `requestUrl` string binnen deze functie do **niet** heeft invloed op de aanvraag voor de afbeelding die kort na deze functieaanroep wordt verzonden. Gebruik de [`doPlugins()`](doplugins.md) in plaats daarvan variabele.
