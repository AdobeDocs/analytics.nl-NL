---
description: Gebruik de lijnvisualisatie om trended (op tijd gebaseerde) gegevenssets weer te geven
title: Lijn
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
feature: Visualizations
role: User, Admin
exl-id: d177b39f-add7-4011-977a-1bdf3a9368cb
source-git-commit: 76abe4e363184a9577622818fe21859d016a5cf7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Lijn {#line}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_line_button"
>title="Lijn"
>abstract="Creeer een lijnvisualisatie die toont hoe de waarden over een periode veranderen. Een lijnvisualisatie kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Lijn in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_zie [ Lijn ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/line) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

De [!UICONTROL Line] visualisatie vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een [!UICONTROL Line] -grafiek kan alleen worden gebruikt wanneer de tijd als dimensie wordt gebruikt.

](assets/line-viz.png) visualisatie van de lijn 0}![

Klik op het tandwielpictogram in het hoogste recht van [!UICONTROL Line] visualisatie om tot [**beschikbare de montages van de Visualisatie**](freeform-analysis-visualizations.md) toegang te hebben. De instellingen worden gecategoriseerd in:

* **Algemeen**: Montages die over visualisatietypen gemeenschappelijk zijn
* **As**: Montages die de x- of y-as van de lijnvisualisatie beïnvloeden
* **Bedekkingen**: Opties om extra context aan de reeks toe te voegen die in uw lijnvisualisatie wordt getoond.

![ Visualisatie montages ](assets/viz-settings-modal.png)

## Korreligheid wijzigen

Een granularity drop-down in de [ visualisatie montages ](freeform-analysis-visualizations.md) laat u een trended visualisatie (b.v. lijn, bar) van dagelijks aan wekelijks aan maandelijks veranderen, enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel.

## min of max tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show min/max]** kunt u een minimum- en maximumwaarde-label bedekken om snel de pieken en dalen in een metrische kleur te markeren. Opmerking: de min/max-waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie.

![ toon min/max ](assets/min-max-labels.png)

## Trendline-bedekking tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show trendline]** kunt u desgewenst een regressie of een gemiddelde trendline voor het verplaatsen van de reeks toevoegen. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven.

Hier volgt een video over het toevoegen van trendlines aan lijnvisualisaties:

>[!VIDEO](https://video.tv.adobe.com/v/330176/?quality=12)

>[!TIP]
>
>Aanbevolen wordt trendlines toe te passen op gegevens die vandaag (gedeeltelijke gegevens) of toekomstige data niet omvatten, aangezien die de trendline zullen scheeftrekken. Als u echter datums in de toekomst wilt opnemen, verwijdert u nullen uit de gegevens om te voorkomen dat de gegevens gedurende die dagen worden schuingetrokken. Ga hiertoe naar de gegevensbrontabel van de visualisatie, kies de metrische kolom en schakel vervolgens **[!UICONTROL Column Settings]** > **[!UICONTROL Interpret zero as no value]** in.

![ Lineaire trendline ](assets/show-linear-trendline.png)

Alle trendlines van het regressiemodel zijn geschikt gebruikend gewone minste vierkanten:

| Model | Beschrijving |
| --- | --- |
| Lineair | Hiermee maakt u een rechte lijn die het best past bij eenvoudige lineaire gegevenssets. Deze lijn is handig wanneer de gegevens met een constante snelheid worden verhoogd of verlaagd. Vergelijking: `y = a + b * x` |
| Logaritmisch | Hiermee maakt u een lijn met een curve die het best past. Deze lijn is handig wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: `y = a + b * log(x)` |
| Exponential | Hiermee maakt u een gekromde lijn. Deze lijn is handig wanneer de gegevenssnelheid voortdurend toeneemt of daalt. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a + e^(b * x)` |
| Voeding | Maakt een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a * x^b` |
| Quadratisch | Vindt het best-past voor een gegevensreeks die als parabool wordt gevormd (naar boven of naar onder bedekken). Vergelijking: `y = a + b * x + c * x^2` |
| Gemiddeld verplaatsen | Hiermee maakt u een vloeiende trendline op basis van een set gemiddelden. Ook gekend als voortschrijdend gemiddelde, gebruikt een voortschrijdend gemiddelde een specifiek aantal gegevenspunten (die door uw &quot;Selectie van Punten&quot;worden bepaald), het gemiddelde van hen, en gebruikt het gemiddelde als punt in de lijn. Voorbeelden zijn het voortschrijdende gemiddelde over 7 dagen of het voortschrijdende gemiddelde over 4 weken. |
