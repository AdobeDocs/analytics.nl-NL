---
description: Analytics en Audience Manager maken beide gebruik van segmenten. Een analysesegment is echter niet precies hetzelfde als een Audience Manager-segment. Deze verschillen dragen deels bij aan de discrepanties die u zult zien in uw Analytics- en Audience Manager-rapporten. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.
title: Segmenten in Analytics en Audience Manager begrijpen
feature: Audience Analytics
exl-id: 2bc662e7-7552-41e1-9d4a-bc7aa81b8c1d
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Segmenten in Analytics en Audience Manager begrijpen

Analytics en Audience Manager maken beide gebruik van segmenten. Een analysesegment is echter niet precies hetzelfde als een Audience Manager-segment. Deze verschillen dragen deels bij aan de discrepanties die u zult zien in uw Analytics- en Audience Manager-rapporten. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.

## Audience Manager Segments {#aam-segments}

Een Audience Manager-segment is een groep bezoekers (gebruikers-id&#39;s) die in aanmerking komen voor een set gedefinieerde kenmerken die worden gecombineerd met logische regels. Er zijn vier criteria die bepalen als een bezoeker (gebruiker - identiteitskaart) deel van een segment in Audience Manager uitmaakt:

* De regels die op de segmenten zelf en de eigenschappen worden geplaatst die omhoog elk segment maken. Deze regels bepalen de voorwaarden een gebruiker - identiteitskaart moet ontmoeten of tentoonstellen om voor een segment worden gekwalificeerd.
* Algorithmic modeling. Gebruikers die voor een bepaald segment in aanmerking komen, kunnen in aanmerking komen voor andere segmenten op basis van algoritmische modellering en analyse.
* Tijd-aan-levende (TTL) intervallen. Het lidmaatschap van het segment kan na een vastgestelde interval verlopen of voor onbepaalde tijd verdergaan.
* Recentie en frequentie. Door te bepalen wanneer en hoe vaak gebruikers een interactie hebben (realisatie van de eigenschap), kunt u segmenten maken op basis van het werkelijke (of waargenomen) interesseniveau van een site, sectie of bepaalde creatieve instellingen.

Audience Manager-segmentlidmaatschap is dynamisch. Gebruikers kunnen een segment invoeren of verlaten, afhankelijk van het feit of ze op het huidige tijdstip in aanmerking komen voor de segmentcriteria. Dit betekent dat de populatie van een Audience Manager-segment in de loop der tijd kan toenemen of afnemen.

Een Audience Manager-segment wordt in Analytics aangeduid als een publiek.

Voor meer informatie, verwijs naar [ Bedienings en Bevolkingsgegevens van het Segment in de Bouwer van het Segment ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=nl-NL) en [ Signalen, Trekken, en Segmenten ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=nl-NL).

## Analysesegmenten {#analytics-segments}

Een segment van Analytics is een het filtreren mechanisme voor gegevens in uw rapporten. Filteren kan plaatsvinden op bezoekers-, bezoek- of raakniveau, en niet alleen op bezoekersniveau zoals in Audience Manager. Er zijn verscheidene belangrijke factoren om te overwegen wanneer het vergelijken van een segment van Analytics aan een segment van Audience Manager:

* De segmenten van de analyse werken op een verschillende reeks gegevens dan de segmenten van Audience Manager. Tijdens gegevensverzameling past Analytics vele verschillende naverwerkingsstappen toe op de gegevens die niet beschikbaar zijn voor Audience Manager. Nabewerking kan onder andere bestaan uit eVar-persistentie, verwerkingsregels, zoekopdrachten (geo-locatie, mobiel apparaat), VISTA en vele andere. Audience Manager ontvangt vooraf verwerkte gegevens via server-side forward (of DIL).

  Veelvoorkomende gegevensdiscrepanties treden op bij het vergelijken van segmenten op basis van dimensies die in Analytics nooit verlopen, met dezelfde dimensie in Audience Manager. ListVars of handelsversies van Vars die nooit verlopen.

  Als eVar bijvoorbeeld blauw is en voor Analytics is ingesteld dat deze nooit verlopen is, bevat elk segment in Analytics met criteria &quot;eVar = blue&quot; altijd deze bezoeker. In Audience Manager zou deze bezoeker na een bepaalde periode uit een op dezelfde wijze gedefinieerd segment kunnen vallen.

* Analysesegmenten hebben meer mogelijkheden dan Adobe Audience Manager-segmenten. Audience Manager-segmenten worden altijd geëvalueerd op bezoekersniveau. Analysesegmenten kunnen worden gedefinieerd op bezoekers-, bezoek- of raakniveau (of een combinatie van deze niveaus). Daarnaast biedt Audience Manager ondersteuning voor geavanceerde segmentatiefuncties, zoals sequentiële segmentatie.

* Zoals eerder vermeld, kunnen Audience Manager-bezoekers een segment betreden of verlaten, afhankelijk van het feit of ze op het huidige tijdstip voor de segmentcriteria in aanmerking komen.

  In Analytics daarentegen worden bezoekers opgenomen in of uitgesloten van een segment dat is gebaseerd op het bereik van de rapportdatum. Eén bezoeker heeft bijvoorbeeld vorige maand een aankoop gedaan. In Adobe Audience Manager zou die bezoeker worden opgenomen in een &quot;koper&quot;-segment, ongeacht het datumbereik. In Analytics, zou een rapport dat op deze maand wordt gebaseerd de bezoeker in het segment niet omvatten. Nochtans, zou een rapport dat op deze maand &amp; vorige maand wordt gebaseerd de bezoeker in het segment omvatten.

Zie de [ Gids van de Segmentatie van de Analyse ](/help/components/segmentation/seg-home.md) voor meer informatie.
