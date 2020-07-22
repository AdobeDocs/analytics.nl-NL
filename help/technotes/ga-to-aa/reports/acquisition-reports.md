---
title: Overnamerapporten in Adobe Analytics
description: Leer hoe u op aankopen gebaseerde rapporten maakt met Analysis Workspace.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 0%

---


# Overnameverslagen

In overnamerapporten ziet u hoe u bezoekers van uw site ontvangt.

In Adobe Analytics worden deze rapporten **Marketingkanalen** genoemd. Zij vereisen wat basis aanvankelijke opstelling, maar staan een veel meer aangepaste mening van kanalen toe.

>[!IMPORTANT]
>
> Opstelling uw de verwerkingsregels van het Kanaal van de Marketing om deze rapporten te gebruiken. Zie Aan de [slag met de Kanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) van de Marketing voor informatie over hoe te om de Kanalen van de Marketing in uw organisatie het best te vormen.

Deze pagina gaat ervan uit dat de gebruiker een basiskennis heeft van het gebruik van Analysis Workspace. Zie [Een basisrapport maken in Analysis Workspace voor Google Analytics-gebruikers](create-report.md) als u het programma nog niet kent in Adobe Analytics.

## Alle verkeer - Kanalen

Hiermee geeft u een geaggregeerde weergave weer van alle kanalen die bezoekers gebruiken om uw site te bereiken.

1. Zoek in het menu Componenten de dimensie **Marketingkanaal** en sleep deze naar het grote tabelgebied in vrije vorm met de naam &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Alle verkeer - Treemaps

Toont een overzicht van kanaalverkeer. Dit rapport is gelijkaardig aan Al Verkeer - Kanalen, maar op een verschillende manier getoond.

1. Klik op het pictogram Visualisaties aan de linkerkant en sleep de Treemap-visualisatie naar de werkruimte boven de lege vrije-vormtabel.
2. Klik op het pictogram Componenten aan de linkerkant en sleep de dimensie **Marketing Channel** naar het grote tabelgebied in de vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.
4. Extra metriek maken extra overgangen. Indien slechts één driehoek gewenst is:
   1. Klik op de bovenste cel van de gewenste metrische waarde om de driehoek te vertegenwoordigen.
   2. Houd Shift ingedrukt en klik op de laatste cel van dezelfde metrische kolom om de kolom blauw te markeren. Indien correct uitgevoerd, is er één treemap aanwezig in de visualisatie.
   3. Klik op de gekleurde stip in de rechterbovenhoek van de driehoekige visualisatie en klik vervolgens op het selectievakje Selectie vergrendelen.

De boomwerkingen kunnen op om het even welke afmeting worden toegepast, niet alleen de Kanalen van de Marketing.

## Alle verkeer - Bron/Normaal

De bron en middelrapporten tonen de domeinen die verkeer aan uw plaats dreef.

* De primaire dimensie **Bron** is beschikbaar in Analysis Workspace als **Verwijzende dimensie van het Domein** .
* De **middelgrote** primaire afmeting is beschikbaar in Analysis Workspace als afmeting van het Type **van** Referteur.
* De primaire dimensie van het **Sleutelwoord** is beschikbaar in Analysis Workspace als dimensie van het Sleutelwoord **van het** Onderzoek.

1. Zoek in het optiemenu de gewenste afmeting die hierboven is vermeld en sleep deze naar het grote tabelgebied in vrije vorm met het label &#39;Hier een afmeting neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Raadpleeg de volgende pagina&#39;s in de gebruikershandleiding van Componenten voor meer informatie over hun respectievelijke dimensie:

* [Referentiedomein](/help/components/dimensions/referring-domain.md)
* [Type referrer](/help/components/dimensions/referrer-type.md)
* [Trefwoord zoeken](/help/components/dimensions/search-keyword.md)

## Alle verkeer - verwijzingen

* De primaire dimensie **Bron** is beschikbaar in Analysis Workspace als **Verwijzende dimensie van het Domein** .
* De primaire dimensie van de **bestemmingspagina** is beschikbaar in Analysis Workspace als **Invoerpagina** .

1. Zoek in het optiemenu de dimensie Refererend domein **of** Itempagina **** en sleep deze naar het grote tabelgebied Vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

Zie de afmeting Verwijzend Domein [](/help/components/dimensions/referring-domain.md) in de de gebruikersgids van Componenten voor meer informatie.

## Google Ads-rapporten en zoekconsole-rapporten

Adobe gebruikt de functie Advertising Analytics in Analysis Workspace om advertenties en zoekgegevens van meerdere platforms, waaronder Google, in te voeren.

De functie voor het analyseren van advertenties moet zijn geconfigureerd om gegevens te retourneren. Zie [Advertising Analytics Help](/help/integrate/c-advertising-analytics/overview.md) voor meer informatie over het inschakelen van deze extra dimensies in Analysis Workspace.

## Sociale rapporten

Sociale rapporten verschaffen vergelijkbare informatie als hun respectieve Gedragsrapport, behalve in de context van sociale netwerken. Deze gegevens zijn beschikbaar in Analysis Workspace door een dimensie met een segment te combineren.

Soms bereiken bezoekers uw site via meerdere kanalen in dezelfde sessie. Een bezoeker klikt bijvoorbeeld op een pagina met sociale media en een paar minuten later bezoekt een zoekprogramma om uw site te bereiken. In deze gevallen kunnen niet-sociale domeinen in dit rapport voorkomen. Als u niet-sociale domeinen wilt uitsluiten, sorteert u het rapport op bezoeken, of creeert u een exemplaar van het segment dat op klappen in plaats van bezoeken moet worden gebaseerd. Zie Containers [van de](/help/components/c-segmentation/seg-overview.md) Segmentatie in de de gebruikersgids van Componenten voor meer informatie.

### Sociaal - netwerkverwijzingen

Het rapport van de Verwijzingen van het Netwerk toont welke sociale netwerkdomeinen verkeer aan uw plaats dreef. Deze gegevens zijn beschikbaar in Analysis Workspace met behulp van de dimensie **Refererend Domein** en **Bezoek van het segment Sociale Plaatsen** .

1. Zoek in het menu Componenten de dimensie Refererend domein **** en sleep deze naar het grote tabelgebied Vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Zoek in het menu Componenten de **bezoeken van het segment Sociale sites** en sleep in het kleine gebied net boven de vrije-vormtabel met het label &#39;Hier een segment neerzetten&#39;.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

### Sociale pagina&#39;s - Landingspagina&#39;s

In het rapport Landing Pages wordt aangegeven op welke pagina&#39;s bezoekers zijn aangekomen nadat ze op een koppeling via een sociaal netwerk hebben geklikt. Deze gegevens zijn beschikbaar in Analysis Workspace met behulp van de dimensie **Pagina** invoeren en **bezoeken vanuit het segment Sociale sites** .

1. Zoek in het menu Componenten de afmetingen voor de **invoerpagina** en sleep deze naar het grote tabelgebied voor vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Zoek in het menu Componenten de **bezoeken van het segment Sociale sites** en sleep in het kleine gebied net boven de vrije-vormtabel met het label &#39;Hier een segment neerzetten&#39;.
3. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

### Sociaal - Omzettingen

Het Conversierapport bevat gegevens over e-commerce in de context van sociale netwerken. Voor het gebruik van deze verslagen op beide platforms is een aanvullende implementatie vereist. Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct zijn geconfigureerd voor Analysis Workspace.

### Sociaal - Plug-ins

Het rapport Plugins laat zien hoe bezoekers werken met ingesloten plug-ins voor sociale media op uw site. Aanvullende implementatie is vereist voor gebruik in Analysis Workspace. Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat deze gegevens correct worden verzameld.

### Sociaal - Gebruikersstroom

Het de stroomrapport van Gebruikers toont het kleven gegevens in de context van bezoekers die door een sociaal netwerk aankomen.

1. Klik op het pictogram voor visualisatie aan de linkerkant en sleep een stroomvisualisatie naar de werkruimte boven de vrije-vormtabel
2. Klik op het pictogram Componenten aan de linkerkant en sleep de **Bezoekingen van het segment Sociale sites** naar het kleine gebied net boven de flowvisualisatie met het label &#39;Hier een segment neerzetten&#39;.
3. Zoek de afmetingen voor **pagina** &#39;s en klik op het pictogram Pijl om de paginawaarden weer te geven. Dimensie-items zijn geel.
4. Zoek de gewenste paginawaarde waarmee u wilt beginnen en sleep deze naar de ruimte met het label Dimensie of item in het midden
5. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

## Campagnes - Alles

Het campagnerapport is beschikbaar in Analysis Workspace met behulp van de dimensie **Trackingcode** . Merk op dat het gebruiken van de het Volgen dimensie van de Code extra implementatie vereist om gegevens te verzamelen.

Het is mogelijk UTM-parameters te verzamelen in Adobe Analytics met behulp van aangepaste variabelen (eVars). Adobe raadt u aan samen te werken met een implementatieconsultant om ervoor te zorgen dat de waarden van de trackingcode correct worden verzameld in Adobe Analytics.

1. Zoek in het menu Componenten de dimensie **Code** bijhouden en sleep deze naar het grote tabelgebied voor vrije vorm met de naam &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Betaalde trefwoorden

Het rapport Betaalde trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een betaalde zoekkoppeling van een zoekmachine klikt. De dimensie Trefwoorden **zoeken - Betaald** is beschikbaar in Analysis Workspace, maar vereist een eenmalige instelling van betaalde zoekdetectie om gegevens te verzamelen. Zie Detectie van [betaalde zoekopdrachten](/help/admin/admin/paid-search-detection/paid-search-detection.md) in de gebruikershandleiding voor Admin voor meer informatie.

1. Zoek in het menu Componenten het trefwoord **Zoeken - Betaalde** dimensie en sleep het naar het grote tabelgebied Vrije vorm met het label &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Campagnes - Organic Keywords

Het rapport met biologische trefwoorden laat zien hoe elk trefwoord wordt uitgevoerd nadat een bezoeker op een biologische zoekkoppeling klikt vanuit een zoekengine. De **zoektrefwoorden - Natuurlijke** dimensie is beschikbaar in Analysis Workspace. Let op: als de detectie van betaalde zoekopdrachten niet is ingesteld, worden met deze dimensie zowel betaalde als natuurlijke trefwoorden verzameld.

1. Zoek in het menu Componenten het trefwoord **Zoeken - Natuurlijk** en sleep het naar het grote tabelgebied in de vrije vorm met het label &#39;Hier een dimensie neerzetten&#39;.
2. Sleep de gewenste metriek naar de werkruimte naast de automatisch gemaakte metrische **Voorvallen** . Zie de [Metrische vertaalgids](common-metrics.md) voor details over hoe te om elke respectieve metrisch te verkrijgen.

## Kostenanalyse

Dit rapport bevat informatie over het bezoek, de kosten en de inkomstenprestaties voor uw betaalde marketingkanalen. Adobe biedt een speciaal product voor het verschaffen van inzicht met de naam Adobe Advertising Cloud. Neem contact op met de accountmanager van uw organisatie als uw organisatie dit product wil gebruiken.
