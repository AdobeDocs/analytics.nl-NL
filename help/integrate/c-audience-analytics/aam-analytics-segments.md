---
description: Analytics en Audience Manager gebruiken beide segmenten. Nochtans, is een segment van de Analyse niet precies het zelfde ding zoals een segment van de Audience Manager. Deze verschillen dragen deels bij aan de discrepanties die u zult zien in uw Analytics en Audience Manager rapporten. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.
title: Segmenten in Analytics en Audience Manager begrijpen
feature: Audience Analytics
exl-id: 2bc662e7-7552-41e1-9d4a-bc7aa81b8c1d
source-git-commit: c947de8eaa4e4dc3a0c10989ef6ae450cebc1f3e
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Segmenten in Analytics en Audience Manager begrijpen

Analytics en Audience Manager gebruiken beide segmenten. Nochtans, is een segment van de Analyse niet precies het zelfde ding zoals een segment van de Audience Manager. Deze verschillen dragen deels bij aan de discrepanties die u zult zien in uw Analytics en Audience Manager rapporten. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.

## Audience Manager Segmenten {#aam-segments}

Een segment van de Audience Manager is een groep bezoekers (gebruiker IDs) die voor een reeks bepaalde eigenschappen kwalificeren die door logische regels worden verbonden. Er zijn vier criteria die bepalen als een bezoeker (gebruiker - identiteitskaart) deel van een segment in Audience Manager uitmaakt:

* De regels die op de segmenten zelf en de eigenschappen worden geplaatst die omhoog elk segment maken. Deze regels bepalen de voorwaarden een gebruiker - identiteitskaart moet ontmoeten of tentoonstellen om voor een segment worden gekwalificeerd.
* Algorithmic modeling. Gebruikers die voor een bepaald segment in aanmerking komen, kunnen in aanmerking komen voor andere segmenten op basis van algoritmische modellering en analyse.
* Tijd-aan-levende (TTL) intervallen. Het lidmaatschap van het segment kan na een vastgestelde interval verlopen of voor onbepaalde tijd verdergaan.
* Recentie en frequentie. Door te bepalen wanneer en hoe vaak gebruikers een interactie hebben (realisatie van de eigenschap), kunt u segmenten maken op basis van het werkelijke (of waargenomen) interesseniveau van een site, sectie of bepaalde creatieve instellingen.

Audience Manager segment lidmaatschap is dynamisch. Gebruikers kunnen een segment invoeren of verlaten, afhankelijk van het feit of ze op het huidige tijdstip in aanmerking komen voor de segmentcriteria. Dit betekent dat de populatie van een segment van de Audience Manager in de loop der tijd kan toenemen of afnemen.

Een segment van de Audience Manager wordt vermeld als publiek in Analytics.

Raadpleeg voor meer informatie [Behandelings- en segmentpopulatiegegevens in Segment Builder](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html) en [Signalen, Traits en Segmenten](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html).

## Analysesegmenten {#analytics-segments}

Een segment van Analytics is een het filtreren mechanisme voor gegevens in uw rapporten. Filteren kan plaatsvinden op bezoekers-, bezoek- of raakniveau, en niet alleen op bezoekersniveau, zoals in de Audience Manager. Er zijn verscheidene belangrijke factoren om te overwegen wanneer het vergelijken van een segment van de Analyse aan een segment van de Audience Manager:

* De segmenten van de analyse werken op een verschillende reeks gegevens dan de segmenten van de Audience Manager. Tijdens gegevensverzameling past Analytics vele verschillende naverwerkingsstappen toe op de gegevens die niet beschikbaar zijn voor Audience Manager. Nabewerking kan onder andere bestaan uit persistentie van eVar, verwerkingsregels, opzoekingen (geo-locatie, mobiel apparaat), VISTA en vele andere. De Audience Manager ontvangt vooraf verwerkte gegevens door server-kant door:sturen (of DIL).

  Veelvoorkomende gegevensdiscrepanties treden op bij het vergelijken van segmenten op basis van dimensies die in Analytics nooit verlopen, met dezelfde dimensie in Audience Manager. ListVars of handelsversies van Vars die nooit verlopen.

  Als eVar = blauw en in Analytics is ingesteld op nooit verlopen, bevat elk segment in Analytics met de criteria &quot;eVar = blauw&quot; altijd deze bezoeker. In Audience Manager zou deze bezoeker na een bepaalde periode uit een op dezelfde wijze gedefinieerd segment kunnen vallen.

* Analysesegmenten hebben meer mogelijkheden dan Adobe Audience Manager-segmenten. De segmenten van de Audience Manager worden altijd geëvalueerd op bezoekersniveau. Analysesegmenten kunnen worden gedefinieerd op bezoekers-, bezoek- of raakniveau (of een combinatie van deze niveaus). Bovendien, steunt de Analyse geavanceerde segmenteringsmogelijkheden die de Audience Manager niet, zoals opeenvolgende segmentatie.

* Zoals eerder vermeld, kunnen de bezoekers van de Audience Manager een segment ingaan of verlaten afhankelijk van of zij voor de segmentcriteria op het huidige tijdstip in aanmerking komen.

  In Analytics daarentegen worden bezoekers opgenomen in of uitgesloten van een segment dat is gebaseerd op het bereik van de rapportdatum. Eén bezoeker heeft bijvoorbeeld vorige maand een aankoop gedaan. In Adobe Audience Manager zou die bezoeker worden opgenomen in een &quot;koper&quot;-segment, ongeacht het datumbereik. In Analytics, zou een rapport dat op deze maand wordt gebaseerd de bezoeker in het segment niet omvatten. Nochtans, zou een rapport dat op deze maand &amp; vorige maand wordt gebaseerd de bezoeker in het segment omvatten.

Zie de [Handleiding voor analysegmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html) voor meer informatie .
