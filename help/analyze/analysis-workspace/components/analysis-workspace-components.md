---
description: 'Componenten in Analysis Workspace bestaan uit afmetingen, metriek, segmenten en datumbereiken die u naar een project kunt slepen en neerzetten. '
title: Overzicht van onderdelen
feature: Workspace Basics
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: 28e8ad7a71cbd8f034fa5fc8ec39a6db537da6f3
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 5%

---

# Overzicht van onderdelen

Componenten in Analysis Workspace bestaan uit afmetingen, metriek, segmenten en datumbereiken die u naar een project kunt slepen en neerzetten.

Als u het menu Componenten wilt openen, klikt u op het pictogram **[!UICONTROL Components]** in de linkertrack. U kunt schakelen tussen [Deelvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html), [Visualisaties](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) en Componenten van de linkerspoorpictogrammen of door [hotkeys](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md) te gebruiken.

![](assets/component-overview.png)

U kunt ook de [Dichtheidsmontages van de Mening ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) voor het project aanpassen om meer waarden in de linkerspoorstaaf tegelijkertijd te zien door naar **[!UICONTROL Project > Project Info & Settings > View Density]** te gaan.

## Dimensies {#dimensions}

[****](https://experienceleague.adobe.com/docs/analytics/components/dimensions/overview.html) Dimensies zijn tekstkenmerken die het gedrag van uw bezoeker beschrijven en die in uw analyse kunnen worden weergegeven, uitgesplitst en vergeleken. Ze zijn te vinden in de linkercomponentrails (oranje sectie) en worden doorgaans toegepast als rijen van een tabel.

Voorbeelden van afmetingen zijn [!UICONTROL Page Name], [!UICONTROL Marketing Channels], [!UICONTROL Device Type] en [!UICONTROL Products]. Dimension worden geleverd door Adobe en worden vastgelegd via uw aangepaste implementatie (eVar, Props, classificaties, enz.).

Elke dimensie bevat ook **dimensiepunten** binnen het. U vindt Dimension-items in de linkercomponentrails door op de pijl naar rechts naast de naam van een willekeurige dimensie te klikken (de items zijn geel).

Voorbeelden van dimensie-items zijn [!UICONTROL Homepage] (binnen de [!UICONTROL Page]-dimensie), [!UICONTROL Paid Search] (binnen de [!UICONTROL Marketing Channel]-dimensie), [!UICONTROL Tablet] (binnen de [!UICONTROL Mobile Device Type]-dimensie), enzovoort.

![](assets/dimensions.png)

## Metrics {#metrics}

[****](https://experienceleague.adobe.com/docs/analytics/components/metrics/overview.html) Metricare kwantitatieve maatstaven voor het gedrag van bezoekers. Ze zijn te vinden in het linkerspoor van de component (groene sectie) en worden doorgaans toegepast als kolommen van een tabel.

Voorbeelden van metriek zijn [!UICONTROL Page views], [!UICONTROL Visits], [!UICONTROL Orders], [!UICONTROL Average Time spent] en [!UICONTROL Revenue/Order]. Metriek worden verstrekt door Adobe, of door uw douaneimplementatie ([!UICONTROL Success events]) gevangen, of gecreeerd gebruikend [Berekende metrische bouwer](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).

![](assets/metrics.png)

## Segmenten {#segments}

[**De**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html) segmentsfilters zijn publieksfilters die op uw analyse worden toegepast. Ze zijn te vinden in de linkercomponentrails (blauw gedeelte) en worden doorgaans toegepast boven aan een deelvenster of boven metrische kolommen in een tabel.

Voorbeelden van segmenten zijn [!UICONTROL Mobile Device Visitors], [!UICONTROL Visits from Email] en [!UICONTROL Authenticated Hits]. Segmenten worden opgegeven door Adobe of gemaakt in de [dropzone](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html) van het deelvenster of gemaakt met de [Segment builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html).

![](assets/segments.png)

## Datumbereik {#date-ranges}

[**Datumbereiken**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) zijn de datums waarop u de analyse uitvoert. Ze zijn te vinden in de linkercomponentrails (paarse sectie) en worden doorgaans toegepast in de kalender van elk deelvenster.

Voorbeelden van datumbereiken zijn juli 2019, [!UICONTROL Last 4 weeks] en [!UICONTROL This month]. Datumbereiken worden opgegeven door Adobe, toegepast in de [deelvensterkalender](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html) of gemaakt met de [Datumbereikbuilder](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html).

![](assets/date-ranges.png)

## Componenthandelingen {#actions}

U kunt componenten (afzonderlijk of door meer dan één te selecteren) direct in de linkerspoorstaaf beheren. Klik met de rechtermuisknop op een component of klik op het pictogram Actie-punt boven aan de lijst met componenten.

![](assets/component-actions.png)

| Component Handeling | Beschrijving |
|--- |--- |
| Tag | U kunt componenten ordenen of beheren door er tags op toe te passen. U kunt vervolgens zoeken op tag in de linkertrack door op het filter te klikken of # te typen. Tags fungeren ook als filters in de componentmanagers. |
| Favorieten | Voeg de component toe aan de lijst met favorieten. Net als tags kunt u zoeken op Favorieten in het linkerspoor en deze filteren in de componentmanagers. |
| Goedkeuren | Markeer componenten zoals Goedgekeurd om aan uw gebruikers te laten weten dat de component door de organisatie is goedgekeurd. Net als tags kunt u zoeken op Goedgekeurd in de linkertrack en door hen filteren in de componentmanagers. |
| Delen | Delen van componenten naar gebruikers in uw organisatie. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals segmenten of berekende maateenheden. |
| Verwijderen | Verwijder componenten die u niet meer nodig hebt. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals segmenten of berekende maateenheden. |

De componenten van de douane kunnen ook door hun respectieve managers van de Component worden beheerd. Bijvoorbeeld [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md).
