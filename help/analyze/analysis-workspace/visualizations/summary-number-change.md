---
description: Gebruik het Summiere Aantal en de visualisaties van de Verandering om belangrijke gegevenspunten in een project te tonen.
title: Samenvattingsnummer en Samenvattingswijziging
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
feature: Visualizations
role: User, Admin
exl-id: d6a08201-ca3a-48ff-983a-3ec6b989deda
source-git-commit: 76abe4e363184a9577622818fe21859d016a5cf7
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 1%

---

# [!UICONTROL Summary Number] en [!UICONTROL Summary Change]

_dit artikel documenteert het Summiere aantal en de Summiere veranderingsvisualisaties in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_zie [ Summiere aantal en Summiere verandering ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/summary-number-change) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** versie van dit artikel._

Hier is een video over deze twee visualisaties:

>[!VIDEO](https://video.tv.adobe.com/v/335564/?quality=12)

## [!UICONTROL Summary Number] visualisatie {#summary-number}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarynumber_button"
>title="Samenvattingsnummer"
>abstract="Maak een visualisatie met totalen en subtotalen."

<!-- markdownlint-enable MD034 -->

Gebruik de visualisatie van [!UICONTROL Summary Number] om een groot aantal te benadrukken dat in een project belangrijk is. Deze visualisatie werkt op de volgende manieren:

* Hiermee selecteert u het totaal van de kolom als er geen cel is geselecteerd.
* Als er één cel is geselecteerd, wordt het overzicht voor die cel weergegeven.
* Als er meer dan één cel is geselecteerd, wordt de eerste geselecteerde cel weergegeven.
* Als de kolom is geselecteerd, wordt de eerste celwaarde in de kolom gekozen.

Klik de **montages van de Visualisatie** binnen binnen aan het hoogste recht om de Summiere montages van het Aantal te vormen:

| Instelling | Definitie |
|--- |--- |
| [!UICONTROL Percentages] | Geef percentages weer in plaats van onbewerkte getallen. |
| [!UICONTROL Legend visible] | De informatie van de vertoning over metrisch getoond. |
| [!UICONTROL Abbreviate value] | Kies of u waarden wilt afbreken en maximaal 3 decimalen wilt weergeven. |
| [!UICONTROL Summarize value by] | Kies of u de maximale, minimale, gemiddelde, mediaan of som voor een selectie gegevens wilt weergeven. |

## [!UICONTROL Summary Change] visualisatie {#summary-change}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarychange_button"
>title="Samenvattingswijziging"
>abstract="Maak een visualisatie die de delta (wijziging) tussen twee getallen toont"

<!-- markdownlint-enable MD034 -->

Gebruik [!UICONTROL Summary Change] visualisatie om de delta (verandering) tussen twee aantallen te tonen. De groene en rode kleur van [!UICONTROL Summary Change] kan door [ polariteit van de douanegebeurtenis ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) of de berekende metrische [ tonen de Naar vorenTrend als ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) optie worden gecontroleerd.

Deze visualisatie werkt op de volgende manieren:

* Als er geen cel is geselecteerd, worden de eerste twee celwaarden in de kolom vergeleken.
* Als er één cel is geselecteerd, wordt 0 weergegeven, omdat de celwaarde dan met zichzelf wordt vergeleken.
* Als twee cellen zijn geselecteerd, wordt de eerste geselecteerde cel als teller en de tweede als noemer genomen.
* Als er meer dan twee cellen zijn geselecteerd, worden alleen de eerste twee ter vergelijking gebruikt.
* Als een bereik cellen is geselecteerd, wordt het eerste veld vergeleken met de laatste cellen in het bereik.
* Als de kolom wordt geselecteerd, vergelijkt het de eerste waarde met zich, die een verandering van 0 toont.


![](assets/summary-change.png)


Klik de **montages van de Visualisatie** binnen binnen binnen aan het hoogste recht om de Summiere montages van de Verandering te vormen:

| Instelling | Definitie |
| --- | --- |
| [!UICONTROL Percentages] | Geef percentages weer in plaats van onbewerkte getallen. |
| [!UICONTROL Legend visible] | De informatie van de vertoning over metrisch getoond. |
| [!UICONTROL Show Percent Change] | Geeft de procentuele wijziging tussen de twee getallen weer. |
| [!UICONTROL Show Raw Difference] | Geeft het onbewerkte verschil weer tussen de twee getallen. Met deze optie kunt u ook waarden afbreken en maximaal drie decimalen weergeven. |
