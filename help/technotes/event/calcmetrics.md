---
title: Afleiden van gegevens die door gebeurtenissen worden beïnvloed
description: Gebruik berekende metriek om trended gegevens te corrigeren die door een gebeurtenis worden beïnvloed.
exl-id: 0fe70c8b-fa07-47e4-b6b3-b55eebad1fef
feature: Curate and Share, Calculated Metrics
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Afleiden van gegevens die door gebeurtenissen worden beïnvloed

Als u gegevens [&#x200B; hebt die door een gebeurtenis &#x200B;](overview.md) worden beïnvloed, kunt u berekende metriek gebruiken om geschatte waarden voor de duur van de gebeurtenis af te leiden. Bijvoorbeeld, als u een gebeurtenis had die een daling van 25% in gegevens veroorzaakte, kunt u dat als vermenigvuldiger in berekende metrisch gebruiken.

Deze stappen werken het beste wanneer u het effect van een gebeurtenis begrijpt, zowel vanuit het perspectief van segmentatie als datumvergelijking. Zorg ervoor om [&#x200B; te volgen data vergelijken die door een gebeurtenis aan vorige waaiers &#x200B;](compare-dates.md) worden beïnvloed en [&#x200B; sluit specifieke data in analyse &#x200B;](segments.md) uit alvorens deze pagina te volgen.

>[!NOTE]
>
>Deze benadering is een schatting gebaseerd op een specifieke reeks inputs en datumbereiken. Het zal geen uitgebreide oplossing voor alle gebruiksgevallen of segmenten van gegevens zijn. Bovendien vereist deze benadering dat het betrokken datumbereik ten minste 1 hit heeft om van te berekenen.

Om een geschatte berekende metrisch voor de beïnvloede tijdspanne tot stand te brengen:

1. Creeer twee segmenten voor &quot;Betrokken dagen&quot;en &quot;sluiten beïnvloede dagen&quot;, zoals die onder [&#x200B; worden geschetst sluit specifieke data in analyse &#x200B;](segments.md) uit.
2. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]**.
3. Klik op **[!UICONTROL Add]**.
4. Sleep beide van de bovenstaande segmenten naar het definitiekanvas. Wijzig de operator tussen de twee in een `+` om ze samen te tellen.
5. Voeg de gewenste metrisch binnen beide segmenten toe. U kunt bijvoorbeeld de metrische waarde &#39;Visits&#39; gebruiken.

   ![&#x200B; de bouwer van het Segment &#x200B;](assets/event_segment_builder.png)

6. Klik op **[!UICONTROL Add]** rechtsboven in de container voor &#39;Betrokken dagen&#39; en klik vervolgens op **[!UICONTROL Static number]** . Plaats het statische aantal aan het percentage dat u uw gegevens wilt compenseren, zoals die onder [&#x200B; worden geschetst vergelijkt data die door een gebeurtenis aan vorige waaiers &#x200B;](compare-dates.md) worden beïnvloed. In dit voorbeeld is de verschuiving 25% of 1,25.

   ![&#x200B; Statisch aantal &#x200B;](assets/event_static_number.png)

7. Pas de &#39;gecorrigeerde&#39; metrische waarde naast elkaar toe in een trended freeform-tabel. Alle dagen buiten de gebeurtenis weerspiegelen hun normale metrische telling, terwijl alle beïnvloede dagen de vermenigvuldigingscompensatie gebruiken.

   ![&#x200B; Corrected metrisch &#x200B;](assets/event_corrected.png)

8. Bekijk de gegevens in een lijnvisualisatie om het effect van uw gecorrigeerde metrisch te zien.

   ![&#x200B; Correcte lijn &#x200B;](assets/event_line.png)
