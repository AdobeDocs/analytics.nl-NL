---
title: registerPreTrackCallback
description: Maak callback-functies voordat u een hit naar Adobe verzendt.
feature: Appmeasurement Implementation
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# registerPreTrackCallback

Met de variabele `registerPreTrackCallback` kan uw organisatie een JavaScript-functie koppelen nadat een URL voor een afbeeldingsaanvraag is gecompileerd, maar voordat deze wordt verzonden. U kunt deze variabele gebruiken om gegevens te verzenden die door AppMeasurement aan een partner of interne infrastructuur worden verzameld.

>[!WARNING]
>
>Maak geen volgende aanroepen zoals [`t()`](t-method.md) of [`tl()`](tl-method.md) binnen de variabele `registerPreTrackCallback` . Het plaatsen van het volgen vraag in deze variabele veroorzaakt een oneindige lijn van beeldverzoeken!

Elke keer dat u de variabele `registerPreTrackCallback` aanroept, koppelt u die functie om te worden uitgevoerd wanneer een afbeeldingsaanvraag-URL wordt gecompileerd. Registreer dezelfde functie niet meerdere keren tijdens het laden van dezelfde pagina.

>[!NOTE]
>
>De timing en volgorde van functies die tussen `registerPreTrackCallback` en `registerPostTrackCallback` worden geactiveerd, zijn niet gegarandeerd. Vermijd afhankelijkheid tussen deze twee functies.

## Pre-track callback die de uitbreiding van SDK van het Web gebruikt

Web SDK kan geen functie verbinden nadat het gegeven wordt gecompileerd maar alvorens het naar Adobe wordt verzonden. Met `onBeforeEventSend` kunt u echter een functie registreren die wordt uitgevoerd vlak voordat gegevens worden verzonden.

1. Login aan de [&#x200B; Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) UI die uw geloofsbrieven van AdobeID gebruikt.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Klik onder [!UICONTROL Data Collection] op de knop **[!UICONTROL Edit on before event send callback code]** .
1. Plaats de gewenste code in de editor.

## Pre-track callback manueel uitvoerend het Web SDK

Web SDK kan geen functie verbinden nadat het gegeven wordt gecompileerd maar alvorens het naar Adobe wordt verzonden. Met `onBeforeEventSend` kunt u echter een functie registreren die wordt uitgevoerd vlak voordat gegevens worden verzonden, vergelijkbaar met `doPlugins` . Zie [&#x200B; Veranderend gebeurtenissen globaal &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Pre-track callback die de uitbreiding van Adobe Analytics gebruikt

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.registerPreTrackCallback in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

`s.registerPreTrackCallback` is een functie die een functie als het enige argument neemt. De geneste functie wordt uitgevoerd vlak voordat een afbeeldingsaanvraag wordt verzonden.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Als u de afbeeldingsaanvraag-URL in uw code wilt gebruiken, verwijst u naar het tekenreeksargument `requestUrl` in de geneste functie. U kunt de variabele `requestUrl` parseren voor het gewenste gebruik. Het aanpassen van deze variabele heeft geen invloed op de gegevensverzameling.

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
>Het plaatsen van paginariabelen of het veranderen van het `requestUrl` koord binnen deze functie beïnvloeden **niet** het beeldverzoek dat kort na deze functievraag wordt verzonden. Gebruik in plaats hiervan de variabele [`doPlugins()`](doplugins.md) .
