---
title: Browserhoogte - ingesloten
description: De hoogte van het browservenster in pixels.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
source-git-commit: 2601b0e5c3fa78237ce693801b8dd8c95b853b81
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Hoogte browser

De &quot;Browser hoogte - gekapt&quot;[&#x200B; afmeting &#x200B;](overview.md) toont de hoogte van het browser venster, die in vooraf bepaalde groepen wordt geclassificeerd. Deze dimensie is handig als u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze afmetingen verschillen van de schermhoogte. Browserhoogte is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de schermhoogte de hoogte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
console.log(`Browser height: ${window.innerHeight} pixels\nScreen height: ${screen.height} pixels`);
```

Browserhoogte is altijd kleiner dan of gelijk aan schermhoogte, aangezien browsernavigatie of -randen niet in de browserhoogte zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van het [`bh` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeasurement verzamelt deze gegevens met de JavaScript-variabele `window.innerHeight` in de browser. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de parameter voor de `bh` querytekenreeks opnemen bij de eerste hit van elk bezoek.

Adobe houdt browserhoogte voor een bezoek aan. Als de hoogte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimension-items

Tot Dimensionen behoren alle verzamelde browserhoogten, geclassificeerd in vooraf gedefinieerde groepen. Als de browserhoogte van een hit bijvoorbeeld `720` is, wordt deze gegroepeerd in het dimensie-item `700 to 799` .
