---
description: Met het gegevenswoordenboek in Analysis Workspace kunnen gebruikers de verschillende componenten in Analysis Workspace, waaronder het beoogde gebruik, die zijn goedgekeurd, duplicaten zijn, catalogiseren en bijhouden, enzovoort.
title: Het gegevenswoordenboek weergeven
feature: Components
role: User, Admin
source-git-commit: 8edd7b1b90e2ac3137bea734e5a0f1cb8004e743
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Componentinformatie weergeven in gegevenswoordenboek

{{release-limited-testing}}

In het gegevenswoordenboek kunt u informatie weergeven over een component, zoals de componentbeschrijving, vergelijkbare componenten, andere componenten waarmee een component vaak wordt gebruikt en meer.

Informatie over een component weergeven in het gegevenswoordenboek:

1. Ga naar het Analysis Workspace-project dat de component bevat die u wilt bekijken.

1. Selecteer [!UICONTROL **Gegevenswoordenboek**] in de linkerspoorstaaf van Analysis Workspace. (Alternatieve manieren om toegang te krijgen tot het gegevenswoordenboek worden beschreven in &quot;Toegang tot het gegevenswoordenboek&quot; in [Overzicht van gegevenswoordenboek](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md).)

   Het venster Gegevenswoordenboek wordt weergegeven.

   ![data-dictionary.png](assets/data-dictionary.png)

   <!--double-check this screenshot. I mocked the admin view up a bit to get rid of the Dictionary health tab.-->

1. Controleer of de rapportsuite die de component bevat die u wilt weergeven, is geselecteerd in de vervolgkeuzelijst. Standaard wordt de rapportsuite weergegeven waarin u zich al bevindt.

1. (Optioneel) Typ in het zoekveld de naam van de component die u wilt weergeven.

   Pictogrammen worden naast componentnamen weergegeven om het type component aan te geven:

   | Pictogram | Betekenis |
   |---------|----------|
   | ![Dimension-pictogram](assets/dimension-icon.png) | Geeft een **dimensie**. Dimension worden geleverd door Adobe. Bestaande afmetingen kunnen niet worden gewijzigd en er kunnen geen nieuwe afmetingen worden gemaakt. |
   | ![Metrisch pictogram](assets/default-metric-icon.png) | Geeft een **standaard metrisch** (niet berekend). De standaardmetriek worden verstrekt door Adobe en kan niet worden gewijzigd. |
   | ![Adobe-pictogram](assets/default-calc-metric-icon.png) | Geeft een **berekend metrisch sjabloon**. Dit zijn berekende metriek die door Adobe worden verstrekt en niet kunnen worden gewijzigd. |
   | ![Pictogram Rekenmachine](assets/calculated-metric-icon-created.png) | Geeft een **berekend metrisch** die door een beheerder van Analytics in uw organisatie werd gecreeerd. <!-- Delete all the comments... Components with this icon can be modified by an Analytics administrator. New calculated metrics can be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![Segmentpictogram](assets/segment-icon.png) | Geeft een **segment**. Deze kunnen segmenten zijn die door Adobe worden verstrekt of door een beheerder van Analytics in uw organisatie worden gecreeerd.<!-- Segments that were created byComponents with this icon can be modified by an Analytics administrator, as described in [Edit component entries in the Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md). New calculated metrics can also be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![Pictogram Datumbereik](assets/date-range-icon.png) | Geeft een **datumbereik**. Dit kunnen datumwaaiers zijn die door Adobe worden verstrekt of door een beheerder van Analytics in uw organisatie worden gecreeerd. <!-- Components with this icon can be modified by an Analytics administrator. New date ranges can also be created by an Analytics administrator, as described in [Create custom date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). --> |

{{dd-filter-criteria}}

1. Selecteer in de lijst met componenten de component die u wilt weergeven.

   De volgende informatie over de component wordt weergegeven:

   {{dd-component-information}}

1. (Optioneel) Sleep een component van het gegevenswoordenboek naar Analysis Workspace.