---
title: Cross-device Analytics
description: Verander uw gegevens van apparaat-geconcentreerd in persoon-geconcentreerd door apparatengegevens samen te stikken.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
source-git-commit: 47824be19d3cc25b3120ce9aed6938f69fe0e096
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Cross-device Analytics

Apparaatanalyse is een functie waarmee analyses worden getransformeerd van een apparaatgecentreerde weergave naar een persoonlijke weergave. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. Adobe ondersteunt twee overkoepelende workflows om apparaatgegevens aan elkaar te koppelen:

* [**Veldgebaseerde stitching**](field-based-stitching.md): Aanbevolen optie voor stitching omdat alleen deterministische overeenkomsten worden gebruikt om apparaten aan elkaar te koppelen.
Staat u toe om een variabele van de Analyse als basis voor dwars-apparaat het stitching in een virtuele rapportreeks te kiezen.
* [**Apparaatgrafiek**](device-graph.md): CDA communiceert met een apparaatgrafiek om apparaten aan elkaar te hechten. De co-op grafiek gebruikt zowel deterministische als probabilistische aanpassing.

>[!NOTE]
>
>Meer informatie over de [Apparaatcoop-einde van levensduur](https://experienceleague.adobe.com/docs/device-co-op/using/about/device-co-op-eol.html).

Met CDA kunt u vragen beantwoorden zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn inzicht in de doeltreffendheid van campagnes als ik rekening houd met cross-device reizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunt u opbrengsten op het mobiele apparaat toewijzen aan de advertentie waarop zij op hun desktopcomputer hebben geklikt.

Uit een geest van partnerschap en transparantie willen we dat onze klanten op de hoogte zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Als zodanig worden Adobe Analytics-gegevens doorgegeven tussen gegevensverwerkingscentrum en door Adobe geleverde instanties van Microsoft Azure van Adobe.

Zie de [Reis-IQ: De pagina Spark van Analytics voor verschillende apparaten](https://adobe.ly/aacda) voor meer informatie over de mogelijkheden en functies van Cross-Device Analytics.

## Vereisten

Voor het gebruik van CDA is het volgende vereist. [Veldgebaseerde stitching](field-based-stitching.md) en [Apparaatgrafiek](device-graph.md) methoden hebben ook hun eigen specifieke voorwaarden .

* Een contract moet worden ondertekend met Adobe die Adobe Analytics Ultimate omvat.
* De analyse van apparaten wordt toegelaten op een per-rapport-reeks basis. Adobe raadt een rapportsuite aan die apparaatoverschrijdende gegevens bevat. Dit houdt in dat gegevens van meerdere apparaattypen (web, app, enz.) worden gebruikt. Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn.

## Beperkingen

Cross-Device Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop deze kan worden gebruikt. [Veldgebaseerde stitching](field-based-stitching.md) en [Apparaatgrafiek](device-graph.md) de methoden hebben ook hun eigen specifieke beperkingen .

* CDA is alleen beschikbaar via Analysis Workspace.
* Cross-Device Analytics werkt niet op meerdere rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Adobe Analytics-rapportsuites kunnen niet worden toegewezen aan meer dan één IMS-org. Aangezien CDA apparaten vastlegt binnen een bepaalde rapportsuite, kan CDA niet worden gebruikt om gegevens te koppelen aan meerdere IMS-organen.
* CDA gebruikt een complexe verwerkingspijpleiding, met veelvoudige afhankelijke componenten. Dit wordt parallel uitgevoerd met de rapportworkflow voor basisanalysemogelijkheden. Daarom wordt een gegevensmismatch van ongeveer 1% voor het totale aantal treffers tussen de originele rapportreeks en de virtuele CDA rapportenreeks verwacht.
* Analytics voor verschillende apparaten maakt gebruik van een virtuele rapportsuite en de verwerking van de rapporttijd, die hun eigen beperkingen hebben. Ze ondersteunen momenteel bijvoorbeeld geen variabelen van marketingkanalen. Zie [Virtuele rapportsuites](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=en) en [Tijdverwerking rapporteren](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en#report-time-processing-limitations) voor meer informatie over deze beperkingen .
* Private Graph gebruikt dezelfde id-syncs als de id [Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#customer-attributes) gevonden in Experience Cloud en Adobe Analytics. De virtuele CDA-rapportensuites (op basis van een privégrafiek of op basis van een veld) zijn echter niet compatibel met de rest van de functie Kenmerken van klant. Met andere woorden, de op kenmerken-gebaseerde afmetingen van de Klant zijn niet beschikbaar voor gebruik met CDA virtuele rapportsuites.
* CDA is momenteel niet compatibel met A4T.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* Actief toezicht op het CDA-stitching-proces door Adobe is beperkt tot uitsluitend productierapporten.
* CDA is momenteel niet compatibel met de Adobe Analytics [API voor gegevensherstel](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/data-repair.md)
* Historische gegevens in de virtuele rapportsuite veranderen op basis van Adobe die apparaten herkent en aansluit. De gegevens in de bronrapportsuite veranderen niet.
* De gegevens in de vorm van titching volgen een latentie van 8 tot 12 uur.
* Toewijzingsgeschiedenisgegevens voor een bepaald apparaat worden maximaal één jaar opgeslagen.
* Als een apparaat een zeer hoog aantal ingangen van de afbeeldingsgeschiedenis binnen een jaar bereikt, wordt de het in kaart brengen geschiedenis beknot. De exacte limiet is afhankelijk van de gebruikte optie voor stitching.
