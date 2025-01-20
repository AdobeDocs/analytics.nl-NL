---
title: Vrije-vormtabel
description: Vrije-vormtabellen vormen de basis voor gegevensanalyse in Workspace
feature: Freeform Tables
role: User, Admin
exl-id: 7a0432f9-2cab-47be-bbd6-ede96cb840a3
source-git-commit: 76abe4e363184a9577622818fe21859d016a5cf7
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Vrije-vormtabel {#freeform-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_button"
>title="Vrije-vormtabel"
>abstract="Maak een lege visualisatie voor vrije tabellen die u kunt opbouwen met dimensies, segmenten, metriek en datumbereiken. U kunt de vrije-vormlijst als basis voor andere visualisaties gebruiken."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de Freeform lijstvisualisatie in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_zie [ Vrije lijst ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/freeform-table/freeform-table) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

In Analysis Workspace is een Freeform-tabel de basis voor interactieve gegevensanalyse. U kunt een combinatie [ componenten ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) in rijen en kolommen slepen en laten vallen om een douanetabel voor uw analyse tot stand te brengen. Aangezien elke component wordt gelaten vallen, werkt de lijst onmiddellijk bij, zodat kunt u snel analyseren en dieper graven.

## Een eenvoudige tabel voor vrije vorm maken

U begint met een lege Vrije-vormtabel.

![ Lege Vrije Lijst van de Vorm ](assets/freeform-table-1.png)

Als u de **[!UICONTROL ** bezoeken **]** metrisch op de **[!UICONTROL ** Daling hier metrisch (of een andere component) **]** laat vallen, bevolkt de Vrije Lijst automatisch met bezoeken per dag voor de kalenderperiode u selecteerde.

![ bezoeken Vrije Lijst van de Vorm ](assets/freeform-table-2.png)

Als u dan de **[!UICONTROL ** dimensie van de Pagina **]** laat vallen om de **[!UICONTROL ** 3} dimensie van de Dag te vervangen kolom, wijst de Freeform lijst automatisch op bezoeken voor elke pagina.**]**

![ bezoeken door de Lijst van de Vrije Vorm van de Pagina ](assets/freeform-table-3.png)

U kunt dan onderbreken, bijvoorbeeld, de **[!UICONTROL ** categorie:5 **]** pagina door de **[!UICONTROL ** dimensie van het Kanaal van de Marketing **]** op de **[!UICONTROL ** categorie te laten vallen:5 **]** rij.

![ de Uitsplitsing van bezoeken door de Lijst van de Vrije Vorm van de Pagina ](assets/freeform-table-4.png)


## Geautomatiseerde tabellen

Zoals hierboven geïllustreerd, is de snelste manier om een lijst te bouwen direct componenten in een leeg project, een paneel, of een vrije vormlijst te laten vallen. Een vrije-vormlijst zal automatisch voor u in een geadviseerde formaat worden gebouwd. [ bekijk het leerprogramma ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/auto-build-freeform-tables-in-analysis-workspace.html).

![](assets/automated-table.png)

## Opbouwfunctie voor tabellen met vrije vorm

Als u verkiest om verscheidene componenten aan uw lijst eerst toe te voegen, dan geef de gegevens terug, kunt u de Bouwer van de Lijst van de Vrije vorm toelaten. Als de builder is ingeschakeld, kunt u in vele dimensies, onderverdelingen, metriek en segmenten slepen en neerzetten om tabellen te maken die complexere vragen beantwoorden. Gegevens worden niet ter plekke bijgewerkt, maar worden bijgewerkt wanneer u op **[!UICONTROL Build]** klikt.

![](assets/table-builder.png)

## Tabelinteracties

U kunt op verschillende manieren werken met een vrije-vormtabel en deze aanpassen:

* **Rijen**
   * U kunt meer rijen in één enkel scherm passen door de de meningsdichtheid van het project [ ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) aan te passen.
   * Elke afmetingsrij kan tot 400 rijen tonen, alvorens paginering voorkomt. Klik op het nummer naast Rijen om meer rijen op een pagina weer te geven. Navigeer naar een andere pagina met de paginapijl in de koptekst.
   * Rijen kunnen worden opgesplitst in extra componenten. Als u veel rijen tegelijk wilt splitsen, selecteert u gewoon meerdere rijen en sleept u de volgende component boven op de geselecteerde rijen. Leer meer over [ onderbrekingen ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html).
   * De rijen kunnen [ worden gefiltreerd ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.html) om een verminderde reeks punten te tonen. De extra montages zijn beschikbaar onder [ montages van de Rij ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.html).

* **Kolommen**
   * Componenten kunnen in kolommen worden gestapeld om gesegmenteerde metriek, analyse op meerdere tabbladen en nog veel meer te maken.
   * De mening van elke kolom kan onder de [ kolommontages ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html) worden aangepast.
   * Verscheidene acties zijn beschikbaar door het [ met de rechtermuisknop aanklikken menu ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/using-the-right-click-menu.html). Het menu bevat verschillende handelingen, afhankelijk van de vraag of u op de tabelkop, de rijen of de kolommen klikt.

## Gegevens vrije-vormentabel exporteren

Leer meer over alle gegevens [ uitvoeropties ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html) voor Analysis Workspace.

* Klik met de rechtermuisknop > **[!UICONTROL Copy data to clipboard]** om de weergegeven tabelgegevens te exporteren. Als een tabel is geselecteerd, staat de optie **[!UICONTROL Copy selection to clipboard]** . De **Ctrl+C** hotkey kopieert ook geselecteerde gegevens.
* Klik met de rechtermuisknop > **[!UICONTROL Download data as CSV]** om de weergegeven tabelgegevens te downloaden als een CSV-bestand. Als een tabel is geselecteerd, staat de optie **[!UICONTROL Download selection as CSV]** .
* Klik met de rechtermuisknop > **[!UICONTROL Project > Download items as CSV]** exporteert maximaal 50.000 dimensieitems voor de geselecteerde dimensie.

Leer meer over alle gegevens [ uitvoeropties ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html) voor Analysis Workspace.

![](assets/export-options.png)

## Video&#39;s

Overzicht van de builder van de tabel voor vrije vorm:

>[!VIDEO](https://video.tv.adobe.com/v/31318/?quality=12)

Filters voor vrije-vormentabel:

>[!VIDEO](https://video.tv.adobe.com/v/23232/?quality=12)

Totaal vrije-vormtabellen:

>[!VIDEO](https://video.tv.adobe.com/v/29273/?quality=12)
