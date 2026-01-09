---
title: Veelgestelde vragen over cross-device analyse
description: Veelgestelde vragen over apparaatanalyse
exl-id: 7f5529f6-eee7-4bb9-9894-b47ca6c4e9be
feature: CDA
role: Admin
source-git-commit: f75a1f6d9f08f422595c24760796abf0f8332ddb
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 0%

---


# Veelgestelde vragen

{{available-existing-customers}}

+++ Hoe kan ik CDA gebruiken om te zien hoe mensen zich van één apparatentype aan een ander bewegen?

U kunt een [!UICONTROL Flow] -visualisatie gebruiken met de dimensie Mobiel apparaattype.

1. Meld u aan bij Adobe Analytics en maak een nieuw leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de dimensie &#39;Mobiel apparaattype&#39; naar de middelste locatie met de naam &#39;Dimension of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

+++

+++ Kan ik zien hoe mensen schakelen tussen verschillende gebruikerservaringen (bijvoorbeeld desktopbrowser versus mobiele browser versus mobiele app)?

In het bovenstaande voorbeeld voor Type mobiele apparaat kunt u zien hoe mensen schakelen tussen typen mobiele apparaten en apparaattypen. U kunt er echter geen onderscheid mee maken tussen desktopbrowsers en mobiele browsers. Als u deze insight wilt gebruiken, kunt u een aangepaste variabele maken (zoals een proxy of eVar) die registreert of de ervaring is opgedaan in een desktopbrowser, mobiele browser of mobiele app. U kunt dan een Stroomdiagram zoals hierboven beschreven tot stand brengen, gebruikend de douanevariabele in plaats van de Mobiele dimensie van het Type van Apparaat. Deze methode biedt een iets andere weergave van gedrag tussen apparaten.

+++

+++ Hoe ver gaat de CDA bezoekers verstikken?

De cross-device stitching van CDA vindt plaats in twee gelijktijdige processen.

* Het eerste proces wordt &quot;live stitching&quot; genoemd, dat optreedt als de gegevensstromen naar Adobe Analytics. Tijdens het live stitching doet CDA het best het kan om de gegevens op persoonniveau te herformuleren. Als de persoon echter onbekend is op het tijdstip van live stitching, valt de CDA terug naar de bezoekersidentiteitskaart om de persoon te vertegenwoordigen.

* Het tweede proces wordt &#39;replay&#39; genoemd. Tijdens replay, gaat CDA achterwaarts in tijd en herstelt historische gegevens, waar mogelijk, binnen een gespecificeerd terugkijkvenster. Dit terugkijkvenster is of 1 dag of 7 dagen, afhankelijk van hoe u CDA vroeg om worden gevormd. Tijdens het afspelen probeert CDA hits opnieuw te verklaren waar de persoon voordien onbekend was.


+++

+++ Hoe verwerkt CDA treffers met tijdstempels?

Adobe behandelt treffers met een tijdstempel alsof ze zijn ontvangen op het tijdstip van de tijdstempel, niet op het moment dat Adobe de hit heeft ontvangen. Tijdstempels ouder dan 1 maand worden nooit vastgezet omdat ze zich buiten het bereik bevinden dat Adobe gebruikt voor stitching.

+++

+++ Hoe vergelijk CDA met aangepaste bezoeker-id&#39;s?

Het gebruiken van een identiteitskaart van de douanebezoeker is een erfenismethode om [ gebruikers over apparaten ](/help/implement/js/xdevice-visid/xdevice-connecting.md) te verbinden. Met een aangepaste bezoeker-id gebruikt u de variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) om expliciet de id in te stellen die wordt gebruikt voor de logica van de bezoeker. De variabele `visitorID` negeert op cookies gebaseerde id&#39;s die aanwezig zijn.

Aangepaste bezoeker-id&#39;s hebben verschillende bijwerkingen die CDA overneemt of minimaliseert. Bijvoorbeeld, heeft de methodologie van identiteitskaart van de douanebezoeker geen [ replay ](replay.md) mogelijkheden. Als een gebruiker tijdens een bezoek voor authentiek verklaart, associeert het eerste deel van het bezoek met een verschillende bezoekersidentiteitskaart dan het laatste deel van het bezoek. De afzonderlijke bezoeker-id&#39;s resulteren in een bezoek en een inflatie van de bezoeker. CDA herstelt historische gegevens zodat ongeoorloofde treffers bij de juiste persoon horen.

+++

+++ Kan ik een upgrade uitvoeren van Aangepaste bezoeker-id naar CDA?

Klanten die al een aangepaste bezoeker-id gebruiken, kunnen een upgrade uitvoeren naar CDA zonder wijzigingen in de implementatie. De variabele `visitorID` wordt nog steeds gebruikt in de bronrapportsuite. Nochtans, negeert CDA de `visitorID` variabele in de virtuele rapportreeks als een gebruiker voor authentiek verklaart.

+++



+++ Hoe behandelt CDA situaties waarin één enkele persoon VEEL apparaten/ECIDs heeft?

In sommige situaties kan een individuele gebruiker een groot aantal ECID&#39;s koppelen. Dit kan voorkomen als de individu veel browsers of apps gebruikt, en kan worden verergerd als zij vaak koekjes ontruimen of de privé browser of incognito het doorbladeren wijze gebruiken.

* **als het gebruiken van op gebied-gebaseerde het stitching**, is het aantal apparaten irrelevant ten gunste van prop/eVar u verkiest helpen het programma geopende gebruikers identificeren. Eén gebruiker kan tot elk aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van CDA om apparaten te verstevigen.

+++

+++ Wat is het verschil tussen de norm Mensen in CDA en de norm van de Unieke Bezoekers buiten CDA?

Zowel [ Mensen ](/help/components/metrics/people.md) als [ Unieke Bezoekers ](/help/components/metrics/unique-visitors.md) metriek richten zich op het tellen van verschillende bezoekers (individuen). Houd er echter rekening mee dat twee verschillende apparaten bij dezelfde persoon kunnen horen. CDA wijst de twee apparaten toe aan dezelfde persoon, terwijl de twee apparaten worden geregistreerd als twee afzonderlijke &#39;Unieke bezoekers&#39; buiten CDA.

+++

+++ Wat is het verschil tussen de &quot;Unieke Apparaten&quot;-norm in CDA en de &quot;Unieke Bezoekers&quot;-norm buiten CDA?

Deze twee metriek zijn ruwweg gelijkwaardig aan elkaar. De verschillen tussen de twee metriek komen voor wanneer:

* Een gedeeld apparaat wordt toegewezen aan meerdere personen. In dit scenario wordt 1 unieke bezoeker geteld, terwijl meerdere unieke apparaten worden geteld.
* Een apparaat heeft zowel niet-vastgezet als vastgezet verkeer van de zelfde bezoeker. Bijvoorbeeld, produceerde browser geïdentificeerde gestippeld verkeer + historisch anonieme verkeer dat niet werd vastgemaakt. In dit geval wordt 1 unieke bezoeker geteld, terwijl 2 unieke apparaten worden geteld.

Zie [ Unieke Apparaten ](/help/components/metrics/unique-devices.md) voor meer voorbeelden en details rond hoe het werkt.

+++

+++ Kan ik CDA-gegevens opnemen met de Adobe Analytics 2.0-API?

Ja. Analysis Workspace gebruikt de 2.0-API om gegevens aan te vragen van Adobe-servers en u kunt API-aanroepen weergeven die Adobe gebruikt om uw eigen rapporten op te stellen:

1. Ga bij het aanmelden bij Analysis Workspace naar [!UICONTROL Help] > [!UICONTROL Enable debugger] .
2. Klik op het pictogram voor foutopsporing in het gewenste deelvenster en selecteer de gewenste visualisatie en tijd voor de aanvraag.
3. Zoek de JSON-aanvraag, die u kunt gebruiken in uw API-aanroep naar Adobe.

+++

+++ Met behulp van Cross-Device Analytics kunnen unieke bezoekers aan elkaar worden gekoppeld. Kan de Commissie bezoeken aan elkaar hechten?

Ja. Als een individu hits verzendt van twee aparte apparaten binnen de time-out voor het bezoek van uw virtuele rapportsuite (standaard ingesteld op 30 minuten), worden deze aan hetzelfde bezoek gekoppeld.

+++

+++ Wat is de ultieme bezoekersidentiteitskaart die CDA gebruikt? Kan ik het uit Adobe Analytics exporteren?

* **als het gebruiken van een apparatengrafiek**, een douaneidentiteitskaart die op hun cluster wordt gebaseerd is het primaire herkenningsteken.
* **als het gebruiken van op gebied-gebaseerde het stitching**, een douanidentiteitskaart die op pro/eVar wordt gebaseerd u kiest is het primaire herkenningsteken.

Beide herkenningstekens worden berekend door Adobe op het tijdstip dat het rapport in werking wordt gesteld, ook gekend als [ rapport-tijd verwerking ](../vrs/vrs-report-time-processing.md). De aard van de verwerking van de rapporttijd betekent dat het niet compatibel is met Data Warehouse, gegevensvoer, of andere de uitvoereigenschappen die Adobe aanbiedt.

+++

+++ Hoe kan ik van de apparatengrafiek naar op gebied-gebaseerde het stitching bewegen, of vice versa?

Via de klantenservice kan worden gevraagd om van apparaatgrafiek naar op het veld gebaseerde stitching te schakelen of andersom. Nochtans, kan het maken van zulk een schakelaar een paar weken of meer nemen om te voltooien en *historische gestaafde gegevens van de vorige methode wordt verloren.*

+++

+++ Hoe gaat Adobe om met unieke limieten voor een prop of eVar die in veldomstandigheden worden gebruikt?

CDA haalt de elementen van de identificatievariabele dimensies voordat deze zijn geoptimaliseerd voor rapportage. U hoeft zich geen zorgen te maken over unieke limieten in het kader van CDA. Nochtans, als u probeerde gebruikend die steun of eVar in een project van Workspace, kunt u nog [ (Laag-verkeer) ](/help/technotes/low-traffic.md) afmetingspunt zien.

+++

+++ Hoeveel van mijn bedrijfsuitrustingen van het rapport kunnen voor CDA worden toegelaten?

Met ingang van 1 mei 2022, zal om het even welke nieuwe implementatie van CDA tot een maximum van drie rapportreeks IDs (RSIDs) per klant worden beperkt. CDA voegt geen rapportsuites samen. Elk rapportenpakket dat is ingeschakeld voor CDA, moet apparaatonafhankelijk zijn (met gegevens van meerdere oppervlakken, zoals het bureaublad, het mobiele web, de mobiele app enz.).

+++

+++ Als mijn organisatie-id meerdere bedrijven in verschillende regio&#39;s heeft, kan ik dan CDA voor al deze bedrijven inschakelen?

Nee. Voor dezelfde organisatie-id kan voor slechts één regio CDA ingeschakeld zijn.

+++

+++ Wat zijn de voor- en nadelen van een 7-daagse replay in plaats van een 1-daagse replay?

Het voordeel van het 7 dagen terugspeelvenster is dat CDA verder in tijd kan terugkeren om eerder anonieme gebeurtenissen met één of andere persoon te associëren die later binnen die 7 dagen het programma opende. De nadelen van het 7-dagen terugkijkvenster zijn 1) replay slechts één keer per week, en 2) de meest recente 7 dagen zijn onderhevig aan verandering.

De voordelen van het gebruiken van het 1-dag replay terugkijkvenster zijn 1) replay looppas elke dag en 2) slechts gisteren is onderhevig aan verandering. Het nadeel van het venster van de 1-dagraadpleging is dat CDA slechts één dag kan terugkeren om te proberen om eerder anonieme gebeurtenissen met een persoon te associëren die gisteren het programma opende.

+++

+++ Wat gebeurt er met de opgeslagen gegevens in mijn virtuele CDA-rapportensuite(s) als mijn bedrijf besluit de kwaliteit van Analytics Ultimate te verlagen?

Als een klant de status van Ultimate afneemt, heeft hij of zij geen toegang meer tot de gegevens in de bijlage. Alle eerder opgeslagen gegevens worden verwijderd. Dit betekent dat de virtuele CDA-rapportensuites nu geen cross-device stitching weerspiegelen. De gegevens zullen gelijkaardig aan de originele unstitched rapportreeks kijken.

+++

+++ Waarom is het totale aantal treffers verschillend tussen mijn bronrapportreeks en CDA virtuele rapportenreeks?

CDA gebruikt een complexe parallelle verwerkingspijpleiding, met veelvoudige afhankelijke componenten. Een gegevensmismatch van ongeveer 1% voor het totale aantal treffers tussen de originele rapportreeks en de virtuele CDA rapportenreeks wordt verwacht.

+++

+++ Waarom wordt de metrische waarde &#39;Identified People&#39; opgevoerd?

Het aantal van metrisch &quot;Identified Mensen&quot;kan lichtjes hoger zijn als de herkenningstekenprop/de waarde van eVar in de botsing van de a [ hash ](/help/implement/validate/hash-collisions.md) loopt.

Voor op veld gebaseerde stitching is de aangepaste id-variabele hoofdlettergevoelig. Het aantal van metrische waarden &quot;Identified People&quot;kan beduidend hoger zijn als de herkenningswaarden niet geval aanpassen. Als `bob` en `Bob` bijvoorbeeld worden verzonden en dezelfde persoon worden verwacht, interpreteert CDA deze twee waarden als afzonderlijk.

+++

+++ Waarom zie ik bij het bekijken van de id prop/eVar niet-nulwaarden voor de &#39;Unidentified People&#39;-meting?

Deze situatie komt gewoonlijk voor wanneer een bezoeker zowel voor authentiek verklaarde als niet voor authentiek verklaarde klusjes in het rapporteringsvenster produceert. De bezoeker behoort tot zowel &quot;Unidentified&quot;als &quot;Identified&quot;in de [ Verkende dimensie van de Staat ](/help/components/dimensions/identified-state.md), veroorzakend een attributie van niet geïdentificeerde hits aan een herkenningsteken. Dit scenario kan veranderen na [ Replay ](replay.md) looppas, afhankelijk van replay frequentie en succestarief.

+++
