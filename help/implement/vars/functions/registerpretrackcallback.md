---
title: registerPreTrackCallback
description: Creeer callback functies alvorens een klap naar Adobe te verzenden.
feature: Variables
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '417'
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

## Pre-track callback die de uitbreiding van SDK van het Web gebruikt

SDK van het Web heeft niet de capaciteit om een functie te verbinden nadat het gegeven wordt gecompileerd maar alvorens het naar Adobe wordt verzonden. U kunt echter `onBeforeEventSend` om een uit te voeren functie te registreren vlak voordat gegevens worden verzonden.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Edit on before event send callback code]** knop.
1. Plaats de gewenste code in de editor.

## Pre-track callback manueel uitvoerend SDK van het Web

SDK van het Web heeft niet de capaciteit om een functie te verbinden nadat het gegeven wordt gecompileerd maar alvorens het naar Adobe wordt verzonden. U kunt echter `onBeforeEventSend` om een functie te registreren die vlak voordat gegevens worden verzonden moet worden uitgevoerd, vergelijkbaar met `doPlugins`. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Pre-track callback die de uitbreiding van Adobe Analytics gebruikt

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.registerPreTrackCallback in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

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
