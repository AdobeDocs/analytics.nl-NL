---
title: Een basisrapport maken in Analysis Workspace
description: Leer hoe u een basisrapport maakt in Analysis Workspace in een indeling die is afgestemd op gebruikers die vertrouwd zijn met hulpmiddelen van derden, zoals Google Analytics.
feature: Third-party Integration
exl-id: 513da3f1-ad24-4d5b-bc35-dbcd3694cbdf
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 18%

---

# Een basisrapport maken in Analysis Workspace voor gebruikers van Google Analytics

Analysis Workspace (een van de belangrijkste functies in Adobe Analytics) biedt een robuust gebied voor een gebruiker om inzicht te krijgen in verzamelde gegevens. De rapportage is zeer verschillend tussen Google Analytics en Adobe Analytics:

* Met de rapportstructuur in Google Analytics kunt u een bepaald type gegevens selecteren, zoals de geografische locatie of het verwijzingsverkeer. Het platform gebruikt een geprefabriceerde rapporteringsmening die op de verwachte beste manier wordt gebaseerd om die gegevens te bekijken.
* De rapportagestructuur in Analysis Workspace biedt een leeg canvas, waardoor u meer flexibiliteit hebt bij het voldoen aan de exacte rapportagevereisten.

Omdat Analysis Workspace meer als een canvas dan prefabriceerde rapporten werkt, is het opnieuw maken van rapporten van Google Analytics eenvoudig een kwestie van het gebruiken van de juiste visualisaties en de componenten.

## Belangrijkste termen die in Workspace worden gebruikt

* **Deelvensters** Dit zijn de overkoepelende bouwstenen van de werkruimte. In bijna alle scenario&#39;s wordt een deelvenster Vrije vorm gebruikt.
* **Visualisaties** Maak alle vrije-vormpanelen. Hun doel is gegevens in verschillende formaten te vertegenwoordigen. Meestal is die indeling een tabel, maar soms gaat het om zaken als een donut of een lijngrafiek. Veel rapporten in Google Analytics bestaan uit het equivalent van twee visualisaties: een lijndiagram en een vrije-vormtabel.
* **Componenten** worden in een visualisatie geplaatst om gegevens te retourneren. Componenten kunnen op verschillende manieren worden gemengd om aan de rapportagebehoeften te voldoen.
   * **Dimension** Dit zijn variabele waarden en bevatten doorgaans tekst. Voorbeelden zijn paginanaam, verwijzende persoon of geografisch land. Ze worden meestal als rijen in een tabel weergegeven.
   * **Metrisch** betekent doorgaans een gebeurtenis of conversie van een bepaalde soort. Voorbeelden zijn veelvoorkomende gebeurtenissen zoals een paginaweergave of iets belangrijkers, zoals een aankoop of registratie. Ze worden meestal gezien als kolommen in tabellen om het aantal keren weer te geven dat de gebeurtenis per dimensie heeft plaatsgevonden.
   * **Segmenten** zijn een subset van uw gegevens en gedraagt zich op dezelfde manier als segmenten in Google Analytics. Met deze filters kunt u aangepaste filters maken, zodat u zich kunt concentreren op een specifiek deel van uw gegevens.
   * **Datumbereiken** Hiermee kunt u gegevens ordenen op het moment dat een gebeurtenis heeft plaatsgevonden. Zij zijn de backbone van het bekijken van tendensen in tijd, en typisch met metrisch samengevoegd.

## Een basisrapport maken in Workspace

Maak een rapport Alle pagina&#39;s (vergelijkbaar met het rapport in Google Analytics) door de juiste componenten naar een werkruimtekanvas te slepen.

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
1. Klik in de bovenste navigatiebalk op Workspace.
1. Klik op de knop &#39;Create New Project&#39; (Nieuw project maken).
1. Controleer of de optie voor &#39;Leeg project&#39; is geselecteerd in het modale pop-upmenu en klik vervolgens op Create (Maken).
1. Links ziet u een lijst met afmetingen, metriek, segmenten en datumbereiken. Zoek de pagina-afmetingen (oranje gekleurd) en sleep deze naar het canvas met de naam &#39;Hier een Dimension neerzetten&#39;.
1. Een rapport met de toppagina&#39;s voor deze maand kunt u zien. Analysis Workspace vult het rapport automatisch in met de opdracht [Voorval](/help/components/metrics/occurrences.md) metrisch.
1. Een tabel in Google Analytics bevat doorgaans 7-8 cijfers. Zoek de metrische waarde voor de stuiteringssnelheid (groen gekleurd) en sleep deze naast de metrische koptekst Voorkomen. Als u de metrische waarde voor de stuiteringsfrequentie naast Voorvallen sleept, worden beide meetwaarden naast elkaar weergegeven.
1. Veel metriek kan naast elkaar worden geplaatst door metriek naast bestaande metrische kopballen te slepen. Zie [algemeen gebruikte meeteenheden](common-metrics.md) voor informatie over hoe te om metriek te verkrijgen typisch die in Google Analytics wordt gebruikt.

   ![Nieuwe metrisch](/help/technotes/ga-to-aa/assets/new_metric.png)

## Begin met een vooraf gebouwd rapportmalplaatje in Werkruimte

Creeer het malplaatje van de Consumptie van de Inhoud (gelijkend op het Alle Rapport van Pagina&#39;s in Google Analytics) door tot een projectmalplaatje toegang te hebben.

1. Klik op de knop &#39;Create New Project&#39; (Nieuw project maken).
1. Zoek en dubbelklik op het pictogram &#39;Inhoudsverbruik (web)&#39; onder Alle sjablonen.
1. Blader door alle vooraf gebouwde visualisaties: Stroom van invoerpagina, bovenste paginatabel, Stroom van pagina afsluiten, Stroom van sectie van entry-site en bovenste sitesecties.

   ![Sjabloonselectie](/help/technotes/ga-to-aa/assets/content_consumption_template.png)

## Experimenteren met de tool

Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metrics naar uw Workspace-project om te zien wat er beschikbaar is.

Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op *[!UICONTROL Project] > [!UICONTROL New]*.

Adobe heeft veel functionaliteit in Analysis Workspace geplaatst in het contextmenu dat met de rechtermuisknop wordt geopend. De meeste visualisaties en componenten kunnen voor meer gedetailleerde analyse en interactie met de rechtermuisknop worden geklikt. Overweeg met de rechtermuisknop op componenten in uw werkruimte te klikken om te zien welke opties beschikbaar zijn.

## Begrijp welke afmetingen en metriek aan gebruik zijn

Als u vertrouwd bent met Analysis Workspace en een specifiek rapport wilt maken dat doorgaans wordt weergegeven in Google Analytics, zoekt u het rapport op de desbetreffende pagina:

* [Real-Time rapporten](realtime-reports.md)
* [Poortverslagen](audience-reports.md)
* [Overnameverslagen](acquisition-reports.md)
* [Gedragsrapporten](behavior-reports.md)
* [Conversierapporten](conversions-reports.md)
