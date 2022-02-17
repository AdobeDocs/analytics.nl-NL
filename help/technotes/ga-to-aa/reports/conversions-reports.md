---
title: Conversierapporten in Adobe Analytics
description: Leer hoe u omzettingsrapporten kunt gebruiken in Adobe Analytics.
feature: Third-party Integration
exl-id: 315b7dc0-1cd9-4beb-8203-88e205375f84
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---

# Conversierapporten

Een &#39;conversie&#39; is een actie die een bezoeker op uw site uitvoert en die rechtstreeks aansluit bij de belangrijkste indicatoren van uw organisatie. Conversierapporten bevatten informatie over de manier waarop bezoekers converteren.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics](create-report.md) als u het gereedschap nog niet kent in Adobe Analytics.

## Doelrapporten

Met doelen kunnen gebruikers van Google Analytics de conversie van een website definiëren. Dit is de standaardmanier om trechters, omgekeerde gedragsstroom, kanaaltrechters en attributie te maken. De doelstellingen in Google Analytics zijn niet retroactief, en kunnen slechts op de admin pagina worden geplaatst. Bovendien zijn ze alleen gebaseerd op een pagina, gebeurtenis, doorgebrachte tijd of gemiddeld aantal pagina&#39;s.

In Adobe Analytics is het concept van een doel niet vereist, omdat meetgegevens in elke context kunnen worden toegepast. Zolang uw implementatie de gebeurtenissen aanpast die u wilt bijhouden, kunt u elk conversierapport bijstellen en direct resultaten voor historische gegevens ophalen.

### Trechter visualisatie

Het trechter visualisatierapport helpt analisten zich te concentreren op een bepaalde reeks stappen die nodig zijn om te converteren. Voordat een bezoeker een aankoop doet, moet hij bijvoorbeeld toegang hebben tot de winkelwagentje, de facturerings- en verzendpagina, de betalingspagina en de pagina voor het controleren van bestellingen.

In Analysis Workspace kunnen deze gegevens worden weergegeven met de functie voor het weergeven van fallout.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een Fallout-visualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik op het componentpictogram aan de linkerkant en zoek het **Pagina&#39;s** dimensie.
3. Klik op het pijlpictogram naast de afmetingen Pagina&#39;s om de paginawaarden weer te geven. Dimension-items zijn gekleurd geel.
4. Zoek de gewenste pagina die als eerste aanraakpunt fungeert en sleep deze naar de ruimte met het label &#39;Aanraakpunt toevoegen&#39; in de visualisatie.
5. Voeg de gewenste aanraakpunten toe door de paginawaarden naar de visualisatie te slepen.

De uitvalvisualisatie is niet beperkt tot de pagina&#39;s-dimensie. Om het even welke afmeting, metrisch, of segment kan worden gebruikt om uw reserverapport aan te passen aan de behoeften van uw organisatie.

![Uitvalvisualisatie](/help/technotes/ga-to-aa/assets/fallout.png)

## E-handelrapporten

De e-commercerapporten worden typisch gebruikt door plaatsen die producten of de diensten verkopen om orden en opbrengst op gekochte voorwerpen te meten. Deze functie is beschikbaar in Adobe Analytics en wordt Producten genoemd rapporten.

Zowel vereisen de e-commercerapporten in Google Analytics als productrapporten in Adobe Analytics aangepaste implementatieveranderingen aan gebruik. Zie de [Producten](/help/components/dimensions/product.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Meerkanaals rapporten van de Trechter

Taalrapporten met meerdere kanalen bieden extra marketingkanaalgegevens die verder gaan dan de verzamelingsrapporten. In deze rapporten wordt vooral aandacht besteed aan de manier waarop bezoekers converteren, in plaats van aan de manier waarop bezoekers uw site bereiken.

>[!NOTE]
>
> Het gebruik van multikanaalrapporten in Adobe Analytics vereist zowel de opstelling van de Kanalen van de Marketing als een douaneimplementatie om de productvariabele en aankoopgebeurtenis aan te passen. Adobe raadt u aan samen te werken met een implementatieconsultant als deze functies nog niet zijn geconfigureerd voor uw rapportsuite.

### Meerdere kanalen - ondersteunde conversies

Bij ondersteunde conversies wordt getoond hoe vaak elk kanaal werd ondersteund met een conversie. In Analysis Workspace **Assistenten bestellen** metrisch kan worden gebruikt.

1. Zoek in het menu Componenten de locatie **Marketingkanaal** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de **Assistenten bestellen** metrisch bovenop automatisch gecreeerd **Voorval** De metrische kopbal om het te vervangen. Aanvullende metriek kan desgewenst naar de werkruimte worden gesleept.

### Meerdere kanalen - bovenste omzettingspaden

Het rapport met de bovenste omzettingspaden toont de paden naar het bovenste kanaal die de gebruiker heeft gekozen voordat deze werden omgezet. Analysis Workspace gebruikt een flowrapport om de bovenste omzettingspaden zichtbaar te maken.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en zoek het **Marketingkanaal** en sleep deze naar het vak met het label Dimension toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;Channel Flow&#39;-visualisatie. In deze flow ziet u de bovenste paden die een bezoeker heeft aangeraakt vóór een aankoop.

Deze stroomvisualisatie is interactief. Klik op elk kanaal om de stroom in een van beide richtingen uit te breiden.

![Stroomvisualisatie](/help/technotes/ga-to-aa/assets/flow.png)

### Multikanaal - Tijdlabel

Het tijdvertragingsrapport geeft de hoeveelheid tijd in dagen weer die een bezoeker heeft geconverteerd naar uw site. In Analysis Workspace zijn deze gegevens beschikbaar via de **Dagen vóór eerste aankoop** dimensie. Deze optie is alleen beschikbaar in de context van een correct geïmplementeerde aankoopgebeurtenis.

1. Zoek in het menu Componenten de locatie **Dagen vóór eerste aankoop** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan de **Orders**, **Eenheden**, of **Ontvangsten** metriek met deze dimensie.

Voor andere typen conversies, waaronder aangepaste gebeurtenissen, worden de **Tijd voorafgaand aan gebeurtenis** dimensie is beschikbaar. Het toont de hoeveelheid tijd, in minuten, die een bezoeker nodig had om de gebeurtenis tijdens het bezoek te activeren.

1. Zoek in het menu Componenten de locatie **Tijd voorafgaand aan gebeurtenis** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Adobe raadt u aan deze dimensie naast aangepaste gebeurtenissen of aankoopgebeurtenissen te gebruiken.

### Meerdere kanalen - padlengte

Het rapport over de padlengte geeft het aantal kanalen weer dat is aangeraakt vóór een conversiegebeurtenis. In Analysis Workspace bevat het deelvenster Kenmerken deze gegevens in een van de visualisaties.

1. Klik op het pictogram Deelvensters aan de linkerkant en sleep een deelvenster Kenmerken boven de vrije-vormtabel
2. Klik op het pictogram Componenten aan de linkerkant en zoek het **Marketingkanaal** en sleep deze naar het vak met het label Dimension toevoegen.
3. Zoek de gewenste conversiegebeurtenis onder Metrisch (bijvoorbeeld Bestellingen) en sleep deze naar het vak Metrisch toevoegen. Berekende meetgegevens worden niet ondersteund in het deelvenster Kenmerken.
4. Klik op Samenstellen.
5. Zoek in het resulterende rapport de &#39;aanraakpunten per reis&#39;-visualisatie. In dit histogram ziet u het aantal kanalen dat een bezoeker heeft aangeraakt vóór een aankoop.
