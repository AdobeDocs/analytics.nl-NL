---
title: Veelgestelde vragen over Cross-device Analytics
description: Veelgestelde vragen over apparaatanalyse
exl-id: 7f5529f6-eee7-4bb9-9894-b47ca6c4e9be
source-git-commit: aa4550d7012f76571f7623428d3d4ee08f728f64
workflow-type: tm+mt
source-wordcount: '1930'
ht-degree: 0%

---

# Veelgestelde vragen

## Hoe kan ik CDA gebruiken om te zien hoe mensen zich van één apparatentype aan een ander bewegen?

U kunt een [!UICONTROL Flow] visualisatie met de dimensie Type mobiel apparaat.

1. Meld u aan bij Adobe Analytics en maak een nieuw leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de afmeting &#39;Mobiel apparaattype&#39; naar de middelste locatie met de naam &#39;Dimension of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

## Kan ik zien hoe mensen schakelen tussen verschillende gebruikerservaringen (bijvoorbeeld desktopbrowser versus mobiele browser versus mobiele app)?

In het bovenstaande voorbeeld voor Type mobiele apparaat kunt u zien hoe mensen schakelen tussen typen mobiele apparaten en apparaattypen. U kunt er echter geen onderscheid mee maken tussen desktopbrowsers en mobiele browsers. Als u dit inzicht wilt, kunt u een aangepaste variabele maken (zoals een proxy of eVar) die registreert of de ervaring is opgedaan in een desktopbrowser, mobiele browser of mobiele app. U kunt dan een Stroomdiagram zoals hierboven beschreven tot stand brengen, gebruikend de douanevariabele in plaats van de Mobiele dimensie van het Type van Apparaat. Deze methode biedt een iets andere weergave van gedrag tussen apparaten.

## Hoe ver gaat de CDA bezoekers verstikken?

De cross-device stitching van CDA vindt plaats in twee gelijktijdige processen.

* Het eerste proces wordt &quot;live stitching&quot; genoemd, dat optreedt als de gegevensstromen naar Adobe Analytics. Tijdens het live stitching doet CDA het best het kan om de gegevens op persoonniveau te herformuleren. Als de persoon echter onbekend is op het tijdstip van live stitching, valt de CDA terug naar de bezoekersidentiteitskaart om de persoon te vertegenwoordigen.

* Het tweede proces wordt &#39;replay&#39; genoemd. Tijdens replay, gaat CDA achterwaarts in tijd en herstelt historische gegevens, waar mogelijk, binnen een gespecificeerd terugkijkvenster. Dit terugkijkvenster is of 1 dag of 7 dagen, afhankelijk van hoe u CDA vroeg om worden gevormd. Tijdens het afspelen probeert CDA hits opnieuw te verklaren waar de persoon voordien onbekend was.

* **Als u een apparaatgrafiek gebruikt**, houdt Adobe apparatenafbeeldingen in de Grafiek Co-op en Privé Grafiek ongeveer 6 maanden. Een ECID die langer dan zes maanden geen activiteit heeft, wordt uit de grafiek verwijderd. Gegevens die al in de CDA zijn vermeld, worden niet beïnvloed, maar latere treffers voor die ECID worden als een nieuwe persoon behandeld.

## Hoe verwerkt CDA treffers met tijdstempels?

Adobe behandelt treffers met een tijdstempel alsof deze op het tijdstip van de tijdstempel zijn ontvangen, en niet wanneer Adobe de treffer heeft ontvangen. Tijdgestempelde treffers ouder dan 1 maand worden nooit vastgezet omdat ze buiten het bereik liggen dat Adobe gebruikt om te stitching.

## Hoe vergelijk CDA met aangepaste bezoeker-id&#39;s?

Het gebruik van een aangepaste bezoeker-id is een oudere methode om [gebruikers verbinden over apparaten](/help/implement/js/xdevice-visid/xdevice-connecting.md). Met een aangepaste bezoeker-id gebruikt u de opdracht [`visitorID`](/help/implement/vars/config-vars/visitorid.md) variabele om expliciet de id in te stellen die voor bezoekerslogica wordt gebruikt. De `visitorID` variabele heeft voorrang op op cookies gebaseerde id&#39;s die aanwezig zijn.

Aangepaste bezoeker-id&#39;s hebben verschillende bijwerkingen die CDA overneemt of minimaliseert. De aangepaste ID-methode van de bezoeker heeft bijvoorbeeld geen [replay](replay.md) mogelijkheden. Als een gebruiker tijdens een bezoek voor authentiek verklaart, associeert het eerste deel van het bezoek met een verschillende bezoekersidentiteitskaart dan het laatste deel van het bezoek. De afzonderlijke bezoeker-id&#39;s leiden tot een bezoek en een inflatie van de bezoeker. CDA herstelt historische gegevens zodat ongeoorloofde treffers bij de juiste persoon horen.

## Kan ik een upgrade uitvoeren van Aangepaste bezoeker-id naar CDA?

Klanten die al een aangepaste bezoeker-id gebruiken, kunnen een upgrade uitvoeren naar CDA zonder wijzigingen in de implementatie. De `visitorID` variable wordt nog gebruikt in de bron rapportreeks. De CDA negeert echter de `visitorID` variabele in de virtuele rapportreeks als een gebruiker voor authentiek verklaart.

## Hoe behandelt de apparatengrafiek gedeelde apparaten?

In sommige situaties is het mogelijk dat meerdere personen zich aanmelden bij hetzelfde apparaat. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

* **Als u een apparaatgrafiek gebruikt** De mogelijkheid om gedeelde apparaten af te handelen, is beperkt. De apparaatgrafiek gebruikt een algoritme om de eigendom van een &quot;cluster&quot;te bepalen, en kan elke keer veranderen dat de cluster wordt gepubliceerd. Gebruikers van het gedeelde apparaat zijn afhankelijk van de cluster waartoe zij behoren.
* **Als u op het veld gebaseerde stitching gebruikt**, vervangt de eigenschap of de eVar die u kiest om aangemelde gebruikers te helpen identificeren andere herkenningstekens. Gedeelde apparaten worden beschouwd als afzonderlijke personen, zelfs als ze van hetzelfde apparaat afkomstig zijn.

## Hoe behandelt CDA situaties waarin één enkele persoon VEEL apparaten/ECIDs heeft?

In sommige situaties kan een individuele gebruiker een groot aantal ECID&#39;s koppelen. Dit kan voorkomen als de individu veel browsers of apps gebruikt, en kan worden verergerd als zij vaak koekjes ontruimen of de privé browser of incognito het doorbladeren wijze gebruiken.

* **Als u een apparaatgrafiek gebruikt**, beperkt CDA het aantal ECID&#39;s dat aan een bepaalde gebruikers-id is gekoppeld tot 50. Als een gebruikers-id aan te veel ECID&#39;s is gekoppeld, wordt in de apparaatgrafiek aangenomen dat de gebruikers-id ongeldig is en wordt de cluster die aan die gebruikers-id is gekoppeld, verwijderd. De gebruikersnaam wordt vervolgens toegevoegd aan een lijst van gewezen personen om te voorkomen dat deze in de toekomst aan clusters wordt toegevoegd. Het resultaat van de rapportage is dat de gebruikers-id niet op alle apparaten is aangesloten.
* **Als u op het veld gebaseerde stitching gebruikt**, is het aantal apparaten irrelevant ten gunste van de prop/eVar die u kiest om aangemelde gebruikers te helpen identificeren. Eén gebruiker kan tot elk aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van CDA om apparaten te verstevigen.

## Wat is het verschil tussen de norm Mensen in CDA en de norm van de Unieke Bezoekers buiten CDA?

Beide [Mensen](/help/components/metrics/people.md) en [Unieke bezoekers](/help/components/metrics/unique-visitors.md) meetgegevens hebben tot doel verschillende bezoekers ( personen ) te tellen . Houd er echter rekening mee dat twee verschillende apparaten bij dezelfde persoon kunnen horen. CDA wijst de twee apparaten toe aan dezelfde persoon, terwijl de twee apparaten worden geregistreerd als twee afzonderlijke &#39;Unieke bezoekers&#39; buiten CDA.

## Wat is het verschil tussen de &quot;Unieke Apparaten&quot;-norm in CDA en de &quot;Unieke Bezoekers&quot;-norm buiten CDA?

Deze twee metriek zijn ruwweg gelijkwaardig aan elkaar. De verschillen tussen de twee metriek komen voor wanneer:

* Een gedeeld apparaat wordt toegewezen aan meerdere personen. In dit scenario wordt 1 unieke bezoeker geteld, terwijl meerdere unieke apparaten worden geteld.
* Een apparaat heeft zowel niet-vastgezet als vastgezet verkeer van de zelfde bezoeker. Bijvoorbeeld, produceerde browser geïdentificeerde gestippeld verkeer + historisch anonieme verkeer dat niet werd vastgemaakt. In dit geval wordt 1 unieke bezoeker geteld, terwijl 2 unieke apparaten worden geteld.

Zie [Unieke apparaten](/help/components/metrics/unique-devices.md) voor meer voorbeelden en details over hoe het werkt.

## Kan ik CDA-meetgegevens opnemen met behulp van de 2.0-API?

Ja. Analysis Workspace gebruikt de 2.0 API om gegevens van Adobe servers aan te vragen, en u kunt API vraag bekijken Adobe gebruikt om uw eigen rapporten te maken:

1. Wanneer u bent aangemeld bij Analysis Workspace, gaat u naar [!UICONTROL Help] > [!UICONTROL Enable debugger].
2. Klik op het pictogram voor foutopsporing in het gewenste deelvenster en selecteer de gewenste visualisatie en tijd voor de aanvraag.
3. Zoek de JSON-aanvraag die u kunt gebruiken in uw API-aanroep naar Adobe.

## Met behulp van Cross-Device Analytics kunnen unieke bezoekers aan elkaar worden gekoppeld. Kan de Commissie bezoeken aan elkaar hechten?

Ja. Als een individu hits verzendt van twee aparte apparaten binnen de time-out voor het bezoek van uw virtuele rapportsuite (standaard ingesteld op 30 minuten), worden deze aan hetzelfde bezoek gekoppeld.

## Wat is de ultieme bezoekersidentiteitskaart die CDA gebruikt? Kan ik het uit Adobe Analytics exporteren?

* **Als u een apparaatgrafiek gebruikt**, is een aangepaste id op basis van hun cluster de primaire id.
* **Als u op het veld gebaseerde stitching gebruikt**, is een aangepaste id die is gebaseerd op de eigenschap prop/eVar die u hebt gekozen, de primaire id.

Beide herkenningstekens worden berekend door Adobe op het tijdstip dat het rapport in werking wordt gesteld, ook gekend als [Verwerking bij rapporttijd](../vrs/vrs-report-time-processing.md). De aard van de verwerking van het Rapport-tijd betekent dat het niet compatibel is met Data Warehouse, gegevensvoer, of andere de uitvoereigenschappen die Adobe aanbiedt.

## Hoe kan ik van de apparatengrafiek naar op gebied-gebaseerde het stitching bewegen, of vice versa?

Via de klantenservice kan worden gevraagd om van apparaatgrafiek naar op het veld gebaseerde stitching of omgekeerd. Een dergelijke omschakeling kan echter een paar weken of langer duren en *historische gegevens van de vorige methode gaan verloren.*

## Hoe hanteert Adobe unieke limieten voor een proxy of eVar die wordt gebruikt bij veldoverstikken?

CDA haalt de elementen van de identificatievariabele dimensies voordat deze zijn geoptimaliseerd voor rapportage. U hoeft zich geen zorgen te maken over unieke limieten in het kader van CDA. Nochtans, als u het gebruiken van die steun of eVar in een project van de Werkruimte probeerde, kunt u nog zien [(Laag verkeer)](/help/technotes/low-traffic.md) dimensie-item.

## Hoeveel van mijn bedrijfsuitrustingen van het rapport kunnen voor CDA worden toegelaten?

Met ingang van 1 mei 2022, zal om het even welke nieuwe implementatie van CDA tot een maximum van drie rapportreeks IDs (RSIDs) per klant worden beperkt. CDA voegt geen rapportsuites samen. Elk rapportenpakket dat is ingeschakeld voor CDA, moet apparaatonafhankelijk zijn (met gegevens van meerdere oppervlakken, zoals het bureaublad, het mobiele web, de mobiele app enz.).

## Als mijn organisatie-id meerdere bedrijven in verschillende regio&#39;s heeft, kan ik dan CDA voor al deze bedrijven inschakelen?

Nee. Voor dezelfde organisatie-id kan voor slechts één regio CDA ingeschakeld zijn.

## Wat zijn de voor- en nadelen van een 7-daagse replay in plaats van een 1-daagse replay?

Het voordeel van het 7 dagen terugspeelvenster is dat CDA verder in tijd kan terugkeren om te proberen om eerder anonieme gebeurtenissen met één of andere persoon te associëren die later binnen die 7 dagen het programma opende. De nadelen van het 7-dagen terugkijkvenster zijn 1) replay slechts één keer per week, en 2) de meest recente 7 dagen zijn onderhevig aan verandering.

De voordelen van het gebruiken van het 1-dag replay terugkijkvenster zijn 1) replay looppas elke dag en 2) slechts gisteren is onderhevig aan verandering. Het nadeel van het venster van de 1-dagraadpleging is dat CDA slechts één dag kan terugkeren om te proberen om eerder anonieme gebeurtenissen met een persoon te associëren die gisteren het programma opende.

## Wat gebeurt er met de opgeslagen gegevens in mijn virtuele CDA-rapportensuite(s) als mijn bedrijf besluit de kwaliteit van Analytics Ultimate te verlagen?

Als een klant van Ultimate downloadt, hebben ze geen toegang meer tot opgeslagen gegevens. Alle eerder opgeslagen gegevens worden verwijderd. Dit betekent dat de virtuele CDA-rapportensuites nu geen cross-device stitching weerspiegelen. De gegevens zullen gelijkaardig aan de originele unstitched rapportreeks kijken.

## Waarom is het totale aantal treffers verschillend tussen mijn bronrapportreeks en CDA virtuele rapportenreeks?

CDA gebruikt een complexe parallelle verwerkingspijpleiding, met veelvoudige afhankelijke componenten. Een gegevensmismatch van ongeveer 1% voor het totale aantal treffers tussen de originele rapportreeks en de virtuele CDA rapportenreeks wordt verwacht.

## Waarom wordt de metrische waarde &#39;Identified People&#39; opgevoerd?

Het getal van de metrische waarde &#39;Identified People&#39; kan iets hoger zijn als de waarde van de id prop/eVar in een waarde [hash-botsing](/help/implement/validate/hash-collisions.md).

Voor op veld gebaseerde stitching is de aangepaste id-variabele hoofdlettergevoelig. Het aantal van metrische waarden &quot;Identified People&quot;kan beduidend hoger zijn als de herkenningswaarden niet geval aanpassen. Als `bob` en `Bob` worden verzonden en naar verwachting dezelfde persoon zijn, interpreteert CDA deze twee waarden als verschillend.

## Waarom zie ik bij het bekijken van de id prop/eVar niet-nul waarden voor de &#39;Unidentified People&#39;-meting?

Deze situatie komt gewoonlijk voor wanneer een bezoeker zowel voor authentiek verklaarde als niet voor authentiek verklaarde klusjes in het rapporteringsvenster produceert. De bezoeker behoort tot zowel &#39;Niet-geïdentificeerd&#39; als &#39;Geïdentificeerd&#39; in het dialoogvenster [Geïdentificeerde staat](/help/components/dimensions/identified-state.md) dimensie, die een attributie van niet-geïdentificeerde treffers aan een herkenningsteken veroorzaakt. Dit scenario kan na [Opnieuw afspelen](replay.md) wordt uitgevoerd, afhankelijk van de herhalingsfrequentie en de successnelheid.