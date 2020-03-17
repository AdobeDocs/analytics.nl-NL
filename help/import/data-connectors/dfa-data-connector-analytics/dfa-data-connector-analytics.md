---
description: 'null'
keywords: DFA
title: DFA Data Connector voor Adobe Analytics
topic: Data connectors
uuid: 8d04909f-6f17-4b7d-a199-99c923253474
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# DFA Data Connector voor Adobe Analytics{#dfa-data-connector-for-adobe-analytics}

In de steeds complexere en competitievere online markt van vandaag, moeten online adverteerders en agentschappen hun inzicht in de online marketing omgeving voortdurend verbeteren, en hun rendement op reclame-uitgaven. Hoewel adverteerders, agentschappen en uitgevers allemaal over afzonderlijke hulpmiddelen beschikken om deze doelstellingen te verwezenlijken, kan het handmatig verzamelen van gegevens uit verschillende gegevenssystemen en processen de doeltreffendheid van online marketingcampagnes ernstig belemmeren, wat leidt tot minder dan optimale campagneprestaties, gegevensdiscrepanties en verwarring.

De integratie DoubleClick for Advertisers (DFA) lost dit probleem op door Adobe® Data Connectors™ te gebruiken, zodat Dubbelklik op DFA automatisch gegevens kan doorgeven aan Rapporten en Analytics.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**

![](assets/data-connectors-home.png)

## Belangrijkste voordelen{#key-benefits}

Belangrijke voordelen van de gegevensconnector - DFA-integratie zijn:

* **Meer conversie**: Geniet van richtingsinzicht voor het optimaliseren van plaatsing van advertentiecampagnes en on-site conversie op basis van gedrag en voorkeuren van bezoekers na klikken.
* **Gedeelde locatie voor gegevens**: Combineer Dubbelklik DFA klik-door en mening - door gegevens met Rapporten &amp; Analytics om dwars-organisatorische samenwerking en capaciteit te verbeteren om objectieve besluiten te nemen.
* **Analyse** van de toegevoegde waarde: Dankzij de geautomatiseerde integratie tussen DFA en Adobe Reports &amp; Analytics kunnen adverteerders en agentschappen minder tijd besteden aan het uitvoeren van gegevens en meer tijd aan het analyseren van rapporten en het ondernemen van actie.
* **Meer inzicht** van de klant: Meer inzicht krijgen in waar bezoekers vandaan komen en wat ze doen op uw site.
* **Metrische gegevens** van levenssucces: Meet de effectiviteit van uw aanschafcampagnes gedurende de gehele levenscyclus van de bezoeker.
* **Geïntegreerde rapportage**: Automatisch gegevens synchroniseren tussen DFA en Rapporten &amp; Analytics voor gestroomlijnde bedrijfsprocessen en rapportering.
* **Analyse** van de levertijdbezoeker: De campagnedoeltreffendheid van de meting door veelvoudige user-defined succesgebeurtenissen en levenwaarde.
* **Kostencijfers**: Optimaliseer het rendement van investeringen door DFA-kostencijfers en de opbrengsten uit deze kosten in één enkel systeem te vergelijken.

## Ad Serving Integration Overzicht{#ad-serving-integration-overview}

Er zijn verschillende manieren waarop deze integratie gegevens vastlegt over de ad-gedreven bezoeker. De eerste manier is door op een advertentie te klikken en aan te komen op een gelabelde bestemmingspagina, die een klik door wordt genoemd:

![](assets/Diagram1.png)

De bezoeker komt op de plaats van een uitgever aan, die de Advertentie ontvangt. Deze advertentie heeft een unieke id, de zogenaamde advertentie-id. Advertenties bestaan uit een Plaatsing plus een Creatief, die beschrijven waar Advertentie op de plaats van de Uitgever is en welke inhoud aan de bezoeker werd getoond. Wanneer de bezoeker deze advertentie, plaatsing, of creatief van de DFA inhoudsservers haalt, volgt het een Indruk aan de Servers van de Vullingslamp DFA voor deze bezoeker (1).

Als de bezoeker op de advertentie klikt (2), wordt de Server van het Vullingslicht gevraagd, die een klik tellen, dan leidt 302 (3) de bezoeker aan de het Bestanden Pagina opnieuw. Wanneer de bezoeker op de Openende pagina is aangekomen, wordt dit genoemd een klik-door. Deze pagina bevat de trackingcode van Adobe die gegevens opvraagt van de DFA Floodlight Server.

Als de bezoeker niet daadwerkelijk op de Openingspagina aankomt nadat de Floodlight-server een klik heeft bijgehouden, wordt dit geen doorklikken genoemd. Sommige advertenties en implementaties kunnen er in feite niet toe leiden dat de browser van de bezoeker zich aan de 302 omleiding houdt. Zie [Metrische verschillen](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md)met elkaar verzoenen voor verdere bespreking over dit onderwerp.

De volgende metrische waarde die door deze integratie wordt vastgelegd, doet zich voor wanneer de bezoeker de advertentie-indruk ontvangt, niet klikt, maar ergens in de nabije toekomst op een andere manier op de bestemmingspagina aankomt.

![](assets/Viewthrough.png)

Dit scenario wordt een mening-door genoemd. Het verschil in dit scenario met het klikthrough-scenario is dat de bezoeker niet op Advertentie klikt, maar in plaats daarvan aan andere activiteiten alvorens aan de het Aanvoeren pagina (2) verder gaat. In het eenvoudigste geval typt de bezoeker de URL van de bestemmingspagina in de browser. In andere gevallen gaat de bezoeker verder met bladeren, maar gebruikt hij later een zoekmachine, die de bezoeker naar de landingspagina stuurt. In elk geval arriveert de gebruiker op de landingspagina.

## Adobe-integratie: Real-time gegevensverzameling{#adobe-integration-real-time-data-collection}

Het volgende cijfer toont hoe de gegevensinzameling werkt.

![](assets/DFA_data_collection.png)

Het gedeelte voor gegevensverzameling van de Adobe-integratie begint wanneer de bezoeker naar de bestemmingspagina komt (1). De Adobe-code voor gegevensverzameling die op de bestemmingspagina wordt uitgevoerd, heeft geen kennis van de geschiedenis die de bezoeker heeft meegemaakt voor advertenties. Het Google DFA-team heeft een service gecoördineerd die wordt uitgevoerd op de DFA Floodlight Server, zodat de Adobe-code query&#39;s kan uitvoeren naar informatie en informatie over de bezoeker die momenteel op de site aanwezig is (2). Om deze gegevens te verkrijgen, wordt het Adobe-beeldbaken tijdelijk vertraagd en worden de gegevens opgevraagd bij de Floodlight-server.

Als de gegevens zijn ontvangen of te lang duren, wordt de hit op de Adobe-trackingservers geactiveerd (3).

De module Integeren is een speciale kern-Adobe JavaScript-module die ervoor zorgt dat het Adobe-beeldbaken wordt vertraagd en gedurende een bepaalde tijd (`s.maxDelay`) wacht op een verzoek van een derde. `s.maxDelay` Hiermee bepaalt u hoe lang de module Integrate wacht op gegevens van de DFA Floodlight-server voordat de afbeeldingstag naar de browser van de bezoeker wordt geactiveerd. Dit gedrag is belangrijk, zodat de basisgegevens van de bezoeker nog steeds worden verzameld, zelfs wanneer de DFA-pilootservers zijn ingedrukt of zwaar zijn geladen. Als de gegevens van de Vullingslamp aankomen voordat deze `s.maxDelay` zijn verlopen, worden de trackinggegevens van Adobe direct geactiveerd en bevatten deze de aanvullende DFA-gegevens.

Wanneer een time-out optreedt, kan de paginacode een Adobe Reports &amp; Analytics-gebeurtenis opgeven die als een Timeout-gebeurtenis moet worden gebruikt. Deze gebeurtenis is nuttig wanneer het diagnostiseren van problemen met de integratie, of wanneer het aanpassen `s.maxDelay`. In gevallen waarin er sprake is van buitensporige vertragingen, moet u deze verhogen `s.maxDelay`. `s.maxDelay` kan echter te hoog worden ingesteld, in welk geval bezoekers de site kunnen verlaten voordat de `s.maxDelay` timer vervalt. .

Soms reageert de Floodlight-server met fouten over de bezoeker. Dit gebeurt gewoonlijk wanneer de Floodlight-server niets weet over de bezoeker, omdat de bezoeker nog geen advertenties heeft gezien of geen DFA-bezoekerscookie heeft. De paginacode kan een variabele van de Omzetting van de Douane (eVar) specificeren die deze fouten zal verzamelen, en kan helpen bij het oplossen van problemen van de implementatie of op kwesties met de transactie van Google wijzen. De meest voorkomende fouten zijn Geen geschiedenis, Geen cookie, Query-fout en Opted Out, zoals in de volgende tabel wordt beschreven:

| Fout | Naam | Beschrijving |
|---|---|---|
| nh | Geen geschiedenis | De bezoeker heeft geen advertenties weergegeven of erop geklikt. |
| nc | Geen cookie | De bezoeker heeft geen DFA-bezoekerscookie. |
| qe | Zoekfout | Er is een fout opgetreden bij het opvragen van gegevens voor de Floodlight-server. |
| oo | Afgemeld | De bezoeker heeft Google-imitatie uitgeschakeld of op tracking geklikt. |

## Adobe-integratie: Night Data Import{#adobe-integration-nightly-data-import}

Het gedeelte van de gegevensverzameling van de integratie verzamelt doorklikgegevens en doorkijkgegevens over sitebezoekers. Om DFA-klikken, -indruk en -kostengegevens te verkrijgen, zijn er een &#39;s nachts proces dat door Google en Adobe wordt gecoördineerd om deze aanvullende gegevens in de geïntegreerde rapportsuite te importeren. Deze metriek wordt ingevoerd door Gegevensbronnen, die betekenen zij in geaggregeerd slechts beschikbaar zijn, en zijn niet op het bezoekniveau.

## VersiesVerschillen{#version-differences}

Er zijn momenteel drie versies van de integratie DFA, versies 1.0, 1.5, en 2.0.

De volgende tabel geeft een overzicht van de functies in elke versie van de integratie.

| Functie | Versie 1.0 | Versie 1.5 | Versie 2.0 |
|---|---|---|---|
| Nauwkeurige cijfers voor DFA-klikken en -indrukken | Ja | Ja | Ja |
| Doorklikken en Doorkijken - Bijhouden | Ja | Ja | Ja |
| Integratie ontvangt gegevens op Advertiser-niveau | Nee | Ja | Ja |
| De integratie ontvangt gegevens op het niveau van de Configuratie van de Vulling | Nee | Nee | Ja |
| Kostencijfers | Nee | Nee | Ja |
| Creative Metrics | Nee | Nee | Ja |
| Query-tekenreeksen langer dan 2 kB | Nee | Ja | Ja |
| Gebruikt de integratiemodule voor optimale gegevensverzameling van derden | Nee | Ja | Ja |
| Time-out en foutcontrole | Nee | Ja | Ja |
| Geen id aan de volgende clientzijde nodig | Nee | Nee | Ja |

### Informatie over versie 1.5 {#section-b5a3e967cfa141ea8f740612336181be}

Versie 1.5 van de integratie introduceert de module Integrate aan de bestemmingspagina Java Script. Met de module Integrate kunt u aanvragen met een vaste grootte indienen bij de DFA-server (ad.doubleclick.net) die de beperkingen voor 2K-verzoeken van de vorige integratie overschrijdt. Er wordt ook een configureerbare time-out geïntroduceerd *`s.maxDelay`* om Adobe-bezoekersgegevens te blijven verzamelen wanneer er netwerkstoringen optreden. Fouten en time-outs kunnen ook worden vastgelegd in analytische variabelen.

De volgende illustratie toont netwerkinteracties op de landingspagina in versie 1.5.

![](assets/DFA_About_1_5.png)

In versie 1.5 vraagt de module Integrate (2) om gegevens van de Floodlight-server (3). De Floodlight-server wordt omgeleid naar de DFA-server, die op dezelfde manier gegevens over de bezoeker retourneert als versie 1.0. Het zal 302 (4) aan een speciale vertaaldienst op integration.112.2o7.net opnieuw richten, die de reactiestructuur in een voorwerp JSON zal veranderen. De module Integrate gebruikt dit JSON-object en geeft de informatie door aan Adobe Tracking (5).

Bij de overgang van versie 1.0 van de integratie naar versie 1.5 moet JavaScript worden gewijzigd. U kunt dit JavaScript verkrijgen door u aan te melden bij uw Adobe Online Marketing Suite-account, het Genesisproduct te kiezen, op Bewerken te klikken bij uw DFA-integratie en door te gaan met de wizard. Als er eerder een Client Site-id is toegewezen, ontvangt u de nieuwe JavaScript-code direct via e-mail nadat u de integratie hebt opgeslagen. Zodra u deze code hebt, zult u ook nieuwe versie van de kern s_code nodig hebben die de integrate module heeft. Deze code kan worden aangevraagd bij uw accountmanager of implementatieconsultant.

Een belangrijke functie van de nieuwe JavaScript-code is dat er geen implementatiewijziging nodig is tussen versie 1.5 en versie 2.0.

### Info over Versie 2.0 {#section-afd56de0c56c4489bb5ddc5798d6709a}

De recentste versie van de integratie DFA brengt gegevens voor een volledige Configuratie van de Vullinglight in de integratie. Vóór versie 2.0 waren de afzonderlijke integraties gekoppeld aan één DFA Advertiser. Met deze verandering, zullen de klikken, de Indrukking, en de metriek van de Kosten voor de volledige Configuratie van de Vullinglight in de geïntegreerde rapportreeks worden omvat. Het is ook mogelijk om dwars-plaats mening doorheen te volgen, wanneer die twee plaatsen binnen de zelfde Configuratie van het Vullingslicht zijn.

De meetgegevens voor de mediadracht zijn ook beschikbaar vanaf versie 2.0 van de integratie. Om media kostenmetriek voor een integratie toe te laten, moet u een gebeurtenis van Rapporten &amp; van Analytics voor Media Kostprijs in de tovenaar van Genesis kiezen, evenals specificeren welke munt de metrische cijfers in de interface DFA zijn.

Verwacht wordt dat de time-outs zullen afnemen met de 2.0-integratie, aangezien de 302 omleidingen zijn geëlimineerd. Het elimineren van deze hop zou onderbrekingen moeten verminderen, en de hoeveelheid DFA gegevens verhogen u kunt integreren.

Als een configuratie van de Vullinglight een gedeelde configuratie in DFA is, de verbetering van versie 1. 5 tot 2.0 zorgt ervoor dat conversiegegevens voor alle gedeelde adverteerders in de configuratie van de Vullingslamp worden opgenomen in de rapportsuite.

### Bijwerken naar versie 2.0 {#section-f0bf90b9a7a1434ab1540b6c0999f4c7}

In de volgende tabel worden de eigenaars voor de migratie naar nieuwere versies van de integratie weergegeven:

| Migratie | Eigenaar | Taken |
|---|---|---|
| Versie 1.0 t/m 1.5 | Client | JavaScript van versie 1.5 implementeren met geïntegreerde module |
| Versie 1.5 t/m 2.0 | Client | Client begint met Google over tijdframes voor upgrade. Na goedkeuring schakelt Google Advanced Ad Serving in. |
