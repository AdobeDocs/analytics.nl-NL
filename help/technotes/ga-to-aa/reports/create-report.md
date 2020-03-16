---
title: Een basisrapport maken in de analysewerkruimte
description: Leer hoe u een basisrapport maakt in de analysewerkruimte in een indeling die is afgestemd op gebruikers die vertrouwd zijn met hulpmiddelen van derden, zoals Google Analytics.
translation-type: tm+mt
source-git-commit: 099662d021c1919f0760e79154536cfd0e23e959

---


# Een basisrapport maken in de analysewerkruimte voor Google Analytics-gebruikers

De analysewerkruimte (een van de belangrijkste functies in Adobe Analytics) biedt een robuust gebied voor een gebruiker om inzicht te krijgen in verzamelde gegevens. Google Analytics en Adobe Analytics melden op zeer verschillende manieren:

* Met de rapportagestructuur in Google Analytics kunt u een bepaald type gegevens selecteren, zoals geografische locatie of verwijzingsverkeer. Het platform gebruikt een geprefabriceerde rapporteringsmening die op de verwachte beste manier wordt gebaseerd om die gegevens te bekijken.
* De rapportstructuur in de Werkruimte van de Analyse verstrekt een leeg canvas, dat meer flexibiliteit in het voldoen aan nauwkeurige rapporteringsbehoeften verstrekt.

Omdat de Werkruimte van de Analyse meer als een canvas dan geprefabriceerde rapporten werkt, is het opnieuw maken van rapporten van de Analyse van Google eenvoudig een kwestie van het gebruiken van de juiste visualisaties en de componenten.

## Belangrijkste termen die in Workspace worden gebruikt

* **Deelvensters** zijn de overkoepelende bouwstenen van de werkruimte. In bijna alle scenario&#39;s wordt een deelvenster Vrije vorm gebruikt.
* **Alle vrije-vormvensters worden weergegeven in visualisaties** . Hun doel is gegevens in verschillende formaten te vertegenwoordigen. Meestal is die indeling een tabel, maar soms gaat het om zaken als een donut of een lijngrafiek. Veel rapporten in Google Analytics bestaan uit het equivalent van twee visualisaties: een lijndiagram en een vrije-vormtabel.
* **Componenten** worden in een visualisatie geplaatst om gegevens te retourneren. Componenten kunnen op verschillende manieren worden gemengd om aan de rapportagebehoeften te voldoen.
   * **Dimensies** zijn variabele waarden en bevatten doorgaans tekst. Voorbeelden zijn paginanaam, verwijzende persoon of geografisch land. Ze worden meestal als rijen in een tabel weergegeven.
   * **Metrisch** zijn doorgaans een gebeurtenis of conversie van een bepaalde soort. Voorbeelden zijn veelvoorkomende gebeurtenissen zoals een paginaweergave of iets belangrijkers, zoals een aankoop of registratie. Ze worden meestal gezien als kolommen in tabellen om het aantal keren weer te geven dat de gebeurtenis per dimensie heeft plaatsgevonden.
   * **Segmenten** zijn een subset van uw gegevens en gedragen zich op dezelfde manier als segmenten in Google Analytics. Met deze filters kunt u aangepaste filters maken, zodat u zich kunt concentreren op een specifiek deel van uw gegevens.
   * **Met datumbereiken** kunt u gegevens ordenen op basis van het tijdstip waarop een gebeurtenis heeft plaatsgevonden. Zij zijn de backbone van het bekijken van tendensen in tijd, en typisch met metrisch samengevoegd.

## Een basisrapport maken in Workspace

Maak een rapport Alle pagina&#39;s (vergelijkbaar met het rapport in Google Analytics) door de juiste componenten naar een werkruimtekanvas te slepen.

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
1. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
1. Klik in de bovenste navigatiebalk op Werkruimte.
1. Klik op de knop Nieuw project maken.
1. Controleer of Leeg project is geselecteerd in het modaal pop-upmenu en klik vervolgens op Maken.
1. Links ziet u een lijst met afmetingen, metriek, segmenten en datumbereiken. Zoek de afmetingen voor de pagina&#39;s (oranje gekleurd) en sleep deze naar het canvas met de naam &#39;Een dimensie hier neerzetten&#39;.
1. Een rapport met de toppagina&#39;s voor deze maand kunt u zien. De Werkruimte van de analyse bevolkt automatisch het rapport met metrische [Gevallen](/help/components/c-variables/c-metrics/metrics-occurrences.md) .
1. Een tabel in Google Analytics bevat doorgaans 7-8 metriek. Zoek de metrische waarde voor de stuiteringssnelheid (groen gekleurd) en sleep deze naast de metrische koptekst Voorkomen. Als u de metrische waarde voor de stuiteringsfrequentie naast Voorvallen sleept, worden beide meetwaarden naast elkaar weergegeven.
1. Veel metriek kan naast elkaar worden geplaatst door metriek naast bestaande metrische kopballen te slepen. Zie [algemeen gebruikte metriek](common-metrics.md) voor informatie over hoe te om metriek te verkrijgen typisch die in de Analytics van Google wordt gebruikt.

   ![Nieuwe metrisch](/help/technotes/ga-to-aa/assets/new_metric.png)

## Begin met een vooraf gebouwd rapportmalplaatje in Werkruimte

Maak de sjabloon Inhoudsverbruik (vergelijkbaar met het rapport Alle pagina&#39;s in Google Analytics) door toegang te krijgen tot een projectsjabloon.

1. Klik op de knop Nieuw project maken.
1. Zoek en dubbelklik op het pictogram &#39;Inhoudsverbruik (web)&#39; onder Alle sjablonen.
1. Blader door alle vooraf gebouwde visualisaties: Stroom van invoerpagina, bovenste paginatabel, Stroom van pagina afsluiten, Stroom van sectie van entry-site en bovenste sitesecties.

   ![Sjabloonselectie](/help/technotes/ga-to-aa/assets/content_consumption_template.png)

## Experimenteren met het gereedschap

Aangezien de Werkruimte van de Analyse een rapporteringshulpmiddel is, heeft het geen invloed op gegevensinzameling. Er zijn geen gevolgen om zonder onderscheid componenten naar een project te slepen om te zien wat werkt. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is.

Als u per ongeluk een ongeldige component naar uw werkruimteproject sleept of een stap wilt terugkeren, drukt u op ctrl+Z (Windows) of cmd+Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door op *[!UICONTROL Project][!UICONTROL New]*> in het menu linksboven te klikken.

Adobe heeft veel functionaliteit in de Werkruimte van de Analyse in het klik contextmenu geplaatst. De meeste visualisaties en componenten kunnen voor meer gedetailleerde analyse en interactie met de rechtermuisknop worden geklikt. Overweeg met de rechtermuisknop op componenten in uw werkruimte te klikken om te zien welke opties beschikbaar zijn.

## Begrijp welke afmetingen en metriek aan gebruik zijn

Als u vertrouwd bent met de Analyse Workspace en een specifiek rapport wilt maken dat doorgaans wordt weergegeven in Google Analytics, zoekt u het rapport op de respectievelijke pagina:

* [Real-Time rapporten](realtime-reports.md)
* [Poortverslagen](audience-reports.md)
* [Overnameverslagen](acquisition-reports.md)
* [Gedragsrapporten](behavior-reports.md)
* [Conversierapporten](conversions-reports.md)
