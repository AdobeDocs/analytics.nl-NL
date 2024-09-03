---
description: Berekende en Geavanceerde berekende metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.
keywords: Berekende waarden;Geavanceerde berekende waarden
title: Berekende en geavanceerde berekende statistieken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 43332660bbf19ffd22409ef48528bcdef81b5e01
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 2%

---

# Berekende en geavanceerde berekende metriek

Berekende en geavanceerde berekende metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.

Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Zo kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u de [!DNL Analytics] -implementatie hoeft te wijzigen. De aangepaste meetgegevens die beschikbaar zijn in elk [!DNL Analytics] -pakket zijn:

* Adobe [!DNL Analytics] Foundation: berekend
* [ Uitgezochte Adobe Analytics ](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html): Berekend + Geavanceerd Berekend
* [ Adobe Analytics Prime ](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html): Berekend + Geavanceerd Berekend
* [ Adobe Analytics Ultimate ](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html): Berekend + Geavanceerd Berekend

Hier is een vergelijking van berekende metriek en geavanceerde berekende metriekmogelijkheden:

| Builder-opties | Berekende cijfers | Geavanceerde berekende meetwaarden |
|---|---|---|
| [ types van Formaat (decimaal, tijd, percenten, munt) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | Ja | Ja |
| [ veranderingen van de Attributie (gebrek, lineair, participatie, enz.) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| [ Metrische types (standaard, totaal) ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| [ pas segmenten ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) toe | Nee | Ja |
| [ Basisfuncties (telling, abs waarde, gemiddelde, enz.) ](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | Nee | Ja |
| [ Geavanceerde functies (regressie, als/toen, t-score, enz.) ](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | Nee | Ja |

## Mogelijkheden {#section_A0A5C275B68A4D628950BBB0B1EE631F}

U kunt

* Maak metrische gegevens over [!UICONTROL Analysis Workspace] , [!UICONTROL Report Builder] , [!UICONTROL Anomaly Detection] en [!UICONTROL Contribution Analysis] .
* Creeer gesegmenteerde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op segmenten.

  >[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12&learn=on)

* De metriek van het aandeel over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.
* (Alleen geavanceerde berekende maatstaven) Segment op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.

* (Alleen geavanceerde berekende maatstaven) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

  >[!VIDEO](https://video.tv.adobe.com/v/25409/?quality=12&learn=on)

## Beperkingen {#section_CB878B02451541D68A68B508D4DBD19A}

Met sommige functies van [!DNL Analytics] kunt u wel gebeurtenissen gebruiken, maar geen berekende meetwaarden:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Cohort Analysis] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segments]
* [!DNL Analytics] for [!DNL Target]

## Gereedschappen {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Hier volgt een kort overzicht van de gereedschappen van [!UICONTROL Calculated metrics] :

| Gereedschap | Mogelijkheden |
|--- |--- |
| Berekende metrische bouwer | <ul><li>Creeer berekende en geavanceerde berekende metriek gebruikend geavanceerde toewijzingsmodellen.</li><li>Segmenten inline toevoegen aan metrische formules</li><li>Vergelijk segmenten in het zelfde rapport. Vergelijk bijvoorbeeld lokale bezoekers met internationale bezoekers.</li><li>statistische functies gebruiken</li><li>Geef gedetailleerde metrische beschrijvingen (toon wat het doet, waar het gebruikt, waar NIET om het te gebruiken)</li><li>Definities kopiëren naar nieuwe metriek</li><li>Een inline metrische voorvertoning opgeven</li><li>Metrische polariteit instellen. Dit geeft aan of het goed of slecht is als een bepaalde aangepaste gebeurtenis (metrisch) omhoog gaat</li><li>Metrische codes</li></ul> |
| Berekend metrisch beheer | <ul><li>Metrische gegevens delen met anderen&lt;/li<li>Metrische gegevens goedkeuren en curven</li><li>Uw gegevens ordenen (labelen) zodat mensen ze kunnen vinden</li><li>Metrisch verwijderen</li><li>Naam van metriek wijzigen</li></ul> |
| Metrische kiezer | Hiermee kunt u metriek zoeken en toevoegen aan of toepassen op het rapport. U kunt ook de sorteervolgorde wijzigen (opties zijn alfabetisch, aanbevolen, vaak gebruikt, onlangs gebruikt). Bovendien kunt u op de Reeksen van het Rapport filtreren om slechts metriek te tonen die in een specifieke rapportreeks wordt gecreeerd.  Klik op het pictogram Metrisch links van een rapport om deze metrische kiezer te openen. |
| API voor Berekende waarden | Deel van de Adobe Analytics 2.0 API-set. |
