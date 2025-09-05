---
title: Overnameverslagen in Adobe Analytics
description: Leer hoe u op aankopen gebaseerde rapporten maakt met Analysis Workspace.
feature: Third-party Integration
exl-id: 2929d34b-8eb0-4105-a49c-02d536929fe0
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 0%

---

# Overnameverslagen

In overnamerapporten ziet u hoe u bezoekers van uw site ontvangt.

In Adobe Analytics, zijn deze rapporten gekend als **de Kanalen van de Marketing**. Zij vereisen wat basis aanvankelijke opstelling, maar staan een veel meer aangepaste mening van kanalen toe.

>[!IMPORTANT]
>
> Opstelling uw de verwerkingsregels van het Kanaal van de Marketing om deze rapporten te gebruiken. Zie [ Begonnen het Worden met de Kanalen van de Marketing ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) voor informatie over hoe te om de Kanalen van de Marketing in uw organisatie het best te vormen.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [ een basisrapport in Analysis Workspace voor de gebruikers van Google Analytics ](create-report.md) tot stand brengen als u nog niet vertrouwd met het hulpmiddel in Adobe Analytics bent.

## Alle verkeer - Kanalen

Hiermee geeft u een geaggregeerde weergave weer van alle kanalen die bezoekers gebruiken om uw site te bereiken.

1. In het menu van Componenten, bepaal de plaats van de **dimensie van het Kanaal van de Marketing** en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

## Alle verkeer - Treemaps

Hiermee wordt een overzicht van het kanaalverkeer weergegeven. Dit rapport is gelijkaardig aan Al Verkeer - Kanalen, maar op een verschillende manier getoond.

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de Treemap-visualisatie naar de werkruimte boven de lege vrije-vormtabel.
2. Klik het pictogram van Componenten op de linkerzijde, dan sleep de **dimensie van het Kanaal van de Marketing** op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Daling een afmeting hier&quot;.
3. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.
4. Extra metriek maken extra overgangen. Indien slechts één driehoek gewenst is:
   1. Klik op de bovenste cel van de gewenste metrische waarde om de driehoek te vertegenwoordigen.
   2. Houd Shift ingedrukt en klik op de laatste cel van dezelfde metrische kolom om de kolom blauw te markeren. Indien correct uitgevoerd, is er één treemap aanwezig in de visualisatie.
   3. Klik op de gekleurde stip in de rechterbovenhoek van de driehoekige visualisatie en klik vervolgens op het selectievakje Selectie vergrendelen.

De boomwerkingen kunnen op om het even welke afmeting worden toegepast, niet alleen de Kanalen van de Marketing.

## Alle verkeer - Source/Medium

Source en de middelgrote rapporten tonen de domeinen die verkeer aan uw plaats drijven.

* De **Source** primaire dimensie is beschikbaar in Analysis Workspace als **Verwijzend de dimensie van het Domein**.
* De **Medium** primaire afmeting is beschikbaar in Analysis Workspace als **afmeting van het Type van Referteur**.
* De **primaire dimensie 0&rbrace; van het Sleutelwoord {is beschikbaar in Analysis Workspace als** 3} dimensie van het Sleutelwoord van het Onderzoek &lbrace;.**&#x200B;**

1. Zoek in het optiemenu de gewenste afmeting die hierboven is vermeld en sleep deze naar het grote tabelgebied in vrije vorm met het label &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de volgende pagina&#39;s in de gebruikershandleiding van Componenten voor meer informatie over hun respectievelijke dimensie:

* [Referentiedomein](/help/components/dimensions/referring-domain.md)
* [Type referentie](/help/components/dimensions/referrer-type.md)
* [Trefwoord zoeken](/help/components/dimensions/search-keyword.md)

## Alle verkeer - verwijzingen

* De **Source** primaire dimensie is beschikbaar in Analysis Workspace als **Verwijzend de dimensie van het Domein**.
* De **het Bestaan van de Pagina** primaire afmeting is beschikbaar in Analysis Workspace als **Ingang pagina** afmeting.

1. In het componentenmenu, bepaal de plaats van **Verwijzend Domein** of **de dimensie van de Pagina van de Ingang** en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Daling een dimensie hier&quot;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

Zie de [ Verwijzende dimensie van het Domein ](/help/components/dimensions/referring-domain.md) in de gebruikersgids van Componenten voor meer informatie.

## Google Ads-rapporten en zoekconsole-rapporten

Adobe gebruikt een functie in Analysis Workspace met de naam Advertising Analytics om advertenties en zoekgegevens van meerdere platforms, waaronder Google, in te voeren.

De functie voor het analyseren van advertenties moet zijn geconfigureerd om gegevens te retourneren. Zie [ Hulp van Advertising Analytics ](/help/integrate/c-advertising-analytics/overview.md) voor details op hoe te om deze extra dimensies in Analysis Workspace toe te laten.

## Sociale rapporten

Sociale rapporten verschaffen vergelijkbare informatie als hun respectieve Gedragsrapport, behalve in de context van sociale netwerken. Deze gegevens zijn beschikbaar in Analysis Workspace door een dimensie met een segment te combineren.

Soms bereiken bezoekers uw site via meerdere kanalen in dezelfde sessie. Een bezoeker klikt bijvoorbeeld op een pagina met sociale media en een paar minuten later bezoekt een zoekprogramma om uw site te bereiken. In deze gevallen kunnen niet-sociale domeinen in dit rapport voorkomen. Als u niet-sociale domeinen wilt uitsluiten, sorteert u het rapport op bezoeken, of creeert u een exemplaar van het segment dat op klappen in plaats van bezoeken moet worden gebaseerd. Zie [ Containers van de Segmentatie ](/help/components/segmentation/seg-overview.md) in de de gebruikersgids van Componenten voor meer informatie.

### Sociaal - netwerkverwijzingen

Het rapport van de Verwijzingen van het Netwerk toont welke sociale netwerkdomeinen verkeer aan uw plaats dreef. Dit gegeven is beschikbaar in Analysis Workspace gebruikend de **Verwijzende dimensie van het Domein** en **bezoeken van Sociale Plaatsen** segment.

1. In het menu van Componenten, bepaal de plaats van de **Verwijzende dimensie van het Domein** en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. In het menu van Componenten, bepaal de plaats van de **Bezoeken van Sociale Plaatsen** segment en sleep binnen op het kleine gebied enkel boven de vrije vormlijst geëtiketteerd &quot;Slaga segment hier&quot;.
3. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

### Sociale pagina&#39;s - Landingspagina&#39;s

In het rapport Landing Pages wordt aangegeven op welke pagina&#39;s bezoekers zijn aangekomen nadat ze op een koppeling via een sociaal netwerk hebben geklikt. Dit gegeven is beschikbaar in Analysis Workspace gebruikend de **dimensie van de Ingang van de Pagina** en **bezoeken van Sociale Plaatsen** segment.

1. In het menu van Componenten, bepaal de plaats van de **dimensie van de Pagina van de Ingang** en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. In het menu van Componenten, bepaal de plaats van de **Bezoeken van Sociale Plaatsen** segment en sleep binnen op het kleine gebied enkel boven de vrije vormlijst geëtiketteerd &quot;Slaga segment hier&quot;.
3. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

### Sociaal - Omzettingen

Het Conversierapport bevat gegevens over e-commerce in de context van sociale netwerken. Voor het gebruik van deze rapporten op beide platforms is een aanvullende implementatie vereist. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor Analysis Workspace.

### Sociaal - Plug-ins

Het Plugins-rapport laat zien hoe bezoekers werken met ingesloten plug-ins voor sociale media op uw site. Aanvullende implementatie is vereist voor gebruik in Analysis Workspace. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct worden verzameld.

### Sociaal - Gebruikersstroom

Het de stroomrapport van Gebruikers toont het kleven gegevens in de context van bezoekers die door een sociaal netwerk aankomen.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik het pictogram van Componenten op de linkerzijde, dan sleep het **Bezoek van Sociale Plaatsen** segment op het kleine gebied net boven de stroomvisualisatie geëtiketteerd &quot;Daling een Segment hier&quot;.
3. Bepaal de plaats van de **dimensie van Pagina&#39;s**, dan klik het pictogram van de Pijl om paginawaarden te openbaren. Dimension-items zijn gekleurd geel.
4. Zoek de gewenste paginawaarde waarmee moet worden begonnen en sleep deze naar de ruimte met het label &#39;Dimension of item&#39; in het midden
5. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

## Campagnes - Alles

Het campagnerapport is beschikbaar in Analysis Workspace gebruikend de **het Volgen dimensie van de Code**. Merk op dat het gebruiken van de het Volgen dimensie van de Code extra implementatie vereist om gegevens te verzamelen.

Het is mogelijk UTM-parameters te verzamelen in Adobe Analytics met behulp van aangepaste variabelen (eVars). Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat de waarden van de trackingcode in Adobe Analytics correct worden verzameld.

1. In het menu van Componenten, bepaal de plaats van de **Volgende dimensie van de Code** en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Betaalde trefwoorden

Het rapport Betaalde trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een betaalde zoekkoppeling van een zoekmachine klikt. De **Trefwoorden van het Onderzoek - de Betaalde** dimensie is beschikbaar in Analysis Workspace, maar vereist een éénmalige opstelling van betaalde onderzoeksopsporing om gegevens te verzamelen. Zie [ Betaalde Opsporing van het Onderzoek ](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) in de Admin gebruikersgids voor opstellingsdetails.

1. In het menu van Componenten, bepaal de plaats van het **Sleutelwoord van het Onderzoek - Betaalde** dimensie en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Organic Keywords

Het rapport met biologische trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een biologische zoekkoppeling klikt vanuit een zoekengine. De **Trefwoorden van het Onderzoek - Natuurlijke** dimensie is beschikbaar in Analysis Workspace. Let op: als de detectie van betaalde zoekopdrachten niet is ingesteld, worden met deze dimensie zowel betaalde als natuurlijke trefwoorden verzameld.

1. In het menu van Componenten, bepaal de plaats van het **Sleutelwoord van het Onderzoek - Natuurlijke** dimensie en sleep het op het grote gebied van de vrije vormlijst geëtiketteerd &quot;Slaga Dimension hier&quot;.
2. Sleep de gewenste metriek op de werkruimte naast de automatisch gecreeerde **metrische voorkomen.** Zie de [ Metrische vertaalgids ](common-metrics.md) voor details op hoe te om elke respectieve metrisch te verkrijgen.

## Kostenanalyse

Dit rapport bevat informatie over het bezoek, de kosten en de inkomstenprestaties voor uw betaalde marketingkanalen. Adobe biedt een speciaal product voor insight, Adobe Advertising Cloud. Neem contact op met het Adobe-accountteam als uw organisatie dit product wil gebruiken.
