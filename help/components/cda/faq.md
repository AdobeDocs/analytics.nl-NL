---
title: Veelgestelde vragen over Cross-device Analytics
description: Veelgestelde vragen over apparaatanalyse
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---


# Veelgestelde vragen

## Hoe kan ik CDA gebruiken om te zien hoe mensen zich van één apparatentype aan een ander bewegen?

U kunt een stroomvisualisatie gebruiken met de dimensie Mobiel apparaattype.

1. Meld u aan bij Adobe Analytics en maak een nieuw leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de afmeting &#39;Mobiel apparaattype&#39; naar de middelste locatie met de naam &#39;Dimension of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

## Kan ik zien hoe mensen schakelen tussen verschillende gebruikerservaringen (bijvoorbeeld desktopbrowser versus mobiele browser versus mobiele app)?

Als u het type mobiel apparaat gebruikt, zoals hierboven is geïllustreerd, kunt u zien hoe mensen van het ene type mobiel apparaat naar het andere bewegen. U kunt echter desktopbrowsers onderscheiden van mobiele browsers. Een manier om dit te doen is een eVar te maken die vastlegt of de ervaring is opgedaan in een desktopbrowser, mobiele browser of mobiele app. Maak vervolgens een stroomdiagram zoals hierboven beschreven, waarbij u uw &quot;ervaring&quot;-eVar gebruikt in plaats van de dimensie Mobiel apparaattype. Dit geeft een iets andere weergave op gedrag tussen apparaten.

## Hoe ver gaat de CDA bezoekers verstikken?

Adobe bewaart de gegevens van het apparaat stitching ongeveer 30 dagen. Als een hulpmiddel aanvankelijk niet wordt geïdentificeerd maar later binnen 30 dagen wordt geïdentificeerd, gaat CDA terug en verklaart dat hulpmiddel dat tot 30 dagen in het verleden aan geïdentificeerde persoon toebehoort. Als een deel van het niet-geïdentificeerde gedrag van een gebruiker buiten het terugkijkvenster van 30 dagen valt, wordt dat gedeelte van de reis van de gebruiker niet vastgemaakt.

* **Als u een apparaatgrafiek** gebruikt, worden apparaattoewijzingen door Adobe ongeveer 6 maanden bewaard in de coop-grafiek en de privégrafiek. Een ECID die langer dan zes maanden geen activiteit heeft, wordt uit de grafiek verwijderd. Gegevens die al in de CDA zijn vermeld, worden niet beïnvloed, maar latere treffers voor die ECID worden als een nieuwe persoon behandeld.

## Hoe verwerkt CDA treffers met tijdstempels?

Adobe behandelt treffers met een tijdstempel alsof deze op het tijdstip van de tijdstempel zijn ontvangen, en niet wanneer Adobe de treffer heeft ontvangen. Tijdgestempelde treffers ouder dan 1 maand worden nooit vastgezet omdat ze buiten het bereik liggen dat Adobe gebruikt om te stitching.

## Hoe vergelijk CDA met aangepaste bezoeker-id&#39;s?

Het gebruik van een aangepaste bezoeker-id is een oudere methode om gebruikers op verschillende apparaten ](/help/implement/js/xdevice-visid/xdevice-connecting.md) aan te sluiten. [ Met een aangepaste bezoeker-id gebruikt u de variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) om expliciet de id in te stellen die voor bezoekerslogica wordt gebruikt. De variabele `visitorID` negeert op cookies gebaseerde id&#39;s die aanwezig zijn.

Aangepaste bezoeker-id&#39;s hebben verschillende bijwerkingen die CDA overneemt of minimaliseert. De aangepaste ID-methodologie van de bezoeker heeft bijvoorbeeld geen [replay](replay.md) mogelijkheden. Als een gebruiker tijdens een bezoek voor authentiek verklaart, associeert het eerste deel van het bezoek met een verschillende bezoekersidentiteitskaart dan het laatste deel van het bezoek. De afzonderlijke bezoeker-id&#39;s leiden tot een bezoek en een inflatie van de bezoeker. CDA herstelt historische gegevens zodat ongeoorloofde treffers bij de juiste persoon horen.

## Kan ik een upgrade uitvoeren van Aangepaste bezoeker-id naar CDA?

Klanten die al een aangepaste bezoeker-id gebruiken, kunnen een upgrade uitvoeren naar CDA zonder wijzigingen in de implementatie. De `visitorID` variabele wordt nog gebruikt in de bron rapportreeks. Nochtans, negeert CDA de `visitorID` variabele in de virtuele rapportreeks als een gebruiker voor authentiek verklaart.

## Hoe behandelt de apparatengrafiek gedeelde apparaten?

In sommige situaties is het mogelijk dat meerdere personen zich aanmelden bij hetzelfde apparaat. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet.

* **Als u een apparaatgrafiek** gebruikt, is de mogelijkheid om gedeelde apparaten af te handelen beperkt. De apparaatgrafiek gebruikt een algoritme om de eigendom van een &quot;cluster&quot;te bepalen, en kan elke keer veranderen dat de cluster wordt gepubliceerd. Gebruikers van het gedeelde apparaat zijn afhankelijk van de cluster waartoe zij behoren.
* **Als u op velden gebaseerde stitching** gebruikt, worden andere id&#39;s overschreven door de proxy of de eVar die u kiest om aangemelde gebruikers te helpen identificeren. Gedeelde apparaten worden beschouwd als afzonderlijke personen, zelfs als ze van hetzelfde apparaat afkomstig zijn.

## Hoe behandelt CDA situaties waarin één enkele persoon VEEL apparaten/ECIDs heeft?

In sommige situaties kan een individuele gebruiker een groot aantal ECID&#39;s koppelen. Dit kan voorkomen als de individu veel browsers of apps gebruikt, en kan worden verergerd als zij vaak koekjes ontruimen of de privé browser of incognito het doorbladeren wijze gebruiken.

* **Als u een apparaatgrafiek** gebruikt, wordt in CDA het aantal ECID&#39;s afgekapt dat aan een bepaalde gebruikers-id is gekoppeld tot 50. Als een gebruikers-id aan te veel ECID&#39;s is gekoppeld, wordt in de apparaatgrafiek aangenomen dat de gebruikers-id ongeldig is en wordt de cluster die aan die gebruikers-id is gekoppeld, verwijderd. De gebruikersnaam wordt vervolgens toegevoegd aan een lijst van afgewezen personen om te voorkomen dat deze in de toekomst aan clusters wordt toegevoegd. Het resultaat van de rapportage is dat de gebruikers-id niet op alle apparaten is aangesloten.
* **Als u op het veld gebaseerde stitching** gebruikt, is het aantal apparaten irrelevant ten gunste van de prop/eVar die u kiest om aangemelde gebruikers te helpen identificeren. Eén gebruiker kan tot elk aantal apparaten behoren zonder dat dit invloed heeft op de mogelijkheid van CDA om apparaten te verstevigen.

## Wat is het verschil tussen de norm Mensen in CDA en de norm van de Unieke Bezoekers buiten CDA?

De [People](/help/components/metrics/people.md) metrisch is gelijkaardig aan [Unieke bezoekers](/help/components/metrics/unique-visitors.md) metrisch in die zin dat het over het aantal unieke individuen rapporteert. Wanneer u echter Apparaatanalyse gebruikt, worden unieke bezoekers gecombineerd wanneer ze anders worden opgenomen als twee afzonderlijke unieke bezoekers buiten CDA. De metrische waarde &#39;Mensen&#39; vervangt de metrische waarde &#39;Unieke bezoekers&#39; wanneer Apparaatanalyse is ingeschakeld. Er is een nieuwe metrische waarde beschikbaar, [Unieke apparaten](/help/components/metrics/unique-devices.md), die ongeveer gelijk is aan Unieke bezoekers buiten de functie voor apparaatanalyse.

## Wat is het verschil tussen de &quot;Unieke Apparaten&quot;-norm in CDA en de &quot;Unieke Bezoekers&quot;-norm buiten CDA?

Deze twee metriek zijn ruwweg gelijkwaardig aan elkaar.

## Kan ik CDA-meetgegevens opnemen met behulp van de 2.0-API?

Ja. Analysis Workspace gebruikt de 2.0 API om gegevens van Adobe servers aan te vragen, en u kunt API vraag bekijken Adobe gebruikt om uw eigen rapporten te maken:

1. Ga bij het aanmelden bij Analysis Workspace naar [!UICONTROL Help] > [!UICONTROL Enable debugger].
2. Klik op het pictogram voor foutopsporing in het gewenste deelvenster en selecteer de gewenste visualisatie en tijd voor de aanvraag.
3. Zoek de JSON-aanvraag die u kunt gebruiken in uw API-aanroep naar Adobe.

## Met behulp van Cross-Device Analytics kunnen unieke bezoekers aan elkaar worden gekoppeld. Kan de Commissie bezoeken aan elkaar hechten?

Ja. Als een individu hits verzendt van twee aparte apparaten binnen de time-out voor het bezoek van uw virtuele rapportsuite (standaard ingesteld op 30 minuten), worden deze aan hetzelfde bezoek gekoppeld.

## Wat is de ultieme bezoekersidentiteitskaart die CDA gebruikt? Kan ik het uit Adobe Analytics exporteren?

* **Als u een apparaatgrafiek** gebruikt, is een aangepaste id op basis van de cluster de primaire id.
* **Als u op velden gebaseerde stitching** gebruikt, is een aangepaste id op basis van de gekozen prop/eVar de primaire id.

Beide herkenningstekens worden berekend door Adobe op het tijdstip dat het rapport in werking wordt gesteld, ook gekend als [rapport-tijd verwerking](../vrs/vrs-report-time-processing.md). De aard van de verwerking van het Rapport-tijd betekent dat het niet compatibel is met Data Warehouse, gegevensvoer, of andere de uitvoereigenschappen die Adobe aanbiedt.

## Hoe kan ik van de apparatengrafiek naar op gebied-gebaseerde het stitching bewegen, of vice versa?

Neem contact op met de accountmanager van uw organisatie als u wilt overschakelen naar andere methoden voor identificatie van CDA. De accountmanager kan uw rapportsuite voorzien van de gewenste methode om personen te identificeren. *Historische gegevens van de vorige methode gaan verloren.*

## Hoe hanteert Adobe unieke limieten voor een eVar die wordt gebruikt in stitching op basis van velden?

CDA trekt eVar dimensie-items vóór zij voor rapportering worden geoptimaliseerd. U hoeft zich geen zorgen te maken over unieke limieten in het kader van CDA. Nochtans, als u het gebruiken van die pro/eVar in een project van de Werkruimte probeerde, kunt u [ (Laag-verkeer) ](/help/technotes/low-traffic.md) afmetingspunt nog zien.
