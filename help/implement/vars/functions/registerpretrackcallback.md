---
title: registerPreTrackCallback
description: Creeer callback functies alvorens een klap naar Adobe te verzenden.
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# registerPreTrackCallback

Met de variabele `registerPreTrackCallback` kan uw organisatie een JavaScript-functie koppelen nadat een URL voor een afbeeldingsaanvraag is gecompileerd, maar voordat deze wordt verzonden. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld.

>[!IMPORTANT]
>
>Roep geen volgende vraag zoals [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen de [`registerPostTrackCallback`](registerposttrackcallback.md) variabele. De volgende functies in deze variabele veroorzaken een oneindige lijn van beeldverzoeken!

Elke keer dat u de variabele `registerPreTrackCallback` aanroept, koppelt u die functie om te worden uitgevoerd telkens wanneer een afbeeldingsverzoek-URL wordt gecompileerd. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die tussen `registerPreTrackCallback` en `registerPostTrackCallback` worden geactiveerd, zijn niet gegarandeerd. Vermijd afhankelijkheden tussen deze twee functies.

## Pre-track callback registreren met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPreTrackCallback in AppMeasurement en aangepaste code-editor

`s.registerPreTrackCallback` is een functie die een functie als zijn enige argument neemt. De geneste functie wordt uitgevoerd vlak voordat een afbeeldingsaanvraag wordt verzonden.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in uw code wilt gebruiken, verwijst u naar het tekenreeksargument `requestUrl` in de geneste functie. U kunt de `requestUrl` variabele voor uw gewenst gebruik ontleden; het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

U kunt aanvullende argumenten in de functie `s.registerPreTrackCallback` opnemen, die in de geneste functie kan worden gebruikt:

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
>Als u paginariabelen instelt of de `requestUrl`-tekenreeks in deze functie wijzigt, heeft dit **niet** invloed op de afbeeldingsaanvraag die kort na deze functieaanroep wordt verzonden. Gebruik in plaats hiervan de variabele [`doPlugins()`](doplugins.md).
