---
title: Conversierapporten in Adobe Analytics
description: Leer hoe u conversierapporten gebruikt in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 3ce18f3f222286aed08c81dd2c958dab7e443df3

---


# Conversierapporten

Een &#39;conversie&#39; is een actie die een bezoeker op uw site uitvoert en die rechtstreeks aansluit bij de belangrijkste indicatoren van uw organisatie. Conversierapporten bevatten informatie over de manier waarop bezoekers converteren.

Deze pagina veronderstelt de gebruiker een basiskennis van het gebruiken van de Werkruimte van de Analyse heeft. Zie Een basisrapport [maken in de Analyse Workspace voor Google Analytics-gebruikers](create-report.md) als u nog niet bekend bent met het hulpprogramma in Adobe Analytics.

## Doelrapporten

De doelstellingen bieden gebruikers van Google Analytics een manier om de omzetting van een website te bepalen. Dit is de standaardmanier om trechters, omgekeerde gedragsstroom, kanaaltrechters en attributie te maken. De doelen in Google Analytics zijn niet retroactief en kunnen alleen worden ingesteld op de beheerpagina. Bovendien zijn ze alleen gebaseerd op een pagina, gebeurtenis, doorgebrachte tijd of gemiddeld aantal pagina&#39;s.

In Adobe Analytics is het concept van een doel niet vereist, omdat metrische gegevens in elke context kunnen worden toegepast. Zolang uw implementatie de gebeurtenissen aanpast die u wilt bijhouden, kunt u elk conversierapport bijstellen en direct resultaten voor historische gegevens ophalen.

### Trechter visualisatie

Het trechter visualisatierapport helpt analisten zich te concentreren op een bepaalde reeks stappen die nodig zijn om te converteren. Voordat een bezoeker een aankoop doet, moet hij bijvoorbeeld toegang hebben tot de winkelwagentje, de facturerings- en verzendpagina, de betalingspagina en de pagina voor het controleren van bestellingen.

In de Werkruimte van de Analyse, kunnen deze gegevens worden bekeken gebruikend de visualisatie van de Vallout.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een Fallout-visualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik op het componentpictogram aan de linkerkant en zoek de dimensie **Pagina** &#39;s.
3. Klik op het pijlpictogram naast de afmetingen Pagina&#39;s om de paginawaarden weer te geven. Dimensiewaarden zijn geel.
4. Zoek de gewenste pagina die als eerste aanraakpunt fungeert en sleep deze naar de ruimte met het label &#39;Aanraakpunt toevoegen&#39; in de visualisatie.
5. Voeg de gewenste aanraakpunten toe door de paginawaarden naar de visualisatie te slepen.

De uitvalvisualisatie is niet beperkt tot de pagina&#39;s-dimensie. Om het even welke afmeting, metrisch, of segment kan worden gebruikt om uw reserverapport aan te passen aan de behoeften van uw organisatie.

![Uitvalvisualisatie](/help/technotes/ga-to-aa/assets/fallout.png)

## E-handelrapporten

De e-commercerapporten worden typisch gebruikt door plaatsen die producten of de diensten verkopen om orden en opbrengst op gekochte voorwerpen te meten. Deze functie is beschikbaar in Adobe Analytics en staat bekend als Products reports.

Zowel in Google Analytics als in productrapporten in Adobe Analytics zijn aangepaste implementatiewijzigingen vereist. Zie de dimensie van [Producten](/help/components/c-variables/dimensionslist/reports-products.md) in de de gebruikersgids van Componenten voor meer informatie.

## Meerkanaals rapporten van de Trechter

Taalrapporten met meerdere kanalen bieden extra marketingkanaalgegevens die verder gaan dan de verzamelingsrapporten. In deze rapporten wordt vooral aandacht besteed aan de manier waarop bezoekers converteren, in plaats van aan de manier waarop bezoekers uw site bereiken.

> [!NOTE]
>
> Het gebruik van multikanaalrapporten in Adobe Analytics vereist zowel de opstelling van de Kanalen van de Marketing als een douaneimplementatie om de productvariabele en aankoopgebeurtenis aan te passen. Adobe raadt u aan samen te werken met een implementatieconsultant als deze functies nog niet zijn geconfigureerd voor uw rapportsuite.

### Meerdere kanalen - ondersteunde conversies

Bij ondersteunde conversies wordt getoond hoe vaak elk kanaal werd ondersteund met een conversie. In de Werkruimte van de Analyse, **helpt** de Orde metrisch kan worden gebruikt.

1. Zoek in het menu Componenten de dimensie **Marketingkanaal** en sleep deze naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de metrische waarde voor **Order Assists** boven op de automatisch gemaakte **kop** Voorkomenom deze te vervangen. Aanvullende metriek kan desgewenst naar de werkruimte worden gesleept.

### Meerdere kanalen - bovenste omzettingspaden

Het rapport met de bovenste omzettingspaden toont de paden naar het bovenste kanaal die de gebruiker heeft gekozen voordat deze werden omgezet. De Werkruimte van de analyse gebruikt een stroomrapport om hoogste omzettingswegen te visualiseren.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant, zoek de dimensie **Marketing Channel** en sleep deze naar het vak Dimensie toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;Channel Flow&#39;-visualisatie. In deze flow ziet u de bovenste paden die een bezoeker heeft aangeraakt vóór een aankoop.

Deze stroomvisualisatie is interactief. Klik op elk kanaal om de stroom in een van beide richtingen uit te breiden.

![Stroomvisualisatie](/help/technotes/ga-to-aa/assets/flow.png)

### Multikanaal - Tijdlabel

Het tijdvertragingsrapport geeft de hoeveelheid tijd in dagen weer die een bezoeker heeft geconverteerd naar uw site. In de Werkruimte van de Analyse, zijn deze gegevens beschikbaar gebruikend de **Dagen vóór Eerste Aankoop** afmeting. Deze optie is alleen beschikbaar in de context van een correct geïmplementeerde aankoopgebeurtenis.

1. Zoek in het menu Componenten de afmetingen **Dagen voor eerste aankoop** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de maatstaven voor **bestellingen**, **eenheden** of **inkomsten** in deze dimensie te gebruiken.

Voor andere soorten omzettingen, met inbegrip van douanegebeurtenissen, is de **Tijd Voorafgaand aan de dimensie van de Gebeurtenis** beschikbaar. Het toont de hoeveelheid tijd, in minuten, die een bezoeker nodig had om de gebeurtenis tijdens het bezoek te activeren.

1. Zoek in het menu Componenten de waarde **Tijd voor gebeurtenis** op en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan deze dimensie naast aangepaste gebeurtenissen of aankoopgebeurtenissen te gebruiken.

### Meerdere kanalen - padlengte

Het rapport over de padlengte geeft het aantal kanalen weer dat is aangeraakt vóór een conversiegebeurtenis. In de Werkruimte van de Analyse, bevat het paneel van Attributie deze gegevens in één van zijn visualisaties.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel
2. Klik op het pictogram Componenten aan de linkerkant, zoek de dimensie **Marketing Channel** en sleep deze naar het vak Dimensie toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;aanraakpunten per reis&#39;-visualisatie. In dit histogram ziet u het aantal kanalen dat een bezoeker heeft aangeraakt vóór een aankoop.
