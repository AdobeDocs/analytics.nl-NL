---
title: Apparaatanalyse
description: Leer hoe u uw gegevens kunt wijzigen van apparaatgericht naar persoonlijke gegevens door apparaatgegevens aan elkaar te koppelen.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
feature: CDA
role: Admin
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Apparaatanalyse

{{available-existing-customers}}

Cross-Device Analytics (CDA) is een functie waarmee Analytics van een apparaat-centric mening in een persoon-centric mening wordt omgezet. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. Adobe ondersteunt twee overkoepelende workflows om apparaatgegevens aan elkaar te koppelen:

* [**op gebied-gebaseerde het stitching**](field-based-stitching.md): geadviseerde het stitching optie omdat het slechts deterministische aanpassing aan verbindingsapparaten samen gebruikt.
Op gebied-gebaseerde het stitching staat u toe om een variabele van de Analyse als basis voor het dwars-apparaat het stitching in een virtuele rapportreeks te kiezen.

* [**grafiek van het Apparaat**](device-graph.md): De Analyses van het inter-Apparaat communiceert met een privé grafiek om apparaten samen te stikken.

Met CDA kunt u vragen beantwoorden zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn inzicht in de doeltreffendheid van campagnes als ik rekening houd met cross-device reizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunt u opbrengsten op het mobiele apparaat toewijzen aan de advertentie waarop zij op hun desktopcomputer hebben geklikt.

Microsoft Azure wordt gebruikt voor Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Als zodanig worden Adobe Analytics-gegevens doorgegeven tussen Adobe Data Processing Center en door Adobe verschafte instanties van Microsoft Azure.

Zie de [ pagina van de Vonk van de Vonk van de Analyse van het Apparaat kruis ](https://express.adobe.com/page/8ZpjsX6Lp5XTM/) om meer over de mogelijkheden en de eigenschappen van Analytics van het Apparaat te leren.

## Vereisten

Het gebruik van Analytics van het Apparaat vereist [ Op gebied-gebaseerde het stitching ](field-based-stitching.md) en [ de grafieken van het Apparaat ](device-graph.md) methodes, en allebei hebben hun eigen specifieke eerste vereisten.

* Er moet een contract worden ondertekend met Adobe dat Adobe Analytics Ultimate omvat.
* Uw organisatie kiest welke rapportsuites om CDA toe te laten. Adobe raadt rapportsuite aan die apparaatoverschrijdende gegevens bevat. Dit houdt in dat gegevens van meerdere apparaten/browsers/app-typen afkomstig zijn. Sommige organisaties verwijzen naar dit concept als een &quot;globale&quot;rapportreeks, hoewel de Analytics van het Apparaat van het dwars-Apparaat strikt niet globaal uit een geografisch perspectief moet zijn.

## Beperkingen

Cross-Device Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop deze kan worden gebruikt. [ Op gebied-gebaseerde het stitching ](field-based-stitching.md) en [ grafiek ](device-graph.md) methodes van het Apparaat hebben ook hun eigen specifieke beperkingen.

* Apparaatanalyse is alleen beschikbaar via Analysis Workspace.
* Cross-Device Analytics werkt niet op meerdere rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Adobe Analytics-rapportreeksen kunnen niet aan meerdere organisatie-id&#39;s worden toegewezen. Aangezien de apparaten van de Analyse van het Apparaat binnen een bepaalde rapportreeks worden vastgezet, kan de dwars-Apparaat Analytics niet worden gebruikt om gegevens over veelvoudige organisatie IDs te binden.
* De Analytics van het dwars-Apparaat gebruikt een complexe verwerkingspijpleiding, met veelvoudige afhankelijke componenten. Deze pijpleiding loopt parallel aan de basis Analytics rapporteringswerkschema. U kunt een gegevenswanverhouding van ongeveer 1% voor het totale aantal treffers tussen de originele rapportreeks en de virtuele het rapportreeks van Analytics van het Interapparaat verwachten.
* Analytics voor verschillende apparaten maakt gebruik van een virtuele rapportsuite en de verwerking van de rapporttijd, die hun eigen beperkingen hebben. Ze ondersteunen momenteel bijvoorbeeld geen variabelen van marketingkanalen. Zie [ Virtuele rapportreeksen ](/help/components/vrs/vrs-about.md) en [ de tijdverwerking van het Rapport ](/help/components/vrs/vrs-report-time-processing.md) voor meer informatie over deze beperkingen.
* De privé Grafiek hefboomwerkingen de zelfde syncs van identiteitskaart zoals de syncs van identiteitskaart die door het [ bezit van de Klant ](https://experienceleague.adobe.com/nl/docs/core-services/interface/services/customer-attributes/attributes) worden gebruikt vermogen dat binnen Experience Cloud en Adobe Analytics wordt gevonden. Virtuele rapportreeksen voor de analyse van apparaten (op basis van een privégrafiek of op basis van een veld) zijn echter niet compatibel met de overige kenmerkfuncties van de klant. Met andere woorden, op kenmerken gebaseerde afmetingen van de klant zijn niet beschikbaar voor gebruik met virtuele rapportensuites voor cross-device analyse.
* Apparaatanalyse is momenteel niet compatibel met A4T.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* De actieve controle van het cross-device analytics stitching proces door Adobe is beperkt tot uitsluitend de reeksen van het productierapport.
* De analyse van het dwars-Apparaat is momenteel niet compatibel met Adobe Analytics [ Reparatie API van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/)
* Historische gegevens in de virtuele rapportsuite worden gewijzigd op basis van het feit dat Adobe apparaten herkent en vastzet. De gegevens in de bronrapportsuite veranderen niet.
* De gegevens in de vorm van titching volgen een latentie van 8 tot 12 uur.
* Toewijzingsgeschiedenisgegevens voor een bepaald apparaat worden maximaal één jaar opgeslagen.
* Als een apparaat een zeer hoog aantal ingangen van de afbeeldingsgeschiedenis binnen een jaar bereikt, wordt de het in kaart brengen geschiedenis beknot. De exacte limiet is afhankelijk van de gebruikte optie voor stitching.
