---
title: Algemene rapportsuites in Adobe Analytics
description: Begrijp de voordelen en de vereisten aan het gebruiken van een globale rapportreeks.
feature: Implementation Basics
exl-id: fa949b1e-80bd-41cf-a294-c840503b568f
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Overwegingen voor algemene rapportsuites

Een algemene rapportsuite is een rapportsuite die gegevens verzamelt van alle domeinen en apps die eigendom zijn van uw organisatie. Deze gegevensverzamelingstechniek vereist voorbereiding en kan coördinatie tussen teams binnen uw organisatie vereisen.

## Voordelen

Adobe beveelt in de meeste gevallen aan een algemene rapportsuite te implementeren.

* **Geaggregeerde gegevens:** De globale rapportsuites laten u toe om de gebeurtenissen van KPI en van het succes over uw eigen plaatsen te zien. De segmentatie en de virtuele rapportsuites kunnen worden gebruikt om plaats-specifieke gegevens te bekijken.
* **Ondersteuning voor apparaatanalyse:** CDA vereist een rapportsuite die gegevens verzamelt van meerdere locaties, zoals uw website en mobiele app. Afzonderlijke apparaten kunnen gegevens samenvoegen als deze correct zijn geïmplementeerd. Zie [Apparaatanalyse](../../components/cda/overview.md) in de gebruikershandleiding van Componenten voor meer informatie.
* **U hebt niet meer dan één rapportsuite nodig:** Alle gegevens kunnen in één enkele rapportreeks worden verzameld, zodat is het minder waarschijnlijk voor een ontwikkelaar om gegevens naar de verkeerde rapportreeks per ongeluk te verzenden.
* **Geen rollups nodig:** Rollups zijn een vrij gedateerde eigenschap die individuele gegevens van de rapportreeks op een dagelijkse basis samenvoegt. Rollups dedupliceren geen bezoek- of bezoekersgegevens, wat tot opgeblazen aantallen kan leiden. Zie [Rolluizen](../../admin/c-manage-report-suites/rollup-report-suite.md) in de gebruikershandleiding voor Admin voor meer informatie.
* **Tijd opslaan:** De projecten van de werkruimte, classificaties, segmenten, en berekende metriek zijn verbonden aan de zelfde globale rapportreeks. Beheerders besteden minder tijd aan het beheren van deze componenten en gegevensbeheer.
* **Nauwkeuriger kenmerk tussen verschillende merken:** Als een bezoek op één plaats dan aan een andere van uw eigen plaatsen alvorens een succesgebeurtenis begint te teweegbrengen, wordt de attributie correct verzameld. Een bezoeker klikt bijvoorbeeld op een betaalde zoekkoppeling en landt op site A. Vervolgens klikken ze op een koppeling naar site B en kopen ze deze. Een algemene rapportsuite kenmerkt zich correct die wordt aangeschaft voor een betaalde zoekopdracht.
* **Vereenvoudigde implementatie:** Aangezien alle merken/sites gegevens naar dezelfde rapportsuite verzenden, worden de implementaties voor elke site uitgelijnd. Dit gedwongen bestuur verzekert een specifieke dimensie of metrisch wordt bewaard in de zelfde eVar of de gebeurtenis. Beheerders, testers, eigenaars van tagbeheer en analisten profiteren van deze vereenvoudiging.

>[!NOTE]
>
>Het coördineren van een globale implementatie van de rapportreeks is een groot project. Adobe raadt aan om samen met een consultant te werken om eventuele complicaties en problemen te verminderen.

## Nieuwe implementatie starten met een algemene rapportsuite

Gebruik de volgende algemene richtlijnen om inzicht te krijgen in het proces van implementatie van een algemene rapportsuite.

1. Maak de algemene rapportsuite in Adobe Analytics. Zie [Een rapportsuite maken](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) in de gebruikershandleiding voor Admin voor meer informatie.
1. Het werk met teams in uw organisatie verantwoordelijk voor elk domein. Vele teams hebben rapporteringsvereisten specifiek voor hun gebied van de zaken.
1. Al deze vereisten registreren en samenvoegen in een [Document voor het ontwerp van oplossingen](solution-design.md). Als de teams gelijkaardige vereisten voor een afmeting hebben, kunnen zij de zelfde douanevariabele gebruiken. Bijvoorbeeld, als de plaats A en plaats B allebei een dimensie van broodkruimels vereisen, kunnen de implementaties voor beide plaatsen die gegevens door eVar1 verzenden.

   >[!IMPORTANT]
   >
   >Zorg ervoor dat om het even welke bepaalde douanevariabele op gelijke wijze over domeinen wordt gebruikt. Gebruik dezelfde eVar of gebeurtenis niet voor verschillende doeleinden op uw sites.
1. Zorg ervoor dat elk domein een gegevenslaag heeft om gegevensinzameling te vereenvoudigen. Gegevens kunnen nog steeds zonder een gegevenslaag worden verzameld, maar de betrouwbaarheid en de levensduur van uw implementatie nemen af, vooral wanneer uw site opnieuw ontwerpen doorloopt.
1. Gebruik labels in Adobe Experience Platform om Analytics te implementeren. De verschillende plaatsen zullen waarschijnlijk verschillende gegevenselementen vereisen. De regels van het gebruik specifiek voor elk domein om ervoor te zorgen elk gegevenselement correct bevolkt is, dan wijs die gegevenselementen aan hun respectieve eVars en gebeurtenissen toe. Zie de [overzicht van tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).
1. Inclusief de [Adobe Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) en gebruiken de [appendVisitorIDsTo](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/appendvisitorid.html) functie. Deze functie voegt bezoekersgegevens samen wanneer de gebruikers van één domein aan een ander klikken.

## Een bestaande implementatie aanpassen met een algemene rapportsuite

Het proces om een bestaande implementatie over veelvoudige plaatsen naar één enkele globale rapportreeks te bewegen vereist meer tijd en coördinatie tussen teams in uw organisatie.

1. Bepaal als u één van uw bestaande rapportreeksen wilt gebruiken, of begin vers met een nieuwe rapportreeks. Als u het gebruik voor bestaande variabelen in uw implementatie wilt veranderen, wordt het beginnen met een nieuwe rapportreeks geadviseerd.
2. Bepaal een cutooverdatum waarop u wilt overschakelen naar een algemene rapportsuite. De beste tijd om een cutover te maken is tussen twee significante rapporteringsperioden, of naast belangrijke veranderingen in uw plaats. Voorbeelden zijn het begin van een fiscaal kwartaal of jaar, tijdens het vernieuwen van een site of het wijzigen van een nieuw tagbeheersysteem.
3. Voer de bovenstaande stappen uit (maak een rapportsuite, verzamel rapportagevereisten in een document voor het ontwerp van de oplossing en stel een gegevenslaag op elke site in). Wanneer u tags implementeert in Adobe Experience Platform, valideert u uw implementatie met een ontwikkelingsversie van uw website.
4. Zodra u hebt bevestigd dat uw implementatie aan dev werkt, druk uw implementatie van markeringen live op de cutooverdatum.

## Gerelateerde pagina&#39;s

[Het schakelen van multi-suite etiketteren naar een globaal rapportpakket en virtuele rapportsuites](../../components/vrs/vrs-considerations.md)
[Rollups en globale rapportsuites vergelijken](../../admin/c-manage-report-suites/rollup-report-suite.md)
