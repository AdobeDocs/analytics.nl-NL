---
description: Adobe Analytics biedt een flexibele rapportinterface waarmee u diverse complexe rapporten kunt genereren. Terwijl de meeste rapporten zeer snel produceren, zou u rapporten kunnen ontmoeten die onderbreking of er niet in slagen om met succes te produceren. Om de mislukkingen van de rapportgeneratie te helpen vermijden, verklaart deze sectie vele factoren die de snelheid van de rapportgeneratie beïnvloeden. Kennis van deze informatie kan u helpen rapporten te structureren, zodat het waarschijnlijker is dat deze met succes worden gegenereerd.
keywords: best practices;failure;timeout;troubleshooting;slow
title: Beste praktijken en het Oplossen van problemen melden
topic: Reports
uuid: d4eef0a3-1d26-4460-8a2b-962001c9f846
translation-type: tm+mt
source-git-commit: 025ac334f9191b6455eea0530a2a21c01199000a

---


# Beste praktijken en het Oplossen van problemen melden

Adobe Analytics biedt een flexibele rapportinterface waarmee u diverse complexe rapporten kunt genereren. Terwijl de meeste rapporten zeer snel produceren, zou u rapporten kunnen ontmoeten die onderbreking of er niet in slagen om met succes te produceren. Om de mislukkingen van de rapportgeneratie te helpen vermijden, verklaart deze sectie vele factoren die de snelheid van de rapportgeneratie beïnvloeden. Kennis van deze informatie kan u helpen rapporten te structureren, zodat het waarschijnlijker is dat deze met succes worden gegenereerd.

>[!Nofferte]
>Deze aanbevelingen zijn op Rapporten &amp; Analytics, Ad hoc Analyse, en de Bouwer van het Rapport van toepassing.
>Zij zijn niet van toepassing op de Werkruimte van de Analyse, die zijn eigen reeks [beste praktijken](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md)heeft. Zij zijn ook niet >van toepassing op [beste praktijken](https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse_bp.html)van Data Warehouse. Een extra set van
>[De API voor rapportage van Adobe Analytics biedt tips en trucs](https://marketing.adobe.com/developer/en_US/get-started/best-practices/c-best-practices) .

## Time-outs en aanvraagwachtrij rapporteren {#section_A42AD7E487C749B7B879BAFA814FFEF9}

**Tijdstippen**

Eén rapport wordt opgedeeld in meerdere aanvragen (één per uitsplitsing) en elk verzoek is onderworpen aan een individuele time-out. De geplande rapporten worden verleend langere onderbrekingsperiodes en zullen waarschijnlijker slagen dan rapporten die direct in een gebruikersinterface worden geproduceerd.

**Wachtrij rapportsuite**

Elke rapportreeks handhaaft een afzonderlijke rij van verzoeken. Als er meerdere rapporten tegelijk worden aangevraagd, zelfs bij afzonderlijke gebruikers, wordt er een klein aantal rapporten tegelijk gegenereerd. Als de rapporten volledig zijn, worden de resterende rapporten geproduceerd in de orde waarin zij werden ontvangen. Dientengevolge, als een groot aantal complexe rapporten reeds in de rij van de rapportreeks zijn, zou een rapport dat typisch snel produceert uit tijd kunnen.

## Factoren die de rapportsnelheid beïnvloeden {#section_6BA937EB6CEC4CBCB71FAAD32F031DC2}

De volgende factoren dragen aan langere rapportgeneratietijden bij. Het verhogen van één van deze factoren zou niet in een onderbreking voor dat rapport kunnen resulteren, maar het zou andere rapporten in de rij van de rapportreeks kunnen vertragen en een volgend rapport aan onderbreking veroorzaken.

**Tijdbereik rapport**

De grootste factor die de tijd van de rapportgeneratie beïnvloedt is het gevraagde aantal maanden. Het verminderen van het aantal maanden van drie tot één vermindert beduidend generatietijd, maar het verminderen van de tijdwaaier van één maand aan één week heeft geen grote invloed op de tijd van de rapportgeneratie.

**Aantal metingen**

Aangezien het aantal metriek stijgt, stijgt de tijd van de rapportruntime. Het verwijderen van metriek verbetert vaak de tijd van de rapportgeneratie.

**Aantal uitsplitsingen**

Binnen een rapport, vertegenwoordigt elke verdeling een afzonderlijk verzoek. Terwijl de individuele verzoeken snel kunnen voltooien, die duizenden onderbrekingen in één enkel rapport in werking stellen kan de tijd van de rapportgeneratie beduidend vertragen en de rij van de rapportreeks beïnvloeden.

**Complexiteit segment**

De segmenten die vele dimensies overwegen of vele (24+) regels hebben verhogen het verwerkingseffect en verhogen de tijd van de rapportgeneratie.

**Aantal unieke waarden**

Rapporten die honderdduizenden unieke waarden bevatten, genereren langzamer dan rapporten die minder unieke waarden bevatten, zelfs als het segment of filter het aantal waarden vermindert die uiteindelijk in een rapport verschijnen. Bijvoorbeeld, produceert een rapport dat onderzoekstermijnen toont typisch langzamer dan andere rapporten, zelfs als een filter wordt toegepast om slechts onderzoekstermen te tonen die een specifieke waarde bevatten.

## Overige rapportopties {#section_FEF85C7FC6E14755A6086AFFF36E0EB4}

Naast het verminderen van de tijdwaaier, het aantal metriek, en het aantal onderverdelingen in een rapport, helpen de volgende richtlijnen betrouwbaarheid van rapportlevering verhogen:

* Het Pakhuis van Gegevens van het gebruik om rapporten te verzoeken die vele onderverdelingen of metriek bevatten. Het Pakhuis van gegevens wordt ontworpen om deze types van rapporten te produceren.
* Plan rapporten die tijdens niet-piekuren moeten worden uitgevoerd. Dit verhoogt de waarschijnlijkheid van een rapport terugkerend omdat de verzoekrij voor een rapportreeks eerder tijdens die tijden leeg zal zijn.
* De Bouwer van het rapport kan worden gebruikt om rapporten in kleinere tijdwaaiers en verzoeken te breken die minder metriek bevatten. U kunt inheemse functionaliteit van Excel dan gebruiken om gegevens van diverse verzoeken in één enkel rapport samen te voegen.

