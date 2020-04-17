---
title: Afleiden van gegevens die door gebeurtenissen worden beïnvloed
description: Gebruik berekende metriek om trended gegevens te corrigeren die door een gebeurtenis worden beïnvloed.
translation-type: tm+mt
source-git-commit: dfc2e036711ee2229160f52ab16fb4299f7722e5

---


# Afleiden van gegevens die door gebeurtenissen worden beïnvloed

Als u gegevens hebt [die door een gebeurtenis](/help/technotes/event-impacted.md)worden beïnvloed, kunt u berekende metriek gebruiken om trended waarden voor de duur van de gebeurtenis af te leiden. Bijvoorbeeld, als u een gebeurtenis had die een daling van 25% in gegevens veroorzaakte, kunt u dat als vermenigvuldiger in berekende metrisch gebruiken.

>[!NOTE] Deze stappen werken het beste wanneer u het effect van een gebeurtenis begrijpt, zowel vanuit het perspectief van segmentatie als datumvergelijking. Zorg ervoor dat u de datums die door een gebeurtenis worden beïnvloed, [vergelijkt met vorige bereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/compare-event.md) en dat u specifieke datums in de analyse [](../c-segmentation/use-cases/exclude-date-range.md) Uitsluiten voordat u deze pagina volgt.

1. Maak twee segmenten voor &#39;Betrokken dagen&#39; en &#39;Betrokken dagen uitsluiten&#39;, zoals beschreven onder Specifieke data in de analyse [](../c-segmentation/use-cases/exclude-date-range.md)uitsluiten.
2. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]**.
3. Klik op **[!UICONTROL Add]**.
4. Sleep beide van de bovenstaande segmenten naar het definitiekanvas. Wijzig de operator tussen de twee in een `+` som.
5. Voeg de gewenste metrisch binnen beide segmenten toe. U kunt bijvoorbeeld de metrische waarde &#39;Visits&#39; gebruiken.

   ![Segment builder](assets/event_segment_builder.png)

6. Klik **[!UICONTROL Add]** in de rechterbovenhoek van de container voor &#39;Betrokken dagen&#39; en klik vervolgens op **[!UICONTROL Static number]**. Stel het statische getal in op het percentage dat u wilt verschuiven in de gegevens, zoals wordt beschreven onder Datums [vergelijken die door een gebeurtenis worden beïnvloed, vergelijken met vorige bereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/compare-event.md). In dit voorbeeld is de verschuiving 25% of 1,25.

   ![Statisch getal](assets/event_static_number.png)

7. Pas de &#39;gecorrigeerde&#39; metrische waarde naast elkaar toe in een trended freeform-tabel. Alle dagen buiten de gebeurtenis weerspiegelen hun normale metrische telling, terwijl alle beïnvloede dagen de vermenigvuldigingscompensatie gebruiken.

   ![Gecorrigeerde metrisch](assets/event_corrected.png)

8. Bekijk de gegevens in een lijnvisualisatie om het effect van uw gecorrigeerde metrisch te zien.

   ![Gecorrigeerde regel](assets/event_line.png)
