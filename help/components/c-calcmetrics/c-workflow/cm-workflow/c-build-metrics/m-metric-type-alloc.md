---
description: Meer informatie over
title: Type en attributie metrisch
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 07590d00341f9016ee0728970483e77cb8d38a9d
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Type en attributie metrisch {#metric-type-attribution}

U kunt metrisch type en [ attributiemodel ](#attribution-models) voor metrisch in een berekende metrische definitie vormen.

1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) in de metrische component.
1. In het dialoogvenster Pop-up:

   ![ Metrisch type en attributie ](assets/cm-type-alloc.png)

   * Geef de waarde **[!UICONTROL Metric type]** op:

     | Metrisch type | Definitie |
     |---|---|
     | **[!UICONTROL Standard]** | Als een formule uit één enkele standaardmetrische norm bestaat, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig om berekende metriek te maken die specifiek zijn voor elk afzonderlijk regelitem. <p>Bijvoorbeeld, ](/help/assets/icons/Event.svg) **[!UICONTROL Orders]** ![ de Gebeurtenis van 0} ](/help/assets/icons/Divide.svg) verdeelt ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Visits]** neemt de orden voor dat specifieke lijnpunt en verdeelt het door het aantal bezoeken voor dat specifieke lijnpunt.![ |
     | **[!UICONTROL Grand total]** | Gebruik **[!UICONTROL Grand total]** voor de rapportageperiode in elk regelitem. Als een formule uit één enkel Eindtotaal metrisch bestaat, toont berekende metrisch het zelfde Grote totale aantal op elk lijnpunt. De grote totale metriek zijn nuttig wanneer u berekende metriek wilt tot stand brengen die tegen totale gegevens vergelijkt. <p>Bijvoorbeeld, ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Orders]** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Visits]** toont het aandeel van orden tegen alle bezoeken, niet alleen de bezoeken aan het specifieke lijnpunt. In dit voorbeeld, specificeert u **[!UICONTROL Grand Total]** voor de ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Visits]** metrisch in uw berekende metrisch, die het automatisch in ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Visits]** zal veranderen. |

   * Geef **[!UICONTROL Attribution]** op.

      1. U kunt:

         * Schakel **[!UICONTROL Use non-default attribution model]** uit om het standaard kolomkenmerkingsmodel, Last Touch, te gebruiken met een terugkijkvenster van 30 dagen.
         * Schakel **[!UICONTROL Use non-default attribution model]** in. In het dialoogvenster **[!UICONTROL Column attribution model]**

            * Selecteer a **[!UICONTROL Model]** van de [ attributiemodellen ](#attribution-models).
            * Selecteer a **[!UICONTROL Container]** van de [ container ](#container) opties.
            * Selecteer a **[!UICONTROL Lookback window]** van de [ raadplegingsvenster ](#lookback-window) opties. Als u **[!UICONTROL Custom Time]** selecteert, kunt u de tijdsperiode definiëren in **[!UICONTROL Minute(s)]** tot **[!UICONTROL Quarter(s)]** .

      1. Selecteer **[!UICONTROL Apply]** om het niet-standaard toewijzingsmodel toe te passen. Selecteer Annuleren om te annuleren.

     Als u al een niet-standaard toewijzingsmodel hebt gedefinieerd, selecteert u **[!UICONTROL Edit]** om de selectie te wijzigen.

Zie [ Voorbeeld ](#example) voor een voorbeeld om een attributiemodel, container, en raadplegingsvenster te gebruiken.


## Attributiemodellen {#attribution-models}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_nondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard attributiemodel in voor de geselecteerde metrische waarde."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attributionmodel"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lasttouch"
>title="Laatste aanraking"
>abstract="100% van het krediet gaat naar de laatste waarde van de dimensie die een bezoeker heeft gezien."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_firsttouch"
>title="Eerste aanraking"
>abstract="100% van het krediet gaat naar de waarde van de eerste dimensie die een bezoeker ziet."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_linear"
>title="Lineair"
>abstract="De creditering wordt gelijkmatig over alle afmetingswaarden verdeeld."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_participation"
>title="Deelname"
>abstract="100% is bestemd voor elke waarde van de dimensie die een bezoeker ziet.<br/> de totalen van de Kolom zijn overdreven."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_sametouch"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_instance"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_ushaped"
>title="U-vorm"
>abstract="40% van de kredieten voor de waarde van de eerste dimensie, 40% tot de laatste, 20% gedeeld door het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jcurve"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jshaped"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_inversej"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_reversejshaped"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_timedecay"
>title="Tijdverlies"
>abstract="Dimension-waarden die het dichtst bij een conversie liggen, krijgen het meeste krediet."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_custom"
>title="Aangepast"
>abstract="Definieer uw eigen op positie gebaseerde toewijzingsweging."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_positionbased"
>title="Aangepast"
>abstract="Definieer uw eigen op positie gebaseerde toewijzingsweging."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_algorithmic"
>title="Algorithmic"
>abstract="Krediet wordt dynamisch bepaald op basis van een statistisch algoritme."

{{attribution-models-details}}


## Container {#container}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_container"
>title="Container"
>abstract="Selecteer een container om het gewenste bereik voor de toewijzing in te stellen."

{{attribution-container}}


## Venster Opzoeken {#lookback-winwow}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="Venster Opzoeken"
>abstract="Deze instelling bepaalt het venster met gegevenstoewijzing dat voor elke conversie wordt toegepast."

{{attribution-lookback-window}}

## Voorbeeld

{{attribution-example}}


<!--
When [building a calculated metric](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md), you can specify the metric type and the attribution model.

## Metric type

To specify the metric type when building a calculated metric:

1. Select the gear icon next to the metric whose type you want to select.

   ![](assets/cm-type-alloc.png) 

1. Choose from the following options:

   |  Metric Type  | Definition  |
   |---|---|
   |  Standard  | These metrics are the same metrics used in standard [!DNL Analytics] reporting. If a formula consisted of a single standard metric, it displays identical data to its non-calculated-metric counterpart. Standard metrics are useful for creating calculated metrics specific to each individual line item. For example, [Orders] / [Visits] takes orders for that specific line item and divides it by the number of visits for that specific line item.  |
   |  Grand total  | Use Grand total for the reporting period in every line item. If a formula consisted of a single Grand total metric, it displays the same total number on every line item. Grand total metrics are useful for creating calculated metrics that compare against site total data. For example, [Orders] / [Total Visits] shows the proportion of orders against ALL visits to your site, not just the visits to the specific line item.  |

## How linear allocation works

[Attribution](/help/analyze/analysis-workspace/attribution/overview.md) is how allocation models in calculated metrics are evaluated.

For a full list of non-default attribution models and lookback windows supported, see [Attribution models and lookback windows](/help/analyze/analysis-workspace/attribution/models.md).

The following example illustrates how calculated metrics with linear allocations work in reporting: 

| | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Hit 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
|Data Sent In|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|
|Last Touch eVar|PROMO A|PROMO A|PROMO A|PROMO B|PROMO B|PROMO C|$10|
|First Touch eVar|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|$10|
|Example prop|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|

In this example, the values A, B, and C were sent into a variable on hits 1, 3, 4, and 6 before a $10 purchase was made on hit 7. In the second row, those values persist across hits on a last touch visit basis. The third row illustrates a first-touch visit persistence. Finally, the last row illustrates how data would be recorded for a prop which does not have persistence.

-->