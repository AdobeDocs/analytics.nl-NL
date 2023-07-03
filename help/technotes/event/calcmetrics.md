---
title: Data afleiden die door gebeurtenissen worden beïnvloed
description: Gebruik berekende metriek om trended gegevens te corrigeren die door een gebeurtenis worden beïnvloed.
exl-id: 0fe70c8b-fa07-47e4-b6b3-b55eebad1fef
feature: Event, Calculated Metrics
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---

# Data afleiden die door gebeurtenissen worden beïnvloed

Als u gegevens hebt [beïnvloed door een gebeurtenis](overview.md)kunt u berekende metriek gebruiken om geschatte waarden af te leiden voor de duur van de gebeurtenis. Bijvoorbeeld, als u een gebeurtenis had die een daling van 25% in gegevens veroorzaakte, kunt u dat als vermenigvuldiger in berekende metrisch gebruiken.

Deze stappen werken het beste wanneer u het effect van een gebeurtenis begrijpt, zowel vanuit het perspectief van segmentatie als datumvergelijking. Zorg ervoor dat u [Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken](compare-dates.md) en [Specifieke data in de analyse uitsluiten](segments.md) voordat u deze pagina volgt.

>[!NOTE]
>
>Deze benadering is een schatting gebaseerd op een specifieke reeks inputs en datumbereiken. Het zal geen uitgebreide oplossing voor alle gebruiksgevallen of segmenten van gegevens zijn. Bovendien vereist deze benadering dat het betrokken datumbereik ten minste 1 hit heeft om van te berekenen.

Om een geschatte berekende metrisch voor de beïnvloede tijdspanne tot stand te brengen:

1. Maak twee segmenten voor &#39;Betrokken dagen&#39; en &#39;Betrokken dagen uitsluiten&#39;, zoals hieronder beschreven [Specifieke data in de analyse uitsluiten](segments.md).
2. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]**.
3. Klik op **[!UICONTROL Add]**.
4. Sleep beide van de bovenstaande segmenten naar het definitiekanvas. Wijzig de operator tussen de twee `+` om ze samen te vatten.
5. Voeg de gewenste metrisch binnen beide segmenten toe. U kunt bijvoorbeeld de metrische waarde &#39;Visits&#39; gebruiken.

   ![Segment builder](assets/event_segment_builder.png)

6. Klikken **[!UICONTROL Add]** in de rechterbovenhoek van de container &quot;Betrokken dagen&quot; klikt u op **[!UICONTROL Static number]**. Stel het statische getal in op het percentage dat u wilt verschuiven in de gegevens, zoals hieronder wordt aangegeven [Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken](compare-dates.md). In dit voorbeeld is de verschuiving 25% of 1,25.

   ![Statisch getal](assets/event_static_number.png)

7. Pas de &#39;gecorrigeerde&#39; metrische waarde naast elkaar toe in een trended freeform-tabel. Alle dagen buiten de gebeurtenis weerspiegelen hun normale metrische telling, terwijl alle beïnvloede dagen de vermenigvuldigingscompensatie gebruiken.

   ![Gecorrigeerde metrisch](assets/event_corrected.png)

8. Bekijk de gegevens in een lijnvisualisatie om het effect van uw gecorrigeerde metrisch te zien.

   ![Gecorrigeerde regel](assets/event_line.png)
