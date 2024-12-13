---
title: Streaming Media Core-meetgegevens
description: De beschikbare metriek wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat.
feature: Metrics
exl-id: f4ff5f84-18b6-4e67-b808-133faeaf8605
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Streaming Media Core-meetgegevens

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Media Core] voor een rapportreeks toelaat. Zie [ Streaming de kernafmetingen van Media ](../dimensions/sm-core.md) voor beschikbare afmetingen.*

Streaming Media core-meetgegevens bieden basisrapportfunctionaliteit voor gegevens die via streaming media collection-bibliotheken zijn verzameld. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Core]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, zijn de volgende metriek beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Gemiddeld aantal minuten | De totale hoeveelheid tijd die aan een bepaald stuk van inhoud wordt doorgebracht, die door zijn lengte voor elk van zijn playbackzittingen wordt gedeeld.<br>`[Time spent] / [Media length]` | Media sluiten | `a.media.averageMinuteAudience` |
| Inhoud is voltooid | Triggers wanneer een stuk van inhoud voltooit. Deze maatstaf betekent niet noodzakelijkerwijs dat ze de inhoud volledig hebben bekeken, maar dat ze vooruit hadden kunnen slaan. Het betekent alleen dat ze het einde van de inhoud hebben bereikt. | `a.media.complete` |
| Gepauzeerde stromen | Een Booleaanse waarde die activeert wanneer een of meer pauzes zijn opgetreden tijdens het afspelen van inhoud. | Media sluiten | `a.media.pause` |
| Gebeurtenissen pauzeren | Het aantal pauzes dat is opgetreden tijdens een afspeelsessie. | Media sluiten | `a.media.pauseCount` |
| Totale pauzeduur | De totale duur van alle pauze-gebeurtenissen, in seconden. | Media sluiten | `a.media.pauseTime` |
| Inhoud start | Het eerste frame met media wordt gebruikt. Als een gebruiker tijdens een advertentie of tijdens het bufferen neerslaat, wordt deze gebeurtenis niet geactiveerd. | Media sluiten | `a.media.play` |
| 10% voortgangsmarkering | De afspeelkop geeft de 10%-markering van de inhoud door op basis van de lengte. Deze markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress10` |
| Voortgangsmarkering van 25% | De afspeelkop geeft de 25%-markering voor inhoud op basis van lengte door. Deze markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress25` |
| 50% voortgangsmarkering | De afspeelkop geeft de 50%-markering van inhoud op basis van lengte door. Deze markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress50` |
| 75% voortgangsmarkering | De afspeelkop geeft de 75%-markering voor inhoud op basis van lengte door. Deze markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress75` |
| 95% voortgangsmarkering | De afspeelkop geeft de 95%-markering voor inhoud op basis van lengte door. Deze markering wordt slechts één keer geteld, zelfs als u achterwaarts zoekt. Als u voorwaarts wilt zoeken, worden overgeslagen markeertekens niet geteld. | Media sluiten | `a.media.progress95` |
| Inhoud wordt hervat | Een Booleaanse waarde die activeert wanneer de inhoud wordt hervat na meer dan 30 minuten buffertijd, pauze of wachttijd. Wordt ook geactiveerd door de speler op de trackPlay VideoInfo. | Media sluiten | `a.media.resume` |
| Weergaven van inhoudssegmenten | Een Booleaanse waarde die activeert op het eerste frame van het bekeken segment. | Media sluiten | `a.media.segmentView` |
| Media wordt gestart | Een Booleaanse waarde die wordt geactiveerd wanneer het medium voor het eerst wordt geladen. Deze gebeurtenis bevat advertenties, buffering en fouten. | Start media | `a.media.view` |
| Tijd van inhoud besteed | De totale gebeurtenisduur voor alle gebeurtenissen van het type PLAY op de hoofdinhoud, in seconden. | Media sluiten | `a.media.timePlayed` |
| Unieke tijd die wordt afgespeeld | De totale hoeveelheid tijd dat de unieke inhoud wordt afgespeeld, in seconden. Deze metrische waarde sluit de tijd uit die wordt afgespeeld wanneer herhaalde inhoud wordt weergegeven, zoals achterwaarts zoeken. | Media sluiten | `a.media.uniqueTimePlayed` |

{style="table-layout:auto"}
