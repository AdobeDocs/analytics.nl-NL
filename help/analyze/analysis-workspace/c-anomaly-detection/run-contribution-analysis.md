---
description: Leer hoe u een analyserapport over de bijdrage uitvoert in Analysis Workspace.
title: Bijdrageanalyse uitvoeren
role: User, Admin
exl-id: 20d1ba8d-3e4e-4702-ae28-5eb6bf00847b
feature: Anomaly Detection
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Bijdrageanalyse uitvoeren

[ Analyse van de Bijdrage ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) is een intensief machine het leren proces dat wordt ontworpen om contribuanten aan een waargenomen anomalie in Adobe Analytics te ontdekken. De bedoeling is de gebruiker te helpen om gebieden van nadruk of mogelijkheden voor extra analyse veel sneller te vinden dan anders mogelijk zou zijn.

>[!NOTE]
>
>De Analyse van de Bijdrage wordt slechts gesteund voor gegevens met dagelijkse granulariteit.

De volgende stappen moeten worden uitgevoerd:

1. Bijdrage-analyse in een project aanroepen.

   ![ de analyse van de Bijdrage van de Looppas ](assets/run-contribution-analysis.png)

   1. Selecteer in een lijnvisualisatie op basis van een vrije-vormtabel met dagelijkse korreligheid een afwijkend gegevenspunt. Selecteer **[!UICONTROL Analyze]** in het pop-upmenu.
   1. Selecteer **[!UICONTROL Run contribution analysis]** in een vrije-vormtabel met dagelijkse korreligheid in het contextmenu op een willekeurige rij. U kunt de analyse zelfs uitvoeren op rijen die geen anomalie tonen.
   1. In een vrije-vormlijst met dagelijkse korreligheid, op een rij die op een anomalie wijst:
      1. Selecteer de indicator ◥ .
      1. Van de ![ Alarm ](/help/assets/icons/Alert.svg) **[!UICONTROL Anomaly detected]** dialoog, uitgezochte **[!UICONTROL Open Contribution Analysis]**.



1. (Facultatief) u kunt het werkingsgebied van (en zo versnellen) de analyse beperken door [ exclusief dimensies ](#exclude-dimensions).

   ![ Excluding dimensies van de analyse van de Bijdrage ](assets/excluding-dimensions.png)

1. Selecteer **[!UICONTROL Run contribution analysis]**.

1. Wacht terwijl de bijdrageanalyse wordt verwerkt. De verwerking kan een aanzienlijke hoeveelheid tijd in beslag nemen, afhankelijk van de grootte van uw rapportsuite en het aantal dimensies. De analyse van de bijdrage voert analyse op de hoogste 50.000 punten per dimensie uit. U wordt ook op de hoogte gebracht over het aantal [ tokens van de bijdrageanalyse ](anomaly-detection.md#contribution-analysis-tokens) resterend.

   ![ analyse die van de Bijdrage ](assets/contribution-analysis-executing.png) uitvoert

1. Analysis Workspace laadt een nieuw **[!UICONTROL Contribution analysis]** -deelvenster rechtstreeks in dit project.

   ![ het paneel van de Analyse van de Bijdrage ](assets/contribution-analysis.png)

   * A [ summiere aantal ](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) visualisatie.
   * Een maandelijkse trended [ lijn ](/help/analyze/analysis-workspace/visualizations/line.md) visualisatie.
   * A **[!UICONTROL Top Items]** [ vrije lijst ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) die toont welke hoogste punten aan deze anomalie bijdragen, die door [ wordt gesorteerd de score van de Bijdrage ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis). De extra kolommen tonen metrisch in kwestie, en **[!UICONTROL Unique Visitors]** metrisch om context te verstrekken.

   * De **[!UICONTROL Generated Segments (Top Item Clusters)]** [ vrije lijst van de vrije vorm ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) identificeert verenigingen van hoogste punten die op de Score van de Bijdrage worden gebaseerd, anomalie voorkomen, en algemeen percentage bijdragend tot anomalische metrisch. Deze vereniging wordt dan gevangen als publiekssegment (Segment 1 van de Bijdrage, Segment 2 van de Bijdrage, enz.). Selecteer ![ Info ](/help/assets/icons/Info.svg) om de definitie van het segment te tonen, die hoogste punten omvat de segmenten uit worden samengesteld:


1. Aangezien de bijdrageanalyse nu deel van Analysis Workspace uitmaakt, kunt u uit een aantal van zijn eigenschappen van een vrije lijstcontextmenu voordeel halen om uw analyse nog betekenisvoller te maken, zoals:

   * [ onderbreking elk afmetingspunt door een andere afmeting ](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [ Trending één of meerdere rijen ](/help/analyze/analysis-workspace/home.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [ voeg een nieuwe visualisaties ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) toe
   * [ creeer alarm ](/help/components/alerts/alerts-overview.md)
   * [Maak of vergelijk segmenten.](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE]
>
>De anomalie die wordt geanalyseerd, wordt met een blauwe punt benadrukt binnen de Analyse van de Bijdrage en de projecten van de Intelligente Alarm verbonden aan het. Deze markering geeft een duidelijkere indicatie van de anomalie die wordt geanalyseerd.


## Afmetingen uitsluiten

Mogelijk wilt u bepaalde dimensies uitsluiten van de bijdrageanalyse. Het kan bijvoorbeeld zijn dat u helemaal niets aan uw browser of hardware kunt schelen en dat u de analyse wilt versnellen door deze te verwijderen.

De uitgesloten dimensie beheren:

* Sleep ongewenste afmetingen naar het deelvenster **[!UICONTROL Excluded Dimensions]** en sla de lijst op door op **[!UICONTROL Set as Default]** te klikken.

* Selecteer **[!UICONTROL Clear All]** om opnieuw te beginnen.

* Selecteer ![ Dimensies ](/help/assets/icons/Dimensions.svg) om een contextmenu te tonen en gebruik ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om het even welke geselecteerde uitgesloten afmeting uit de lijst te verwijderen.

  ![](assets/excluded-dimensions-list.png)

Nadat u de afmetingen hebt gewijzigd om uit te sluiten, selecteert u nogmaals **[!UICONTROL Run contribution analysis]** .

