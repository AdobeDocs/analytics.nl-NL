---
description: Leer hoe u componenten aan een project kunt toevoegen in Analysis Workspace
title: Componenten in Analysis Workspace gebruiken
feature: Workspace Basics
role: User, Admin
source-git-commit: 0928628c9cffa91f90fa5d8af535eb834bb7502d
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 0%

---

# Componenten in Analysis Workspace gebruiken

Componenten vormen de feitelijke gegevens van elk project in Analysis Workspace. Componenten bestaan uit afmetingen, metriek, segmenten en datumbereiken. U kunt componenten aan een project toevoegen door hen in visualisaties of panelen te slepen.

Voor overzichtsinformatie over de types van componenten kunt u toevoegen, zie [Overzicht van componenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).

>[!TIP]
>
>Voor informatie over elke component selecteert u het pictogram Info naast de naam van een component in de linkertrack van Analysis Workspace of raadpleegt u de [Handleiding Analytics Components](/help/components/home.md).

## Beginnen met het toevoegen van componenten aan een project

1. [Een project maken in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md) als je dat nog niet hebt gedaan.

1. [Deelvenster toevoegen](/help/analyze/analysis-workspace/c-panels/panels.md) of [een visualisatie toevoegen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) naar het project in Analysis Workspace.

   Als u een component aan een leeg project toevoegt, wordt automatisch een vrije lijstvisualisatie gecreeerd.

1. Selecteer de **[!UICONTROL Components]** in de linkerspoorstaaf.

   ![](assets/build-components.png)

1. Blader naar of zoek naar de component die u wilt toevoegen en sleep deze naar een deelvenster of een visualisatie in uw project.

   U kunt bijvoorbeeld een segment naar de neerzetzone van het segment in een deelvensterkop slepen.

   ![een segment neerzetten in de neerzetzone](assets/segment-dropzone.png)

1. Voor meer gedetailleerde informatie gaat u verder met een van de volgende secties, afhankelijk van het componenttype dat u toevoegt:

   * [Afmetingen toevoegen aan een project](#add-dimensions-to-a-project)

   * [Metriek toevoegen aan een project](#add-metrics-to-a-project)

   * [Segmenten toevoegen aan een project](#add-segments-to-a-project)

   * [Datumbereiken toevoegen aan een project](#add-date-ranges-to-a-project)

## Afmetingen toevoegen aan een project

[Dimensionen](/help/components/dimensions/overview.md) zijn variabelen in Adobe Analytics die doorgaans tekenreekswaarden bevatten. Veelvoorkomende afmetingen zijn [Pagina](/help/components/dimensions/page.md), [Verwijzen naar domein](/help/components/dimensions/referring-domain.md)of een [eVar](/help/components/dimensions/evar.md). In tegenstelling tot [cijfers](/help/components/metrics/overview.md) bevatten numerieke waarden die aan een afmeting binden. Een basisrapport toont rijen van koordwaarden (afmeting), tegen een kolom van numerieke waarden (metrisch).

1. Begin een dimensie aan uw project in Analysis Workspace toe te voegen, zoals beschreven in [Beginnen met het toevoegen van componenten aan een project](#begin-adding-components-to-a-project).

1. Kies een van de volgende methoden om afmetingen toe te voegen en het type gegevens te bepalen dat u wilt analyseren:

   * Sleep een dimensie naar een visualisatie (zoals een vrije-vormlijst) in Analysis Workspace.

     ![Afmetingen toevoegen aan een project](assets/add-dimensions.png)

   * Sleep een of meer afmetingen van de linkerspoorstaaf naar de neerzetzone van het segment om een ad-hocsegment te maken, zoals beschreven in [Segmenten toevoegen aan een project](#add-segments-to-a-project).

     ![een segment neerzetten in de neerzetzone](assets/segment-dropzone.png)

Ga voor meer informatie over het gebruik van dimensies in Analysis Workspace naar [Voorvertoningsafmetingen](/help/analyze/analysis-workspace/components/dimensions/view-dimensions.md), [Afmetingen onderverdelingen](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md), en [Afmetingen van tijd tot tijd](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md).

## Metriek toevoegen aan een project

[Metrisch](/help/analyze/analysis-workspace/components/apply-create-metrics.md) kunt u gegevenspunten kwantificeren in Analysis Workspace. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

Om metrisch aan een project in Analysis Workspace toe te voegen:

1. Een metrische waarde toevoegen aan uw project in Analysis Workspace, zoals wordt beschreven in [Beginnen met het toevoegen van componenten aan een project](#begin-adding-components-to-a-project).

1. Kies een van de volgende methoden om metrisch toe te voegen in Analysis Workspace:

   * Sleep metrisch aan de metrische dalingsstreek in een lege lijst Freeform om te zien dat metrisch over de de datumperiode van het project trended.

     ![Metrisch toevoegen aan een project](assets/add-metrics.png)

   * Sleep metrisch wanneer een afmeting aanwezig is om dat metrisch vergeleken bij elk afmetingspunt te zien.

   * Sleep metrisch bovenop een bestaande metrische kopbal om het te vervangen.

   * Sleep metrisch naast een kopbal om beide metriek naast elkaar te zien.

Ga voor meer informatie over het gebruik van metriek in Analysis Workspace naar [Metrisch](/help/analyze/analysis-workspace/components/apply-create-metrics.md).

## Segmenten toevoegen aan een project

[Segmenten](/help/components/segmentation/seg-overview.md) kunt u subsets van bezoekers identificeren op basis van kenmerken of specifieke interacties.

Een segment toevoegen aan een project in Analysis Workspace:

1. Beginnen met het toevoegen van een segment aan uw project in Analysis Workspace, zoals beschreven in [Beginnen met het toevoegen van componenten aan een project](#begin-adding-components-to-a-project).

1. Kies een van de volgende methoden om het deelvenster te filteren:

   * Sleep een afzonderlijk segment van de linkerspoorstaaf naar de neerzetzone van het segment.

     ![een segment neerzetten in de neerzetzone](assets/segment-dropzone.png)

   * Houd Shift of Ctrl ingedrukt als u meerdere segmenten in de linkertrack wilt selecteren en houd Shift ingedrukt terwijl u ze op de neerzetzone van het segment neerzet.

     ![meerdere segmenten in de neerzetzone neerzetten](assets/segment-dropzoone-multiple.png)

     Hiermee maakt u een vervolgkeuzemenu waarin gebruikers van het deelvenster het filter kunnen kiezen dat zij willen toepassen. Het vervolgkeuzemenu bevat een [!UICONTROL **Geen filter**] die gebruikers kunnen selecteren, zodat het deelvenster ongefilterd blijft.

     U kunt de (x) selecteren om het even welke optie uit het drop-down menu te verwijderen. Als u de [!UICONTROL **Geen filter**] en is een filter vereist.

   * Maak ad-hocsegmenten door niet-segmentcomponenten naar de neerzetzone te slepen. Dit kan u de tijd en moeite besparen om naar de Bouwer van het Segment te gaan. Segmenten die op deze manier worden gemaakt, worden automatisch gedefinieerd als raaksegmenten. Deze definitie kan worden gewijzigd door op het informatiepictogram (i) naast het segment te klikken, vervolgens op het pictogram voor het bewerken van de vorm van een potlood te klikken en dit te bewerken in de Segment Builder.

     Ad hoc segmenten zijn een type van snel segment, en zijn lokaal aan het project. Ze komen niet in de linkerspoorstaaf voor als je ze niet openbaar maakt.

     Zie voor meer informatie [Snelle segmenten](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

Voor meer informatie over hoe u de sectie van de segmentdaling op een paneel kunt gebruiken om uw paneel te filtreren, zie [Valzone](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Overzicht van deelvensters](/help/analyze/analysis-workspace/c-panels/panels.md).

## Datumbereiken toevoegen aan een project

[Datumbereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md) bepaalt het rapporttijdkader in Analysis Workspace, en kan op één of meerdere panelen binnen een project worden toegepast.

Elk deelvenster bevat standaard een datumbereik. Er zijn meerdere manieren om een datumbereik voor een deelvenster bij te werken. U kunt een datumbereik voor een deelvenster in Analysis Workspace bijwerken door een datumbereikcomponent van de linkertrack te slepen:

1. Beginnen met het toevoegen van een datumbereik aan uw project in Analysis Workspace, zoals beschreven in [Beginnen met het toevoegen van componenten aan een project](#begin-adding-components-to-a-project).

1. Sleep een datumbereik van de linkertrack naar het huidige datumbereik in de rechterbovenhoek van het deelvenster.

   ![een datumbereik neerzetten](assets/daterange-drop.png)

Zie voor meer informatie over het gebruik van kalenders en datumbereiken in Analysis Workspace [Overzicht van kalender- en datumbereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).
