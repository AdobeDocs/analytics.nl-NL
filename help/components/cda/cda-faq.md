---
title: Veelgestelde vragen over cross-device analyse
description: Veelgestelde vragen over apparaatanalyse
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Veelgestelde vragen

>[!NOTE] De documentatie van de Analyse van verschillende apparaten kan worden gewijzigd aangezien de eigenschap verder wordt ontwikkeld. Controleer regelmatig of er updates zijn.

**Hoe kan ik CDA gebruiken om te zien hoe mensen zich van één apparatentype aan een ander bewegen?**

U kunt een stroomvisualisatie gebruiken met de dimensie Mobiel apparaattype.

1. Meld u aan bij Adobe Analytics en maak een nieuw leeg Workspace-project.
2. Klik op het tabblad Visualisatie aan de linkerkant en sleep een stroomvisualisatie naar het canvas aan de rechterkant.
3. Klik op het tabblad Componenten aan de linkerkant en sleep de afmeting &#39;Mobiel apparaattype&#39; naar de middelste locatie met de naam &#39;Afmeting of Item&#39;.
4. Dit stroomrapport is interactief. Klik op een van de waarden om de stromen naar volgende of vorige pagina&#39;s uit te vouwen. Gebruik het met de rechtermuisknop aanklikken menu om kolommen uit of samen te vouwen. Binnen hetzelfde stroomrapport kunnen ook verschillende afmetingen worden gebruikt.

**Kan ik zien hoe mensen schakelen tussen verschillende gebruikerservaringen (bijvoorbeeld desktopbrowser versus mobiele browser versus mobiele app)?**

Als u het type mobiel apparaat gebruikt, zoals hierboven is geïllustreerd, kunt u zien hoe mensen van het ene type mobiel apparaat naar het andere bewegen. U kunt echter desktopbrowsers onderscheiden van mobiele browsers. Dit kunt u onder andere doen door een eVar te maken waarin wordt vastgelegd of de ervaring is opgedaan in een desktopbrowser, mobiele browser of mobiele app. Maak vervolgens een Stroomdiagram zoals hierboven beschreven, met uw &quot;ervaring&quot;-eVar in plaats van de dimensie Mobiel apparaattype. Dit geeft een iets andere weergave van gedrag tussen apparaten.

**Hoe ver gaat de CDA bezoekers verstikken?**

* Adobe bewaart de gegevens van het apparaat stitching ongeveer 30 dagen. Als een apparaat aanvankelijk niet door de grafiek van de Coop of van de Privé grafiek wordt geïdentificeerd, maar later binnen 30 dagen wordt geïdentificeerd, gaat CDA terug en verklaart dat apparaat aan geïdentificeerde persoon tot 30 dagen in het verleden behoort. Als een deel van het niet-geïdentificeerde gedrag van een gebruiker buiten het terugkijkvenster van 30 dagen valt, wordt dat gedeelte van de reis van de gebruiker niet vastgemaakt.
* Adobe bewaart apparatenafbeeldingen in de Grafiek Co-op en PrivéGrafiek ongeveer 6 maanden. Een ECID die langer dan zes maanden geen activiteit heeft, wordt uit de grafiek verwijderd. Gegevens die al in de CDA zijn vermeld, worden niet beïnvloed, maar latere treffers voor die ECID worden als een nieuw individu behandeld.

**Hoe verwerkt CDA treffers met tijdstempels?**

Adobe behandelt treffers met een tijdstempel alsof deze zijn ontvangen op het tijdstip van de tijdstempel, niet op het moment dat Adobe de treffer heeft ontvangen. Tijdgestempelde treffers ouder dan 1 maand kunnen niet worden vastgezet, omdat ze buiten het bereik vallen waarin Adobe gegevens bijhoudt die voor stitching worden gebruikt.

**Hoe vergelijk CDA met aangepaste bezoeker-id&#39;s?**

[De aangepaste bezoeker-id](/help/implement/vars/config-vars/visitorid.md) is een oudere methode om gebruikers op verschillende apparaten [te](/help/implement/js/xdevice-visid/xdevice-connecting.md)verbinden. Met een aangepaste bezoeker-id gebruikt u de `s.visitorID` variabele om expliciet de id in te stellen die wordt gebruikt voor de logica van de bezoeker. De `s.visitorID` variabele negeert op cookies gebaseerde id&#39;s die aanwezig zijn.

Aangepaste bezoeker-id&#39;s hebben verschillende bijwerkingen die CDA overneemt of minimaliseert. De methode voor de aangepaste bezoeker-id heeft bijvoorbeeld geen terugzoekmogelijkheden. Als een gebruiker tijdens een bezoek voor authentiek verklaart, associeert het eerste deel van het bezoek met een verschillende bezoekersidentiteitskaart dan het laatste deel van het bezoek. De afzonderlijke bezoeker-id&#39;s resulteren in een bezoek en een inflatie van de bezoeker. Met het terugkijkvenster van 30 dagen van CDA kan het teruggaan in tijd om vorig gedrag als het behoren tot van de zelfde persoon te herhalen, die unauthenticated cross-device gedrag samen met voor authentiek verklaard cross-device gedrag met nul of minimale inflatie brengt.

**Kan ik een upgrade uitvoeren van Aangepaste bezoeker-id naar CDA?**

Klanten die al een aangepaste bezoeker-id gebruiken, kunnen een upgrade uitvoeren naar CDA. De onderliggende op cookie gebaseerde id&#39;s in de basisrapportsuite worden `s.visitorID` nog steeds genegeerd. Nochtans, binnen de virtuele rapportreeks, negeert CDA `s.visitorID` voor apparaten die door de apparatengrafiek worden geïdentificeerd.

**Hoe behandelt de apparatengrafiek gedeelde apparaten?**

In sommige situaties is het mogelijk dat meerdere personen zich aanmelden bij hetzelfde apparaat. De voorbeelden omvatten een gedeeld apparaat thuis, gedeelde PCs in een bibliotheek, of een kiosk in een detailhandelsafzet. In deze gevallen geeft de id vanuit deze gedeelde apparaten synchroon aan de apparaatgrafiek aan dat meerdere gebruikers zich in de loop der tijd aan dat apparaat koppelen. In de apparaatgrafiek (coop of privégrafiek) wordt de ECID op dat apparaat niet aan een van deze gebruikers gekoppeld. In plaats daarvan koppelt de grafiek ECID aan een &quot;cluster&quot;die alle bijbehorende gebruikers omvat. De grafiek probeert dit cluster zo stabiel mogelijk te houden in plaats van voortdurend de ECID te schakelen tussen clusters in de loop van de tijd. Als gevolg hiervan kan CDA geen onderscheid maken tussen individuele gebruikers op een gedeeld apparaat. Alle gebruikers van het gedeelde apparaat worden beschouwd als één enkele &quot;persoon&quot;binnen CDA.

**Hoe behandelt de apparatengrafiek situaties waarin één enkele persoon VEEL apparaten/ECIDs heeft?**

In sommige situaties kan een individuele gebruiker een groot aantal ECID&#39;s koppelen. Dit kan voorkomen als de individu veel browsers of apps gebruikt, en kan worden verergerd als zij vaak koekjes ontruimen of de privé browser of incognito het doorbladeren wijze gebruiken. In de apparaatgrafiek wordt het aantal ECID&#39;s vastgelegd dat aan een bepaalde gebruikers-id is gekoppeld tot 200. Als een gebruikers-id aan te veel ECID&#39;s is gekoppeld, wordt in de apparaatgrafiek aangenomen dat de gebruikers-id ongeldig is en wordt de cluster die aan die gebruikers-id is gekoppeld, verwijderd. De gebruikersnaam wordt dan op de zwarte lijst weergegeven zodat deze in de toekomst niet opnieuw wordt genummerd. Het resultaat in CDA is dat het gedrag van gebruikers-id niet op verschillende apparaten is aangesloten.

**Wat is het verschil tussen de &#39;People&#39;-norm in CDA en de &#39;Unique Visitors&#39;-norm buiten CDA?**

De maatstaf &#39;Mensen&#39; is vergelijkbaar met de maatstaf &#39;Unieke bezoekers&#39; in die zin dat deze het aantal unieke individuen rapporteert. Wanneer u echter Apparaatanalyse gebruikt, worden unieke bezoekers gecombineerd wanneer ze anders worden opgenomen als twee afzonderlijke unieke bezoekers buiten CDA. De metrische waarde &#39;Mensen&#39; vervangt de metrische waarde &#39;Unieke bezoekers&#39; wanneer de functie voor apparaatanalyse is ingeschakeld.

**Wat is het verschil tussen de &quot;Unieke Apparaten&quot;-norm in CDA en de &quot;Unieke Bezoekers&quot;-norm buiten CDA?**

Deze twee metriek zijn ruwweg gelijkwaardig aan elkaar.

**Kan ik CDA-meetgegevens opnemen met behulp van de 2.0-API?**

Ja. De analysewerkruimte gebruikt de 2.0-API om gegevens van de servers van Adobe aan te vragen, en u kunt API-aanroepen bekijken die Adobe gebruikt om uw eigen rapporten te maken:

1. Open de ontwikkelaarsgereedschappen van uw browser terwijl u zich hebt aangemeld bij Analyse Workspace (F12 voor de meeste browsers).
1. Typ in de browserconsole `adobeTools.showDebugger()`. De pagina wordt opnieuw geladen met de foutopsporingspictogrammen in de rechterbovenhoek van elk deelvenster.
1. Klik op het pictogram voor foutopsporing in het gewenste deelvenster en selecteer de gewenste visualisatie en tijd voor de aanvraag.
1. Zoek de JSON-aanvraag die u kunt gebruiken in uw API-aanroep naar Adobe.

**Met behulp van Cross-Device Analytics kunnen unieke bezoekers aan elkaar worden gekoppeld. Kan zij bezoeken bij elkaar houden?**

Ja. Als een individu hits verzendt van twee aparte apparaten binnen de time-out voor het bezoek van uw virtuele rapportsuite (standaard ingesteld op 30 minuten), worden deze aan hetzelfde bezoek gekoppeld.

**Wat is de ultieme bezoekersidentiteitskaart die CDA gebruikt? Kan ik het exporteren uit Adobe Analytics?**

Apparaatanalyse berekent gebonden gegevens met een &#39;cluster-id&#39;. Deze id wordt door Adobe berekend op het moment dat het rapport wordt uitgevoerd, ook wel Report-Time-verwerking genoemd. De aard van de verwerking van de rapporttijd betekent dat niet compatibel met het Pakhuis van Gegevens, gegevensvoer, of andere de uitvoereigenschappen van Adobe aanbiedt.
