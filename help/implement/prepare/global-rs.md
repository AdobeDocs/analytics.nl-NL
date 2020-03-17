---
title: Algemene rapportsuite in Adobe Analytics
description: Begrijp de voordelen en de vereisten aan het gebruiken van een globale rapportreeks.
translation-type: tm+mt
source-git-commit: d7c4412feb85f4381d8811b29fc23c9c85d23555

---


# Overwegingen voor algemene rapporten

Een algemene rapportsuite is een rapportsuite die gegevens verzamelt van alle domeinen en apps die eigendom zijn van uw organisatie. Deze gegevensverzamelingstechniek vereist voorbereiding en kan coördinatie tussen teams binnen uw organisatie vereisen.

## Voordelen

Adobe raadt u in de meeste gevallen aan een algemene rapportsuite te implementeren.

* **Geaggregeerde gegevens:** De globale rapportsuites laten u toe om de gebeurtenissen van KPI en van het succes over uw eigen plaatsen te zien. De segmentatie en de virtuele rapportsuites kunnen worden gebruikt om plaats-specifieke gegevens te bekijken.
* **Ondersteuning voor apparaatanalyse:** CDA vereist een rapportsuite die gegevens verzamelt van meerdere locaties, zoals uw website en mobiele app. Afzonderlijke apparaten kunnen gegevens samenvoegen als deze correct zijn geïmplementeerd. Zie [Apparaatanalyse](../../components/cda/cda-home.md) in de gebruikershandleiding van Componenten voor meer informatie.
* **U hebt niet meer dan één rapportsuite nodig:** Alle gegevens kunnen in één enkele rapportreeks worden verzameld, zodat is het minder waarschijnlijk voor een ontwikkelaar om gegevens naar de verkeerde rapportreeks per ongeluk te verzenden.
* **Geen rollups nodig:** Rollups zijn een vrij gedateerde eigenschap die individuele gegevens van de rapportreeks op een dagelijkse basis samenvoegt. Rollups dedupliceren geen bezoek- of bezoekersgegevens, wat tot opgeblazen aantallen kan leiden. Zie [Rollups](../../admin/c-manage-report-suites/rollup-report-suite.md) in de gebruikershandleiding voor Admin voor meer informatie.
* **Tijd opslaan:** De projecten van de werkruimte, classificaties, segmenten, en berekende metriek zijn verbonden aan de zelfde globale rapportreeks. Beheerders besteden minder tijd aan het beheren van deze componenten en gegevensbeheer.
* **Nauwkeuriger kenmerk tussen verschillende merken:** Als een bezoek op één plaats dan aan een andere van uw eigen plaatsen alvorens een succesgebeurtenis begint te teweegbrengen, wordt de attributie correct verzameld. Een bezoeker klikt bijvoorbeeld op een betaalde zoekkoppeling en landt op site A. Vervolgens klikken ze op een koppeling naar site B en kopen ze deze. Een algemene rapportsuite kenmerkt zich correct die wordt aangeschaft voor een betaalde zoekopdracht.
* **Vereenvoudigde implementatie:** Aangezien alle merken/sites gegevens naar dezelfde rapportsuite verzenden, worden de implementaties voor elke site uitgelijnd. Dit gedwongen bestuur verzekert een specifieke dimensie of metrisch wordt bewaard in zelfde eVar of gebeurtenis. Beheerders, testers, eigenaars van tagbeheer en analisten profiteren van deze vereenvoudiging.

> [!NOTE] Het coördineren van een globale implementatie van de rapportreeks is een groot project. Adobe raadt u aan om samen met een consultant de problemen en complicaties te verhelpen.

## Nieuwe implementatie starten met een algemene rapportsuite

Gebruik de volgende algemene richtlijnen om inzicht te krijgen in het proces van implementatie van een algemene rapportsuite.

1. Maak de algemene rapportsuite in Adobe Analytics. Zie [Een rapportsuite](../../admin/admin-console/create-report-suite.md) maken in de handleiding voor Admin-gebruikers voor meer informatie.
2. Het werk met teams in uw organisatie verantwoordelijk voor elk domein. Vele teams hebben rapporteringsvereisten specifiek voor hun gebied van de zaken.
3. Leg al deze vereisten vast in een [ontwerpdocument](solution-design.md)van de Oplossing en stel ze samen. Als de teams gelijkaardige vereisten voor een afmeting hebben, kunnen zij de zelfde douanevariabele gebruiken. Bijvoorbeeld, als de plaats A en plaats B allebei een dimensie van broodkruimels vereisen, kunnen de implementaties voor beide plaatsen die gegevens door eVar1 verzenden.
   > [!IMPORTANT] Zorg ervoor dat om het even welke bepaalde douanevariabele gelijkaardig over domeinen wordt gebruikt. Gebruik niet hetzelfde eVar of dezelfde gebeurtenis voor verschillende doeleinden op uw sites.
4. Zorg ervoor dat elk domein een gegevenslaag heeft om gegevensinzameling te vereenvoudigen. Gegevens kunnen nog steeds zonder een gegevenslaag worden verzameld, maar de betrouwbaarheid en de levensduur van uw implementatie nemen af, vooral wanneer uw site opnieuw ontwerpen doorloopt.
5. Gebruik Adobe Experience Platform Launch om Analytics te implementeren. De verschillende plaatsen zullen waarschijnlijk verschillende gegevenselementen vereisen. De regels van het gebruik specifiek voor elk domein om ervoor te zorgen elk gegevenselement correct bevolkt is, dan wijs die gegevenselementen aan hun respectieve eVars en gebeurtenissen toe. Zie Overzicht van [starten](https://docs.adobe.com/content/help/en/launch/using/overview.html) in de gebruikershandleiding bij Adobe Experience Platform Launch.
6. Neem de [Adobe Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/home.html) op en gebruik de [functie appendVisitorIDsTo](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/appendvisitorid.html) . Deze functie voegt bezoekersgegevens samen wanneer de gebruikers van één domein aan een ander klikken.

## Een bestaande implementatie aanpassen met een algemene rapportsuite

Het proces om een bestaande implementatie over veelvoudige plaatsen naar één enkele globale rapportreeks te bewegen vereist meer tijd en coördinatie tussen teams in uw organisatie.

1. Bepaal als u één van uw bestaande rapportreeksen wilt gebruiken, of begin vers met een nieuwe rapportreeks. Als u het gebruik voor bestaande variabelen in uw implementatie wilt veranderen, wordt het beginnen met een nieuwe rapportreeks geadviseerd.
2. Bepaal een cutooverdatum waarop u wilt overschakelen naar een algemene rapportsuite. De beste tijd om een cutover te maken is tussen twee significante rapporteringsperioden, of naast belangrijke veranderingen in uw plaats. Voorbeelden zijn het begin van een fiscaal kwartaal of jaar, tijdens het vernieuwen van een site of het wijzigen van een nieuw tagbeheersysteem.
3. Voer de bovenstaande stappen uit (maak een rapportsuite, verzamel rapportagevereisten in een document voor het ontwerp van de oplossing en stel een gegevenslaag op elke site in). Bij het implementeren van Starten valideert u uw implementatie met een ontwikkelingsversie van uw website.
4. Zodra u hebt bevestigd dat uw implementatie aan dev werkt, duw uw implementatie van de Lancering live op de cutooverdatum.

## Gerelateerde pagina&#39;s

[Het schakelen van multi-suite het etiketteren naar een globale rapportreeks en virtuele rapportreeksen](../../components/vrs/vrs-considerations.md)[het Vergelijken van rollups en globale rapportreeksen](../../admin/c-manage-report-suites/rollup-report-suite.md)
