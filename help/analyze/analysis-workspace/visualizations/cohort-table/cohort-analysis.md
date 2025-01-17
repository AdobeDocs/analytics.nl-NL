---
title: Wat is Cohort Analyse en hoe werkt het?
description: Dig dieper in de gegevens rond uw publiek en onderbreek in verwante groepen met de Analyse van de Cohort. Meer informatie over cohortanalyse in Analysis Workspace.
feature: Cohort Analysis
role: User, Admin
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: d4ad8b988ebcc177c76777b20a54cc20e8241d4d
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Overzicht van de cohortingtabel {#cohort-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_button"
>title="Cohortingtabel"
>abstract="Maak een cohortvisualisatie om gebruikers te groeperen op basis van de voltooiing van een gebeurtenis en de doorlopende betrokkenheid te analyseren en in de loop van de tijd te verdraaien."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_panel"
>title="Cohortingtabel"
>abstract="Groepeer gebruikers op basis van voltooiing van een gebeurtenis en analyseer vervolgens hun doorlopende betrokkenheid en loop de tijd door.<br/><br/>**Parameters **<br/>**criteria van de Opname**: De componenten die worden gebruikt om uw aanvankelijke bezoekerscohorts te bepalen.<br/>**criteria van de Terugkeer**: De componenten die worden gebruikt om te bepalen als een bezoeker is teruggekeerd."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

*Dit artikel documenteert de lijst van de Cohort in **Adobe Analytics**.<br/> zie [ Lijst van de Cohort ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/cohort-table/cohort-analysis) voor de **Customer Journey Analytics**versie van dit artikel.*

>[!ENDSHADEBOX]

Een *`cohort`* is een groep personen die gemeenschappelijke kenmerken delen over een opgegeven periode. [!UICONTROL Cohort Analysis] is bijvoorbeeld handig als u wilt weten hoe een cohort werkt met een merk. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (De Verklaringen van [!UICONTROL Cohort Analysis] zijn beschikbaar op het Web, zoals bij [ Analyse 101 van de Cohort ](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke dimensies, metriek, en segmenten) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [ Kromme en Aandeel ](/help/analyze/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u met [!UICONTROL Cohort Analysis] kunt doen:

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Herken wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.

[!UICONTROL Cohort Analysis] is beschikbaar voor alle Adobe Analytics-klanten met toegangsrechten tot [!UICONTROL Analysis Workspace] .

Video over Cohort-tabellen in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/25965/?quality=12)

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] biedt geen ondersteuning voor niet-segmenteerbare metriek (inclusief berekende metriek), niet-gehele metriek (zoals Opbrengst) of Voorvallen.
>
>Alleen metriek die in segmenten kan worden gebruikt, kan in [!UICONTROL Cohort Analysis] worden gebruikt en kan slechts met >1 tegelijk worden verhoogd.

## Cohortanalyse-mogelijkheden

De volgende secties beschrijven de eigenschappen van de Analyse van de Cohort die voor nauwkeurige controle over de cohorts toestaan u bouwt.

Voor meer gedetailleerde informatie over het creëren van een cohort en het runnen van a [!UICONTROL Cohort Analysis] rapport, zie [ een rapport van de Analyse van de Cohort ](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md) vormen.

### [!UICONTROL Retention] Tabel

Een [!UICONTROL Retention] -cohortrapport retourneert bezoekers: in elke gegevenscel worden het onbewerkte aantal en het onbewerkte percentage bezoekers in de cohort weergegeven die de actie tijdens die periode hebben uitgevoerd. U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/retention-report.png)

Hier volgt een video over het berekenen van rolretentie:

>[!VIDEO](https://video.tv.adobe.com/v/25962/?quality=12)

### [!UICONTROL Churn] Tabel

Een [!UICONTROL Churn] -cohort is het omgekeerde van een retentietabel en toont de bezoekers die in de loop der tijd niet of niet aan de retourcriteria voor uw cohort hebben voldaan. U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/churn-report.png)

Hier is een video over de analyse van de kurn:

>[!VIDEO](https://video.tv.adobe.com/v/25966/?quality=12)

### [!UICONTROL Rolling Calculation]

Hiermee kunt u de retentie of het verloop berekenen op basis van de vorige kolom, niet de opgenomen kolom.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Tabel

Hiermee wordt de tijd gemeten die is verstreken vóór en na de opnemingsgebeurtenis. Dit is een uitstekend instrument voor pre- en postanalyse. De kolom **[!UICONTROL Included]** bevindt zich in het midden van de tabel en de tijdsperioden vóór en na de gebeurtenis include worden aan beide zijden weergegeven.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Maak cohorten op basis van een geselecteerde afmeting en niet op basis van een tijd, de standaardinstelling. Gebruik afmetingen zoals [!UICONTROL marketing channel] , [!UICONTROL campaign] , [!UICONTROL product] , [!UICONTROL page] , [!UICONTROL region] of een andere dimensie in Adobe Analytics om te tonen hoe de retentie verandert op basis van de verschillende waarden van deze afmetingen.

![](assets/cohort-customizable-cohort-row.png)
