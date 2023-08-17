---
description: Met Analytics for Target (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren.
title: Analyses voor venster Doel (A4T)
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 32dfab4b10d3637aba53081f747d2650fc33a8f0
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Analyses voor venster Doel (A4T)

Met het deelvenster Analyse voor doel (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren. Het stelt u ook in staat om optillen en vertrouwen te zien voor maximaal drie succesmetingen. Navigeer naar een rapportsuite met A4T-componenten om het deelvenster A4T te openen. Klik vervolgens op het deelvensterpictogram helemaal links en sleep het deelvenster Analyse voor doel naar uw Analysis Workspace-project.

Hier volgt een kort video-overzicht van het deelvenster A4T:

>[!VIDEO](https://video.tv.adobe.com/v/37247/?quality=12)

## Deelvensterinvoer {#Input}

U kunt het deelvenster A4T configureren met behulp van de volgende invoerinstellingen:

| Instelling | Beschrijving |
|---|---|
| Doelactiviteit | Selecteer een activiteit in de lijst Doelactiviteiten of sleep een activiteit vanuit de linkerrail. Opmerking: de lijst is gevuld met de laatste zes maanden van activiteiten die ten minste één hit hadden. Als u geen activiteit ziet in de lijst, kan deze ouder zijn dan 6 maanden. Het kan nog steeds worden toegevoegd vanaf de linkerspoorlijn, die een terugkijkperiode van maximaal 18 maanden heeft. |
| Werking | Selecteer uw ervaring met besturing. U kunt deze desgewenst wijzigen in de vervolgkeuzelijst. |
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
| Conversiepercentage | Metrisch/Normaliserend met succes |
| Optillen | Vergelijkt de omrekeningskoers voor elke ervaring met controle. Opmerking: Lift is een &#39;vergrendelde metrische methode&#39; voor het bepalen van de ervaring. Lift kan niet worden afgebroken of worden gebruikt met andere afmetingen. |
| Lift (onder) | Vertegenwoordigt de slechtste lift die een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben.<br>Zie [Statistische berekeningen](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html?lang=en) en [Complete betrouwbaarheidscalculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx?lang=en) Excel-bestand voor meer informatie. |
| Lift (middellang) | Vertegenwoordigt de middelpuntlift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben. Dit is &quot;optillen&quot;in Rapporten &amp; Analytics.<br>Zie [Statistische berekeningen](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html?lang=en) en [Complete betrouwbaarheidscalculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx?lang=en) Excel-bestand voor meer informatie. |
| Lift (boven) | Vertegenwoordigt de beste hefervaring een variant over de controle, met een 95% betrouwbaarheidsinterval kon hebben.<br>Zie [Statistische berekeningen](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html?lang=en) en [Complete betrouwbaarheidscalculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx?lang=en) Excel-bestand voor meer informatie. |
| Vertrouwen | De studenten t-test berekent het betrouwbaarheidsniveau, dat op de waarschijnlijkheid wijst dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Een vast voorwaardelijk opmaakbereik van 75%/85%/95% is toegepast op de metrische waarde. Deze opmaak kan indien nodig worden aangepast onder Kolominstellingen. Opmerking: Vertrouwen is een &#39;vergrendelde metrische waarde&#39; die wordt gebruikt voor de doelervaring. Vertrouwen kan niet worden afgebroken of met andere dimensies worden gebruikt.<br>Zie [Statistische berekeningen](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html?lang=en) en [Complete betrouwbaarheidscalculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx?lang=en) Excel-bestand voor meer informatie. |

Net als bij elk deelvenster in Analysis Workspace kunt u uw analyse voortzetten door extra tabellen toe te voegen en [visualisaties](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) Hiermee kunt u uw Adobe Target-activiteiten analyseren. U kunt ook een segment toepassen op deelvensterniveau of in de vrije-vormtabel. Als u deze tabel toevoegt in de vrije-vormtabel, moet u de tabel over de hele tabel bedekken om de berekening voor de lift en het vertrouwen te behouden. Segmenten op kolomniveau worden momenteel niet ondersteund.

## Veelgestelde vragen {#FAQ}

| Vraag | Antwoord |
|---|---|
| Welke activiteitentypes worden gesteund in A4T? | [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup.html) over welke soorten activiteiten worden ondersteund. |
| Worden berekende meetwaarden ondersteund in lift- en betrouwbaarheidsberekeningen? | Nee. [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) waarom berekende meetwaarden niet worden ondersteund in lift &amp; trust. Berekende metriek kunnen in A4T worden gebruikt rapporterend buiten deze metriek, echter. |
| Waarom zouden unieke bezoekers van Target en Analytics verschillen? | [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) informatie over variaties van unieke bezoekers tussen producten. |
| Wanneer ik een klapsegment voor een specifieke activiteit van het Doel in mijn analyse toepast, waarom zie ik verwante ervaringen terugkomen? | De dimensie A4T is een lijstvariabele, wat betekent het vele activiteiten (en ervaringen) in één keer kan bevatten. [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) |
| Worden extreme orders door de betrouwbaarheidsmaatstaf gecompenseerd of wordt een Bonferroni-correctie toegepast voor meerdere aanbiedingen? | Nee. [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) over hoe Analytics vertrouwen berekent. |
| Kunnen meetgegevens voor optillen en vertrouwen worden gebruikt met andere dimensies of uitsplitsingen? | Lift en het vertrouwen zijn &quot;gesloten metriek&quot;aan de dimensie van de Ervaringen van het Doel omdat zij een controle en een variant vereisen om over te berekenen. Als zodanig kunnen ze niet worden uitgesplitst of gebruikt met andere dimensies. |
| Wanneer wordt de lift en het vertrouwen opnieuw berekend? | U kunt optillen en vertrouwen op elk moment dat het deelvenster wordt uitgevoerd (of opnieuw wordt uitgevoerd), het datumbereik van het deelvenster wijzigen of een segment toepassen op het deelvenster of de tabel. Wanneer het toepassen van een segmentfilter op de vrije vormlijst, moet het over alle kolommen worden toegepast of de lift en het vertrouwen zal niet correct bijwerken. Op dit moment worden segmenten op kolomniveau niet ondersteund. |

Ga voor meer informatie over Analytics voor Target-rapportage naar [A4T-rapportage](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/reporting.html)
