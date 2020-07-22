---
title: Conversierapporten in Adobe Analytics
description: Leer hoe u conversierapporten kunt gebruiken in Adobe Analytics.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---


# Conversierapporten

Een &#39;conversie&#39; is een actie die een bezoeker op uw site uitvoert en die rechtstreeks aansluit bij de belangrijkste indicatoren van uw organisatie. Conversierapporten bevatten informatie over de manier waarop bezoekers converteren.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor Google Analytics-gebruikers](create-report.md) als u het programma nog niet kent in Adobe Analytics.

## Doelrapporten

De doelstellingen bieden Google Analytics-gebruikers een manier om de conversie van een website te definiëren. Dit is de standaardmanier om trechters, omgekeerde gedragsstroom, kanaaltrechters en attributie te maken. De doelen in Google Analytics zijn niet met terugwerkende kracht en kunnen alleen worden ingesteld op de beheerpagina. Bovendien zijn ze alleen gebaseerd op een pagina, gebeurtenis, doorgebrachte tijd of gemiddeld aantal pagina&#39;s.

In Adobe Analytics is het concept van een doel niet vereist, omdat meetgegevens in elke context kunnen worden toegepast. Zolang uw implementatie de gebeurtenissen aanpast die u wilt bijhouden, kunt u elk conversierapport bijstellen en direct resultaten voor historische gegevens ophalen.

### Trechter visualisatie

Het trechter visualisatierapport helpt analisten zich te concentreren op een bepaalde reeks stappen die nodig zijn om te converteren. Voordat een bezoeker een aankoop doet, moet hij bijvoorbeeld toegang hebben tot de winkelwagentje, de facturerings- en verzendpagina, de betalingspagina en de pagina voor het controleren van bestellingen.

In Analysis Workspace kunnen deze gegevens worden weergegeven met de functie voor het weergeven van fallout.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een Fallout-visualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik op het componentpictogram aan de linkerkant en zoek de dimensie **Pagina** &#39;s.
3. Klik op het pijlpictogram naast de afmetingen Pagina&#39;s om de paginawaarden weer te geven. Dimensie-items zijn geel.
4. Zoek de gewenste pagina die als eerste aanraakpunt fungeert en sleep deze naar de ruimte met het label &#39;Aanraakpunt toevoegen&#39; in de visualisatie.
5. Voeg de gewenste aanraakpunten toe door de paginawaarden naar de visualisatie te slepen.

De uitvalvisualisatie is niet beperkt tot de pagina&#39;s-dimensie. Om het even welke afmeting, metrisch, of segment kan worden gebruikt om uw reserverapport aan te passen aan de behoeften van uw organisatie.

![Uitvalvisualisatie](/help/technotes/ga-to-aa/assets/fallout.png)

## E-handelrapporten

De e-commercerapporten worden typisch gebruikt door plaatsen die producten of de diensten verkopen om orden en opbrengst op gekochte voorwerpen te meten. Deze functie is beschikbaar in Adobe Analytics en wordt Producten genoemd rapporten.

Zowel in Google Analytics- als in productrapporten in Adobe Analytics zijn aangepaste implementatiewijzigingen vereist. Zie de dimensie van [Producten](/help/components/dimensions/product.md) in de de gebruikersgids van Componenten voor meer informatie.

## Meerkanaals rapporten van de Trechter

Taalrapporten met meerdere kanalen bieden extra marketingkanaalgegevens die verder gaan dan de verzamelingsrapporten. In deze rapporten wordt vooral aandacht besteed aan de manier waarop bezoekers converteren, in plaats van aan de manier waarop bezoekers uw site bereiken.

>[!NOTE]
>
> Voor het gebruik van multikanaalrapporten in Adobe Analytics is zowel de installatie van Marketing Channels als een aangepaste implementatie vereist om ruimte te bieden aan de productvariabele en de aankoopgebeurtenis. Adobe raadt u aan samen te werken met een implementatieconsultant als deze functies nog niet zijn geconfigureerd voor uw rapportsuite.

### Meerdere kanalen - ondersteunde conversies

Bij ondersteunde conversies wordt getoond hoe vaak elk kanaal werd ondersteund met een conversie. In Analysis Workspace kunt u de metrische waarde voor **Orderassistenten** gebruiken.

1. Zoek in het menu Componenten de dimensie **Marketingkanaal** en sleep deze naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de metrische waarde voor **Order Assists** boven op de automatisch gemaakte **kop** Voorkomenom deze te vervangen. Aanvullende metriek kan desgewenst naar de werkruimte worden gesleept.

### Meerdere kanalen - bovenste omzettingspaden

Het rapport met de bovenste omzettingspaden toont de paden naar het bovenste kanaal die de gebruiker heeft gekozen voordat deze werden omgezet. Analysis Workspace gebruikt een flowrapport om de bovenste omzettingspaden zichtbaar te maken.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant, zoek de dimensie **Marketing Channel** en sleep deze naar het vak Dimensie toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;Channel Flow&#39;-visualisatie. In deze flow ziet u de bovenste paden die een bezoeker heeft aangeraakt vóór een aankoop.

Deze stroomvisualisatie is interactief. Klik op elk kanaal om de stroom in een van beide richtingen uit te breiden.

![Stroomvisualisatie](/help/technotes/ga-to-aa/assets/flow.png)

### Multikanaal - Tijdlabel

Het tijdvertragingsrapport geeft de hoeveelheid tijd in dagen weer die een bezoeker heeft geconverteerd naar uw site. In Analysis Workspace zijn deze gegevens beschikbaar met de dimensie **Dagen voor eerste aankoop** . Deze optie is alleen beschikbaar in de context van een correct geïmplementeerde aankoopgebeurtenis.

1. Zoek in het menu Componenten de afmetingen **Dagen voor eerste aankoop** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de maatstaven voor **bestellingen**, **eenheden** of **inkomsten** in deze dimensie te gebruiken.

Voor andere soorten omzettingen, met inbegrip van douanegebeurtenissen, is de **Tijd Voorafgaand aan de dimensie van de Gebeurtenis** beschikbaar. Het toont de hoeveelheid tijd, in minuten, die een bezoeker nodig had om de gebeurtenis tijdens het bezoek te activeren.

1. Zoek in het menu Componenten de waarde **Tijd voor gebeurtenis** op en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan deze dimensie naast aangepaste gebeurtenissen of aankoopgebeurtenissen te gebruiken.

### Meerdere kanalen - padlengte

Het rapport over de padlengte geeft het aantal kanalen weer dat is aangeraakt vóór een conversiegebeurtenis. In Analysis Workspace bevat het deelvenster Kenmerken deze gegevens in een van de visualisaties.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel
2. Klik op het pictogram Componenten aan de linkerkant, zoek de dimensie **Marketing Channel** en sleep deze naar het vak Dimensie toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;aanraakpunten per reis&#39;-visualisatie. In dit histogram ziet u het aantal kanalen dat een bezoeker heeft aangeraakt vóór een aankoop.
