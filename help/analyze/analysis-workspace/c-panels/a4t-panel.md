---
description: Met Analytics for Target (A4T) kunt u uw Adobe Target-activiteiten en -ervaringen in Analysis Workspace analyseren.
title: Analyses voor venster Doel (A4T)
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 9a29057e71627d4c77a1d039d7fd5b0ec9c0f447
workflow-type: tm+mt
source-wordcount: '1129'
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
>abstract="Doelactiviteiten en ervaringen in Analysis Workspace analyseren.<br/><br>**Parameters **<br/>**activiteit van het Doel**: De activiteit van het Doel die zal worden geanalyseerd.<br/>**ervaring van de Controle**: De ervaring van de controle voor de geselecteerde activiteit van het Doel.<br/>**Normaliserend metrisch**: Bezoekers, bezoeken, of impressies. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast.<br/>**metriek van het Succes**: Tot 3 standaard (niet-berekende) succesmetriek om de activiteit van het Doel tegen te analyseren."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

*Dit artikel documenteert Analytics voor het paneel van het Doel in ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg)**Adobe Analytics**.<br/> zie [ het paneel van de Experimentatie ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/a4t-panel) voor informatie over hoe te om verschillende gebruikerservaringen, marketing, of overseinensvariaties in ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) te vergelijken **Customer Journey Analytics**.*

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

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Target Activity]** | Selecteer een activiteit in de lijst Doelactiviteiten of sleep een activiteit vanuit de linkerrail. Opmerking: de lijst is gevuld met de laatste zes maanden van activiteiten die ten minste één hit hadden. Als u geen activiteit ziet in de lijst, kan deze ouder zijn dan 6 maanden. Het kan nog steeds worden toegevoegd vanaf de linkerspoorlijn, die een terugkijkperiode van maximaal 18 maanden heeft. |
| **[!UICONTROL Control Experience]** | Selecteer uw ervaring met besturing. U kunt deze desgewenst wijzigen in de vervolgkeuzelijst. |
| **[!UICONTROL Normalizing metric]** | U kunt kiezen uit Unieke bezoekers, Bezoekingen of Activiteitenindrukkingen. Unieke bezoekers wordt aanbevolen voor de meeste gevallen waarin u analyses gebruikt. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Het beïnvloedt ook hoe de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast. |
| **[!UICONTROL Success metrics]** | Selecteer maximaal drie standaard (niet-berekende) succesgebeurtenissen uit de vervolgkeuzelijsten of sleep- en neerzetmetriek uit het linkerspoor. Elke metrisch zal een specifieke lijst en visualisatie in het teruggegeven paneel hebben. |
| C**[!UICONTROL alendar date range]* | Deze wordt automatisch ingevuld op basis van het bereik voor de activiteitsdatum van Adobe Target. U kunt deze desgewenst wijzigen. |

![ Bouwer van het Comité ](assets/a4t-panel-builder2.png)

### Deelvensteruitvoer {#panel-output}

De Analytics voor het paneel van het Doel keert een rijke reeks gegevens en visualisaties terug om u te helpen beter begrijpen hoe uw activiteit en ervaringen van Adobe Target presteren. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. U kunt het deelvenster op elk gewenst moment bewerken door in de rechterbovenhoek op het potlood te klikken.

Voor elke succesmetrische metrisch u selecteerde, zullen één vrije lijst en één trend van de omzettingssnelheid worden getoond:

![ teruggegeven ](assets/a4t-rendered.png)

Elke vrije-vormlijst toont de volgende metrische kolommen:

| Metrisch | Beschrijving |
|---|---|
| **[!UICONTROL Normalizing metrics]** | Unieke bezoekers, bezoeken of activiteitsimpressies. |
| **[!UICONTROL Success metric]** | De metrische waarde die is geselecteerd in de builder |
| **[!UICONTROL Conversion rate]** | Metrisch/Normaliserend met succes |
| **[!UICONTROL Lift]** | Vergelijkt de omrekeningskoers voor elke ervaring met controle. Opmerking: Lift is een &#39;vergrendelde metrische methode&#39; voor het bepalen van de ervaring. Lift kan niet worden afgebroken of worden gebruikt met andere afmetingen. |
| **[!UICONTROL Lift (Lower)]** | Vertegenwoordigt de slechtste lift die een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Lift (Mid)]** | Vertegenwoordigt de middelpuntlift een variantervaring over de controle, met een 95% betrouwbaarheidsinterval kon hebben. <br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Lift (Upper]**) | Vertegenwoordigt de beste hefervaring een variant over de controle, met een 95% betrouwbaarheidsinterval kon hebben.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |
| **[!UICONTROL Confidence]** | De studenten t-test berekent het betrouwbaarheidsniveau, dat op de waarschijnlijkheid wijst dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Een vast voorwaardelijk opmaakbereik van 75%/85%/95% is toegepast op de metrische waarde. Deze opmaak kan indien nodig worden aangepast onder Kolominstellingen. Opmerking: Vertrouwen is een &#39;vergrendelde metrische waarde&#39; die wordt gebruikt voor de doelervaring. Vertrouwen kan niet worden afgebroken of met andere dimensies worden gebruikt.<br> zie [ Statistische berekeningen ](https://experienceleague.adobe.com/docs/target/using/reports/statistical-methodology/statistical-calculations.html) en [ Volledige het dossier van Excel van de Rekenmachine van het Vertrouwen ](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) voor meer informatie. |

Zoals met om het even welk paneel in Analysis Workspace, kunt u uw analyse voortzetten door extra lijsten en [ visualisaties ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) toe te voegen die u zullen helpen uw activiteiten van Adobe Target analyseren. U kunt ook een segment toepassen op deelvensterniveau of in de vrije-vormtabel. Als u deze tabel toevoegt in de vrije-vormtabel, moet u de tabel over de hele tabel bedekken om de berekening voor de lift en het vertrouwen te behouden. Segmenten op kolomniveau worden momenteel niet ondersteund.

## Veelgestelde vragen {#FAQ}

| Vraag | Antwoord |
|---|---|
| Welke activiteitstypen worden ondersteund in Analytics for Target? | [ leer meer ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup.html) over welke activiteitentypes worden gesteund. |
| Worden berekende meetwaarden ondersteund in lift- en betrouwbaarheidsberekeningen? | Nee. [ leer meer ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) over waarom de berekende metriek in lift &amp; vertrouwen niet gesteund zijn. Berekende metriek kan in Analytics voor Doel worden gebruikt rapporteert buiten deze metriek, echter. |
| Waarom zouden unieke bezoekers van Target en Analytics verschillen? | [ leer meer ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) over varianties van unieke bezoekers tussen producten. |
| Wanneer ik een klapsegment voor een specifieke activiteit van het Doel in mijn analyse toepast, waarom zie ik verwante ervaringen terugkomen? | De analyse voor de dimensie van het Doel is een lijstvariabele, wat betekent het vele activiteiten (en ervaringen) kan tegelijkertijd bevatten. [Meer informatie](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) |
| Worden extreme orders door de betrouwbaarheidsmaatstaf gecompenseerd of wordt een Bonferroni-correctie toegepast voor meerdere aanbiedingen? | Nee. [ leer meer ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) over hoe de Analytics vertrouwen berekent. |
| Kunnen meetgegevens voor optillen en vertrouwen worden gebruikt met andere dimensies of uitsplitsingen? | Lift en het vertrouwen zijn &quot;gesloten metriek&quot;aan de dimensie van de Ervaringen van het Doel omdat zij een controle en een variant vereisen om over te berekenen. Als zodanig kunnen ze niet worden uitgesplitst of gebruikt met andere dimensies. |
| Wanneer wordt de lift en het vertrouwen opnieuw berekend? | U kunt optillen en vertrouwen op elk moment dat het deelvenster wordt uitgevoerd (of opnieuw wordt uitgevoerd), het datumbereik van het deelvenster wijzigen of een segment toepassen op het deelvenster of de tabel. Wanneer het toepassen van een segmentfilter op de vrije vormlijst, moet het over alle kolommen worden toegepast of de lift en het vertrouwen zal niet correct bijwerken. Op dit moment worden segmenten op kolomniveau niet ondersteund. |

Voor meer informatie betreffende Analytics voor Doel het melden, bezoek [ Analytics voor Doel het melden ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/reporting.html)
