---
title: Cross-device Analytics
description: Verander uw gegevens van apparaat-geconcentreerd in persoon-geconcentreerd door apparatengegevens samen te stikken.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
source-git-commit: 844df9d632f9e9cceb6c882f81360a83891e2143
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Cross-device Analytics

Apparaatanalyse is een functie waarmee analyses worden getransformeerd van een apparaatgecentreerde weergave naar een persoonlijke weergave. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. Adobe ondersteunt twee overkoepelende workflows om apparaatgegevens aan elkaar te koppelen:

* [**Veldgebaseerde stitching**](field-based-stitching.md): Staat u toe om een variabele van de Analyse als basis voor dwars-apparaat het stitching in een virtuele rapportreeks te kiezen. Gebruikt deterministische aanpassing om apparaten aan elkaar te koppelen. Adobe raadt aan om voor de meeste deterministische gevallen van overeenkomend gebruik op basis van veldomstandigheden te kiezen.
* [**Apparaatgrafiek**](device-graph.md): CDA communiceert met een apparaatgrafiek om apparaten aan elkaar te hechten. De co-op grafiek gebruikt zowel deterministische als probabilistische aanpassing.

>[!NOTE]
>
>Lees meer over [Apparaatco-op einde-van-leven](https://experienceleague.adobe.com/docs/device-co-op/using/about/device-co-op-eol.html).

Met CDA kunt u vragen beantwoorden zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn inzicht in de doeltreffendheid van campagnes als ik rekening houd met cross-device reizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunt u opbrengsten op het mobiele apparaat toewijzen aan de advertentie waarop zij op hun desktopcomputer hebben geklikt.

Uit een geest van partnerschap en transparantie willen wij dat onze klanten zich bewust zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Als dusdanig, worden de gegevens van Adobe Analytics overgegaan - en - tussen Adobe verwerkend centrum en Adobe geleverde instanties van Microsoft Azure.

Zie de [Reis-IQ: Pagina](https://adobe.ly/aacda) van de Vonk van de Analyse van het Apparaat voor meer informatie over de mogelijkheden en de eigenschappen van Analytics van het Apparaat.

## Vereisten

Voor het gebruik van CDA is het volgende vereist. [Veldgebaseerde ](field-based-stitching.md) stitchingings- en  [Device ](device-graph.md) grafietechnieken hebben ook hun eigen specifieke voorwaarden.

* Een contract moet worden ondertekend met Adobe die Adobe Analytics Ultimate omvat.
* De analyse van apparaten wordt toegelaten op een per-rapport-reeks basis. Adobe raadt een rapportsuite aan die apparaatoverschrijdende gegevens bevat. Dit houdt in dat gegevens van meerdere apparaattypen (web, app, enz.) worden gebruikt. Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn.

## Beperkingen

Cross-Device Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop deze kan worden gebruikt. [Veldgebaseerde ](field-based-stitching.md) stitchingings- en  [Device-](device-graph.md) grafische methoden hebben ook hun eigen specifieke beperkingen.

* CDA is alleen beschikbaar via Analysis Workspace.
* Cross-Device Analytics werkt niet op meerdere rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Adobe Analytics-rapportsuites kunnen niet worden toegewezen aan meer dan één IMS-org. Aangezien CDA apparaten vastlegt binnen een bepaalde rapportsuite, kan CDA niet worden gebruikt om gegevens te koppelen aan meerdere IMS-organen.
* Private Graph gebruikt dezelfde ID-syncs als de [Customer Attributes](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#customer-attributes)-mogelijkheden in Experience Cloud en Adobe Analytics. De virtuele CDA-rapportensuites (op basis van een privégrafiek of op basis van een veld) zijn echter niet compatibel met de rest van de functie Kenmerken van klant. Met andere woorden, op kenmerken gebaseerde afmetingen van de klant zijn niet beschikbaar voor gebruik in virtuele CDA-rapportensuites.
* CDA is momenteel niet compatibel met A4T.
* Analytics voor verschillende apparaten maakt gebruik van een virtuele rapportsuite en de verwerking van de rapporttijd, die hun eigen beperkingen hebben. Zie [Virtuele rapportsuites](../vrs/vrs-about.md) en [Tijd verwerking rapporteren](../vrs/vrs-report-time-processing.md) voor meer informatie over deze beperkingen.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* Actief toezicht op het CDA-stitching-proces door Adobe is beperkt tot uitsluitend productierapporten.
* CDA is momenteel niet compatibel met de Adobe Analytics [Data Repair API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/data-repair.md)
* Historische gegevens in de virtuele rapportsuite veranderen op basis van Adobe die apparaten herkent en aansluit. De gegevens in de bronrapportsuite veranderen niet.
* De gegevens in de vorm van titching volgen een latentie van 8 tot 12 uur.
