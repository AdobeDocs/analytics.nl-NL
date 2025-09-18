---
title: bufferRequests
description: Verbeter de betrouwbaarheid van het vastleggen van aanvragen voor het bijhouden van koppelingen voor browsers die de pagina direct verwijderen.
feature: Appmeasurement Implementation
exl-id: f103deb4-f449-4325-b1a0-23e58a3c9ba0
role: Admin, Developer
source-git-commit: 325c035c0b5a9cc828be22ef7781d3b67f104476
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# bufferRequests

Met de methode `bufferRequests()` kunt u afbeeldingsaanvragen op de huidige pagina in cache plaatsen in plaats van ze naar Adobe te verzenden. Het teweegbrengen van deze methode is nuttig in scenario&#39;s waar browser niet [`navigator.sendBeacon()` steunt ](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon) of anders beeldverzoeken annuleert wanneer een pagina leegt. Veel versies van WebKit-browsers, zoals Safari, laten vaak zien hoe een afbeeldingsaanvraag wordt gestopt wanneer op een koppeling wordt geklikt. De methode `bufferRequests()` is beschikbaar voor alle versies van AppMeasurement v2.25.0 of hoger.

Wanneer u [`t()`](t-method.md) of [`tl()`](tl-method.md) aanroept op een volgende pagina in dezelfde browsersessie en `bufferRequests()` nog niet is aangeroepen op die pagina, worden alle gebufferde aanvragen verzonden naast de afbeeldingsaanvraag van die pagina. Gebufferde aanvragen worden in de juiste volgorde verzonden, waarbij de afbeeldingsaanvraag van de huidige pagina als laatste wordt verzonden.

>[!TIP]
>
>De tijdstempel van gebufferde aanvragen wordt gedeeld met de pagina die de gegevens verzendt. Als u precies meer precisie wilt in de seconde een gebufferd verzoek wordt geregistreerd, kunt u de [`timestamp`](../page-vars/timestamp.md) paginariabele plaatsen alvorens het verzoek als buffer op te nemen. Als u deze variabele gebruikt, zorg ervoor dat [ facultatieve Tijdstempels ](/help/admin/tools/manage-rs/edit-settings/general/timestamp-configuration.md) wordt toegelaten - als het niet is, worden alle timestamped hits permanent verloren!

## Beperkingen

Houd rekening met de volgende beperkingen wanneer u de methode `bufferRequests()` aanroept. Aangezien deze methode [`Window.sessionStorage` ](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) gebruikt, zijn veel van de zelfde beperkingen van toepassing:

* De bestemmingsverbinding moet op het zelfde domein en subdomain verblijven. Gebufferde aanvragen werken niet in verschillende domeinen of subdomeinen, zelfs niet als beide dezelfde Adobe Analytics-implementatie hebben. Deze beperking betekent ook dat u geen gebufferde verzoeken kunt gebruiken om uitgangsverbindingen te volgen.
* De doelkoppeling moet hetzelfde protocol gebruiken als de huidige pagina. U kunt geen gebufferde aanvragen verzenden tussen HTTP en HTTPS.
* Gebufferde aanvragen worden opgeslagen totdat u `t()` of `tl()` aanroept zonder `bufferRequests()` eerst aan te roepen, of totdat de browser of het tabblad wordt gesloten. Als een browsersessie wordt beëindigd voordat u die gegevens naar Adobe kunt verzenden, gaan niet-verzonden gebufferde aanvragen permanent verloren.
* Als browser niet de [ Opslag API van het Web ](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) of [ JSON API ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON) steunt, wordt een waarschuwing output aan de browser console en AppMeasurement probeert onmiddellijk het beeldverzoek te verzenden gebruikend de `t()` methode.

## Gebufferde verzoeken in het Web SDK

De SDK van het Web biedt momenteel niet de capaciteit aan om verzoeken te bufferen.

## Gebufferde aanvragen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.bufferRequests() in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `bufferRequests()` aan voordat u `t()` of `tl()` aanroept. Wanneer `bufferRequests()` wordt geroepen, worden de verdere het volgen vraag geschreven aan zittingsopslag in plaats van verzonden naar de servers van de gegevensinzameling van Adobe.

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
