---
title: Browserhoogte - ingesloten
description: De hoogte van het browservenster in pixels.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Hoogte browser

De afmetingen &#39;Browserhoogte - gespaard&#39; geven de hoogte van het browservenster weer, geclassificeerd in groepen van 100 pixels. Deze dimensie is handig als u wilt weten waar de &quot;vouw&quot; zich op uw site bevindt voor bezoekers. Door te begrijpen waar uw vouw zich bevindt, kunt u inhoud optimaliseren voor weergave.

Deze dimensie is anders dan de schermhoogte. Browserhoogte is het aantal pixels binnen de zichtbare ruimte van de browser, terwijl de schermhoogte de hoogte van de gehele monitor in pixels is. Als u het verschil tussen deze twee variabelen op uw eigen computer wilt zien, opent u de browserconsole (F12 in de meeste browsers) en kopieert en plakt u de volgende code in de console:

```javascript
"Browser height: " + window.innerHeight + " pixels\nScreen height: " + screen.height + " pixels";
```

Browserhoogte is altijd kleiner dan of gelijk aan schermhoogte, aangezien browsernavigatie of -randen niet in de browserhoogte zijn opgenomen.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`bh` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de JavaScript-variabele `window.innerHeight` in de browser. Als u een bibliotheek AppMeasurement gebruikt (zoals door Adobe Experience Platform Launch), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `bh` vraagkoord op de eerste klap van elk bezoek omvat.

Adobe houdt de browserhoogte tijdens een bezoek vast. Als de hoogte van de browser halverwege het bezoek wordt aangepast, wordt de aanpassing niet geregistreerd.

## Dimensie-items

Dimensie-items omvatten alle verzamelde browserhoogten, geclassificeerd in groepen van 100 pixels. Als de browserhoogte van een hit bijvoorbeeld is `720`, wordt deze in het dimensie-item gegroepeerd `700 to 799`.
