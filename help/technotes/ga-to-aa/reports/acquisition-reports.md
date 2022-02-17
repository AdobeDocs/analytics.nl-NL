---
title: Overnameverslagen in Adobe Analytics
description: Leer hoe u op aankopen gebaseerde rapporten maakt met Analysis Workspace.
feature: Third-party Integration
exl-id: 2929d34b-8eb0-4105-a49c-02d536929fe0
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 0%

---

# Overnameverslagen

In overnamerapporten ziet u hoe u bezoekers van uw site ontvangt.

In Adobe Analytics worden deze rapporten **Marketingkanalen**. Zij vereisen wat basis aanvankelijke opstelling, maar staan een veel meer aangepaste mening van kanalen toe.

>[!IMPORTANT]
>
> Opstelling uw de verwerkingsregels van het Kanaal van de Marketing om deze rapporten te gebruiken. Zie [Aan de slag met marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) voor informatie over hoe te om de Kanalen van de Marketing in uw organisatie het best te vormen.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics](create-report.md) als u het gereedschap nog niet kent in Adobe Analytics.

## Alle verkeer - Kanalen

Hiermee geeft u een geaggregeerde weergave weer van alle kanalen die bezoekers gebruiken om uw site te bereiken.

1. Zoek in het menu Componenten de locatie **Marketingkanaal** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Alle verkeer - Treemaps

Toont een overzicht van kanaalverkeer. Dit rapport is gelijkaardig aan Al Verkeer - Kanalen, maar op een verschillende manier getoond.

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de Treemap-visualisatie naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep vervolgens het gereedschap **Marketingkanaal** afmeting op het grote vrije gebied van de lijstlijst geëtiketteerd &quot;Slaat hier een afmeting neer.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.
4. Extra metriek maken extra overgangen. Indien slechts één driehoek gewenst is:
   1. Klik op de bovenste cel van de gewenste metrische waarde om de driehoek te vertegenwoordigen.
   2. Houd Shift ingedrukt en klik op de laatste cel van dezelfde metrische kolom om de kolom blauw te markeren. Indien correct uitgevoerd, is er één treemap aanwezig in de visualisatie.
   3. Klik op de gekleurde stip in de rechterbovenhoek van de driehoekige visualisatie en klik vervolgens op het selectievakje Selectie vergrendelen.

De boomwerkingen kunnen op om het even welke afmeting worden toegepast, niet alleen de Kanalen van de Marketing.

## Alle verkeer - Bron/Normaal

De bron en middelrapporten tonen de domeinen die verkeer aan uw plaats dreef.

* De **Bron** de primaire dimensie is in Analysis Workspace beschikbaar als de **Referentiedomein** dimensie.
* De **Normaal** de primaire dimensie is in Analysis Workspace beschikbaar als de  **Type referentie** dimensie.
* De **Trefwoord** de primaire dimensie is in Analysis Workspace beschikbaar als de **Trefwoord zoeken** dimensie.

1. Zoek in het optiemenu de gewenste afmeting die hierboven is vermeld en sleep deze naar het grote tabelgebied in vrije vorm met het label &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de volgende pagina&#39;s in de gebruikershandleiding van Componenten voor meer informatie over hun respectievelijke dimensie:

* [Referentiedomein](/help/components/dimensions/referring-domain.md)
* [Type referrer](/help/components/dimensions/referrer-type.md)
* [Trefwoord zoeken](/help/components/dimensions/search-keyword.md)

## Alle verkeer - verwijzingen

* De **Bron** de primaire dimensie is in Analysis Workspace beschikbaar als de **Referentiedomein** dimensie.
* De **Openingspagina** de primaire dimensie is in Analysis Workspace beschikbaar als de **Itempagina** dimensie.

1. Zoek in het optiemenu van de componenten de **Referentiedomein** of **Itempagina** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de [Referentiedomein](/help/components/dimensions/referring-domain.md) voor meer informatie in de gebruikershandleiding van Componenten.

## Google Ads-rapporten en zoekconsole-rapporten

Adobe gebruikt in Analysis Workspace een functie met de naam Advertising Analytics om advertenties en zoekgegevens van meerdere platforms, waaronder Google, in te voeren.

De functie voor het analyseren van advertenties moet zijn geconfigureerd om gegevens te retourneren. Zie [Advertising Analytics Help](/help/integrate/c-advertising-analytics/overview.md) voor meer informatie over het inschakelen van deze extra afmetingen in Analysis Workspace.

## Sociale rapporten

Sociale rapporten verschaffen vergelijkbare informatie als hun respectieve Gedragsrapport, behalve in de context van sociale netwerken. Deze gegevens zijn beschikbaar in Analysis Workspace door een dimensie met een segment te combineren.

Soms bereiken bezoekers uw site via meerdere kanalen in dezelfde sessie. Een bezoeker klikt bijvoorbeeld op een pagina met sociale media en een paar minuten later bezoekt een zoekprogramma om uw site te bereiken. In deze gevallen kunnen niet-sociale domeinen in dit rapport voorkomen. Als u niet-sociale domeinen wilt uitsluiten, sorteert u het rapport op bezoeken, of creeert u een exemplaar van het segment dat op klappen in plaats van bezoeken moet worden gebaseerd. Zie [Segmenteringscontainers](/help/components/segmentation/seg-overview.md) in de gebruikershandleiding van Componenten voor meer informatie.

### Sociaal - netwerkverwijzingen

Het rapport van de Verwijzingen van het Netwerk toont welke sociale netwerkdomeinen verkeer aan uw plaats dreef. Deze gegevens zijn in Analysis Workspace beschikbaar via de **Referentiedomein** dimensie en **Bezoeken van sociale sites** segment.

1. Zoek in het menu Componenten de locatie **Referentiedomein** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Zoek in het menu Componenten de locatie **Bezoeken van sociale sites** en sleep in het kleine gebied net boven de vrije-vormtabel met het label &#39;Hier een segment neerzetten&#39;.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

### Sociale pagina&#39;s - Landingspagina&#39;s

In het rapport Landing Pages wordt aangegeven op welke pagina&#39;s bezoekers zijn aangekomen nadat ze op een koppeling via een sociaal netwerk hebben geklikt. Deze gegevens zijn in Analysis Workspace beschikbaar via de **Itempagina** dimensie en **Bezoeken van sociale sites** segment.

1. Zoek in het menu Componenten de locatie **Itempagina** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Zoek in het menu Componenten de locatie **Bezoeken van sociale sites** en sleep in het kleine gebied net boven de vrije-vormtabel met het label &#39;Hier een segment neerzetten&#39;.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

### Sociaal - Omzettingen

Het Conversierapport bevat gegevens over e-commerce in de context van sociale netwerken. Voor het gebruik van deze verslagen op beide platforms is een aanvullende implementatie vereist. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor Analysis Workspace.

### Sociaal - Plug-ins

Het rapport Plugins laat zien hoe bezoekers werken met ingesloten plug-ins voor sociale media op uw site. Aanvullende implementatie is vereist voor gebruik in Analysis Workspace. Adobe raadt aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct worden verzameld.

### Sociaal - Gebruikersstroom

Het de stroomrapport van Gebruikers toont het kleven gegevens in de context van bezoekers die door een sociaal netwerk aankomen.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik op het pictogram Componenten aan de linkerkant en sleep vervolgens het gereedschap **Bezoeken van sociale sites** segment op het kleine gebied net boven de stroomvisualisatie met het label &#39;Hier een segment neerzetten&#39;.
3. Zoek de **Pagina&#39;s** en klikt u op het pictogram Pijl om de paginawaarden weer te geven. Dimension-items zijn gekleurd geel.
4. Zoek de gewenste paginawaarde waarmee moet worden begonnen en sleep deze naar de ruimte met het label &#39;Dimension of item&#39; in het midden
5. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

## Campagnes - Alles

Het campagnerapport is in Analysis Workspace beschikbaar via de **Trackingcode** dimensie. Merk op dat het gebruiken van de het Volgen dimensie van de Code extra implementatie vereist om gegevens te verzamelen.

Het is mogelijk UTM-parameters te verzamelen in Adobe Analytics met behulp van aangepaste variabelen (eVars). Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat codewaarden in Adobe Analytics correct worden verzameld.

1. Zoek in het menu Componenten de locatie **Trackingcode** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Betaalde trefwoorden

Het rapport Betaalde trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een betaalde zoekkoppeling van een zoekmachine klikt. De **Trefwoorden zoeken - Betaald** dimensie is beschikbaar in Analysis Workspace, maar vereist een eenmalige instelling van betaalde zoekdetectie om gegevens te verzamelen. Zie [Detectie van betaalde zoekopdracht](/help/admin/admin/paid-search-detection/paid-search-detection.md) in de gebruikershandleiding voor Admin voor meer informatie over de installatie.

1. Zoek in het menu Componenten de locatie **Trefwoord zoeken - Betaald** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Organic Keywords

Het rapport met biologische trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een biologische zoekkoppeling klikt vanuit een zoekengine. De **Trefwoorden zoeken - Natuurlijk** -dimensie is beschikbaar in Analysis Workspace. Let op: als de detectie van betaalde zoekopdrachten niet is ingesteld, worden met deze dimensie zowel betaalde als natuurlijke trefwoorden verzameld.

1. Zoek in het menu Componenten de locatie **Trefwoord zoeken - Natuurlijk** en sleep deze naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een Dimension neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte gegevens **Voorval** metrisch. Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Kostenanalyse

Dit rapport bevat informatie over het bezoek, de kosten en de inkomstenprestaties voor uw betaalde marketingkanalen. Adobe biedt een speciaal product voor inzicht dat Adobe Advertising Cloud wordt genoemd. Neem contact op met de accountmanager van uw organisatie als uw organisatie dit product wil gebruiken.
