---
description: Leer hoe u dimensies en dimensies kunt onderverdelen in Analysis Workspace.
keywords: Analysis Workspace
title: Afmetingen onderbreken
feature: Dimensions
role: User, Admin
exl-id: 0d26c920-d0d9-4650-9cf0-b67dbc4629e1
source-git-commit: ff38740116ac6f12033ebdc17cffa3250a30f3f7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Afmetingen onderverdelingen

U kunt uw gegevens in Analysis Workspace op onbeperkte manieren voor uw specifieke behoeften opsplitsen; bouwt vragen gebruikend relevante metriek, dimensies, segmenten, tijdlijnen, en andere waarden van de analyseonderbreking.

1. In a [ Vrije lijst ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md), van het contextmenu van één of meerdere geselecteerde rijen, uitgezochte **[!UICONTROL Breakdown]** ![ ChevronRight ](/help/assets/icons/ChevronRight.svg).

   ![ Resultaat van de Stap die alarm van geselecteerde selectie toont.](assets/breakdown.png)

1. Selecteer in het submenu **[!UICONTROL Dimensions]** , **[!UICONTROL Metrics]** , **[!UICONTROL Segments]** of **[!UICONTROL Date ranges]** en selecteer vervolgens een item. Of eenvoudig onderzoek naar een component op het **[!UICONTROL *gebied van het Onderzoek *]**.

U kunt metriek onderverdelen door afmetingspunten of publiekssegmenten over geselecteerde tijdsperioden. U kunt ook verder naar beneden boren tot een meer korrelig niveau.

>[!NOTE]
>
>Het aantal uitsplitsingen dat in de tabel moet worden weergegeven, is beperkt tot 200. Deze limiet neemt toe voor uitsplitsingen exporteren.

## Uitsplitsing naar positie

Standaard zijn uitsplitsingen vast op statische rijitems. Stel dat u de bovenste pagina&#39;s met dimensies (Homepage, Zoekresultaten, Afhandeling) opsplitst op Marketingkanaal. Dan verlaat u het project en keert twee weken later terug. Nadat u het project opnieuw hebt geopend, zijn de bovenste drie pagina&#39;s gewijzigd. In plaats daarvan zijn Homepage, Zoekresultaten en Afhandeling de bovenste 4-6 pagina&#39;s. Standaard worden uw uitsplitsingen naar marketingkanaal nog steeds weergegeven onder Homepage, Zoekresultaten en Afhandeling, ook al bevinden ze zich nu in de rijen 4-6.

In tegenstelling, **Uitsplitsing door positie**, onderbreekt altijd top 3 punten, ongeacht wat deze punten zijn. Verwijzend naar het voorbeeld, wanneer u uw project opnieuw opent, zijn de onderbrekingen van het Kanaal van de Marketing gebonden aan de hoogste 3 pagina&#39;s in de lijst. En niet naar Homepage, zoekresultaten en afhandeling, die nu in de rijen 4 tot en met 6 staan. Zie [ montages van de Rij ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md) hoe te om dit het plaatsen te vormen.



## Toewijzingsmodellen toepassen op uitsplitsingen

Voor elke uitsplitsing binnen een tabel kan ook een toewijzingsmodel worden toegepast. Dit attributiemodel kan hetzelfde zijn of verschillen van de bovenliggende kolom. Bijvoorbeeld, kunt u lineaire Orden op uw afmeting van de Kanalen van de Marketing analyseren maar U-Vormde Orden op de specifieke het volgen codes binnen een Kanaal toepassen. Als u het toewijzingsmodel wilt bewerken dat is toegepast op een uitsplitsing, beweegt u de muisaanwijzer over het uitsplitsingsmodel en selecteert u **[!UICONTROL Edit]** .

![ Vergelijking van de Attributie van de Orde die de montages van de Onderbreking tonen ](assets/breakdown-attribution.png)

Dit is het verwachte gedrag wanneer het toepassen van attributiemodellen op onderverdelingen of het uitgeven van hen:

* Als u een attributie toepast terwijl er geen andere attributies bestaan, wordt de attributie toegepast op de gehele kolomstructuur.

* Als u een uitsplitsing toevoegt nadat een toewijzing is toegepast, wordt de standaardinstelling gebruikt voor de opgegeven uitsplitsing die is toegevoegd (als die dimensie een standaardinstelling heeft). Anders wordt de uitsplitsing van de bovenliggende kolom gebruikt. Sommige dimensies hebben een standaardtoewijzing. De tijdafmetingen en de referentie gebruiken bijvoorbeeld Gelijke aanraking. De dimensie van het Product gebruikt Last Touch. Andere afmetingen hebben geen gebrek, en zullen de toewijzing van de ouderkolom gebruiken.

* Als de kolomstructuur al kenmerken bevat, heeft het wijzigen van de toewijzing alleen invloed op de eigenschap die u bewerkt.

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Dimension in Analysis Workspace ](https://video.tv.adobe.com/v/23971?quality=12&learn=on){target="_blank"} voor een demo video.


>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de onderbrekingen van Dimension ](https://video.tv.adobe.com/v/23969?quality=12&learn=on){target="_blank"} voor een demo video.


>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Toevoegend dimensies en metriek ](https://video.tv.adobe.com/v/30606?quality=12&learn=on){target="_blank"} voor een demo video.


>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Werkend met afmetingen in een Vrije Lijst van de Vorm ](https://video.tv.adobe.com/v/40179?quality=12&learn=on){target="_blank"} voor een demo video.


>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Dimension onderbreking door positie ](https://video.tv.adobe.com/v/24033){target="_blank"} voor een demo video.


>[!ENDSHADEBOX]



<!--
# Break down dimensions

Break down dimensions and dimension items in Analysis Workspace.

Break down your data in unlimited ways for your specific needs; build queries using relevant metrics, dimensions, segments, time lines, and other analysis breakdown values.

1. [Create a project](/help/analyze/analysis-workspace/home.md) with a data table.
1. In the data table, right-click a line item and select **[!UICONTROL Breakdown]** > *`<item>`*.

   ![Step Result](assets/fa_data_table_actions.png)

   You can break down metrics by dimension items or audience segments across selected time periods. You can also drill down further to a more granular level.

   >[!NOTE]
   >
   >The number of breakdowns to show in the table is limited to 200. This limit will increase for exporting breakdowns.

## Apply attribution models to breakdowns

Any breakdown within a table can also have any attribution model applied to it. This attribution model can be the same or different from the parent column. For example, you can analyze linear Orders on your Marketing Channels dimension but apply U-Shaped Orders to the specific tracking codes within a Channel. To edit the attribution model applied to a breakdown, hover over the breakdown model and click **[!UICONTROL Edit]**:

![Breakdown settings](assets/breakdown_settings.png)

This is the expected behavior when applying attribution models to breakdowns or editing them:

* If you apply an attribution when no other attributions exist, then the attribution applies to the entire column tree.

* If you add a breakdown after an attribution has been applied, it will use the default for the given breakdown that was added, if that dimension has a default. Otherwise it will use the breakdown from the parent column. Some dimensions have a default allocation.  For example, [!UICONTROL Time] dimensions and [!UICONTROL Referrer] use [!UICONTROL Same Touch]. The [!UICONTROL Product] dimension uses [!UICONTROL Last Touch]. Other dimensions don't have a default, and will use the parent column allocation.

* If there are already attributions in the column tree, changing the attribution only impacts the one you are editing.

## Videos


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Adding dimensions and metrics to your project in Analysis Workspace](https://video.tv.adobe.com/v/30606?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Working with dimensions in a Freeform Table](https://video.tv.adobe.com/v/40179?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [dimension breakdowns by position](https://video.tv.adobe.com/v/24033?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]


-->