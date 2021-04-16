---
description: Soms vallen bepaalde metriek niet binnen een acceptabel verschil wanneer Adobe Analytics-metriek wordt vergeleken met DFA-metriek. Hieronder volgt een lijst met metrische definities en mogelijke redenen voor variaties.
keywords: DFA
title: Metrische verschillen met elkaar verzoenen
feature: Data Connectors
uuid: aa3ca006-d3cf-410e-a000-781ab17fb9e3
exl-id: bfe0f9cb-1bbc-40f9-b996-0002d5143889
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '1270'
ht-degree: 0%

---

# Metrische verschillen met elkaar verzoenen{#reconciling-metric-discrepancies}

Soms vallen bepaalde metriek niet binnen een acceptabel verschil wanneer Adobe Analytics-metriek wordt vergeleken met DFA-metriek. Hieronder volgt een lijst met metrische definities en mogelijke redenen voor variaties.

Deze sectie omvat de volgende onderwerpen:

## Metrische definities{#metric-definitions}

Adobe gebruikt de volgende termijnen wanneer het spreken over metriek met betrekking tot de integratie DFA:

**Afbeeldingen**: Impressies hebben betrekking op het aantal keren dat een advertentie is weergegeven. Impressies worden ad-hocgemeld, maar kunnen ook worden samengevoegd tot ad-hocgroepen of andere multi-ad-hocgroepen. De metrische impressies in Analytics worden ingevoerd uit DFA via de niwekelijkse invoer van gegevensbronnen.

**Klik**: Klik op het aantal keren dat op een advertentie is geklikt, zoals in het rapport van DFA. De klikken worden geregistreerd op de DFA omleidingspagina alvorens de bezoeker op de website van de klant landt. Net als bij impressies wordt de metrische kliks in Analytics geïmporteerd uit DFA via het importeren van niight-gegevensbronnen.

**Klikdoorhalingen**: Klikken en doorlopen verwijzen naar het aantal keren dat de gebruiker na het klikken op een advertentie naar de openingspagina is gekomen. Deze metrische waarde kan enigszins verschillen van klikken.

**Weergavedoorvoer**: Weergave-Duwen verwijzen naar het aantal keren dat een bezoeker na het bekijken van een advertentie naar de website van de klant is gekomen, maar NIET op de advertentie heeft geklikt. De bezoeker moet naar de site komen binnen het venster view-through, dat standaard is ingesteld op 30 dagen. De indruk moet zich meer recentelijk hebben voorgedaan dan bij de laatste klik. Beeld-overgangen worden geregistreerd eens per campagne, per bezoek en geteld wanneer de integratie mening-door eVar met DFA campagne ID bevolkt, en de mening-door gebeurtenis wordt geplaatst.

## Mogelijke redenen voor discrepanties{#possible-reasons-for-discrepancies}

Vermeldt een aantal redenen waarom gegevensdiscrepanties kunnen optreden tussen Adobe Analytics- en DFA-rapporten.

### Gebruikers in de Safari-browser en andere browsers die cookies van derden blokkeren {#section-4b0dc429a54a4744a33976b0bb2d1b2a}

Cookieacceptatie door derden is doorgaans de grootste oorzaak van discrepantie tussen Adobe Analytics en DFA. Safari en sommige andere browsers blokkeren cookies van derden standaard. Dit betekent dat Safari standaard het cookie van de eerste partij accepteert dat door de meeste analytische implementaties wordt gebruikt, maar het cookie van de derde partij dat door DFA wordt gebruikt, afwijst.

Een voorbeeld van gegevens van onze Analytics 15 bèta-klanten liet minder dan 0,5% van de gebruikers zien die cookies van de eerste fabrikant doorgaans afwijzen, terwijl 5-12% cookies van derden afwijst (veel van deze afwijzingen zijn waarschijnlijk te wijten aan de standaardbrowserinstellingen).

Deze discrepantie kan resulteren in grote verschillen in de gegevens die door Analytics en DFA worden verzameld.

### Waarom zouden in DFA gerapporteerde indrukken hoger zijn dan in Adobe Analytics gerapporteerde indrukken? {#section-db0ad070a65a4985bcc589b2d0d30b90}

* DFA verzendt gegevens naar Adobe-gegevensverzamelingsservers in een nachtelijke batch, zodat de gegevens in Analytics maximaal 2 dagen achter de DFA-rapporten kunnen staan.
* Adobe gebruikt SAINT-classificaties om geïmporteerde DFA-volgcodes in te delen in verschillende aggregatieniveaus (naam van de campagne, naam van de plaatsing, naam van de advertentie, enz.) Als de discrepantie bij het uitvoeren van een classificatierapport verschijnt, voert u een eenvoudige test uit om te zien of de classificaties nog niet met ingevoerde metriek hebben gevangen:

   * Zoek in het classificatierapport een regelitem met de naam &quot;Geen&quot;.
   * Voer een uitsplitsing van dit lijstitem in dezelfde variabele uit met het onbewerkte DFA ID-rapport (zoals campagne-id).
   * Neem in dit rapport nota van niet-geclassificeerde DFA tracking codes in de vorm `DFA:XXXXX:XXXXX`.
   * Als veel van deze volgcodes bestaan, onderzoek het nachtelijke SAINT classificatieproces.

### Waarom zou DFA klikken hoger kunnen zijn dan Adobe Analytics kliks-doorklikt? {#section-2fce4608ed044bdc9cf812cb719d5d35}

* DFA registreert een klik alvorens de bezoeker op de klantenwebsite landt. Analytics registreert Click-Throughs nadat de het landen pagina laadt en voert het Adobe JavaScript baken uit. Gewoonlijk zijn er verschillen omdat de bezoeker niet naar de bestemmingspagina komt nadat een klik is gevolgd door DFA, of omdat de timer `s.maxDelay` wordt geraakt.
* Zorg ervoor dat alle plaatsen en creatieve elementen in de configuratie van de Floodlight de clickThroughParam in de bestemmingspagina-URL bevatten (bijvoorbeeld &quot;`?CID=1`&quot;). Als u deze parameter niet instelt, zal de Adobe Analytics JavaScript alle doorklikacties missen die plaatsvinden na de eerste hit van het bezoek.
* Zorg ervoor dat alle plaatsen en creatieven een landingspagina hebben die is gelabeld met het JavaScript en de DFA-integratiemodule heeft, en dat de Floodlight Configuration-id op die landingspagina overeenkomt met de Floodlight-configuratie-id van de advertenties die worden aangeboden. Vaak zijn er verschillen omdat de landingspagina voor advertenties is ingesteld op een site van derden of de gehoste advertenties.
* Als u rijke media advertenties of Flash (swf) advertenties gebruikt, zorg ervoor dat wanneer DFA kliktracker wordt geraakt, dat browser van de bezoeker ook naar de het Landen pagina met `clickThroughParam` inbegrepen in het vraagkoord wordt opnieuw gericht. Als u de browser niet omleidt, wordt een doorklikken niet opgenomen.
* Timeouts zijn gevallen waarin DFA-gegevens mogelijk beschikbaar zijn geweest, maar het JavaScript-bestand heeft in de tijd geen reactie ontvangen. Wanneer een bezoeker op de landingspagina aankomt, vraagt Adobe JavaScript de informatie van de bezoeker van de dienst fls.doubleclick.net van DFA. De parameter `s.maxDelay` bepaalt hoe lang de JavaScript wacht op de FLS-gegevens (Floodlight Service). Als `s.maxDelay` te hoog is, kunnen bezoekers de site verlaten voordat Adobe de raakgegevens verzamelt. dat wil zeggen dat er geen klikgegevens worden vastgelegd. Als `s.maxDelay` te laag is ingesteld, kan de internetverbinding van de bezoeker de FLS-gegevens niet op tijd ophalen; Dit betekent dat de hit naar Adobe wordt verzonden zonder DFA-klikgegevens.
* Beide verkeer zou de DFA klikaantallen kunnen opblazen. Bots kunnen functionaliteit hebben om op een advertentie te klikken, maar hebben mogelijk niet de complexiteit om een Analytics-baken uit te voeren of de synchrone scripttag in werking te stellen om de Floodlight-servers te laden die om gegevens vragen. Als deze bots niet uit het cijfer van de Klik worden verwijderd, zou dit een bron van discrepantie kunnen zijn.
* Bezoekers die de pagina verlaten voordat `s.maxDelay` vervalt en DFA-gegevens terugsturen, gaan verloren. er worden geen DFA- of bezoekersgegevens voor hen verzameld.
* Analytics probeert dubbele Click-through te identificeren en te verwijderen zodat zij slechts één keer per campagne per bezoek worden geteld. DFA telt bezoekers die &quot;terug&quot;klikken en door de advertentie overgaan veelvoudige tijden als extra klikt ACM, terwijl de Analytics deze niet als veelvoudige kliks telt.
* DFA Floodlight-tags zijn niet afhankelijk van JavaScript ingeschakeld, maar Analytics wel. Hierdoor kunnen er gevallen zijn waarin DFA een hit vastlegt wanneer Analytics dit niet doet. Gebruik het JavaScript-rapport Analytics in het menu Bezoekersprofiel om te bepalen of dit een probleem kan zijn.

### Waarom zouden DFA post-IMAGE activiteiten hoger kunnen zijn dan Adobe Analytics view-through? {#section-5daa91039c404df48b6a3447c20406f7}

* Analytics probeert dubbele Click-through te identificeren en te verwijderen zodat zij slechts één keer per campagne per bezoek worden geteld. DFA telt bezoekers die &quot;terug&quot;klikken en door de advertentie overgaan veelvoudige tijden als extra klikt ACM, terwijl de Analytics deze niet als veelvoudige kliks telt.
* DFA Floodlight-tags zijn niet afhankelijk van JavaScript uitgeschakeld, maar Analytics wel. Hierdoor kunnen er gevallen zijn waarin DFA een hit vastlegt wanneer Analytics dit niet doet.
* DFA telt Post-Impressie activiteiten wanneer het gebruiken van de markeringen van het Vullingslicht, die op de website van de cliënt kunnen worden geplaatst. Analytics telt View-through nadat het JavaScript-baken (verzoek om afbeelding) is uitgevoerd. De plaatsing van de code op de Web-pagina kan bepalen als een geaborteerde paginading als post-imperiale activiteit of een mening-door telt.

### Wat gebeurt er als de verschillen ver buiten een aanvaardbare marge liggen en de mogelijke redenen hiervoor niet van toepassing zijn? {#section-ca50eb75dd5d4d0396f4668b44d7547c}

Raadpleeg uw Integratie Consultant, of Adobe Client Care, om de discrepanties te documenteren en deze te melden aan het technische team van Data Connectors. U kunt uw verzoek versnellen door over 2 tot 3 dagen gegevens te beschikken waarin de desbetreffende cijfers worden vergeleken (op het niveau van de campagnecode). In uw verzoek, identificeer alle acties u reeds hebt ondernomen om de discrepantie met elkaar in overeenstemming te brengen.
