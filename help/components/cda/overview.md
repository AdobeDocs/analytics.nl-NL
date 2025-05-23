---
title: Apparaatanalyse
description: Verander uw gegevens van apparaat-geconcentreerd in persoon-geconcentreerd door apparatengegevens samen te stikken.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
feature: CDA
role: Admin
source-git-commit: cfa5cc02ba3a7349b51a904f29bab533c0f1c603
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%

---

# Apparaatanalyse

{{available-existing-customers}}

Cross-Device Analytics (CDA) is een functie waarmee Analytics van een apparaat-centric mening in een persoon-centric mening wordt omgezet. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. Adobe ondersteunt twee overkoepelende workflows om apparaatgegevens aan elkaar te koppelen:

* [**op gebied-gebaseerde het stitching**](field-based-stitching.md): geadviseerde het stitching optie omdat het slechts deterministische aanpassing aan verbindingsapparaten samen gebruikt.
Staat u toe om een variabele van de Analyse als basis voor dwars-apparaat het stitching in een virtuele rapportreeks te kiezen.

* [**grafiek van het Apparaat**](device-graph.md): CDA communiceert met een privé grafiek om apparaten samen te stikken.

Met CDA kunt u vragen beantwoorden zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn inzicht in de doeltreffendheid van campagnes als ik rekening houd met cross-device reizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunt u opbrengsten op het mobiele apparaat toewijzen aan de advertentie waarop zij op hun desktopcomputer hebben geklikt.

Uit een geest van partnerschap en transparantie willen we dat onze klanten op de hoogte zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. De Adobe gebruikt Azure om de gegevens van de apparatengrafiek op te slaan en dwars-apparatenstitching uit te voeren. Als zodanig worden Adobe Analytics-gegevens tussen het gegevensverwerkingscentrum van Adobe en door Adobe geleverde instanties van Microsoft Azure doorgegeven.

Zie [ IQ van de Reis: De pagina van de Vonk van de Vonk van de Analyse van het Apparaat kruis ](https://adobe.ly/aacda) om meer over de mogelijkheden en de eigenschappen van Analytics van het Apparaat te leren.

## Vereisten

Voor het gebruik van CDA is het volgende vereist. [ op gebied-gebaseerde het stitching ](field-based-stitching.md) en [ grafiek ](device-graph.md) methodes van het Apparaat hebben ook hun eigen specifieke eerste vereisten.

* Een contract moet worden ondertekend met Adobe die Adobe Analytics Ultimate omvat.
* Uw organisatie kiest welke rapportsuites om CDA toe te laten. Adobe raadt rapportsuites aan die apparaatgegevens bevatten. Dit zijn gegevens van meerdere apparaten/browsers/app-typen. Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn.

## Beperkingen

Cross-Device Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop deze kan worden gebruikt. [ Op gebied-gebaseerde het stitching ](field-based-stitching.md) en [ grafiek ](device-graph.md) methodes van het Apparaat hebben ook hun eigen specifieke beperkingen.

* CDA is alleen beschikbaar via Analysis Workspace.
* Cross-Device Analytics werkt niet op meerdere rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Adobe Analytics-rapportreeksen kunnen niet aan meerdere organisatie-id&#39;s worden toegewezen. Aangezien CDA apparaten in een bepaalde rapportsuite vastlegt, kan CDA niet worden gebruikt om gegevens aan te sluiten op meerdere organisatie-id&#39;s.
* CDA gebruikt een complexe verwerkingspijpleiding, met veelvoudige afhankelijke componenten. Dit wordt parallel uitgevoerd met de rapportworkflow voor basisanalysemogelijkheden. Daarom wordt een gegevensmismatch van ongeveer 1% voor het totale aantal treffers tussen de originele rapportreeks en de virtuele CDA rapportenreeks verwacht.
* Analytics voor verschillende apparaten maakt gebruik van een virtuele rapportsuite en de verwerking van de rapporttijd, die hun eigen beperkingen hebben. Ze ondersteunen momenteel bijvoorbeeld geen variabelen van marketingkanalen. Zie [ Virtuele rapportreeksen ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=nl-NL) en [ de tijdverwerking van het Rapport ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=nl-NL#report-time-processing-limitations) voor meer informatie over deze beperkingen.
* De privé Grafiek leverages de zelfde syncs van identiteitskaart zoals die gebruikt door het [ vermogen van de Klant ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=nl-NL#customer-attributes) binnen Experience Cloud en Adobe Analytics worden gevonden die. De virtuele CDA-rapportensuites (op basis van een privégrafiek of op basis van een veld) zijn echter niet compatibel met de overige kenmerkfuncties van de klant. Met andere woorden, op kenmerken gebaseerde afmetingen van de klant zijn niet beschikbaar voor gebruik met virtuele CDA-rapportensuites.
* CDA is momenteel niet compatibel met A4T.
* De 1.4-API wordt niet ondersteund. Power BI connectors en Report Builder vertrouwen beide op de 1.4 API en zijn daarom niet compatibel met CDA.
* Actief toezicht op het CDA-stitching-proces door Adobe is beperkt tot uitsluitend productierapporten.
* CDA is momenteel niet compatibel met de Adobe Analytics [ API van de Reparatie van Gegevens ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/data-repair.md)
* Historische gegevens in de virtuele rapportsuite veranderen op basis van Adobe die apparaten herkent en aansluit. De gegevens in de bronrapportsuite veranderen niet.
* De gegevens in de vorm van titching volgen een latentie van 8 tot 12 uur.
* Toewijzingsgeschiedenisgegevens voor een bepaald apparaat worden maximaal één jaar opgeslagen.
* Als een apparaat een zeer hoog aantal ingangen van de afbeeldingsgeschiedenis binnen een jaar bereikt, wordt de het in kaart brengen geschiedenis beknot. De exacte limiet is afhankelijk van de gebruikte optie voor stitching.
