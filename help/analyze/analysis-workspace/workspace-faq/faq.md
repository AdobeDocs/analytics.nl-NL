---
description: Veelgestelde vragen over werkruimte
title: Veelgestelde vragen en werkruimte voor probleemoplossing
translation-type: tm+mt
source-git-commit: 7fbeac0488fbe9b3d10d7c1242f31250f1c7dc16

---


# Veelgestelde vragen

| Vraag | Antwoord |
|--- |--- |
| Wat zijn de eerste vereisten voor het gebruiken van de Werkruimte van de Analyse? | [Gegevens naar Adobe Analytics verzenden met Adobe Experience Platform Launch](/help/implement/launch/validate-publish-prod.md): Het gebruiken van de Werkruimte van de Analyse vereist een werkende implementatie. Zorg ervoor dat uw organisatie gegevens naar Adobe verzendt voordat u het hulpprogramma gebruikt. Andere implementaties, zoals DTM of oudere handmatige implementaties, kunnen ook werken. |
| Wat zijn het Beleid en de toegangseisen voor de Werkruimte van de Analyse? | Zie [Beheervereisten](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Zal het gebruiken van de Werkruimte van de Analyse gegevensinzameling beïnvloeden? | Aangezien de Werkruimte van de Analyse een rapporteringshulpmiddel is, heeft het geen invloed op gegevensinzameling. Er zijn geen gevolgen om zonder onderscheid componenten naar een project te slepen om te zien wat werkt. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is. Als u per ongeluk een ongeldige component naar uw werkruimteproject sleept of een stap wilt terugkeren, drukt u op ctrl+Z (Windows) of cmd+Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door op *[!UICONTROL Project][!UICONTROL New]*> in het menu linksboven te klikken. |
| Hoeveel rapportsuites kunnen in een project van de Werkruimte van de Analyse worden getoond? | U kunt projecten in de Werkruimte van de Analyse met gegevens van meer [veelvoudige rapportreeksen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html)nu tot stand brengen. |
| Hoe implementeert u de analysewerkruimte? | Er is geen speciale implementatie vereist. De analysewerkruimte is beschikbaar voor alle bedrijven met Analytics Standard of Premium. Nochtans, zijn de standaardtoestemmingen op inhoud (zoals rapportsuites en projectcomponenten) van toepassing, en voor het leiden en het delen van projecten. Zie [Beheer en Toegangsvereisten](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Wijzigt de vooraf geconfigureerde rapporten in Adobe Analytics in de analysewerkruimte? | Nee. Omdat dit een aparte omgeving is, zijn er geen wijzigingen in uw bestaande of vooraf geconfigureerde rapporten in Adobe Analytics. U kunt nog standaardrapporten &amp; Analytics en de rapporten van de Bouwer van het Rapport gebruiken gebruikend de Werkruimte van de Analyse. |
| Kan ik de Werkruimte van de Analyse voor het Warehouse van Gegevens gebruiken? | De Werkruimte van de analyse wordt niet geadviseerd voor bulkgegevensuitvoer. Het is een visualisatiewerkruimte die dashboardachtige analyseprojecten maakt. |
| Hoe kan ik prestaties van de Werkruimte van de Analyse optimaliseren? | Zie [Prestaties](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md)optimaliseren. |
| Hoe vergelijken de mogelijkheden van de Werkruimte van de Analyse met Ad hoc Analyse? | Zie [Analyse van werkruimte vergeleken met ad hoc Analyse](/help/analyze/analysis-workspace/workspace-faq/adhocanalysis-vs-analysisworkspace.md). |

## Problemen oplossen

**Wanneer ik metrisch over sleep, zegt het &quot;Ongeldige gegevens&quot;.**

Ongeldige gegevens betekenen dat Adobe geen gegevens kan retourneren met de combinatie van afmetingen en metriek die in het rapport wordt gebruikt. Twee metriek die bijvoorbeeld boven op elkaar zijn gestapeld, kunnen niet als gegevens worden geretourneerd, omdat er geen manier is om twee metriek op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

**Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul.**

Als u een werkruimterapport hebt gemaakt maar er geen gegevens zijn, kunt u een aantal dingen controleren:

* Controleer de rapportreeks tweemaal en zorg ervoor het met gegevens wordt bevolkt.
* Als u een segment in uw rapport toepaste, zouden de segmentcriteria geen gegevens kunnen aanpassen. Probeer het segment te verwijderen of de segmentdefinitie aan te passen.
* Controleer de datumwaaier in de hogere juiste hoek en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer naar uw website en gebruik [Foutopsporing](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) om te controleren of er gegevens worden verzameld.