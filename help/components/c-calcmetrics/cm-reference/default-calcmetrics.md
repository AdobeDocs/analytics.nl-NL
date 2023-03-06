---
description: Adobe verstrekt diverse berekende metriek die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Referentie van basisfuncties
feature: Calculated Metrics
exl-id: 1a49435c-96d1-4617-bd1a-a5d3b74e3ebd
source-git-commit: 2874ea66765e650a92bc39537d6a9eb8cebcd6a4
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 6%

---

# Standaard berekende cijfers

Adobe Analytics biedt verschillende Metriek Berekend voor de meest gebruikte gevallen. Deze berekende metriek zijn standaard beschikbaar in Analysis Workspace.

Hieronder volgt een lijst van elke Berekende metrische waarde die door Adobe wordt verstrekt, met de beoogde functie en de onderliggende formule die wordt gebruikt om deze te berekenen:

>[!NOTE]
>
>Naast de standaard Berekende metriek die op deze pagina wordt beschreven, kunt u extra Berekende Metriek aan een Reeks van het Rapport ook toevoegen.
>
>U kunt:
> * Standaardwaarden voor berekende metingen toevoegen voor streamingmedia, zoals beschreven in [Berekende cijfers](/https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * Aangepaste berekende metriek maken van bestaande metriek, zoals beschreven in [Berekende en Geavanceerde berekende (Afgeleide) Metriek](/help/components/c-calcmetrics/cm-overview.md).



| Berekende metrische naam | -functie | Formule |
|---------|----------|---------|
| Bouncepercentage | De verhouding tussen bezoeken die precies één treffer bevatten, en het aantal bezoeken op die pagina. Hierdoor kunt u beter begrijpen welke dimensie-items de hoogste stuitsnelheid hebben of kunt u een totale stuitsnelheid van uw site in de loop van de tijd zien. | Bouncepercentage |
| Ontvangsten/bezoekers | Het gemiddelde bedrag aan inkomsten dat door elke individuele bezoeker van de site wordt gegenereerd. | <p>Omzet</p><p>/</p><p>Unieke bezoekers</p> |
| Bestellingen/Bezoeker | Het gemiddelde aantal orders of transacties dat door elke individuele bezoeker van de site wordt gegenereerd | <p>Standaardvolgorde</p><p>/</p><p>Bezoeker</p> |
| Ontvangsten/bezoeken | Het gemiddelde bedrag aan inkomsten dat wordt gegenereerd door één enkel bezoek aan de locatie. | <p>Omzet</p><p>/</p><p>Unieke bezoeken</p> |
| Opbrengsten/opdracht | Het gemiddelde bedrag aan opbrengsten dat door elke voltooide transactie of opdracht op de locatie wordt gegenereerd. | <p>Omzet</p><p>/</p><p>Volgorde</p> |
| Bestellingen/bezoeken | Het percentage bezoeken aan de site dat resulteert in een voltooide transactie. | <p>Volgorde</p><p>/</p><p>Bezoeken</p> |
| Paginaweergaven/bezoeken | Het gemiddelde aantal pagina&#39;s dat een gebruiker weergeeft tijdens één bezoek aan de site. | <p>Paginaweergaven</p><p>/</p><p>Bezoeken</p> |
| Bezoeken/Bezoeker | Het gemiddelde aantal bezoeken dat een unieke bezoeker aan de site brengt. | <p>Bezoeken</p><p>/</p><p>Unieke bezoekers</p> |
| Opnieuw laden / Pagina&#39;s | Het percentage paginaweergaven dat heeft geresulteerd in het opnieuw laden of vernieuwen van de pagina. | <p>Opnieuw geladen</p><p>/</p><p>Paginaweergaven</p> |
| Gewogen stuiterende waarde | -functie | if(bezoeken>percentiel(bezoeken),bounceraat,0) |
| Assistenten bestellen | Het aantal keren dat een kanaal of bron heeft bijgedragen aan de reis van een klant naar een aankoop, maar niet tot de uiteindelijke aankoop heeft geleid. | <p>Bestellingen (deelname\|Bezoek)</p><p>-</p><p>Orders</p> |
| Afsluitingsfrequentie | Het percentage bezoekers dat de site verlaat na weergave van een bepaalde pagina. | <p>Gesloten</p><p>/</p><p>Bezoeken</p> |
| Invoersnelheid | Het percentage bezoekers dat de site op een bepaalde pagina is binnengekomen, in vergelijking met het totale aantal sessies op de site. | <p>Geopend</p><p>/</p><p>Bezoeken</p> |
| Gemiddelde tijd op de site | De gemiddelde hoeveelheid tijd die een bezoeker aan de plaats doorbrengt alvorens weg te gaan of weg te navigeren. | Gemiddelde tijd die op de site wordt besteed (seconden) |
| Tijd besteed/gebruiker (staat) | De tijdsduur dat de gemiddelde bezoeker in een bepaalde staat doorbrengt terwijl hij op de site is | Tijd besteed per bezoeker (seconden) metrisch + Mobiel App-segment |
| Gebruikers (mobiel) | Het totale aantal gebruikers van een mobiele app | Unieke metrische bezoekers + segment voor mobiele App Users |
| Toepassingsgebruikers | Het totale aantal gebruikers van een mobiele app | Unieke metrische bezoekers + Mobiel App-segment |
| Statusweergaven | Het aantal weergaven voor de verschillende staten of schermen van de app | Metrische paginaweergaven + Mobile App-segment |
| Handelingen | Het totale aantal acties dat in de app is uitgevoerd | De metrisch van de Instanties van de Verbinding van de douane + heeft een segment van de Actie |
| Koppelingsklikken bij overname | Het aantal keren dat de mensen op een verbinding klikken die wordt ontworpen om verkeer naar de plaats te drijven. | Metrische campagne-Click-through |
| Paginasnelheid | Het aantal extra paginaweergaven dat door een stuk inhoud wordt gegenereerd. Dit kan u helpen bepalen welke inhoud extra betrokkenheid drijft. | <p>Paginaweergaven</p><p>/</p><p>Bezoeken</p> |
| Omzetsnelheid | Het percentage bezoekers dat de gewenste actie heeft uitgevoerd, zoals een aankoop. | <p>Orders</p><p>/</p><p>Bezoeken</p> |
| Gemiddelde sessieduur (mobiel) | De gemiddelde hoeveelheid tijd die bezoekers gedurende één sessie aan de site doorbrengen. | Leeg |
| Experience Cloud ID-dekking | Het percentage bezoekers met een Experience Cloud-id. | <p>Bezoekers met Experience Cloud ID</p><p>/</p><p>Unieke bezoekers</p> |
| Contentsnelheid | De snelheid waarmee nieuwe inhoud wordt gemaakt en gepubliceerd op de site en hoe snel de betrokkenheid van de gebruiker wordt gegenereerd. | <p>Paginaweergaven</p><p>/</p><p>Bezoeken</p> |
| ITP 2.1 Unieke bezoekers / Unieke bezoekers | Het percentage unieke bezoekers dat een browser gebruikt die wordt beïnvloed door de cookiebeperkingen van ITP 2.1. Met andere woorden, klanten die geen implementatie CNAME gebruiken. (Dit geldt voor klanten die cookies instellen via JavaScript op de client.) | <p>Unieke Visitors - metrische informatie + ITP Visitors - segment</p><p>/</p><p>Unieke bezoekers</p> |
| Unieke bezoekers/unieke bezoekers die na 7 dagen terugkeren | Het percentage unieke bezoekers dat na een periode van 7 of meer dagen terugkeert. | <p>Unieke Visitors metrisch + Gebruikers die na 7 dagen segment terugkeren</p><p>/</p><p>Unieke bezoekers</p> |
| Paginaweergaven / Unieke bezoeker | Het gemiddelde aantal weergegeven pagina&#39;s voor elke unieke bezoeker van de site. | <p>Paginaweergaven</p><p>/</p><p>Unieke bezoekers</p> |
| Bezoekers | Het gemiddelde aantal bezoeken dat een unieke bezoeker aan de site brengt. | <p>Bezoeken</p><p>/</p><p>Unieke bezoekers</p> |
| Geschatte unieke bezoekers (ITP 2.1) | <p>Voor ITP-bezoekers (gebruikers in Safari-browsers) verdeelt Unieke bezoekers met 2 of minder.</p><p>Hierbij wordt ervan uitgegaan dat u cookies instelt met JavaScript op de client (geen CNAME-implementatie). Implementaties die cookies instellen met JavaScript op de client werden beïnvloed vanaf ITP 2.1. Zie: [https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/)</p> | <p>Unieke metrische bezoekers + ITP Bezoekers (ITP 2.1, niet-CNAME implementaties) segment</p><p>/</p><p>Unieke metrische bezoekers + het segment van de Bezoekers niet-ITP (ITP 2.1, niet-CNAME implementaties)</p> |
| Paginaweergaven / geschatte unieke bezoekers (ITP 2.1) | Het gemiddelde aantal weergegeven pagina&#39;s voor geschatte unieke bezoekers (ITP 2.1). | <p>Unieke metrische bezoekers + ITP Bezoekers (ITP 2.1, niet-CNAME implementaties) segment</p><p>/</p><p>Unieke metrische bezoekers + het segment van de Bezoekers niet-ITP (ITP 2.1, niet-CNAME implementaties)</p> |

{style="table-layout:auto"}
