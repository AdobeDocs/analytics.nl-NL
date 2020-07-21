---
title: Cross-device Analytics
description: Verander uw gegevens van apparaat-geconcentreerd in persoon-geconcentreerd door apparatengegevens samen te stikken.
translation-type: tm+mt
source-git-commit: eb2bee26dd58dcff13b4ddf41c6f6ab337d8d374
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# Cross-device Analytics

Analytics op verschillende apparaten is een functie waarmee Analytics van een apparaatgecentreerde weergave wordt getransformeerd naar een persoonlijk gecentreerde weergave. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. Adobe ondersteunt twee overkoepelende workflows om apparaatgegevens aan elkaar te koppelen:

* [**Veldgebaseerde stitching **](field-based-stitching.md): Staat u toe om een variabele van Analytics als basis voor dwars-apparaat het stitching in een virtuele rapportreeks te kiezen. Gebruikt deterministische aanpassing om apparaten aan elkaar te koppelen. Adobe raadt u aan om op het veld gebaseerde stitching te gebruiken voor de meeste deterministische gevallen van overeenkomend gebruik.
* [**Apparaatgrafiek **](device-graph.md): CDA communiceert met een apparaatgrafiek om apparaten aan elkaar te hechten. De co-op grafiek gebruikt zowel deterministische als probablistische aanpassing.

Met CDA kunt u vragen beantwoorden zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik rekening houd met apparatuurreizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunnen inkomsten worden toegeschreven aan de advertentie waarop ze op hun desktopcomputer hebben geklikt.

Uit een geest van partnerschap en transparantie willen wij dat onze klanten zich bewust zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Daarom worden Adobe Analytics-gegevens afwisselend doorgegeven tussen het gegevensverwerkingscentrum van Adobe en de door Adobe geleverde instanties van Microsoft Azure.

Zie de [Reis IQ: Analytics Spark-pagina](http://adobe.ly/aacda) voor verschillende apparaten voor meer informatie over de mogelijkheden en functies van Analytics voor verschillende apparaten.

## Vereisten

Voor het gebruik van CDA is het volgende vereist. [Veldgebaseerde stitching](field-based-stitching.md) en de grafiekmethodes van het [Apparaat](device-graph.md) hebben ook hun eigen specifieke eerste vereisten.

* Er moet een contract worden ondertekend met Adobe Analytics Ultimate.
* Analytics voor verschillende apparaten wordt ingeschakeld op basis van een aantal afzonderlijke rapporten. Adobe raadt een rapportsuite aan die apparaatgegevens bevat (gegevens van meerdere apparaattypen (web, app, enz.). Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn.

## Beperkingen

Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop het kan worden gebruikt. [Veldgebaseerde stitching](field-based-stitching.md) - en [Apparaatgrafiekmethoden](device-graph.md) hebben ook hun eigen specifieke beperkingen.

* CDA is alleen beschikbaar via Analysis Workspace.
* Analytics voor meerdere apparaten werkt niet in verschillende rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Adobe Analytics-rapportsuites kunnen niet aan meer dan één IMS org worden toegewezen. Aangezien CDA apparaten vastlegt binnen een bepaalde rapportsuite, kan CDA niet worden gebruikt om gegevens te koppelen aan meerdere IMS-organen.
* CDA is momenteel niet compatibel met Customer Attributes. Deze twee eigenschappen kunnen in afzonderlijke virtuele rapportreeksen samenvallen die de zelfde bronrapportreeks van verwijzingen voorzien.
* Analytics voor verschillende apparaten gebruikt een virtuele rapportsuite en meldt tijdverwerking, die hun eigen beperkingen hebben. Zie [Virtuele rapportsuites](../vrs/vrs-about.md) en de tijdverwerking [van het](../vrs/vrs-report-time-processing.md) Rapport voor meer informatie over deze beperkingen.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* Historische gegevens in de virtuele rapportsuite veranderen op basis van het herkennen en aansluiten van apparaten door Adobe. De gegevens in de bronrapportsuite veranderen niet.
