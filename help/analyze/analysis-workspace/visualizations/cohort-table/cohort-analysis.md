---
title: Wat is Cohort Analyse en hoe werkt het?
description: Dig dieper in de gegevens rond uw publiek en onderbreek in verwante groepen met de Analyse van de Cohort. Meer informatie over cohortanalyse in Analysis Workspace.
feature: Visualisaties
role: User, Admin
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Meer informatie over [!UICONTROL Cohort Analysis] in Adobe Analytics

A *`cohort`* is een groep mensen die gemeenschappelijke kenmerken over een gespecificeerde periode delen. [!UICONTROL Cohort Analysis] is bijvoorbeeld handig als u wilt weten hoe een cohort werkt met een merk. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (Verklaringen van [!UICONTROL Cohort Analysis] zijn beschikbaar op het Web, zoals bij [Cohortanalyse 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke dimensies, metriek, en segmenten) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [Curate and Share](/help/analyze/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met [!UICONTROL Cohort Analysis]:

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Herken wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.
* Bekijk een [!UICONTROL Cohort Analysis] rapport binnen een Geleide Rapport van de Analyse.

[!UICONTROL Cohort Analysis] is beschikbaar voor alle Adobe Analytics-klanten met toegangsrechten tot  [!UICONTROL Analysis Workspace].

[Videozelfstudie](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace.html)  Cohortinganalyse (4:36)

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis]
>
>ondersteunt geen niet-segmenteerbare metriek (inclusief berekende metriek), niet-gehele metriek (zoals Opbrengst) of Voorvallen. Alleen metriek die in segmenten kan worden gebruikt, kan worden gebruikt in
>[!UICONTROL Cohort Analysis]en kunnen slechts met één worden verhoogd.

## Cohortanalyse-mogelijkheden

Met de volgende mogelijkheden kunt u de cohorten die u maakt, nauwkeurig instellen:

### [!UICONTROL Retention] Tabel

Het cohortrapport [!UICONTROL Retention] retourneert bezoekers: in elke gegevenscel worden het onbewerkte aantal en het onbewerkte percentage bezoekers in de cohort weergegeven die de actie in die periode hebben uitgevoerd . U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/retention-report.png)

### [!UICONTROL Churn] Tabel

Een [!UICONTROL Churn]-cohort is het omgekeerde van een retentietabel en toont de bezoekers die in de loop der tijd niet of niet aan de retourcriteria voor uw cohort hebben voldaan. U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/churn-report.png)

### [!UICONTROL Rolling Calculation]

Hiermee kunt u de retentie of het verloop berekenen op basis van de vorige kolom, niet de opgenomen kolom.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Tabel

Hiermee wordt de tijd gemeten die is verstreken vóór en na de opnemingsgebeurtenis. Dit is een uitstekend instrument voor pre- en postanalyse. De kolom **[!UICONTROL Included]** bevindt zich in het midden van de tabel en de tijdsperioden vóór en na de gebeurtenis include worden aan beide zijden weergegeven.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Maak cohorten op basis van een geselecteerde afmeting en niet op basis van een tijd, de standaardinstelling. Gebruik afmetingen zoals [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region] of een andere dimensie in Adobe Analytics om aan te geven hoe de retentie verandert op basis van de verschillende waarden van deze afmetingen.

![](assets/cohort-customizable-cohort-row.png)

Voor instructies op hoe te opstelling en een cohortrapport in werking te stellen, ga naar [vorm een rapport van de Analyse van de Cohort](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).
