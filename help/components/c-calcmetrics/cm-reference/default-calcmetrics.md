---
description: Adobe biedt verschillende berekende maatstaven die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Berekende standaardwaarden
feature: Calculated Metrics
exl-id: 84468e63-f967-41cd-8084-525b1b90957a
source-git-commit: c132b21229aebea8121b156e1f4302a26b483ef5
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Berekende standaardwaarden

Adobe Analytics biedt verschillende berekende maatstaven voor de meest gebruikte gevallen. Deze berekende maatstaven zijn standaard beschikbaar in Analysis Workspace.

Hieronder volgt een lijst van elke berekende metrische waarde die door Adobe wordt verstrekt, met de beoogde functie en de onderliggende formule die wordt gebruikt om deze te berekenen:

>[!NOTE]
>
>Naast de standaard berekende metriek die op deze pagina wordt beschreven, kunt u extra berekende metriek aan een rapportreeks ook toevoegen.
>
>U kunt:
>
> * Voeg standaard berekende metriek voor de Streaming Inzameling van Media toe, zoals die in [ wordt beschreven Berekende metriek ](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html?lang=nl-NL)
> * Creeer douane berekende metriek van bestaande Metriek, zoals die in [ wordt beschreven Berekende en geavanceerde berekende metriek ](/help/components/c-calcmetrics/cm-overview.md).
>

>[!TIP]
>
>Gebruik het [ Woordenboek van Gegevens ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) om de definitie van een gebrek te inspecteren berekende metrisch en de individuele componenten die omhoog die definitie maken.
>



| Metrische naam berekend | Functie | Formule |
| --- | --- | --- |
| Koppelingsklikken bij overname | Het aantal keren dat de mensen op een verbinding klikken die wordt ontworpen om verkeer naar de plaats te drijven. | `[Campaign Click-throughs]` |
| Handelingen | Het totale aantal acties dat in de app is uitgevoerd | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| Toepassingsgebruikers | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Gemiddelde sessieduur (mobiel) | De gemiddelde tijd die bezoekers tijdens één sessie aan de site doorbrengen. | Leeg |
| Gemiddelde tijd op de site | De gemiddelde hoeveelheid tijd die een bezoeker aan de plaats doorbrengt alvorens of weg te gaan. | `[Average Time Spent on Site (Seconds)]` |
| Stuitsnelheid | De verhouding tussen bezoeken die precies één treffer bevatten, en het aantal bezoeken op die pagina. Deze metrische waarde kan u helpen begrijpen welke afmetingspunten de hoogste stuiterende tarief hebben, of om een bijeengevoegde totale stuitsnelheid van uw plaats in tijd te zien. | `[Bounces] / [Entries]` |
| Verhouding van beide paginaweergaven | De verhouding tussen beide paginaweergaven en het totale aantal paginaweergaven. | `[Bot Page Views] / [Page Views]` |
| Inhoudssnelheid | De snelheid waarmee nieuwe inhoud wordt gemaakt en gepubliceerd op de site en hoe snel de betrokkenheid van de gebruiker wordt gegenereerd. | `[Page Views] / [Visits]` |
| Conversiesnelheid | Het percentage bezoekers dat de gewenste actie heeft uitgevoerd, zoals een aankoop. | `[Orders] / [Visits]` |
| Invoersnelheid | Het percentage bezoekers dat de site op een bepaalde pagina is binnengekomen, in vergelijking met het totale aantal sessies op de site. | `[Entries] / [Visits]` |
| Geschatte unieke bezoekers (ITP 2.1) | Voor ITP-bezoekers (gebruikers in Safari-browsers) verdeelt u Unieke bezoekers met 2 of minder. Deze berekende metrisch veronderstelt dat u koekjes gebruikend cliënt-kant JavaScript (het gebruiken van geen implementatie CNAME) plaatst. Implementaties die cookies instellen met client-side JavaScript werden beïnvloed vanaf ITP 2.1. Zie [ Intelligente het volgen preventie ](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) voor details. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Experience Cloud ID-dekking | Het percentage bezoekers met een Experience Cloud-id. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| Afsluitingsfrequentie | Het percentage bezoekers dat de site verlaat na weergave van een bepaalde pagina. | `[Exits] / [Visits]` |
| ITP 2.1 Unieke bezoekers / Unieke bezoekers | Het percentage unieke bezoekers dat een browser gebruikt die wordt beïnvloed door de cookiebeperkingen van ITP 2.1. | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| Assistenten bestellen | Het aantal keren dat een kanaal of bron heeft bijgedragen aan de reis van een klant naar een aankoop, maar niet tot de uiteindelijke aankoop heeft geleid. | `[Orders (Visit Participation)] - [Orders]` |
| Bestellingen/bezoeken | Het percentage bezoeken aan de site dat resulteert in een voltooide transactie. | `[Orders] / [Visits]` |
| Bestellingen/Bezoeker | Het gemiddelde aantal orders of transacties dat door elke individuele bezoeker van de site wordt gegenereerd | `[Orders] / [Unique Visitors]` |
| Paginaweergaven / geschatte unieke bezoekers (ITP 2.1) | Het gemiddelde aantal weergegeven pagina&#39;s voor geschatte unieke bezoekers (ITP 2.1). | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Paginaweergaven / Unieke bezoeker | Het gemiddelde aantal weergegeven pagina&#39;s voor elke unieke bezoeker van de site. | `[Page Views] / [Unique Visitors]` |
| Paginaweergaven/bezoeken | Het gemiddelde aantal pagina&#39;s dat een gebruiker weergeeft tijdens één bezoek aan de site. | `[Page Views] / [Visits]` |
| Paginagrootte | Het aantal extra paginaweergaven dat door een stuk inhoud wordt gegenereerd. Deze maatstaf kan u helpen bepalen welke inhoud extra betrokkenheid drijft. | `[Page Views] / [Visits]` |
| Opnieuw laden / Pagina&#39;s | Het percentage paginaweergaven dat heeft geresulteerd in het opnieuw laden of vernieuwen van de pagina. | `[Reloads] / [Page Views]` |
| Opbrengsten/opdracht | Het gemiddelde bedrag aan opbrengsten dat door elke voltooide transactie of opdracht op de locatie wordt gegenereerd. | `[Revenue] / [Orders]` |
| Ontvangsten/bezoeken | Het gemiddelde bedrag aan inkomsten dat wordt gegenereerd door één enkel bezoek aan de locatie. | `[Revenue] / [Visits]` |
| Ontvangsten/bezoekers | Het gemiddelde bedrag aan inkomsten dat door elke individuele bezoeker van de site wordt gegenereerd. | `[Revenue] / [Unique Visitors]` |
| Statusweergaven | Het aantal weergaven voor de verschillende staten of schermen van de app | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| Tijd besteed/gebruiker (staat) | De tijdsduur dat de gemiddelde bezoeker in een bepaalde staat doorbrengt terwijl hij op de site is | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| Unieke bezoekers/unieke bezoekers die na 7 dagen terugkeren | Het percentage unieke bezoekers dat na een periode van 7 of meer dagen terugkeert. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| Gebruikers (mobiel) | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Bezoeken/Bezoeker | Het gemiddelde aantal bezoeken dat een unieke bezoeker aan de site brengt. | `[Visits] / [Unique Visitors]` |
| Gewogen stuiterende waarde | Functie | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |

{style="table-layout:auto"}
