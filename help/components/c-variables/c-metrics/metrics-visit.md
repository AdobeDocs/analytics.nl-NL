---
description: Een reeks paginaweergaven in een vergadering. Metrische bezoeken worden algemeen gebruikt in rapporten die het aantal gebruikerszittingen binnen de geselecteerde tijdspanne tonen.
keywords: visit
title: Bezoek
topic: Metrics
uuid: 91317487-f116-4546-8cd2-421418c49a7a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bezoek

Een reeks paginaweergaven in een vergadering. Metrische bezoeken worden algemeen gebruikt in rapporten die het aantal gebruikerszittingen binnen de geselecteerde tijdspanne tonen.

> [!NOTE] Voor informatie over hoe bezoeken en mobiele toepassingslanceringen worden berekend, zie Bezoeken en Mobiele Lanceringen [van de Toepassing van de](https://helpx.adobe.com/analytics/kb/compare-visits-and-mobile-app-launches.html) Vergelijking in de Kennisbank.

De meting van het bezoek wordt altijd geassocieerd met een tijdsperiode, zodat u weet of om een nieuw bezoek te tellen als de zelfde bezoeker aan uw plaats terugkeert. Een sessie begint wanneer de gebruiker voor het eerst op uw site arriveert en eindigt onder een van de volgende scenario&#39;s:

* **30 minuten inactiviteit:** Bijna alle sessies eindigen op deze manier. Als er meer dan 30 minuten zijn verlopen tussen afbeeldingsaanvragen, wordt een nieuw bezoek gestart.
* **12 uur consistente activiteit:** Als een gebruiker een verzoek om afbeeldingen gedurende 12 uur zonder tussenruimte van meer dan 30 minuten brandt, wordt automatisch een nieuw bezoek gestart.
* **2500 hits:** Als een gebruiker een groot aantal hits genereert zonder een nieuwe sessie te starten, wordt een nieuw bezoek geteld na 2500 afbeeldingsverzoeken.
* **100 hits in 100 seconden**: Als een bezoek uit meer dan 100 hits bestaat die in minder dan 100 seconden voorkomen, beëindigt het bezoek automatisch. Dit gedrag geeft typisch beide activiteit aan, en deze beperking wordt afgedwongen om deze verwerkings-intensieve bezoeken te verhinderen latentie te verhogen en de tijd te verhogen het vergt om rapporten te produceren.

> [!NOTE] De definitie van een bezoek kan voor een rapportreeks worden verkort indien specifiek gevraagd, maar het kan niet worden verlengd. Zorg ervoor dat een van de ondersteunde gebruikers van uw organisatie contact opneemt met de klantenservice om deze wijziging aan te vragen.

De volgende scenario&#39;s beginnen geen nieuw bezoek:

* De gebruiker die de tab sluit, deze opnieuw opent en binnen 30 minuten terugnavigeert naar uw site. De gebruiker kan ook zijn browser sluiten of de computer opnieuw opstarten en nog steeds als één bezoek worden geteld (als de bezoeker binnen de tijdsperiode van 30 minuten naar uw site terugkeert).
* Gebruikers die op meerdere tabbladen door uw site bladeren. Hoewel het bladeren met meerdere tabbladen bezoekers of bezoekers niet verhoogt, doet het gebruik van een aparte browser dit. De reden hiervoor is dat de verschillende tabbladen verwijzen naar dezelfde cookies, maar afzonderlijke browsers niet.

Een bezoek komt niet altijd overeen met een browsersessie. Als een bezoeker bijvoorbeeld de browser sluit, de browser opnieuw opent en vijf minuten later naar uw site komt, wordt dit herkend als een voortzetting van hetzelfde bezoek. Dit betekent ook dat als een bezoeker 35 minuten op de ene pagina blijft, het bezoek gesloten en verwerkt zal zijn, en een nieuw bezoek zal beginnen als zij door aan een andere pagina klikken.

Wanneer een bezoek eindigt, zijn alle variabelen met een bezoekafloop verlopen en blijven niet meer bestaan. De meting van het bezoeknummer wordt verhoogd bij het volgende bezoek voor deze bezoeker.

> [!NOTE] Als u Analytics gebruikt als rapportagebron voor Adobe Target, raadpleegt u het [minimaliseren van het aantal opgeblazen bezoekers en bezoekers in A4T](https://marketing.adobe.com/resources/help/en_US/target/a4t/minimizing-inflated-visit-and-visitor-counts-a4t.html) in de [!DNL Target] documentatie.

Raadpleeg de handleiding voor de implementatie van Adobe Analytics voor meer informatie [Unieke bezoekers](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_overview.html) identificeren.

**Tijdvakken**

Een bezoek wordt gerapporteerd in elke periode waarin de activiteit plaatsvond. Stel bijvoorbeeld dat een bezoek begint om 11.45 uur op 1 december en doorgaat tot 2 december om 12.30 uur. Het bezoek wordt geteld op 1 december en 2 december. Deze rapportage is van toepassing op andere tijdsperiodes, waaronder wekelijks, maandelijks, driemaandelijks en jaarlijks.
