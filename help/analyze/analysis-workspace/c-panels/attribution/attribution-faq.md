---
title: Veelgestelde vragen over kenmerken
description: Antwoorden op veelgestelde vragen over attributie.
translation-type: tm+mt
source-git-commit: f4fbe120e15d28da21b51849ff374ca4e2136ec7

---


# Veelgestelde vragen over kenmerken

**Wat is het regelitem &quot;Geen&quot; wanneer u een kenmerk gebruikt?**

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Probeer een langer tijdbereik op te nemen in het rapportvenster.

**Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?**

Deze extra datums zijn het gevolg van het terugzoekvenster van de bezoeker. Zie [Gegevens die buiten het rapporteringsvenster](https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html) in KB van Analytics voor meer informatie verschijnen. Adobe is van plan deze extra rijen in een volgende release uit te filteren.

**Kan ik een aangepast terugkijkvenster met mijn attributiemodellen gebruiken?**

Attributiemodellen vertrouwen momenteel op een bezoeker of een venster voor het terugzoeken van bezoekers. Één van beiden van deze raadplegingsvensters is aanpasbaar door of de rapporteringsdatumwaaier (voor bezoekersraadpleging) te veranderen of door een definitie van het douanebezoek als deel van virtuele rapportreeksen te gebruiken. Zie Tijdverwerking [van](../../../../components/vrs/vrs-report-time-processing.md) rapport voor meer informatie.

**Wanneer moet ik een terugzoekopdracht voor bezoekerskenmerk gebruiken?**

De keuze van de terugzoekfunctie voor attributie hangt af van het gebruikte geval. Als conversies doorgaans langer duren dan één bezoek, wordt het aangeraden een bezoeker terug te zoeken. Het maken van een virtuele rapportsuite met een definitie voor een langer bezoek is ook een potentiële oplossing.

**Hoe vergelijken props en eVars wanneer het gebruiken van attributie?**

Attribution wordt opnieuw berekend tijdens de uitvoering van het rapport, zodat er geen verschil is tussen een prop of eVar (of een andere dimensie) voor het maken van attributiemodellen. Props kunnen blijven bestaan met een terugzoekvenster of toewijzingsmodel en instellingen voor eVar-toewijzing/vervaldatum worden genegeerd.

**Zijn de attribuutmodellen beschikbaar in andere mogelijkheden van Analytics, zoals de Diefstal van Gegevens of het Pakhuis van Gegevens?**

Nee. De modellen van de attributie gebruiken rapporttijd verwerking, die slechts in de Werkruimte van de Analyse beschikbaar is. Zie Tijdverwerking [van](../../../../components/vrs/vrs-report-time-processing.md) rapport voor meer informatie.

**Zijn toewijzingsmodellen alleen beschikbaar als ik een virtuele rapportsuite gebruik waarvoor verwerking van rapporttijd is ingeschakeld?**

Attributiemodellen zijn beschikbaar buiten virtuele rapportsuites. Terwijl zij de verwerking van de rapporttijd op de achtergrond gebruiken, zijn de attributiemodellen beschikbaar aan zowel standaardrapportreeksen als virtuele rapportreeksen.

**Welke afmetingen en metriek worden niet gesteund?**

Het deelvenster Kenmerken ondersteunt alle afmetingen. Niet-ondersteunde meetgegevens zijn:

* Unieke bezoekers
* Bezoeken
* Voorval
* Paginaweergaven
* A4T-meetwaarden
* Metrische tijdwaarden
* Bounces
* Stuitpercentage
* Berichten
* Afsluiten
* Pagina&#39;s niet gevonden
* Zoekopdrachten
* Bezoeken van één pagina
* Enkelvoudige toegang

**Kan ik een aangepast terugkijkvenster met mijn attributiemodellen gebruiken?**

Ja, gebruikend de optie van het douane raadplegingsvenster, kunnen de raadplegingsvensters aan om het even welke datumwaaier tot 90 dagen voorafgaand aan uw rapporterend venster worden gevormd. Zie Tijdverwerking [van](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-report-time-processing.html) rapport voor meer informatie.

**Werkt de toewijzing met classificaties?**

Ja, classificaties worden volledig ondersteund.

**Werkt de toewijzing met gegevensbronnen?**

Ja, de meeste gegevensbronnen worden ondersteund. Attributie is niet mogelijk bij gegevensbronnen op overzichtsniveau omdat deze niet aan een bezoekersidentificatie van Analytics zijn gekoppeld. De gegevensbronnen van identiteitskaart van de transactie worden ook gesteund, tenzij zij in een virtuele rapportreeks met toegelaten verwerking van de rapporttijd worden gebruikt.

**Werkt attributie met de integratie van Advertising Analytics?**

Metagegevensafmetingen, zoals type en trefwoord, werken met kenmerk. Metrische gegevens (zoals afbeeldingen, kosten, klikken, gemiddelde positie en gemiddelde kwaliteitsscore) gebruiken echter gegevensbronnen op overzichtsniveau en zijn daarom niet compatibel.
