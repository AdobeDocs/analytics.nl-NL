---
description: In het rapport Single Page Visits (Bezoek één pagina) worden de pagina's die bezoekers van uw website invoeren en afsluiten weergegeven zonder stappen uit te voeren om andere pagina's weer te geven. Dit probleem is nu opgelost.
title: Bezoek één pagina
topic: Reports
uuid: 5ca52be8-c7f5-464a-8a06-55e8271760b4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bezoek één pagina

In het rapport Single Page Visits (Bezoek één pagina) worden de pagina&#39;s die bezoekers van uw website invoeren en afsluiten weergegeven zonder stappen uit te voeren om andere pagina&#39;s weer te geven. Dit probleem is nu opgelost.

Dit rapport wordt het meest meestal gebruikt in de context van het [!UICONTROL Pages] rapport, nochtans kan het ook in alle verkeersvariabelen met [!UICONTROL pathing] toegelaten worden bekeken. U kunt dit rapport gebruiken om invoerpagina&#39;s te identificeren die een bezoeker waarschijnlijk het minst zullen dwingen om uw site verder te verkennen, of om te bepalen hoeveel bezoeken uit één pagina bestaan. Met deze informatie kunt u de inhoud optimaliseren om het afsluiten op deze pagina&#39;s te beperken.

## Eigenschappen van rapport {#section_2D30F939FE0648EF983DD7C1BAB1181B}

* Een identiek rapport kan worden teruggewonnen door een [!UICONTROL Pages] rapport te trekken, gebruikend [!UICONTROL Single Access] als metrisch.

* Een bezoek van één pagina wordt beschouwd als een bezoek dat één unieke waarde bevat, en niet als één verzoek om een afbeelding.

   * In de context van een [pagina-rapport](/help/components/c-variables/dimensionslist/reports-pages.md)kan slechts één unieke pagina tijdens het bezoek worden geactiveerd.
   * In de context van een rapport [met](/help/components/c-variables/dimensionslist/reports-site-sections.md)sitesecties wordt één unieke sitesectie tijdens het bezoek geactiveerd.
   * In de context van een [verkeersvariabele](/help/admin/admin/c-traffic-variables/traffic-var.md), bevolkt een bezoek dit rapport als één enkele unieke waarde in brand wordt gestoken.

* Bezoeken op één pagina kunnen uit veel afbeeldingsverzoeken bestaan, zolang de variabele in de context van het rapport maar één unieke waarde bevat. Zodra een tweede unieke waarde is ingevuld, wordt het bezoek niet langer beschouwd als een bezoek van één pagina.
* Dit wordt beschouwd als een soort tekenrapport. Standaard is voor de [!UICONTROL Pages] variabele paden ingeschakeld. Nochtans, heeft om het even welke verkeersvariabele ook dit vermogen. Het toelaten van het kleven op extra verkeersvariabelen is afhankelijk van uw contract. Neem contact op met de accountmanager van uw organisatie voor meer informatie.
* Dit rapport kan een onderzoeksfilter gebruiken om van specifieke lijnpunten de plaats te bepalen.
* Dit rapport kan zowel in [trended](/help/components/c-variables/dimensionslist/reports-types.md) als in [gerangschikte](/help/components/c-variables/dimensionslist/reports-types.md) indelingen worden weergegeven.

* Dit rapport bevat geen uitsplitsingen.
* De enige metrische waarde beschikbaar binnen dit rapport is [!UICONTROL Visits].

