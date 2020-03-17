---
description: Analytics en Audience Manager gebruiken beide segmenten. Nochtans, is een segment van Analytics niet precies het zelfde ding zoals een segment van de Manager van de Audience. Deze verschillen dragen gedeeltelijk bij aan de discrepanties die u zult zien in uw rapporten van Analytics en Audience Manager. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.
title: Begrijp segmenten in Analytics en de Manager van de Publiek
uuid: 13f7d1d7-6a3f-42f1-822e-8d3523999efa
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Begrijp segmenten in Analytics en de Manager van de Publiek

Analytics en Audience Manager gebruiken beide segmenten. Nochtans, is een segment van Analytics niet precies het zelfde ding zoals een segment van de Manager van de Audience. Deze verschillen dragen gedeeltelijk bij aan de discrepanties die u zult zien in uw rapporten van Analytics en Audience Manager. Dientengevolge, is het belangrijk en nuttig om deze verschillen te proberen te begrijpen wanneer u met segmenten in beide oplossingen begint te werken.

## Segmenten van Audience Manager {#section_417DC4B5648547778A27E42CE1D09900}

Een segment van de Manager van de Audience is een groep bezoekers (gebruiker IDs) die voor een reeks bepaalde eigenschappen kwalificeren die door logische regels worden aangesloten. Er zijn vier criteria die bepalen als een bezoeker (gebruiker - identiteitskaart) deel van een segment in de Manager van het Publiek uitmaakt:

* De regels die op de segmenten zelf en de eigenschappen worden geplaatst die omhoog elk segment maken. Deze regels bepalen de voorwaarden een gebruiker - identiteitskaart moet ontmoeten of tentoonstellen om voor een segment worden gekwalificeerd.
* Algorithmic modeling. Gebruikers die voor een bepaald segment in aanmerking komen, kunnen in aanmerking komen voor andere segmenten op basis van algoritmische modellering en analyse.
* Tijd-aan-levende (TTL) intervallen. Het lidmaatschap van het segment kan na een vastgestelde interval verlopen of voor onbepaalde tijd verdergaan.
* Recentie en frequentie. Door te bepalen wanneer en hoe vaak gebruikers een interactie hebben (realisatie van de eigenschap), kunt u segmenten maken op basis van het werkelijke (of waargenomen) interesseniveau van een site, sectie of bepaalde creatieve instellingen.

Het segmentlidmaatschap van Audience Manager is dynamisch. Gebruikers kunnen een segment invoeren of verlaten, afhankelijk van het feit of ze op het huidige tijdstip in aanmerking komen voor de segmentcriteria. Dit betekent de bevolking van een segment van de Manager van de Publiek kan in tijd stijgen of verminderen.

Een segment van de Manager van de Publiek wordt vermeld als publiek in Analytics.

Voor meer informatie, verwijs naar de Gegevens van de Bevolking van het [Spoor en van het Segment in de Bouwer](https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html) van het Segment en [Signalen, Verrichtingen, en Segmenten](https://marketing.adobe.com/resources/help/en_US/aam/c_signal_trait_segment.html).

## Analysesegmenten {#section_62EC584BB7134E10923BCBA7F9BD89A8}

Een segment van Analytics is een het filtreren mechanisme voor gegevens in uw rapporten. Filteren kan plaatsvinden op bezoekers-, bezoek- of raakniveau, in plaats van alleen op bezoekersniveau zoals in Audience Manager. Er zijn verscheidene belangrijke factoren om te overwegen wanneer het vergelijken van een segment van Analytics aan een segment van de Manager van de Audience:

* De segmenten van Analytics werken op een verschillende reeks gegevens dan de segmenten van de Manager van de Publiek. Tijdens gegevensinzameling, past de Analyse vele verschillende naverwerkingsstappen op de gegevens toe die niet beschikbaar aan de Manager van de Publiek zijn. Nabewerkingsprogramma&#39;s kunnen onder andere bestaan uit persistentie van eVar, verwerkingsregels, opzoekingen (geo-locatie, mobiel apparaat), VISTA en vele andere. Audience Manager ontvangt vooraf verwerkte gegevens via server-side door:sturen (of DIL).

   De gemeenschappelijke gegevensdiscrepanties komen voor wanneer het vergelijken van segmenten die op dimensies worden gebaseerd die nooit in Analytics, aan de zelfde dimensie in de Manager van de Publiek verlopen. ListVars of handelsversies van Vars die nooit verlopen.

   Bijvoorbeeld, als eVar = blauw en om in Analytics wordt geplaatst nooit verlopen, zal om het even welk segment in Analytics met criteria &quot;eVar = blauw&quot;altijd deze bezoeker omvatten. In Audience Manager zou die bezoeker na een bepaalde periode uit een op dezelfde wijze gedefinieerd segment kunnen vallen.

* De segmenten van Analytics hebben meer mogelijkheden dan de segmenten van AAM. De segmenten van de Manager van het publiek worden altijd geëvalueerd op een bezoekersniveau. Analysesegmenten kunnen worden gedefinieerd op bezoekers-, bezoek- of raakniveau (of een combinatie van deze niveaus). Daarnaast ondersteunt Analytics geavanceerde segmentatiemogelijkheden die Audience Manager niet ondersteunt, zoals sequentiële segmentatie.
* Zoals eerder vermeld, kunnen de bezoekers van de Manager van de Publiek een segment ingaan of uitvallen afhankelijk van of zij voor de segmentcriteria op het huidige punt in tijd in aanmerking komen.

   In Analytics daarentegen worden bezoekers opgenomen in of uitgesloten van een segment dat is gebaseerd op het bereik van de rapportdatum. Eén bezoeker heeft bijvoorbeeld vorige maand een aankoop gedaan. In AAM, zou die bezoeker in een &quot;koper&quot;segment, ongeacht de datumwaaier worden omvat. In Analytics, zou een rapport dat op deze maand wordt gebaseerd de bezoeker in het segment niet omvatten. Nochtans, zou een rapport dat op deze maand &amp; vorige maand wordt gebaseerd de bezoeker in het segment omvatten.

Zie de [handleiding](https://marketing.adobe.com/resources/help/en_US/analytics/segment/) Analytics Segmentation voor meer informatie.
