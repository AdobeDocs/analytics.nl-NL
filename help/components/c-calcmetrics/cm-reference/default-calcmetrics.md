---
description: Adobe verstrekt diverse berekende metriek die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Berekende standaardwaarden
feature: Calculated Metrics
source-git-commit: b383e856374791be7d85b1f25566e8d98a099ec8
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 1%

---

# Berekende standaardwaarden

Adobe Analytics biedt verschillende berekende maatstaven voor de meest gebruikte gevallen. Deze berekende maatstaven zijn standaard beschikbaar in Analysis Workspace.

Hieronder volgt een lijst van elke berekende metrische waarde die door Adobe wordt verstrekt, met de beoogde functie en de onderliggende formule die wordt gebruikt om deze te berekenen:

>[!NOTE]
>
>Naast de standaard berekende metriek die op deze pagina wordt beschreven, kunt u extra berekende metriek aan een rapportreeks ook toevoegen.
>
>U kunt:
> * Standaardberekende waarden toevoegen voor streamingmedia, zoals beschreven in [Berekende cijfers](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * Aangepaste berekende metriek maken van bestaande metriek, zoals beschreven in [Berekende en geavanceerde berekende (afgeleide) meetwaarden](/help/components/c-calcmetrics/cm-overview.md).



| Metrische naam berekend | -functie | Formule |
|---------|----------|---------|
| Bouncepercentage | De verhouding tussen bezoeken die precies één treffer bevatten, en het aantal bezoeken op die pagina. Hierdoor kunt u beter begrijpen welke dimensie-items de hoogste stuitsnelheid hebben of kunt u een totale stuitsnelheid van uw site in de loop van de tijd zien. | `[Bounces] / [Entries]` |
| Ontvangsten/bezoekers | Het gemiddelde bedrag aan inkomsten dat door elke individuele bezoeker van de site wordt gegenereerd. | `[Revenue] / [Unique Visitors]` |
| Bestellingen/Bezoeker | Het gemiddelde aantal orders of transacties dat door elke individuele bezoeker van de site wordt gegenereerd | `[Orders] / [Unique Visitors]` |
| Ontvangsten/bezoeken | Het gemiddelde bedrag aan inkomsten dat wordt gegenereerd door één enkel bezoek aan de locatie. | `[Revenue] / [Visits]` |
| Opbrengsten/opdracht | Het gemiddelde bedrag aan opbrengsten dat door elke voltooide transactie of opdracht op de locatie wordt gegenereerd. | `[Revenue] / [Orders]` |
| Bestellingen/bezoeken | Het percentage bezoeken aan de site dat resulteert in een voltooide transactie. | `[Orders] / [Visits]` |
| Paginaweergaven/bezoeken | Het gemiddelde aantal pagina&#39;s dat een gebruiker weergeeft tijdens één bezoek aan de site. | `[Page Views] / [Visits]` |
| Bezoeken/Bezoeker | Het gemiddelde aantal bezoeken dat een unieke bezoeker aan de site brengt. | `[Visits] / [Unique Visitors]` |
| Opnieuw laden / Pagina&#39;s | Het percentage paginaweergaven dat heeft geresulteerd in het opnieuw laden of vernieuwen van de pagina. | `[Reloads] / [Page Views]` |
| Gewogen stuiterende waarde | -functie | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |
| Assistenten bestellen | Het aantal keren dat een kanaal of bron heeft bijgedragen aan de reis van een klant naar een aankoop, maar niet tot de uiteindelijke aankoop heeft geleid. | `[Orders (Visit Participation)] - [Orders]` |
| Afsluitingsfrequentie | Het percentage bezoekers dat de site verlaat na weergave van een bepaalde pagina. | `[Exits] / [Visits]` |
| Invoersnelheid | Het percentage bezoekers dat de site op een bepaalde pagina is binnengekomen, in vergelijking met het totale aantal sessies op de site. | `[Entries] / [Visits]` |
| Gemiddelde tijd op de site | De gemiddelde hoeveelheid tijd die een bezoeker aan de plaats doorbrengt alvorens weg te gaan of weg te navigeren. | `[Average Time Spent on Site (Seconds)]` |
| Tijd besteed/gebruiker (staat) | De tijdsduur dat de gemiddelde bezoeker in een bepaalde staat doorbrengt terwijl hij op de site is | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| Gebruikers (mobiel) | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Toepassingsgebruikers | Het totale aantal gebruikers van een mobiele app | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Statusweergaven | Het aantal weergaven voor de verschillende staten of schermen van de app | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| Handelingen | Het totale aantal acties dat in de app is uitgevoerd | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| Koppelingsklikken bij overname | Het aantal keren dat de mensen op een verbinding klikken die wordt ontworpen om verkeer naar de plaats te drijven. | `[Campaign Click-throughs]` |
| Paginasnelheid | Het aantal extra paginaweergaven dat door een stuk inhoud wordt gegenereerd. Dit kan u helpen bepalen welke inhoud extra betrokkenheid drijft. | `[Page Views] / [Visits]` |
| Omzetsnelheid | Het percentage bezoekers dat de gewenste actie heeft uitgevoerd, zoals een aankoop. | `[Orders] / [Visits]` |
| Gemiddelde sessieduur (mobiel) | De gemiddelde hoeveelheid tijd die bezoekers gedurende één sessie aan de site doorbrengen. | Leeg |
| Experience Cloud ID-dekking | Het percentage bezoekers met een Experience Cloud-id. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| Contentsnelheid | De snelheid waarmee nieuwe inhoud wordt gemaakt en gepubliceerd op de site en hoe snel de betrokkenheid van de gebruiker wordt gegenereerd. | `[Page Views] / [Visits]` |
| ITP 2.1 Unieke bezoekers / Unieke bezoekers | Het percentage unieke bezoekers dat een browser gebruikt die wordt beïnvloed door de cookiebeperkingen van ITP 2.1. Met andere woorden, klanten die geen implementatie CNAME gebruiken. (Dit geldt voor klanten die cookies instellen via JavaScript op de client.) | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| Unieke bezoekers/unieke bezoekers die na 7 dagen terugkeren | Het percentage unieke bezoekers dat na een periode van 7 of meer dagen terugkeert. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| Paginaweergaven / Unieke bezoeker | Het gemiddelde aantal weergegeven pagina&#39;s voor elke unieke bezoeker van de site. | `[Page Views] / [Unique Visitors]` |
| Bezoekers | Het gemiddelde aantal bezoeken dat een unieke bezoeker aan de site brengt. | `[Visits] / [Unique Visitors]` |
| Geschatte unieke bezoekers (ITP 2.1) | Voor ITP-bezoekers (gebruikers in Safari-browsers) verdeelt u Unieke bezoekers met 2 of minder. Deze berekende metrische waarde veronderstelt dat u koekjes gebruikend cliënt-kant JavaScript (het gebruiken van geen implementatie CNAME) plaatst. Implementaties die cookies instellen met JavaScript op de client werden beïnvloed vanaf ITP 2.1. Zie [Intelligente traceringspreventie](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) voor meer informatie. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Paginaweergaven / geschatte unieke bezoekers (ITP 2.1) | Het gemiddelde aantal weergegeven pagina&#39;s voor geschatte unieke bezoekers (ITP 2.1). | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |

{style="table-layout:auto"}
