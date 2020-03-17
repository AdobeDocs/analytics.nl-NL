---
description: 'null'
title: Overzicht van uitval
uuid: 2d98899e-e401-4d7a-8af0-de0002f84178
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Overzicht van uitval

Vallout-visualisaties bieden meer opties voor het samenstellen van uw uitvalrapporten. Uit de uitvalrapporten blijkt waar bezoekers een vooraf gedefinieerde reeks pagina&#39;s hebben verlaten (uitgevallen) en doorlopen (doorgevallen).

Met uitvalvisualisaties kunt u

* Voer zij aan zij vergelijkingen van twee verschillende segmenten in het zelfde rapport uit.
* Taalstappen slepen, neerzetten en opnieuw rangschikken (aanraakpunten)
* Waarden van verschillende afmetingen en maateenheden mixen en afstemmen
* Een multidimensionaal uitvalrapport maken
* Identificeer waar de klanten onmiddellijk na het vallen gaan

Bij Uitvallen worden de conversie- en uitvalsnelheden tussen elke stap of elk aanraakpunt in een reeks weergegeven.

U kunt bijvoorbeeld de uitvalpunten van een bezoeker bijhouden tijdens een aankoopproces. Selecteer gewoon een begin- en een eindaanraakpunt en voeg tussenliggende aanraakpunten toe om een websitenavigatiepad te maken. Maar je kunt ook multidimensionale fallouts doen.

Een uitvalvisualisatie is handig voor het analyseren van:

* Conversiepercentages via specifieke processen op uw site (zoals een aankoop- of registratieproces).
* Algemene verkeersstromen met een groter bereik: Van de mensen die de homepage zagen, toont deze stroom hoeveel er doorgingen om een onderzoek uit te voeren, en toen hoeveel van hen uiteindelijk naar een specifiek punt gingen kijken.
* Correlaties tussen gebeurtenissen op uw site. Correlaties laten zien welk percentage van de mensen die naar je privacybeleid keken, een product heeft gekocht.

[Volledige visualisatie op YouTube](https://www.youtube.com/watch?v=VcrfHSyIoj8&index=52&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:15)

## Segmentatie als basis voor flow en fallout {#section_654F37A398C24DDDB1552A543EE29AA9}

De segmenten die op de panelen van de Werkruimte worden toegepast werken lichtjes verschillend dan segmenten die op reserve en stroomrapporten in Rapporten &amp; Analytics of Ad hoc Analyse worden toegepast. Meestal leveren ze precies dezelfde resultaten op. Het belangrijkste verschil is dat Rapporten &amp; Analytics en Ad hoc Analyse het segment bij elke stap van de opeenvolging toepassen. Dit kan tot iets verschillende resultaten leiden.

Laten we een voorbeeld nemen van fallout met twee stappen:

![](assets/fallout_segments1.png)

Als u dan een segment op het het paneelniveau van de Werkruimte toepast, combineert het segment met de reserve als dit:

![](assets/fallout_seg.png)

Als het segment daarentegen wordt berekend met behulp van Rapporten en Analyses en ad hoc analyse, wordt het segment op deze manier gecombineerd:

![](assets/fallout_segments3.png)

In rapporten en analyses en ad hoc-analyse wordt het segment gecombineerd met elke stap. Wanneer de containers zich op hetzelfde niveau bevinden als de uitval (bv. bezoek of bezoekersniveau), zal dit ertoe leiden dat het aantal bezoeken of bezoekers gelijk wordt gesteld.

Als het segment dat op het paneel wordt toegepast kleiner is dan het valniveau (bijvoorbeeld raakniveau), geeft het segment echter verschillende resultaten vanwege de manier waarop het wordt gecombineerd met het rapport. Om te herhalen, in de meeste omstandigheden komen de aantallen in de Werkruimte van de Analyse overeen die in Rapporten &amp; Analytics en Ad hoc Analyse. Ze komen alleen **niet** overeen als alle onderstaande gevallen waar zijn:

* Het segment bevindt zich niet op hetzelfde niveau als de uitval.
* Het segment heeft een variabele waarbij de bezoeker/bezoeker meerdere waarden kan hebben tijdens een bezoek/bezoeker.

In het zeldzame geval waar u de Werkruimte van de Analyse moet hebben de Rapporten &amp; van de Analyse manier aanpassen om segmenten toe te passen aan val/stroom, eenvoudig laat vallen het segment in elke reservestap in Werkruimte en het zal in de zelfde aantallen resulteren.
