---
description: Als u toepassingsbeheer inschakelt, worden de variabelen van de mobiele oplossing geactiveerd die de levensstijl en andere meetgegevens van mobiele toepassingen vastleggen.
title: Toepassingsbeheer
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---

# Toepassingsbeheer

Als u toepassingsbeheer inschakelt, worden de variabelen van de mobiele oplossing geactiveerd die de levensstijl en andere meetgegevens van mobiele toepassingen vastleggen.

Deze integratie tussen Adobe Analytics en mobiele services:

* Hiermee kunt u uw KPI-gegevens (Key Performance Indicator) delen van Mobile Services naar Adobe Analytics.
* Hiermee kunt u locatie bijhouden inschakelen.
* Hiermee voegt u nieuwe rapporten toe onder Analytics > Reports > Mobile App.
* Hiermee voegt u 25 nieuwe mobiele Adobe-classificaties toe.
* Hiermee voegt u 5 nieuwe mobiele Adobe-meetgegevens toe.
* Hiermee voegt u nieuwe mobiele Adobe-afmetingen toe.
* Synchroniseert elke 15 minuten data met Analytics

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL App Management]** > **[!UICONTROL App Reporting]**.

## Stap 1. App-rapporten inschakelen {#section_FBADF80AED2B4978A904ABB770B3B931}

Schakel App Reports v3.0 in om de volgende metingen te meten:

* **Verwerving** - URL&#39;s met verwijzingen bijhouden voor downloadcampagnes voor apps.
* **Levenscyclus** - het basisniveau van rapportage dat wordt verschaft door metingen die worden verzonden bij elke app-introductie.
* **Toepassingshandelingen** - rapporten en plakken op basis van handelingen in de app.
* **Lifetime-waarde** - Begrijp hoe gebruikers in de loop der tijd waarde opbouwen met app-KPI&#39;s (zoals aankopen, weergaven, voltooide video, sociale aandelen, uploaden van foto&#39;s).
* **Geteste gebeurtenissen** - meet de hoeveelheid tijd die verstrijkt (in-app en totale tijd) tussen de belangrijkste handelingen in de app (bijvoorbeeld het tijdstip voor de eerste aankoop).

## Stap 2. Locatie bijhouden inschakelen {#section_2CCBD205191C4CA3B7B71A6F11FF97EC}

Als u Locatie bijhouden inschakelt, kunt u:

* Breedte- en lengtegegevens bijhouden en hierover rapporteren in Analysis Workspace en Mobile Services.
* Identificeer, creeer en visualiseer specifieke Punten van Interesse (POIs) binnen de Mobiele Diensten. POI&#39;s moeten worden gedefinieerd in het configuratiebestand van de mobiele SDK.
* Bluetooth-bakens bijhouden (UUID, major, minor en proximity).

## Stap 3. (Optioneel) Verouderde rapportage en kenmerken voor achtergrondHits inschakelen/uitschakelen {#section_1708BCAA87AA4884986F7532759C5DD4}

Ingeschakelde achtergrondopdrachten (resultaten die worden gegenereerd wanneer de app op de achtergrond wordt uitgevoerd) betekenen dat deze als normale voorgrondhits worden behandeld. Zij komen nu voor in de reguliere rapportage en dit beïnvloedt ook de toerekening. Deze configuratie is gewoonlijk slechts wenselijk om consistentie met erfenisimplementaties te handhaven.

We raden u aan achtergrondtreffers op te nemen in een [virtuele rapportsuite](/help/components/vrs/vrs-about.md). Hierdoor kunt u de treffers zien, maar dit heeft geen negatieve invloed op het bezoek en het aantal bezoekers.
Mobiele classificaties worden ingeschakeld nadat u **[!UICONTROL App Management]** > **[!UICONTROL App Reporting]**.

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie als &#39;pop-muziektermen&#39; en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (ook bekend als Instanties). Klik-door), en omzetting aan succesgebeurtenissen.

| Classificatie | Definitie |
|--- |--- |
| Eerste startdatum | Datum van eerste lancering na installatie of herinstallatie.   MM/DD/YYYY |
| Toepassings-id | Hiermee slaat u de toepassingsnaam en -versie op in de volgende indeling:   `[AppName] [BundleVersion]`  Bijvoorbeeld: `myapp 1.1.` |
| Startnummer | Aantal keren dat de toepassing is gestart of van de achtergrond is verwijderd. |
| Dagen sinds eerste gebruik | Aantal dagen sinds eerste run. |
| Dagen sinds laatste gebruik | Aantal dagen sinds laatste gebruik. |
| Uur van dag | Meet het tijdstip waarop de app is gestart en gebruikt de numerieke notatie van 24 uur. Wordt gebruikt voor tijdsverdeling om piekgebruikstijden te bepalen. |
| Weekdag | Aantal weken dat de app is gestart. |
| Apparaatnaam | Hiermee slaat u de apparaatnaam op.  Een door komma&#39;s gescheiden tekenreeks van twee cijfers die het apparaat identificeert. Het eerste aantal vertegenwoordigt typisch de apparatengeneratie, en het tweede aantal versies verschillende leden van de apparatenfamilie. |
| Versie besturingssysteem | Versie van besturingssysteem. |
| Resolutie | Breedte x Hoogte in werkelijke pixels. |
| Lifetime-waarde (eVar) | Bevolkt door trackLifetimeValue-methoden. |
| Verwervingsbron |  |
| Aankoop normaal |  |
| Verwervingstermijn |  |
| Inhoud overname |  |
| Naam overname |  |
| Locatie (tot 10 km) | Bevolkt door trackLocation-methoden. |
| Locatie (tot 100 m) | Bevolkt door trackLocation-methoden. |
| Locatie (tot 1 m) | Bevolkt door trackLocation-methoden. |
| Naam van belangenpunt | Wordt gevuld door trackLocation-methoden wanneer het apparaat zich in een gedefinieerde POI bevindt. |
| Afstand tot belangencentrum | Wordt gevuld door trackLocation-methoden wanneer het apparaat zich in een gedefinieerde POI bevindt. |
| Berichtings-id in de app |  |
| Online bericht in de app |  |
| Inschakelen met duwen |  |
| Payload-id |  |
