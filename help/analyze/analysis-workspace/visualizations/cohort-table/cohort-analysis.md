---
title: Wat is Cohort Analyse en hoe werkt het?
description: Dig dieper in de gegevens rond uw publiek en onderbreek in verwante groepen met de Analyse van de Cohort. Meer informatie over cohortanalyse in Analysis Workspace.
feature: Cohort Analysis
role: User, Admin
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: fbb9c742ca169e727cffa9b8e5e93ba23ced0ebf
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Meer informatie over [!UICONTROL Cohort Analysis] in Adobe Analytics

A *`cohort`* is een groep personen die gemeenschappelijke kenmerken delen over een bepaalde periode. [!UICONTROL Cohort Analysis] is bijvoorbeeld handig als u wilt weten hoe een cohort werkt met een merk. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (Toelichting van [!UICONTROL Cohort Analysis] zijn beschikbaar op het web, bijvoorbeeld op [Cohortanalyse 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke dimensies, metriek, en segmenten) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [Curven en delen](/help/analyze/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met [!UICONTROL Cohort Analysis]:

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Herken wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.

[!UICONTROL Cohort Analysis] is beschikbaar voor alle Adobe Analytics-klanten met toegangsrechten voor [!UICONTROL Analysis Workspace].

Video over Cohort-tabellen in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/25965/?quality=12)

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] ondersteunt geen niet-segmenteerbare metriek (inclusief berekende metriek), niet-gehele metriek (zoals Opbrengst) of Voorvallen.
>
>Alleen metriek die in segmenten kan worden gebruikt, kan worden gebruikt in [!UICONTROL Cohort Analysis]en kunnen slechts met >1 tegelijk worden verhoogd.

## Cohortanalyse-mogelijkheden

Met de volgende mogelijkheden kunt u de cohorten die u maakt, nauwkeurig instellen:

### [!UICONTROL Retention] Tabel

A [!UICONTROL Retention] het cohort rapport geeft bezoekers terug : in elke gegevenscel worden het onbewerkte aantal en het onbewerkte percentage bezoekers in de cohort weergegeven die de actie in die periode hebben uitgevoerd . U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/retention-report.png)

Hier volgt een video over het berekenen van rolretentie:

>[!VIDEO](https://video.tv.adobe.com/v/25962/?quality=12)

### [!UICONTROL Churn] Tabel

A [!UICONTROL Churn] cohort is het omgekeerde van een retentietabel en toont de bezoekers die in de loop der tijd niet of niet aan de terugkeercriteria voor uw cohort voldeden. U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/churn-report.png)

Hier is een video over de analyse van de kurn:

>[!VIDEO](https://video.tv.adobe.com/v/25966/?quality=12)

### [!UICONTROL Rolling Calculation]

Hiermee kunt u de retentie of het verloop berekenen op basis van de vorige kolom, niet de opgenomen kolom.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Tabel

Hiermee wordt de tijd gemeten die is verstreken vóór en na de opnemingsgebeurtenis. Dit is een uitstekend instrument voor pre- en postanalyse. De **[!UICONTROL Included]** de kolom bevindt zich in het midden van de tabel en de tijdsperiodes voor en na de opnemingsgebeurtenis worden aan beide zijden weergegeven.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Maak cohorten op basis van een geselecteerde afmeting en niet op basis van een tijd, de standaardinstelling. Afmetingen gebruiken zoals [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region]of een andere dimensie in Adobe Analytics om aan te geven hoe de retentie verandert op basis van de verschillende waarden van deze dimensies.

![](assets/cohort-customizable-cohort-row.png)

Ga voor instructies over het instellen en uitvoeren van een cohortrapport naar [Een rapport Cohortanalyse configureren](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).
