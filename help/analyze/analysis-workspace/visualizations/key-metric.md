---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Samenvatting van metrische sleutel
feature: Visualizations
role: User, Admin
exl-id: c74e77ff-15d6-48f1-a845-85bdf3444c3a
source-git-commit: b2e91c9981b328aa34e03dcd3b713438732ea6b1
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Samenvatting van metrische sleutel {#key-metric-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_keymetricsummary_button"
>title="Samenvatting van metrische sleutel"
>abstract="Maak een visualisatie die een combinatie is van de diagrammen voor de regel, de samenvattingswijziging en het samenvattingsnummer. Gebruik deze visualisatie om te vergelijken hoe belangrijk de metriek tussen twee periodes trending."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de Zeer belangrijke metrische summiere visualisatie in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [ Zeer belangrijke metrische samenvatting ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/key-metric) voor_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie laat u zien hoe belangrijke metrisch binnen één enkel tijdkader trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisatie laat zien hoe de metrische waarde wordt afgenomen voor de primaire datumbereiken en de vergelijkingsdatumbereiken

* **[!UICONTROL Summary percent change]** toont de metrische toename of daling tussen de primaire en vergelijkingsdatumwaaiers

* Huidige totale waarde ([!UICONTROL **summiere aantal**]) voor metrisch

## Gebruik hoofdletters

Deze visualisatie is gericht op verschillende veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Gebruiken

1. Voeg a ![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie toe. Zie [ een visualisatie aan een paneel ](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.

1. Configureer de visualisatie door een **[!UICONTROL Metric]** , een **[!UICONTROL Primary date range]** , een **[!UICONTROL Comparison date range]** (optioneel) en een **[!UICONTROL Filter]** (optioneel) te selecteren:

   ![ Zeer belangrijke metrische configuratie die de opties voor metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, en segment tonen.](assets/key-metrics-config.png)

   | Optie | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel.<p>Maak een keuze uit de beschikbare datumbereiken in de gegevensweergave.</p> <p>Kies [!UICONTROL **de datumwaaier van het Comité**] als u de zelfde datumwaaier wilt gebruiken die op het paneel wordt gebruikt waar de visualisatie wordt gevestigd.</p> |
   | **[!UICONTROL Comparison date range]** | Het datumbereik dat u wilt vergelijken met het primaire datumbereik. |
   | **[!UICONTROL Filter (optional)]** | Filters waarin u interesse hebt voor deze samenvatting. |

   {style="table-layout:auto"}

   >[!NOTE]
   >
   >Wanneer het [!UICONTROL **Primaire datumwaaier**] gebied aan [!UICONTROL **de datumwaaier van het Comité**] wordt geplaatst, **[!UICONTROL Comparison date range]** kan automatisch bijwerken, afhankelijk van of de **[!UICONTROL Comparison date range]** optie u kiest met betrekking tot de primaire datumwaaier of vast is.
   >
   >* **Relatief:** als het **[!UICONTROL Comparison date range]** gebied aan een optie wordt geplaatst die met betrekking tot de primaire datumwaaier (zulke [!UICONTROL **Vorige dag**], [!UICONTROL **Zelfde dag vorige week**], [!UICONTROL **Zelfde dag 4 weken voorafgaand**], etc.) is, dan om het even welke updates aan het [!UICONTROL **Primaire datumwaaier**] gebied veroorzaken **[!UICONTROL Comparison date range]** om onmiddellijk bij te werken aan de periode volgt het datumbereik van het deelvenster.
   >* **Vast:** als het [!UICONTROL **gebied van de Vergelijkingsdatum**] aan een vaste datumwaaier (zoals **wordt geplaatst 3 die Februari, 2023**), dan veranderingen in het [!UICONTROL **Primaire datareaal**] worden aangebracht gebied of de waaier van de paneeldatum hebben geen effect op de [!UICONTROL **waaier van de Vergelijkingsdatum**]. Nochtans, veroorzaken om het even welke updates aan de waaier van de paneeldatum de [!UICONTROL **Primaire datumwaaier**] om automatisch bij te werken.

1. Selecteer **[!UICONTROL Build]** .

De output van de belangrijkste metrische samenvatting kijkt als:

![ Zeer belangrijke metrische output die de metische, summiere verandering, samenvattingsaantal, en lijngrafieken tonen.](assets/key-metrics.png)

Houd rekening met het volgende wanneer u de uitvoer weergeeft:

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als een vergelijkingsdatumbereik niet is opgegeven tijdens de configuratie of verborgen is in de visualisatie-instellingen, wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging is verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:


## Configureren

Na het bouwen van visualisatie, kunt u de originele configuratie uitgeven.

1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Configure visualization]** bij de bovenkant van visualisatie.

   U wordt teruggezet naar de originele configuratiedialoog.

1. Wijzig desgewenst de instellingen. Selecteer **[!UICONTROL Reset]** om de huidige instellingen opnieuw in te stellen. Selecteer **[!UICONTROL Build]** om de visualisatie opnieuw op te bouwen.

## Instellingen

Als onderdeel van de visualisatie-instellingen zijn specifieke metrische summiere instellingen voor de sleutel beschikbaar.

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Emphasize percent change]** | Samenvattingswijziging in opvallende vetgedrukte tekst weergeven in het midden van de visualisatie |
| **[!UICONTROL Emphasize number value]** | Samenvattingsnummer in opvallende, vette letters weergeven in het midden van de visualisatie |
| **[!UICONTROL Legend visible]** | De legenda onder aan de visualisatie weergeven of verbergen |
| **[!UICONTROL Show annotations]** | Annotaties die zijn toegevoegd door een beheerder tonen of verbergen |
| **[!UICONTROL Hide title]** | De titel van de visualisatie verbergen. |
| **[!UICONTROL Percentages]** | Geeft de visualisatie weer in een percentage in plaats van in een getal. |
| **[!UICONTROL Show trendlines]** | Trendlines tonen in de visualisatie. |
| **[!UICONTROL Show max and min on trendlines]** | Minimum- en maximumwaarden tonen of verbergen in primaire en vergelijkingslijngrafieken |
| **[!UICONTROL Show comparison percentage and trendline]** | Vergelijkingsgegevens tonen of verbergen. Wanneer deze optie is verborgen, zijn zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| **[!UICONTROL Show total number]** | Samenvattingsnummer tonen of verbergen |
| **[!UICONTROL Show raw difference]** | Onbewerkt verschil tonen of verbergen tussen de totale waarde van de metrische waarde in het primaire datumbereik en het secundaire datumbereik |
| **[!UICONTROL Abbreviate value]** | Selecteer **[!UICONTROL Abbreviate value]** om de getalwaarde op een intelligente manier te verkorten. Als deze optie is geselecteerd, voert u een getal in om de hoeveelheid afkorting te definiëren. Bijvoorbeeld:<br/><table><tr><td>**Oorspronkelijke waarde**</td><td>**Afkorting**</td><td>**Resultaat**</td></tr><tr><td>$ 12.011.141,25</td><td>Niet geselecteerd</td><td align="right">$ 12.011.141,25</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 1</td><td align="right">$ 12 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 2</td><td align="right">$ 12,0 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, ingesteld op 2</td><td align="right">$ 12,011M</td></tr><tr><td>$ 12.011.141,25</td><td>Selecteren, instellen op 3</td><td align="right">$ 12,011M</td></tr></table> |

## Visualisatie bewerken

Na het bouwen van visualisatie, kunt u de originele configuratie nog uitgeven.

1. Klik op het potloodpictogram in de rechterbovenhoek van de visualisatie (naast het tandwielpictogram voor instellingen).

   ![ visualisatie geeft pictogram uit ](assets/edit-icon.png)

   U wordt nu teruggezet naar de originele configuratiemening.

1. Wijzig desgewenst het metrische bereik, het primaire datumbereik, het vergelijkingsdatumbereik of het filter.

>[!MORELIKETHIS]
>
>[ voeg een visualisatie aan een paneel toe ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisatie-instellingen ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Contextmenu Visualisatie ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)

