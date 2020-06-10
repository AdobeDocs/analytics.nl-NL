---
description: Met Analytics for Target (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen analyseren in de analysewerkruimte.
title: Analyses voor venster Doel (A4T)
translation-type: tm+mt
source-git-commit: f688748e21b2b494845c682b380b12d3d346bfd3
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 3%

---


# Analyses voor venster Doel (A4T)

>[!IMPORTANT]
>
>**[!UICONTROL Analytics for Target (A4T)]** momenteel wordt slechts beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

Met het deelvenster Analyse voor doel (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen analyseren in de analysewerkruimte. Het stelt u ook in staat om optillen en vertrouwen te zien voor maximaal drie succesmetingen. Navigeer naar een rapportsuite met A4T-componenten om het deelvenster A4T te openen. Klik vervolgens op het deelvensterpictogram helemaal links en sleep de Analyse voor het deelvenster Doel naar het project Analyse-werkruimte.

## A4T Panel Builder

U kunt het deelvenster A4T als volgt configureren:

| Instelling | Beschrijving |
|---|---|
| Doelactiviteit | Selecteer een activiteit in de lijst Doelactiviteiten of sleep een activiteit vanuit de linkerrail.<br>**Opmerking:**De lijst bevat de laatste zes maanden van activiteiten die ten minste één hit hadden. Als u geen activiteit ziet in de lijst, kan deze ouder zijn dan 6 maanden. Het kan nog steeds worden toegevoegd vanaf de linkerspoorlijn, die een terugkijkperiode van maximaal 18 maanden heeft. |
| Controle | Selecteer uw ervaring met besturing. U kunt deze desgewenst wijzigen in de vervolgkeuzelijst. |
| Metrisch normaliseren | U kunt kiezen uit Unieke bezoekers, Bezoekingen of Activiteitenindrukkingen. Unieke bezoekers wordt aanbevolen voor de meeste gevallen waarin u analyses gebruikt. |
| Succeswaarden | Selecteer maximaal drie standaard (niet-berekende) succesgebeurtenissen uit de vervolgkeuzelijsten of sleep- en neerzetmetriek uit het linkerspoor. Elke metrisch zal een specifieke lijst en visualisatie in het teruggegeven paneel hebben. |
| Datumbereik van agenda | Deze wordt automatisch ingevuld op basis van het bereik van de activiteitsdatum van Adobe Target. U kunt deze desgewenst wijzigen. |

![](assets/a4t-panel-builder.png)

## Uitvoer van deelvenster A4T

Het deelvenster Analytics voor Target bevat een uitgebreide set gegevens en visualisaties waarmee u beter kunt begrijpen hoe uw Adobe Target-activiteiten en -ervaringen werken. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. U kunt het deelvenster op elk gewenst moment bewerken door in de rechterbovenhoek op het potlood te klikken.

Voor elke succesmetrische metrisch u selecteerde, zullen één vrije lijst en één trend van de omzettingssnelheid worden getoond:

![](assets/a4t-rendered.png)

Elke vrije-vormlijst toont de volgende metrische kolommen:

| Metrisch | Beschrijving |
|---|---|
| Metriek normaliseren | Unieke bezoekers, bezoeken of activiteitsimpressies. |
| Metrisch met succes | De metrische waarde die is geselecteerd in de builder |
| Omrekeningskoers | Metrisch/Normaliserend met succes |
| Optillen | Vergelijkt de omrekeningskoers voor elke ervaring met controle.<br>**Opmerking:**Optillen is een &quot;vergrendelde metrische methode&quot; voor doelervaringen; het kan niet worden uitgesplitst of met andere afmetingen worden gebruikt. |
| Lift (onder) | Vertegenwoordigt de slechtste lift een variantervaring over de controle kon hebben. |
| Lift (middellang) | Vertegenwoordigt de middelpuntlift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben. Dit is &quot;optillen&quot;in Rapporten &amp; Analytics. |
| Lift (boven) | Vertegenwoordigt de beste lift een variantervaring over de controle kon hebben. |
| Vertrouwen | De studenten t-test berekent het betrouwbaarheidsniveau, dat op de waarschijnlijkheid wijst dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Een vast voorwaardelijk opmaakbereik van 75%/85%/95% is toegepast op de metrische waarde. Deze opmaak kan indien nodig worden aangepast onder Kolominstellingen. <br>**Opmerking:**Vertrouwen is een &#39;vergrendelde maatstaf&#39; voor ervaringen met Adobe Target. Het kan niet worden gesplitst of met andere afmetingen worden gebruikt. |

Net als bij elk deelvenster in de analysewerkruimte kunt u uw analyse voortzetten door extra tabellen en [visualisaties](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) toe te voegen die u helpen uw Adobe-doelactiviteiten te analyseren.

## Veelgestelde vragen over het deelvenster A4T

| Vraag | Antwoord |
|---|---|
| Welke activiteitentypes worden gesteund in A4T? | [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup.html) informatie over welke typen activiteiten worden ondersteund. |
| Worden berekende metriek gesteund in A4T rapportering? | Nee. [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) weten over waarom berekende meetgegevens niet worden ondersteund? |
| Waarom zouden unieke bezoekers van Target en Analytics verschillen? | [Meer](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) informatie over variaties van unieke bezoekers tussen producten. |

Voor meer informatie over Analytics voor Target-rapportage gaat u naar [A4T-rapportage](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/reporting.html)
