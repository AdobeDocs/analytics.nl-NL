---
title: Best practices en probleemoplossing rapporteren
description: Tips voor aanbevolen procedures en probleemoplossing bij het genereren van rapporten.
keywords: aanbevolen procedures;fout;timeout;problemen;traag
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 1c09f514-42ab-4698-bdee-d1b509da3f11
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Best practices en probleemoplossing rapporteren

*Deze Help-pagina verwijst naar best practices voor rapporten en analyses. Voor Analysis Workspace, zie [Analysis Workspace-prestaties optimaliseren](../analysis-workspace/workspace-faq/optimizing-performance.md). Zie voor Data Warehouse [Aanbevolen werkwijzen voor Data Warehouse](/help/export/data-warehouse/data-warehouse-bp.md).*

Adobe Analytics biedt een flexibele rapportinterface waarmee u diverse complexe rapporten kunt genereren. Terwijl de meeste rapporten zeer snel produceren, kunt u rapporten ontmoeten die onderbreking of er niet in slagen om te produceren. Deze pagina verklaart factoren die de snelheid van de rapportgeneratie beïnvloeden. Kennis van deze informatie kan u helpen rapporten te structureren, zodat deze beter met succes kunnen worden gegenereerd.

## Time-outs en aanvraagwachtrij rapporteren

* **Tijdstippen**: Eén rapport wordt opgedeeld in meerdere aanvragen (één per uitsplitsing) en elk verzoek is onderworpen aan een individuele time-out. De geplande rapporten worden verleend langere onderbrekingsperiodes en zullen waarschijnlijker slagen dan rapporten die direct in een gebruikersinterface worden geproduceerd.
* **Wachtrij rapportsuite**: Elke rapportreeks handhaaft een afzonderlijke rij van verzoeken. Als er meerdere rapporten tegelijk worden aangevraagd, zelfs bij afzonderlijke gebruikers, wordt er een klein aantal rapporten tegelijk gegenereerd. Als de rapporten volledig zijn, worden de resterende rapporten geproduceerd in de orde waarin zij werden ontvangen. Dientengevolge, als een groot aantal complexe rapporten reeds in de rij van de rapportreeks zijn, zou een rapport dat typisch snel produceert uit tijd kunnen.

## Factoren die rapportsnelheid beïnvloeden

De volgende factoren dragen aan langere rapportgeneratietijden bij. Het verhogen van één van deze factoren beïnvloedt typisch geen prestaties, maar het zou andere rapporten in de rij van de rapportreeks kunnen vertragen en een volgend rapport aan onderbreking veroorzaken.

* **Tijdbereik rapport**: De grootste factor die de tijd van de rapportgeneratie beïnvloedt is het gevraagde aantal maanden. Het verminderen van het aantal maanden van drie tot één vermindert beduidend generatietijd, maar het verminderen van de tijdwaaier van één maand aan één week heeft geen grote invloed op de tijd van de rapportgeneratie.
* **Aantal metingen**: Aangezien het aantal metriek stijgt, stijgt de tijd van de rapportruntime. Het verwijderen van metriek verbetert vaak de tijd van de rapportgeneratie.
* **Aantal uitsplitsingen**: Binnen een rapport, vertegenwoordigt elke verdeling een afzonderlijk verzoek. Terwijl de individuele verzoeken snel kunnen voltooien, die duizenden onderbrekingen in één enkel rapport in werking stellen kan de tijd van de rapportgeneratie beduidend vertragen en de rij van de rapportreeks beïnvloeden.
* **Complexiteit segment**: De segmenten die vele dimensies overwegen of vele (24+) regels hebben verhogen het verwerkingseffect en verhogen de tijd van de rapportgeneratie.
* **Aantal unieke waarden**: Rapporten die honderdduizenden unieke waarden bevatten, genereren langzamer dan rapporten die minder unieke waarden bevatten, zelfs als het segment of filter het aantal waarden vermindert die uiteindelijk in een rapport verschijnen. Bijvoorbeeld, produceert een rapport dat onderzoekstermijnen toont typisch langzamer dan andere rapporten, zelfs als een filter wordt toegepast om slechts onderzoekstermen te tonen die een specifieke waarde bevatten.

## Overige rapportopties

De volgende richtlijnen helpen betrouwbaarheid van rapportlevering verhogen:

* Gebruik Data Warehouse om rapporten aan te vragen die vele onderverdelingen of metriek bevatten. Data Warehouse wordt ontworpen om deze types van rapporten te produceren.
* Plan rapporten die tijdens niet-piekuren moeten worden uitgevoerd. Dit verhoogt de waarschijnlijkheid van een rapport terugkerend omdat de verzoekrij voor een rapportreeks eerder tijdens die tijden leeg zal zijn.
* Report Builder kan worden gebruikt om rapporten in kleinere tijdwaaiers en verzoeken te breken die minder metriek bevatten. U kunt inheemse functionaliteit van Excel dan gebruiken om gegevens van diverse verzoeken in één enkel rapport samen te voegen.
