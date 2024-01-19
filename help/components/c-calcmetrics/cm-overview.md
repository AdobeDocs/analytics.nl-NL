---
description: Berekende en Geavanceerde Berekende (of Afgeleide) Metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.
keywords: Berekende metriek;Afgeleide Metriek;Geavanceerde Berekende Metriek
title: Berekende en geavanceerde berekende (afgeleide) cijfers
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 2%

---

# Berekende en geavanceerde berekende (afgeleide) meetwaarden

Berekende en geavanceerde berekende (of afgeleide) metriek zijn douanemetriek die u van bestaande metriek kunt tot stand brengen.

Met onze gereedschappen voor berekende meetwaarden kunt u op zeer flexibele wijze metriek bouwen, beheren en beheren. Met deze services kunt u als marketers, productmanagers en analisten vragen stellen over de gegevens zonder dat u uw [!DNL Analytics] uitvoering. De aangepaste maatstaven die beschikbaar zijn in elke [!DNL Analytics] pakket is:

* Adobe [!DNL Analytics] Stichting: Berekend
* [Adobe Analytics selecteren](https://www.adobe.com/nl/data-analytics-cloud/analytics/select.html): Berekend + Geavanceerd berekend
* [Adobe Analytics Prime](https://www.adobe.com/nl/data-analytics-cloud/analytics/prime.html): Berekend + Geavanceerd berekend
* [Adobe Analytics Ultimate](https://www.adobe.com/nl/data-analytics-cloud/analytics/ultimate.html): Berekend + Geavanceerd berekend

Hier is een vergelijking van berekende metriek en geavanceerde berekende metriekmogelijkheden:

| Builder-opties | Berekende cijfers | Geavanceerde berekende (afgeleide) metriek |
|---|---|---|
| [Indelingstypen (decimaal, tijd, percentage, valuta)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | Ja | Ja |
| [Wijzigingen in het kenmerk (standaard, lineair, deelname, enz.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| [Metrische typen (standaard, totaal)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| Basisoperatoren (toevoegen, verwijderen, vermenigvuldigen, verdelen) | Ja | Ja |
| [Segmenten toepassen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | Nee | Ja |
| [Basisfuncties (aantal, abs-waarde, gemiddelde, enz.)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | Nee | Ja |
| [Geavanceerde functies (regressie, indien/toen, t-score, enz.)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | Nee | Ja |

## Mogelijkheden {#section_A0A5C275B68A4D628950BBB0B1EE631F}

U kunt

* Metrische gegevens maken over [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection], en [!UICONTROL Contribution Analysis].
* Creeer gesegmenteerde metriek die bij rapportruntime worden afgeleid, zonder het moeten de implementatie veranderen. Deze kunnen historisch worden bekeken omdat ze zijn gebaseerd op segmenten.

  >[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12&learn=on)

* De metriek van het aandeel over rapportsuites. Dit betekent dat alle pas gecreëerde metriek op alle rapportsuites in het zelfde login bedrijf van toepassing is.
* (Alleen geavanceerde berekende maatstaven) Segment op maateenheden. U kunt bijvoorbeeld een metrische waarde maken voor &quot;Nieuwe bezoekers&quot;, met een aantal personen voor wie dit de eerste sessie is.

* (Alleen geavanceerde berekende maatstaven) Neem statistische functies op om uw gegevens beter te kunnen beschrijven. Bijvoorbeeld, kunt u het aantal punten in een rapport tellen of in het aantal standaardafwijkingen voor elk punt toevoegen.

  >[!VIDEO](https://video.tv.adobe.com/v/25409/?quality=12&learn=on)

## Beperkingen {#section_CB878B02451541D68A68B508D4DBD19A}

Sommige [!DNL Analytics] Met functies kunt u wel gebeurtenissen gebruiken, maar niet berekende meetwaarden:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Cohort Analysis] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segments]
* [!DNL Analytics] for [!DNL Target]

## Gereedschappen {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Hier volgt een kort overzicht van het [!UICONTROL Calculated metrics] gereedschappen:

| Gereedschap | Mogelijkheden |
|--- |--- |
| Berekende metrische bouwer | <ul><li>Creeer berekende en geavanceerde berekende metriek gebruikend geavanceerde toewijzingsmodellen.</li><li>Segmenten inline toevoegen aan metrische formules</li><li>Vergelijk segmenten in het zelfde rapport. Vergelijk bijvoorbeeld lokale bezoekers met internationale bezoekers.</li><li>statistische functies gebruiken</li><li>Geef gedetailleerde metrische beschrijvingen (toon wat het doet, waar het gebruikt, waar NIET om het te gebruiken)</li><li>Definities kopiëren naar nieuwe metriek</li><li>Een inline metrische voorvertoning opgeven</li><li>Metrische polariteit instellen. Dit geeft aan of het goed of slecht is als een bepaalde aangepaste gebeurtenis (metrisch) omhoog gaat</li><li>Metrische codes</li></ul> |
| Berekend metrisch beheer | <ul><li>Metriek delen met anderen&lt;/li><li>Metrische gegevens goedkeuren en curven</li><li>Uw gegevens ordenen (labelen) zodat mensen ze kunnen vinden</li><li>Metrisch verwijderen</li><li>Naam van metriek wijzigen</li></ul> |
| Metrische kiezer | Hiermee kunt u metriek zoeken en toevoegen aan of toepassen op het rapport. U kunt ook de sorteervolgorde wijzigen (opties zijn alfabetisch, aanbevolen, vaak gebruikt, onlangs gebruikt). Bovendien kunt u op de Reeksen van het Rapport filtreren om slechts metriek te tonen die in een specifieke rapportreeks wordt gecreeerd.  Klik op het pictogram Metrisch links van een rapport om deze metrische kiezer te openen. |
| API voor Berekende waarden | Deel van de Adobe Analytics 2.0 API-set. |