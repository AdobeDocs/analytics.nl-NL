---
description: Met Analytics for Target (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren.
title: Analyses voor venster Doel (A4T)
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 2aaa8c0d13755b40ec701ca6342ab773103a0422
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%

---

# Analyses voor venster Doel {#analyze-for-target-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_button"
>title="Analyses voor doel"
>abstract="Doelactiviteiten en ervaringen in Analysis Workspace analyseren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_panel"
>title="Analyses voor venster Doel"
>abstract="Doelactiviteiten en ervaringen in Analysis Workspace analyseren.<br/><br>**Parameters **<br/>**activiteit van het Doel**: De activiteit van het Doel die wordt geanalyseerd.<br/>**ervaring van de Controle**: De ervaring van de controle voor de geselecteerde activiteit van het Doel.<br/>**Normaliserend metrisch**: Bezoekers, bezoeken, of impressies. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast.<br/>**metriek van het Succes**: Tot 3 standaard (niet-berekende) succesmetriek om de activiteit van het Doel tegen te analyseren."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_Dit artikel documenteert Analytics voor het paneel van het Doel in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_zie [ het paneel van de Experimentatie ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/a4t-panel) voor informatie over hoe te om verschillende gebruikerservaringen, marketing, of overseinensvariaties in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** te vergelijken._

>[!ENDSHADEBOX]

Met het deelvenster Analyse voor doel kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren. Met dit deelvenster kunt u ook de optillen en het vertrouwen van maximaal drie succesmetingen bekijken. Navigeer naar een rapportsuite met Analytics voor Target-componenten voor toegang tot de Analytics voor het venster Doel. Selecteer vervolgens het deelvensterpictogram helemaal links en sleep het deelvenster Analyse voor doel naar uw Analysis Workspace-project.

+++Hier is een kort video-overzicht van het deelvenster Analytics voor Doel:

>[!VIDEO](https://video.tv.adobe.com/v/37247/?quality=12)

+++

## Gebruiken

Een deelvenster **[!UICONTROL Analytics for Target]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Analytics for Target]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.

1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.

### Deelvensterinvoer {#panel-nput}

U kunt Analytics voor het paneel van het Doel vormen gebruikend deze inputmontages:

![ A4T de input van het Comité ](assets/a4t-panel-input.png)

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Target Activity]** | Maak een keuze in een lijst met doelactiviteiten. De lijst is gevuld met de laatste zes maanden van activiteiten die ten minste één hit hadden. Als u geen activiteit ziet in de lijst, kan deze ouder zijn dan 6 maanden. Het kan nog steeds worden toegevoegd vanaf de linkerspoorlijn, die een terugkijkperiode van maximaal 18 maanden heeft. |
| **[!UICONTROL Control Experience]** | Selecteer de besturingservaring. |
| **[!UICONTROL Normalizing metric]** | Selecteer Bezoekers, Bezoekingen of Impressies. [!UICONTROL Visitors] wordt aanbevolen voor de meeste gevallen van analysegebruik. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast. |
| **[!UICONTROL Success metrics]** | Selecteer maximaal drie standaard (niet-berekende) succesgebeurtenissen in het keuzemenu of sleep en zet de metriek neer van Metrics in de rail Components. Elke metrisch heeft een specifieke lijst en visualisatie in het teruggegeven paneel. |

Selecteer **[!UICONTROL Build]** om het deelvenster te maken.

### Deelvensteruitvoer {#panel-output}

De Analytics voor het paneel van het Doel keert een rijke reeks gegevens en visualisaties terug om u te helpen beter begrijpen hoe uw activiteit en ervaringen van Adobe Target presteren. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. Voor elk succes selecteerde metrisch u, één [ Vrije lijst van de Vorm ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) en één [ lijn ](/help/analyze/analysis-workspace/visualizations/line.md) visualisatie die de trend van de omzettingstarief toont wordt getoond:

![ teruggegeven ](assets/a4t-panel-output.png)

Elke vrije-vormlijst toont de volgende metrische kolommen:

| Metrisch | Beschrijving |
|---|---|
| **[!UICONTROL Normalizing metrics]** | De normaliserende metrisch die in het inputpaneel wordt geselecteerd: Unieke Bezoekers, Bebezoeken, of de Impressies van de Activiteit. |
| **[!UICONTROL Success metric]** | De succesmetrische waarde die is geselecteerd in het invoerpaneel. |
| **[!UICONTROL Conversion rate]** | De metrische waarde voor Succes/Normalisatie. |
| **[!UICONTROL Lift]** | Vergelijkt de omrekeningskoers voor elke ervaring met controle. Nota: De lift is a *gesloten metrisch* aan de Ervaringen van het Doel; het kan niet worden gebroken of met andere afmetingen worden gebruikt. |
| **[!UICONTROL Lift (Lower)]** | Deze waarde vertegenwoordigt de slechtste lift die een variantervaring over de controle, met een 95% betrouwbaarheidsinterval zou kunnen hebben.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Lift (Mid)]** | Deze waarde vertegenwoordigt de middelpuntlift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben. <br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Lift (Upper)]** | Deze waarde vertegenwoordigt de beste lift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Confidence]** | De studenten t-test berekent het betrouwbaarheidsniveau, dat op de waarschijnlijkheid wijst dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Een vast voorwaardelijk opmaakbereik van 75%/85%/95% is toegepast op de metrische waarde. Deze opmaak kan indien nodig worden aangepast onder Kolominstellingen. Opmerking: Vertrouwen is een &#39;vergrendelde metrische waarde&#39; die wordt gebruikt voor de doelervaring. Vertrouwen kan niet worden afgebroken of met andere dimensies worden gebruikt.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |

Zoals met om het even welk paneel in Analysis Workspace, kunt u uw analyse voortzetten door extra lijsten en [ visualisaties ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations) toe te voegen die u helpen uw activiteiten van Adobe Target analyseren. U kunt ook een segment toepassen op deelvensterniveau of in de vrije-vormtabel. Als u deze tabel toevoegt in de vrije-vormtabel, moet u de tabel over de hele tabel bedekken om de berekening voor de lift en het vertrouwen te behouden. Segmenten op kolomniveau worden momenteel niet ondersteund.

Het gebruik ![ geeft ](/help/assets/icons/Edit.svg) uit om het paneel opnieuw te vormen en te bouwen.

## Veelgestelde vragen {#FAQ}

| Vraag | Antwoord |
|---|---|
| Welke activiteitstypen worden ondersteund in Analytics for Target? | [ leer meer ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup) over welke activiteitentypes worden gesteund. |
| Worden berekende meetwaarden ondersteund in lift- en betrouwbaarheidsberekeningen? | Nee. [ leer meer ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) over waarom de berekende metriek in lift &amp; vertrouwen niet gesteund zijn. Berekende metriek kan in Analytics voor Doel worden gebruikt rapporteert buiten deze metriek, echter. |
| Waarom zouden unieke bezoekers van Target en Analytics verschillen? | [ leer meer ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) over de variaties van unieke bezoekers tussen producten. |
| Wanneer ik een klapsegment voor een specifieke activiteit van het Doel in mijn analyse toepast, waarom zie ik verwante ervaringen terugkomen? | De analyse voor de dimensie van het Doel is een lijstvariabele, wat betekent het vele activiteiten (en ervaringen) kan tegelijkertijd bevatten. [Meer informatie](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) |
| Worden extreme orders door de betrouwbaarheidsmaatstaf gecompenseerd of wordt een Bonferroni-correctie toegepast voor meerdere aanbiedingen? | Nee. [ leer meer ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) over hoe de Analytics vertrouwen berekent. |
| Kunnen meetgegevens voor optillen en vertrouwen worden gebruikt met andere dimensies of uitsplitsingen? | Lift en het vertrouwen zijn &quot;gesloten metriek&quot;aan de dimensie van de Ervaringen van het Doel omdat zij een controle en een variant vereisen om over te berekenen. Als zodanig kunnen ze niet worden uitgesplitst of gebruikt met andere dimensies. |
| Wanneer wordt de lift en het vertrouwen opnieuw berekend? | U kunt optillen en vertrouwen altijd opnieuw berekenen wanneer het deelvenster wordt gemaakt, het datumbereik van het deelvenster wordt gewijzigd of een segment wordt toegepast op het deelvenster of de tabel. Wanneer u een segmentfilter op de vrije lijst toepast, moet het segment over alle kolommen worden toegepast of de lift en het vertrouwen werken niet correct bij. Segmenten op kolomniveau worden niet ondersteund. |

Voor meer informatie betreffende Analytics voor Doel het melden, bezoek [ Analytics voor Doel het melden ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/reporting)
