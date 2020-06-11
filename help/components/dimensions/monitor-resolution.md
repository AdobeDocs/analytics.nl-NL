---
title: Monitorresolutie
description: De resolutie van de monitor van de bezoeker in pixel.
translation-type: tm+mt
source-git-commit: ad206649488a1a2dead717cdfe53f4c630ba3f3b
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Monitorresolutie

De dimensie &#39;Monitorresolutie&#39; geeft de hoogte en breedte van de actieve weergave in pixels aan. Deze dimensie is handig wanneer u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers of hoe breed bezoekers hun browservenster kunnen maken. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze dimensie is anders dan de hoogte en breedte van de browser. De hoogte/breedte van de browser is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de monitorresolutie het aantal pixels van de gehele monitor is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserafmetingen zijn altijd kleiner dan monitorresolutie, omdat browsernavigatie of -randen niet in de afmetingen zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`s` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `screen.width` en `screen.height` in de browser. Als u een AppMeturement-bibliotheek gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `s` vraagkoord in beeldverzoeken omvat.

## Dimensiewaarden

Tot de maatwaarden behoren alle verzamelde monitorresoluties. Voorbeelden hiervan zijn `1920 x 1080`, `1366 x 768`en `1280 x 720`.
