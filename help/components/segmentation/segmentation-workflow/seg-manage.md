---
description: In Segmentbeheer kunt u op verschillende manieren segmenten curven, zoals delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.
title: Segmenten beheren (Segmentbeheer)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: cfae0661dfa9c61daea33c3a52204793ce3d35c1
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 3%

---

# Segmentbeheer

In Segmentbeheer kunt u op verschillende manieren segmenten curven, zoals delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.

De manager van het Segment van Analytics toont u alle segmenten u bezit en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle segmenten in de organisatie zien. Dit overzicht bevat de gebruikersinterface en de mogelijkheden van Segmentbeheer.

![Segmentbeheer](assets/segments-manager.png)

## Toegang tot Segmentbeheer

1. Selecteer in Adobe Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Segments]**.

   of

   Selecteer in een bestaand rapport het pictogram Segmenten ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in de linkernavigatie selecteert u vervolgens **[!UICONTROL Manage]**.

## Beschikbare handelingen in Segmentbeheer

In Segmentbeheer kunt u:

* [Segmenten filteren](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Segmenten markeren als favorieten](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Segmenten goedkeuren](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Segmenten een label geven](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Segmenten delen](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Een segment exporteren naar een CSV-bestand.

* [Segmenten kopiëren](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Segmenten verwijderen](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Kolommen configureren

U kunt de informatie vormen die voor elk segment in de Manager van het Segment wordt getoond door de kolommen te vormen die worden getoond.

De zichtbare kolommen configureren in Segmentbeheer:

1. Selecteer in Adobe Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Segments]**.

1. Selecteer in Segmentbeheer de optie **Kolommen aanpassen** pictogram ![Het pictogram Kolommen aanpassen](assets/customize-columns-icon.png)Selecteer vervolgens de kolommen die u wilt weergeven in Segmentbeheer.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden worden verstrekt in de bouwer van het Segment. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de Segment Builder te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elk segment, zodat u segmenten kunt markeren als favorieten. Zie voor meer informatie [Segmenten markeren als favorieten](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Rapportsuites | Deze kolom geeft aan in welke rapportsuite het segment het laatst is opgeslagen. |
   | Eigenaar | Geeft aan wie eigenaar is van het segment. Als niet-beheerder, kunt u slechts segmenten zien u bezit of die met u werden gedeeld. |
   | Labels (niet gecontroleerd in kolomkiezer, vandaar dat de kolom niet wordt weergegeven) | Tags die op het segment zijn toegepast, door u of door personen die het segment met u hebben gedeeld. |
   | Gedeeld met | Hier worden personen of groepen weergegeven (alleen Admin) of Alle personen (alleen Admin) waarmee u het segment hebt gedeeld. <p>Wanneer een segment door u of met u wordt gedeeld, toont een aandeelpictogram naast de segmentnaam.</p> |
   | Datum gewijzigd | Hiermee geeft u de datum weer waarop het segment voor het laatst is gewijzigd. |
   | Gebruikt in | Toont hoeveel componenten het segment momenteel binnen wordt gebruikt. <p>Bijvoorbeeld, als het segment in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom zoals [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar het segment wordt gebruikt (bijvoorbeeld [!UICONTROL **Projecten (40)**], [!UICONTROL **Waarschuwingen (2)**]).</p><p>Segmenten kunnen in elk van de volgende componenttypen worden gebruikt:</p> <ul><li>Waarschuwingen</li><li>Projecten</li><li>Geplande projecten</li><li>Berekende standaarden</li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</p><p>U kunt de [Gegevenswoordenboek](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt.</p><p>De [!UICONTROL **Gebruikt in**] wordt niet standaard weergegeven. [Kolommen configureren](#configure-columns) om het weer te geven.</p> |
   | Laatst gebruikt | Hiermee geeft u de datum weer waarop het segment voor het laatst is gebruikt in een van de volgende componenttypen: <ul><li>Waarschuwingen</li><li>Berekende standaarden</li><li>Projecten</li><li>Geplande projecten</li><li>Segmenten</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</p><p>U kunt de [Gegevenswoordenboek](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}

## Hoe kan ik-video {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

Dit [Adobe Analytics-video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html) geeft een kort overzicht van hoe te om de Manager van het Segment te gebruiken.


