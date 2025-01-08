---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Samenvatting van metrische sleutel
feature: Visualizations
role: User, Admin
exl-id: c74e77ff-15d6-48f1-a845-85bdf3444c3a
source-git-commit: 00276353ef5555955d9dc178c692da0dbfb7eac2
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Samenvatting van metrische sleutel

Met de [!UICONTROL Key metric summary] -visualisatie kunt u zien hoe een belangrijke metrische waarde binnen één tijdlijn trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisaties die tonen hoe metrisch voor de primaire en vergelijkingsdatumwaaiers trending is

* **[!UICONTROL Summary percent change]** die de metrische toename of daling tussen de primaire en vergelijkingsdatumwaaiers toont

* Huidige totale waarde ([!UICONTROL **summiere aantal**]) voor metrisch

## Gebruik hoofdletters

Deze visualisatie is gericht op verschillende veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Vorm de Belangrijkste metrische samenvatting

1. Sleep de **[!UICONTROL Key metric summary]** visualisatie van het **[!UICONTROL Visualizations]** menu in de linkerspoorstaaf in een paneel.

   ![](assets/key-metric-config.png)

1. Configureer de visualisatie met de volgende opties:

   | Configuratie-instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel.<p>Maak een keuze uit de beschikbare datumbereiken in uw rapportsuite.</p> <p>Kies [!UICONTROL **de datumwaaier van het Comité**] als u de zelfde datumwaaier wilt gebruiken die op het paneel wordt gebruikt waar de visualisatie wordt gevestigd.</p> |
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

## De uitvoer weergeven

De uitvoer moet er ongeveer als volgt uitzien:

![](assets/key-metric-output.png)

Houd rekening met het volgende wanneer u de uitvoer weergeeft:

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als een vergelijkingsdatumbereik niet is opgegeven tijdens de configuratie of verborgen is in de visualisatie-instellingen, wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging is verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:

![](assets/key-metric-output2.png)

## Visualisatie-instellingen

De Belangrijkste metrische samenvatting biedt veelvoudige flexibele montages aan om betere rapportering en communicatie van belangrijke metriek toe te laten. Instellingen zijn toegankelijk via het tandwielpictogram in de rechterbovenhoek van de visualisatie.

![](assets/key-metric-settings.png)

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Emphasize percent change]** | Samenvattingswijziging in opvallende vetgedrukte tekst weergeven in het midden van de visualisatie |
| **[!UICONTROL Emphasize number value]** | Samenvattingsnummer in opvallende, vette letters weergeven in het midden van de visualisatie |
| **[!UICONTROL Legend visible]** | De legenda onder aan de visualisatie weergeven of verbergen |
| **[!UICONTROL Show annotations]** | Annotaties die zijn toegevoegd door een beheerder tonen of verbergen |
| **[!UICONTROL Show sparklines]** | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels |
| **[!UICONTROL Show min and max on sparklines]** | Minimum- en maximumwaarden tonen of verbergen in primaire en vergelijkingslijngrafieken |
| **[!UICONTROL Show comparison]** | Vergelijkingsgegevens tonen of verbergen. Wanneer deze optie is verborgen, zijn zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| **[!UICONTROL Show total number]** | Samenvattingsnummer tonen of verbergen |
| **[!UICONTROL Show raw difference]** | Onbewerkt verschil tonen of verbergen tussen de totale waarde van de metrische waarde in het primaire datumbereik en het secundaire datumbereik |
| **[!UICONTROL Abbreviate value]** | Verkort getalwaarden om gecommuniceerde inzichten te vereenvoudigen (bijvoorbeeld 20.000 -> 20K) |

## Visualisatie bewerken

Na het bouwen van visualisatie, kunt u de originele configuratie nog uitgeven.

1. Klik op het potloodpictogram in de rechterbovenhoek van de visualisatie (naast het tandwielpictogram voor instellingen).

   ![](assets/edit-icon.png)

   U wordt nu teruggezet naar de originele configuratiemening.

1. Verander metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, of het segment zoals aangewezen.
