---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Hoofdmetrische samenvatting
feature: Visualizations
role: User, Admin
exl-id: c74e77ff-15d6-48f1-a845-85bdf3444c3a
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Samenvatting van metrische sleutel {#key-metric-summary}

>[!CONTEXTUALHELP]
>id="workspace_keymetricsummary_button"
>title="Samenvatting van metrische sleutel"
>abstract="Maak een visualisatie die een combinatie is van de diagrammen voor de regel, de samenvattingswijziging en het samenvattingsnummer. Gebruik deze visualisatie om te vergelijken hoe belangrijk de metriek tussen twee periodes trending."


>[!BEGINSHADEBOX]

_dit artikel documenteert de Zeer belangrijke metrische summiere visualisatie in_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [&#x200B; Zeer belangrijke metrische samenvatting &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/key-metric) voor_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


![&#x200B; KeyMetrics &#x200B;](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie laat u zien hoe belangrijke metrisch binnen één enkel tijdkader trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisatie laat zien hoe de metrische waarde wordt afgenomen voor de primaire datumbereiken en de vergelijkingsdatumbereiken

* **[!UICONTROL Summary percent change]** toont de metrische toename of daling tussen de primaire en vergelijkingsdatumwaaiers

* Huidige totale waarde ([!UICONTROL **summiere aantal**]) voor metrisch

## Gebruik hoofdletters

Deze visualisatie is gericht op verschillende veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Gebruiken

1. Voeg a ![&#x200B; KeyMetrics &#x200B;](/help/assets/icons/KeyMetrics.svg) **[!UICONTROL Key metric summary]** visualisatie toe. Zie [&#x200B; een visualisatie aan een paneel &#x200B;](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.

1. Configureer de visualisatie door een **[!UICONTROL Metric]** , een **[!UICONTROL Primary date range]** , een **[!UICONTROL Comparison date range]** (optioneel) en een **[!UICONTROL Filter]** (optioneel) te selecteren:

   ![&#x200B; Zeer belangrijke metrische configuratie die de opties voor metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, en segment tonen.](assets/key-metrics-config.png)

   | Optie | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel.<p>Maak een keuze uit de beschikbare datumbereiken in de gegevensweergave.</p> <p>Kies [!UICONTROL **de datumwaaier van het Comité**] als u de zelfde datumwaaier wilt gebruiken die op het paneel wordt gebruikt waar de visualisatie wordt gevestigd.</p> |
   | **[!UICONTROL Comparison date range]** | Het datumbereik dat u wilt vergelijken met het primaire datumbereik. |
   | **[!UICONTROL Segment (optional)]** | Elk segment waarin u geïnteresseerd bent voor deze samenvatting. |

   {style="table-layout:auto"}

   >[!NOTE]
   >
   >Wanneer het [!UICONTROL **Primaire datumwaaier**] gebied aan [!UICONTROL **de datumwaaier van het Comité**] wordt geplaatst, **[!UICONTROL Comparison date range]** kan automatisch bijwerken, afhankelijk van of de **[!UICONTROL Comparison date range]** optie u kiest met betrekking tot de primaire datumwaaier of vast is.
   >
   >* **Relatief:** als het **[!UICONTROL Comparison date range]** gebied aan een optie wordt geplaatst die met betrekking tot de primaire datumwaaier (zulke [!UICONTROL **Vorige dag**], [!UICONTROL **Zelfde dag vorige week**], [!UICONTROL **Zelfde dag 4 weken voorafgaand**], etc.) is, dan om het even welke updates aan het [!UICONTROL **Primaire datumwaaier**] gebied veroorzaken **[!UICONTROL Comparison date range]** om onmiddellijk bij te werken aan de periode volgt het datumbereik van het deelvenster.
   >* **Vast:** als het [!UICONTROL **gebied van de Vergelijkingsdatum**] aan een vaste datumwaaier (zoals **wordt geplaatst 3 die Februari, 2023**), dan veranderingen in het [!UICONTROL **Primaire datareaal**] worden aangebracht gebied of de waaier van de paneeldatum hebben geen effect op de [!UICONTROL **waaier van de Vergelijkingsdatum**]. Nochtans, veroorzaken om het even welke updates aan de waaier van de paneeldatum de [!UICONTROL **Primaire datumwaaier**] om automatisch bij te werken.

1. Selecteer **[!UICONTROL Build]** .

De output van de belangrijkste metrische samenvatting kijkt als:

![&#x200B; Zeer belangrijke metrische output die de metische, summiere verandering, samenvattingsaantal, en lijngrafieken tonen.](assets/key-metrics.png)

Houd rekening met het volgende wanneer u de uitvoer weergeeft:

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als een vergelijkingsdatumbereik niet is opgegeven tijdens de configuratie of verborgen is in de visualisatie-instellingen, wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging is verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:


## Configureren

Na het bouwen van visualisatie, kunt u de originele configuratie uitgeven.

1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Configure visualization]** bij de bovenkant van visualisatie.

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

Nadat u de visualisatie hebt gemaakt, kunt u de oorspronkelijke configuratie bewerken.

1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) in de hoogste juiste hoek van visualisatie.


   U wordt nu teruggenomen naar de originele [&#x200B; configuratiemening &#x200B;](#configure).

1. Verander metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, of het segment zoals aangewezen.

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie &#x200B;](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)

