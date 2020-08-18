---
description: Gebruik de lijnvisualisatie om trended (op tijd gebaseerde) gegevenssets weer te geven
title: Lijn
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
translation-type: tm+mt
source-git-commit: 34db4e99589827fd41f642788e3409834b96d78a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 2%

---


# Lijn

Deze visualisatie vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijngrafiek kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

## Visualisatie-instellingen

>[!IMPORTANT]
>
> Sommige instellingen voor lijnvisualisatie, zoals Trendline tonen, worden momenteel beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html).

Klik op het tandwielpictogram rechtsboven in de lijnvisualisatie voor toegang tot de beschikbare [**visualisatie-instellingen**](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html#section_D3BB5042A92245D8BF6BCF072C66624B) . Instellingen worden gecategoriseerd in:

* Algemeen - instellingen die veel voorkomen in verschillende visualisatietypen
* As - instellingen die van invloed zijn op de x- of y-as van de lijnvisualisatie
* Bedekkingen - opties voor het toevoegen van extra context aan de reeks die wordt weergegeven in uw lijnvisualisatie.

### Korreligheid wijzigen

Met een keuzelijst met granulariteit in de [visualisatie-instellingen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#section_D3BB5042A92245D8BF6BCF072C66624B) kunt u een trendvisualisatie (bijvoorbeeld lijn, balk) wijzigen van dagelijks naar wekelijks, enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel.

### min of max tonen

Onder **Visualisatie-instellingen > Bedekkingen > min/max** tonen kunt u een label voor een minimum- en maximumwaarde bedekken om snel de pieken en dalen in een metrische kleur te markeren.

### Trendline-bedekking tonen

Onder **Visualisatie-instellingen > Bedekkingen > Trendline** tonen, kunt u een regressietrendline toevoegen aan de lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven.

Alle modellen zijn geschikt met behulp van de kleinste vierkantjes:

| Model | Beschrijving |
|---|---|
| Lineair | Hiermee maakt u een rechte lijn die het best past bij eenvoudige lineaire gegevenssets. Deze lijn is handig wanneer de gegevens met een constante snelheid worden verhoogd of verlaagd. Vergelijking: y = a + b * x |
| Logaritmisch | Hiermee maakt u een lijn met een curve die het best past. Deze lijn is handig wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: y = a + b * log(x) |
| Exponential | Hiermee maakt u een gekromde lijn. Deze lijn is handig wanneer de gegevenssnelheid voortdurend toeneemt of daalt. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: y = a +<sup>eb * x |
| Voeding | Maakt een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: y = a *<sup>xb |
| Quadratisch | Vindt het best-past voor een gegevensreeks die als parabool wordt gevormd (naar boven of naar onder bedekken). Vergelijking: y = a + b * x + c * x<sup>2 |
| Polynomiaal | Nuttig wanneer uw gegevensset fluctueert, zoals het analyseren van winsten en verliezen over een grote gegevensset. Vergelijking: y = a + b * x + ... + k *<sup>xorder |
