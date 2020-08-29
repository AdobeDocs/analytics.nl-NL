---
description: Met Analytics for Target (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren.
title: Analyses voor venster Doel (A4T)
translation-type: tm+mt
source-git-commit: 3d9bfabba6752f85173814c0e18d485122f7aa76
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 2%

---


# Analyses voor venster Doel (A4T)

Met het deelvenster Analyse voor doel (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren. Het stelt u ook in staat om optillen en vertrouwen te zien voor maximaal drie succesmetingen. Navigeer naar een rapportsuite met A4T-componenten om het deelvenster A4T te openen. Klik vervolgens op het deelvensterpictogram helemaal links en sleep het deelvenster Analyse voor doel naar uw Analysis Workspace-project.

## Deelvensterinvoer {#Input}

U kunt het deelvenster A4T configureren met behulp van de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Doelactiviteit | Selecteer een activiteit in de lijst Doelactiviteiten of sleep een activiteit vanuit de linkerrail.<br>**Opmerking:** De lijst bevat de laatste zes maanden van activiteiten die ten minste één hit hadden. Als u geen activiteit ziet in de lijst, kan deze ouder zijn dan 6 maanden. Het kan nog steeds worden toegevoegd vanaf de linkerspoorlijn, die een terugkijkperiode van maximaal 18 maanden heeft. |
| Controle | Selecteer uw ervaring met besturing. U kunt deze desgewenst wijzigen in de vervolgkeuzelijst. |
| Metrisch normaliseren | U kunt kiezen uit Unieke bezoekers, Bezoekingen of Activiteitenindrukkingen. Unieke bezoekers wordt aanbevolen voor de meeste gevallen waarin u analyses gebruikt. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast. |
| Succeswaarden | Selecteer maximaal drie standaard (niet-berekende) succesgebeurtenissen uit de vervolgkeuzelijsten of sleep- en neerzetmetriek uit het linkerspoor. Elke metrisch zal een specifieke lijst en visualisatie in het teruggegeven paneel hebben. |
| Datumbereik van agenda | Deze wordt automatisch ingevuld op basis van het bereik voor de activiteitsdatum van Adobe Target. U kunt deze desgewenst wijzigen. |

![Deelvensterbouwer](assets/a4t-panel-builder2.png)

## Deelvensteruitvoer {#Output}

De Analytics voor het paneel van het Doel keert een rijke reeks gegevens en visualisaties terug om u te helpen beter begrijpen hoe uw activiteit en ervaringen van Adobe Target presteren. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. U kunt het deelvenster op elk gewenst moment bewerken door in de rechterbovenhoek op het potlood te klikken.

Voor elke succesmetrische metrisch u selecteerde, zullen één vrije lijst en één trend van de omzettingssnelheid worden getoond:

![Gerenderd](assets/a4t-rendered.png)


Elke vrije-vormlijst toont de volgende metrische kolommen:

| Metrisch | Beschrijving |
|---|---|
| Metriek normaliseren | Unieke bezoekers, bezoeken of activiteitsimpressies. |
| Metrisch met succes | De metrische waarde die is geselecteerd in de builder |
| Omrekeningskoers | Metrisch/Normaliserend met succes |
| Optillen | Vergelijkt de omrekeningskoers voor elke ervaring met controle.<br>**Opmerking:** Lift is &quot;gesloten metrisch&quot;aan de Ervaringen van het Doel; het kan niet worden uitgesplitst of met andere afmetingen worden gebruikt. |
| Lift (onder) | Vertegenwoordigt de slechtste lift een variantervaring over de controle kon hebben. |
| Lift (middellang) | Vertegenwoordigt de middelpuntlift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben. Dit is &quot;optillen&quot;in Rapporten &amp; Analytics. |
| Lift (boven) | Vertegenwoordigt de beste lift een variantervaring over de controle kon hebben. |
| Vertrouwen | De studenten t-test berekent het betrouwbaarheidsniveau, dat op de waarschijnlijkheid wijst dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Een vast voorwaardelijk opmaakbereik van 75%/85%/95% is toegepast op de metrische waarde. Deze opmaak kan indien nodig worden aangepast onder Kolominstellingen. <br>**Opmerking:** Vertrouwen is &quot;gesloten metrisch&quot;aan de Ervaringen van het Doel; het kan niet worden uitgesplitst of met andere afmetingen worden gebruikt. |

Net als bij elk deelvenster in Analysis Workspace kunt u uw analyse voortzetten door extra tabellen en [visualisaties](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) toe te voegen die u helpen uw Adobe Target-activiteiten te analyseren.

## FAQs {#FAQ}

| Vraag | Antwoord |
|---|---|
| Welke activiteitentypes worden gesteund in A4T? | [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup.html) informatie over welke typen activiteiten worden ondersteund. |
| Worden berekende meetwaarden ondersteund in lift- en betrouwbaarheidsberekeningen? | Nee. [Lees meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) over waarom berekende meetgegevens niet worden ondersteund in lift en vertrouwen. Berekende metriek kunnen in A4T worden gebruikt rapporterend buiten deze metriek, echter. |
| Waarom zouden unieke bezoekers van Target en Analytics verschillen? | [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) informatie over variaties van unieke bezoekers tussen producten. |
| Wanneer ik een klapsegment voor een specifieke activiteit van het Doel in mijn analyse toepast, waarom zie ik verwante ervaringen terugkomen? | De dimensie A4T is een lijstvariabele, wat betekent het vele activiteiten (en ervaringen) in één keer kan bevatten. [Meer informatie](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) |
| Worden extreme orders door de betrouwbaarheidsmaatstaf gecompenseerd of wordt een Bonferroni-correctie toegepast voor meerdere aanbiedingen? | Nee. [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) informatie over hoe Analytics het vertrouwen berekent. |
| Kunnen meetgegevens voor optillen en vertrouwen worden gebruikt met andere dimensies of uitsplitsingen? | Lift en het vertrouwen zijn &quot;gesloten metriek&quot;aan de dimensie van de Ervaringen van het Doel omdat zij een controle en een variant vereisen om over te berekenen. Als zodanig kunnen ze niet worden uitgesplitst of gebruikt met andere dimensies. |
| Wanneer wordt de lift en het vertrouwen opnieuw berekend? | De optillen en het vertrouwen zullen op elk ogenblik opnieuw berekenen het paneel in werking wordt gesteld (of re-looppas), verandert de waaier van de paneeldatum, of een segment wordt toegepast op het paneel of de lijst. |

Voor meer informatie over Analytics voor Target-rapportage gaat u naar [A4T-rapportage](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/reporting.html)
