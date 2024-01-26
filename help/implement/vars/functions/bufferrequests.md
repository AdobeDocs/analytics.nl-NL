---
title: bufferRequests
description: Verbeter de betrouwbaarheid van het vastleggen van aanvragen voor het bijhouden van koppelingen voor browsers die de pagina direct verwijderen.
feature: Variables
exl-id: f103deb4-f449-4325-b1a0-23e58a3c9ba0
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# bufferRequests

De `bufferRequests()` Met deze methode kunt u afbeeldingsaanvragen op de huidige pagina in de cache plaatsen in plaats van ze naar de Adobe te verzenden. Het uitproberen van deze methode is handig in situaties waarin een browser geen ondersteuning biedt [`navigator.sendBeacon()`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon) of annuleert op een andere manier afbeeldingsaanvragen wanneer een pagina wordt verwijderd. Veel versies van WebKit-browsers, zoals Safari, laten vaak zien hoe een afbeeldingsaanvraag wordt gestopt wanneer op een koppeling wordt geklikt. De `bufferRequests()` Deze methode is beschikbaar voor alle versies van AppMeasurement v2.25.0 of hoger.

Wanneer u [`t()`](t-method.md) of [`tl()`](tl-method.md) op een volgende pagina in dezelfde browsersessie en `bufferRequests()` nog niet op die pagina is aangeroepen, worden alle aanvragen voor gebufferde afbeeldingen verzonden naast de afbeeldingsaanvraag van die pagina. Gebufferde aanvragen worden in de juiste volgorde verzonden, waarbij de afbeeldingsaanvraag van de huidige pagina als laatste wordt verzonden.

>[!TIP]
>
>De tijdstempel van gebufferde aanvragen wordt gedeeld met de pagina die de gegevens verzendt. Als u nauwkeuriger in precies wilt wanneer een als buffer optredende aanvraag wordt geregistreerd, kunt u plaatsen [`timestamp`](../page-vars/timestamp.md) paginariabele alvorens het verzoek als buffer op te treden. Als u deze variabele gebruikt, zorg ervoor dat [Tijdstempels optioneel](/help/technotes/timestamps-optional.md) is ingeschakeld - als dit niet het geval is, gaan alle treffers met een tijdstempel permanent verloren!

## Beperkingen

Wanneer u de `bufferRequests()` , houd rekening met de volgende beperkingen. Aangezien deze methode wordt gebruikt [`Window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API), zijn veel van dezelfde beperkingen van toepassing:

* De bestemmingsverbinding moet op het zelfde domein en subdomain verblijven. Gebufferde aanvragen werken niet in verschillende domeinen of subdomeinen, zelfs niet als beide dezelfde Adobe Analytics-implementatie hebben. Deze beperking betekent ook dat u geen gebufferde verzoeken kunt gebruiken om uitgangsverbindingen te volgen.
* De doelkoppeling moet hetzelfde protocol gebruiken als de huidige pagina. U kunt geen gebufferde aanvragen verzenden tussen HTTP en HTTPS.
* De gebufferde verzoeken worden opgeslagen tot u roept `t()` of `tl()` zonder aanroep `bufferRequests()` eerst, of tot browser of lusje wordt gesloten. Als een browsersessie wordt beëindigd voordat u die gegevens naar de Adobe kunt verzenden, gaan niet-verzonden gebufferde aanvragen permanent verloren.
* Als een browser de functie [Web Storage-API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) of de [JSON API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON), wordt een waarschuwing uitgevoerd naar de browserconsole en probeert het AppMeasurement de afbeeldingsaanvraag onmiddellijk te verzenden met de `t()` methode.

## Gebufferde verzoeken in de SDK van het Web

De SDK van het Web biedt momenteel niet de capaciteit aan om verzoeken te bufferen.

## Gebufferde aanvragen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.bufferRequests() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de `bufferRequests()` methode vóór aanroepen `t()` of `tl()`. Wanneer `bufferRequests()` wordt geroepen, worden de verdere het volgen vraag geschreven aan zittingsopslag in plaats van verzonden naar de servers van de de gegevensinzameling van de Adobe.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Flag the request to be buffered
s.bufferRequests();

// The t() or tl() method then writes the data to session storage instead of sending it to Adobe
s.tl(true,"o","Example link click");

// On a subsequent page, the tracking call sends both the above link tracking call and the page view call
s.t();
```
