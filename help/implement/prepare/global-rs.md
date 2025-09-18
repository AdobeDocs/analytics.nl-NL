---
title: Algemene rapportsuites in Adobe Analytics
description: Begrijp de voordelen en de vereisten aan het gebruiken van een globale rapportreeks.
feature: Implementation Basics
exl-id: fa949b1e-80bd-41cf-a294-c840503b568f
role: Admin, Developer, Leader
source-git-commit: 2d5348a4a6377313f5aab229214d97a02c826939
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Overwegingen voor algemene rapporten

Een algemene rapportsuite is een rapportsuite die gegevens verzamelt van alle domeinen en apps die eigendom zijn van uw organisatie. Deze gegevensverzamelingstechniek vereist voorbereiding en kan coördinatie tussen teams binnen uw organisatie vereisen.

## Voordelen

Adobe raadt in de meeste gevallen aan een algemene rapportsuite te implementeren.

* **samengevoegde gegevens:** Globale rapportreeksen laten u toe om de gebeurtenissen van KPI en van het succes over uw bezeten plaatsen te zien. De segmentatie en de virtuele rapportsuites kunnen worden gebruikt om plaats-specifieke gegevens te bekijken.
* **Steun voor Analytics van het Apparaat:** CDA vereist een rapportreeks die gegevens van veelvoudige plaatsen, zoals uw website en mobiele app verzamelt. Afzonderlijke apparaten kunnen gegevens samenvoegen als deze correct zijn geïmplementeerd. Zie [ Analytics van het Apparaat ](../../components/cda/overview.md) in de de gebruikersgids van Componenten voor meer informatie.
* **geen behoefte aan meer dan één rapportreeks:** Alle gegevens kunnen in één enkele rapportreeks worden verzameld, zodat is het minder waarschijnlijk voor een ontwikkelaar om gegevens naar de verkeerde rapportreeks per ongeluk te verzenden.
* **geen behoefte aan rollups:** Rollups zijn een vrij gedateerde eigenschap die individuele gegevens van de rapportreeks op een dagelijkse basis samenvoegt. Rollups dedupliceren geen bezoek- of bezoekersgegevens, wat tot opgeblazen aantallen kan leiden. Zie [ Rollups ](../../admin/tools/manage-rs/rollup-report-suite.md) in de Admin gebruikersgids voor meer informatie.
* **sparen tijd:** de projecten van Workspace, classificaties, segmenten, en berekende metriek zijn gebonden aan de zelfde globale rapportreeks. Beheerders besteden minder tijd aan het beheren van deze componenten en gegevensbeheer.
* **nauwkeurigere dwars-brand attributie:** als een bezoek op één plaats dan aan een andere van uw bezeten plaatsen alvorens een succesgebeurtenis teweeg te brengen begint, wordt de attributie nauwkeurig verzameld. Een bezoeker klikt bijvoorbeeld op een betaalde zoekkoppeling en landt op site A. Vervolgens klikken ze op een koppeling naar site B en kopen ze deze. Een algemene rapportsuite kenmerkt zich correct die wordt aangeschaft voor een betaalde zoekopdracht.
* **Vereenvoudigde implementatie:** Aangezien alle merken/plaatsen gegevens in de zelfde rapportreeks verzenden, worden uw implementaties over elke plaats gericht. Dit gedwongen bestuur zorgt ervoor dat een specifieke dimensie of metrisch wordt opgeslagen in dezelfde eVar of gebeurtenis. Beheerders, testers, eigenaars van tagbeheer en analisten profiteren van deze vereenvoudiging.

>[!NOTE]
>
>Het coördineren van een globale implementatie van de rapportreeks is een groot project. Adobe raadt aan om samen met een consultant de problemen en complicaties te verminderen.

## Nieuwe implementatie starten met een algemene rapportsuite

Gebruik de volgende algemene richtlijnen om inzicht te krijgen in het proces van implementatie van een algemene rapportsuite.

1. Maak de algemene rapportsuite in Adobe Analytics. Zie [ een rapportreeks ](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md) in de Admin gebruikersgids voor meer informatie creëren.
1. Het werk met teams in uw organisatie verantwoordelijk voor elk domein. Vele teams hebben rapporteringsvereisten specifiek voor hun gebied van de zaken.
1. Verslag en bijeenvoegen al deze vereisten in het ontwerpdocument van het a [ Oplossing ](solution-design.md). Als de teams gelijkaardige vereisten voor een afmeting hebben, kunnen zij de zelfde douanevariabele gebruiken. Bijvoorbeeld, als plaats A en plaats B allebei een dimensie van broodkruimels vereisen, kunnen de implementaties voor beide plaatsen die gegevens door eVar1 verzenden.

   >[!IMPORTANT]
   >
   >Zorg ervoor dat om het even welke bepaalde douanevariabele gelijkaardig over domeinen wordt gebruikt. Gebruik niet dezelfde eVar of gebeurtenis voor verschillende doeleinden op uw sites.
1. Zorg ervoor dat elk domein een gegevenslaag heeft om gegevensinzameling te vereenvoudigen. Gegevens kunnen nog steeds zonder een gegevenslaag worden verzameld, maar de betrouwbaarheid en de levensduur van uw implementatie nemen af, vooral wanneer uw site opnieuw ontwerpen doorloopt.
1. Gebruik labels in Adobe Experience Platform om Analytics te implementeren. De verschillende plaatsen zullen waarschijnlijk verschillende gegevenselementen vereisen. De regels van het gebruik specifiek voor elk domein om ervoor te zorgen elk gegevenselement correct bevolkt is, dan wijs die gegevenselementen aan hun respectieve eVars en gebeurtenissen toe. Verwijs naar het [ overzicht van markeringen ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).
1. Omvat de [ Dienst van identiteitskaart van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html) en gebruik de [`appendVisitorIDsTo` ](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/appendvisitorid.html) functie. Deze functie voegt bezoekersgegevens samen wanneer de gebruikers van één domein aan een ander klikken.

## Een bestaande implementatie aanpassen met een algemene rapportsuite

Het proces om een bestaande implementatie over veelvoudige plaatsen naar één enkele globale rapportreeks te bewegen vereist meer tijd en coördinatie tussen teams in uw organisatie.

1. Bepaal als u één van uw bestaande rapportreeksen wilt gebruiken, of begin vers met een nieuwe rapportreeks. Als u het gebruik voor bestaande variabelen in uw implementatie wilt veranderen, wordt het beginnen met een nieuwe rapportreeks geadviseerd.
2. Bepaal een cutooverdatum waarop u wilt overschakelen naar een algemene rapportsuite. De beste tijd om een cutover te maken is tussen twee significante rapporteringsperioden, of naast belangrijke veranderingen in uw plaats. Voorbeelden zijn het begin van een fiscaal kwartaal of jaar, tijdens het vernieuwen van een site of het wijzigen van een nieuw tagbeheersysteem.
3. Voer de bovenstaande stappen uit (maak een rapportsuite, verzamel rapportagevereisten in een document voor het ontwerp van de oplossing en stel een gegevenslaag op elke site in). Wanneer u tags implementeert in Adobe Experience Platform, valideert u uw implementatie met een ontwikkelingsversie van uw website.
4. Zodra u hebt bevestigd dat uw implementatie aan dev werkt, druk uw implementatie van markeringen live op de cutooverdatum.

>[!MORELIKETHIS]
>
>[ Bewegend van multi-suite het etiketteren aan een globale rapportreeks en virtuele rapportsuites ](../../components/vrs/vrs-considerations.md)
>&#x200B;>[Het vergelijken van rollups en globale rapportsuites ](../../admin/tools/manage-rs/rollup-report-suite.md)
